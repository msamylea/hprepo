# hprepo
 
### Document Assessment Toolset

Advanced, end-to-end document assessment tools to extract signatures, detect forgery, analyze and view PDF version changes, detect and view suspicious PDF physical modifications (for example, signatures pasted into the document to circumvent forgery detection).

- Two custom trained models:
 - Signature Detection Model (YoloV11)
 - Forgery Detection Model (Ensemble Model / Torch)

- Datasets:  
-- [signature_detection.zip and forgery_detection.zip](https://drive.google.com/drive/folders/1vsTLWSvGFWEsAqAYu8qpZ-VBWBY6AY1z?usp=sharingp:// "signature_detection.zip and forgery_detection.zip")



## Installation
This repo is intended for use with [HP AI Studio](https://zdocs.datascience.hp.com/downloads).

Install HP AI Studio, select New Workspace, then select Deep Learning GPU. Give your workspace a name and click Next. 
After it finishes loading and installing, click the Project Setup tab, then click Setup on the left side of this tab.  You should see GitHub Repository.
![image](https://github.com/user-attachments/assets/df905f70-f0e6-4d51-8133-1c31c06de862)

Next, click Clone. Enter https://github.com/msamylea/hprepo.git as the repository to clone and select a local folder to download the repository into.  Complete any required authentication steps with GitHub and finish.

If you want to train the models yourself, you can download the datasets used from the link above, extract them to folders on your local PC, and then add them ass Assets under the Asset tab.  This will make them available via the datafabric folder in HP AI Studio once the workspace is restarted. The training code is located under /share/model_training_scripts/.  If you choose to train the models, you must update the paths for the data locations, experiment name, and run ids, as those may vary per install and/or run.

> **NOTE: It is not necessary to retrain the models, as this takes a very long time.  Pretrained copies are included in the repository along with code to register the models to MLFlow if desired.**

Navigate to the Jupyter Notebooks section (it will be a tab with an X in a white circle beside it).  

Under the Shared folder, you will find the code included in this repository.  To get started right away, you can simply open document_processing.ipynb and run the code cell by cell in order.  Sample files are included under signature_samples and test_pdfs to use the different functions.


### :notebook: Pre-Requisites
Per the HP AI Studio page:
```
Z by HP AI Studio currently runs on the x64 processor architecture and requires the following:

Windows 10 (build 19041 and higher) or Windows 11
Ubuntu 22.04 OS
AMD Ryzen™ 9 processor, Intel Core™ i5 12th generation processor, or higher
Minimum 50 GB of available storage
16GB of RAM
Internet access
To enable GPU compute, NVIDIA® GPU compatible with driver version 528.89 or newer, and a minimum of 8GB of VRAM is recommended.

AI Studio supports up to 4 compatible NVIDIA GPUs on Windows.

Hardware Recommendations:
GPU: NVIDIA® GPU card with CUDA® Compute capability driver version 528.89 or newer (560+ recommended).
Software Requirements:
WSL 2 (Windows Subsystem for Linux) must be enabled on setups running Windows OS. Refer to WSL Recommended Setup for more details.
or Ubuntu 22.04

Installation Requirements:
Internet connection
Local administrative / root user permissions
An active AI Studio user license
```
  
### Repository Structure and Files

```
├── model_training_scripts
│   ├── register_models
│   │   ├── register_forgery_model.ipynb
│   │   ├── register_signature_model.ipynb
│   │   ├── forgery_detect_model.pt
│   │   ├── signature_detect_model.pt
│   ├── genuine
│   │   ├── jpg files
├── signature_samples
│   ├── forged
│   │   ├── jpg files
│   ├── genuine
│   │   ├── jpg files
├── test_pdfs
│   ├── forged
│   │   ├──forged.pdf
│   ├── valid
│   │   ├──valid.pdf
│   ├── versioned_pdfs
│   │   ├──sample.pdf
├── train_forgery_model
│   ├── best_signature_ensemble.pth
│   ├── features_dataset.npz
│   ├── forgery_detection_model.ipynb
├── train_signature_model
│   ├── best.pt
│   ├── train_yolo_detect.ipynb
├── document_processing.ipynb
```

### Model Architecture
#### Forgery Detection Model

![forgery_detect_model pt](https://github.com/user-attachments/assets/8c3d69dc-69a0-4eb1-ae04-a96f805cc392)

#### Signature Detection Model

![signature_detect_model pt](https://github.com/user-attachments/assets/e1be1a1d-e96a-406d-bc5c-73f3ff191020)

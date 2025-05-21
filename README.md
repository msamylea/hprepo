# hprepo
 
### Document Assessment Toolset

Advanced, end-to-end document assessment tools to extract signatures, detect forgery, analyze and view PDF version changes, detect and view suspicious PDF physical modifications (for example, signatures pasted into the document to circumvent forgery detection).

- Two custom trained models:
 - Signature Detection Model (YoloV11)
 - Forgery Detection Model (Ensemble Model / Torch)

- Datasets:
-- [signature_detection.zip and forgery_detection.zip](https://drive.google.com/drive/folders/1vsTLWSvGFWEsAqAYu8qpZ-VBWBY6AY1z?usp=sharingp:// "signature_detection.zip and forgery_detection.zip")



## :zap: Usage
Write about how to use this project.

###  :electric_plug: Installation
- Steps on how to install this project, to use it.
- Be very detailed here, For example, if you have tools which run on different operating systems, write installation steps for all of them.

```
$ add installations steps if you have to.
```

###  :package: Commands
- Commands to start the project.

##  :wrench: Development
If you want other people to contribute to this project, this is the section, make sure you always add this.

### :notebook: Pre-Requisites
List all the pre-requisites the system needs to develop this project.
- A tool
- B tool

###  :nut_and_bolt: Development Environment
Write about setting up the working environment for your project.
- How to download the project...
- How to install dependencies...
  
### Repository Structure and Files

```
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

# hprepo
 
### Document Assessment Toolset

Advanced, end-to-end document assessment tools to extract signatures, detect forgery, analyze and view PDF version changes, detect and view suspicious PDF physical modifications (for example, signatures pasted into the document to circumvent forgery detection).

- Two custom trained models:
-- Signature Detection Model (YoloV11)
-- Forgery Detection Model (Ensemble Model / Torch)

- Datasets:
-- [signature_detection.zip and forgery_detection.zip](https://drive.google.com/drive/folders/1vsTLWSvGFWEsAqAYu8qpZ-VBWBY6AY1z?usp=sharingp:// "signature_detection.zip and forgery_detection.zip")

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

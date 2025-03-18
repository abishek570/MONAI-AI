# VitaVision AI



## Overview

VitaVision AI is an advanced AI-powered medical diagnosis system designed to predict diseases and segment the diseased area using multitasking model architectures. The system is fine-tuned on a comprehensive datasets encompassing diseases which will classify the disease and then segment the disease to serve the disease severity and metadata. It will generate a detailed report on the diagnosis of the disease by providing description, symptoms and prescriptions.


## Models

- **Densenet121 (Fine-tuned)** - Used based on the datasets for classification task
- **UNet Model** - Used based on the datasets for segmentation tasks
- **Llama2-uncensored** - Used for text generation task
## Datasets

The dataset is used to train with two models 
1. The dataset used for the classification model should be in the folder structure,
    ```
    dataset/
    │── train/
    │   ├── normal/
    │   │   ├── patient_01.png
    │   │   ├── patient_02.png
    │   │   ├── ...
    │   ├── tumor/
    │   │   ├── patient_03.png
    │   │   ├── patient_04.png
    │   │   ├── ...
    │   ├── stroke/
    │   │   ├── patient_05.png
    │   │   ├── patient_06.png
    │   │   ├── ...
    │
    │── val/
    │   ├── normal/
    │   ├── tumor/
    │   ├── stroke/
    │
    │── test/
    │   ├── normal/
    │   ├── tumor/
    │   ├── stroke/
    │
    ```
2. The dataset used for the segmentation task should be in the folder structure for single disease,
    ```
    dataset/
    │── train/
    │   ├── images/
    │   │   ├── patient_01.png
    │   │   ├── patient_02.png
    │   │   ├── ...
    │   ├── masks/
    │   │   ├── patient_01.png
    │   │   ├── patient_02.png
    │
    │── val/
    │   ├── images/
    │   │   ├── patient_11.png
    │   │   ├── patient_12.png
    │   ├── masks/
    │   │   ├── patient_11.png
    │   │   ├── patient_12.png
    │
    │── test/
    │   ├── images/
    │   │   ├── patient_21.png
    │   │   ├── patient_22.png
    │   ├── masks/
    │   │   ├── patient_21.png
    │   │   ├── patient_22.png
    │
    ```    
## Datasets Example

## Original Dataset

These datasets are used for training classification models which includes images in PNG, JPG, or DICOM (DCM) formats. DICOM files provide richer metadata, including patient details, scan modality (MRI, CT, ultrasound), and acquisition settings. Organizing data with proper labels and metadata enables efficient preprocessing, feature extraction, and model training for accurate disease classification.

![Original Dataset]("D:\My repo\MONAI-AI\assets\original.png")

## Masked Dataset

The masked dataset, combined with the original dataset, is used for segmentation process to identify the diseased regions. It includes PNG, JPG, or DICOM (DCM) formats. Masks help predict the precise location, size, and volume of abnormalities, while DICOM files provide additional metadata for enhanced medical analysis and diagnosis.

![Masked Dataset]("D:\My repo\MONAI-AI\assets\masked.png")
# VitaVision AI



## Overview

VitaVision AI is an advanced AI-powered medical diagnosis system designed to predict diseases and sege=ment the diseased are using a multitasking model architectures. The system is fine-tuned on a comprehensive datasets encompassing diseases which will classify the disease and then segment the disease to serve the disease severity and metadata. It will generate a detailed report on the diagnosis of the disease by providing description, symptoms and prescriptions.


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
### Datasets Example
![Image](https://github.com/abishek570/MONAI-AI/blob/main/Screenshot%202025-03-18%20174531.png)


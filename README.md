<!-- README for ImageData-DS4002 -->

# ImageData-DS4002

<!-- Project Overview -->
## 📌 Project Overview

This is a **Pet Breed Classification** project. We train a convolutional neural network (CNN) to identify dog and cat breeds from images. The workflow covers **data organization**, **preprocessing**, **model training**, and **evaluation**.

### Key Features:
- **Data Organization**: Automatically sorts raw images into breed-specific folders  
- **Data Augmentation**: Applies rotations, flips, zooms, and brightness adjustments
- **Transfer Learning**:
- **Evaluation**: 

<!-- Section 1: Software & Platform -->
## Section 1: Software & Platform

This project was developed using the following software and tools:

- **Programming Language:** Python 3.x  
- **IDE:** VS Code (or any Python editor)  
- **Key Packages:**  
  - `tensorflow` (with Keras)  
  - `numpy`  
  - 
- **Platform Tested On:** macOS, Windows, Linux  
- **Install dependencies:**  
  ```bash
  pip install -r requirements.txt
  ```

<!-- Section 2: Project Folder Structure -->
## Section 2: A Map of your documentation
ImageData-DS4002/  
├── DATA/  
│   ├── InputData/  
│   │   └── images/  
│   └── AnalysisData/  
│       └── organized_images/  
├── OUTPUT/  
│   ├── Accuracy and Loss.png  
│   └── Confusion Matrix.png  
├── SCRIPTS/  
│   ├── DataCollectionScripts/  
│   │   ├── data_organization.py  
│   │   └── data_preprocessing.py  
│   └── AnalysisScripts/  
│       └── Model_Training_and_Evaluation.ipynb  
├── LICENSE  
├── README.md  
└── requirements.txt  

<!-- Section 3: Instructions for Reproducing Results -->
## Section 3: Instructions for Reproducing Results
Follow these steps to reproduce our results:

1. **Create the Google Collab**  
   Under the SCRIPTS/AnalysisScripts folder you can find a file Model_Training_and_Evaluation.ipynb, upload this to Google Collab.

   For this assignment we connected to Google Collab's A100 GPU, which is from Collab Pro. Do not run the code yet.
2. **Collect & Prepare Data**   
   - Go to the Oxford-IIIT Pet Dataset website: https://www.robots.ox.ac.uk/~vgg/data/pets/  
     Download the “Images” archive (`images.tar.gz`) and extract its contents into the `DATA/InputData/` folder.
   - In your local IDE or terminal, run the organization script to sort raw images into breed subfolders and extract its contents into the `DATA/AnalysisData/` folder:  
     ```bash
     python ./SCRIPTS/DataCollectionScripts/data_organization.py
     ```  
   - Next, run the preprocessing script to resize, augment, normalize, and split the images:  
     ```bash
     python ./SCRIPTS/DataCollectionScripts/data_preprocessing.py
     ```
3. 
   

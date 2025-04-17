<!-- README for ImageData-DS4002 -->

# ImageData-DS4002

<!-- Project Overview -->
## 📌 Project Overview

This is a **Pet Breed Classification** project. We train a convolutional neural network (CNN) to identify dog and cat breeds from images. The workflow covers **data organization**, **preprocessing**, **model training**, and **evaluation**.

### Key Features:
- **Data Organization**: Automatically sorts raw images into breed-specific folders  
- **Data Augmentation**: Applies rotations, flips, zooms, and brightness adjustments
- **Transfer Learning**: Builds on a pre‑trained CNN backbone and fine‑tunes it for pet‑breed recognition
- **Evaluation**: Reports overall accuracy and generates performance visualizations such as loss/accuracy curves and a confusion matrix

<!-- Section 1: Software & Platform -->
## Section 1: Software & Platform

This project was developed using the following software and tools:

- **Programming Language:** Python 3.x  
- **IDE:** VS Code (or any Python editor)  
- **Key Packages:**  
  - `tensorflow` (with Keras)  
  - `numpy`  
  - `matplotlib`  
  - `seaborn`  
  - `scikit-learn`  
  - `Pillow`  
- **Platform Tested On:** macOS, Windows  
- **Install dependencies:**  
  ```bash
  pip install -r requirements.txt
  ```

<!-- Section 2: Project Folder Structure -->
## Section 2: A Map of your documentation
ImageData-DS4002/  
├── DATA/  
│   ├── DataAppendix  
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

1. **Create the Google Colab**  
   - In `SCRIPTS/AnalysisScripts` locate `Model_Training_and_Evaluation.ipynb` and upload it to Google Colab.  
   - Switch runtime to **GPU → A100** (Colab Pro).  
   - **Do not run the notebook yet.**
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
3. **Train & Evaluate the Model in Colab**  
   - Mount Google Drive or upload the `DATA/AnalysisData/organized_images/` directory to Colab.  
   - Run all cells in `Model_Training_and_Evaluation.ipynb`.  

4. **Inspect Results**  
   - Review training/validation performance in the output graphs.  
   

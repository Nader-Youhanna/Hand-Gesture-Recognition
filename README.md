# Hand Gesture Recognition Project

**This project aims to put your understanding of machine learning algorithms into practice
with a real world problem.**
## Environment

you can download all the packages used using conda or pip
1. This will create new environment from scratch with all listed modules.

    conda env create -f environment.yml

    if this option stuck at solving environment step, you may need to run : conda config --set channel_priority strict

2. If you already have an env and want to install the modules only you can use
The --prune option removes any packages that are not listed in the environment.yml file.

    conda env update -f environment.yml

3. Or using pip
    
    pip install -r requirements-pip.txt


## Dataset
Hand Gesture of the Colombian sign language

### Option 1: download the processed data

download https://drive.google.com/drive/u/2/folders/1o9wzwaJVfrbpCFJ0rIyed1QvARh0JAtn

unzip the zipfile and put it all into `data folder`

### Option 2: run the data insertion script data_insertion.py

It will handle everything from downloading into extracting data into /data folder.

However you would need to have gdown library installed. (included in requirements.txt)

## Data Preparation
# 1. Data Visualization
![normal](https://github.com/Nader-Youhanna/Hand-Gesture-Recognition/assets/62957935/d8abcb72-a9df-405c-8150-328c2388e527)


# 2. Illumination Processing
We perform illumination processing in order to remove shadows and segment the hand and the background
![illuminated](https://github.com/Nader-Youhanna/Hand-Gesture-Recognition/assets/62957935/d619d84f-d055-4d87-a9b7-d7f45b9aa3ff)

# 3. Alignment of images
We detect each hand's orientation and orient all images in the same direction
![aligned](https://github.com/Nader-Youhanna/Hand-Gesture-Recognition/assets/62957935/4a273fc2-8ece-461d-b826-6f071eb4476b)

# 4. Edge Detection
We perform edge detection
![edge_detected](https://github.com/Nader-Youhanna/Hand-Gesture-Recognition/assets/62957935/532f16ce-5f50-421c-90c7-f78f0527b7a8)

## Feature Extraction
We use:
- Hog Features
- RI HOG Features
- LBP Features
- SIFT Features
- DAISY Features
- Fourrier Descriptor Features
- ORB Features
- Hu moments Features
- Convex Hull Features
- Elliptical fourrier descriptor features

We found DAISY features to give the best results
We then perform PCA to reduce the feature's dimensionality

## Model Training
We use a small Neural Network with 2 layers
We use ReLU activation functions, categorical cross entropy loss function and adam optimizer

## Model Evaluation
Accuracy: 79.6%

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
![normal](https://github.com/Nader-Youhanna/Hand-Gesture-Recognition/assets/62957935/ef1b38ea-0060-4efd-93ba-0f5edb6d6e35)

# 2. Illumination Processing
We perform illumination processing in order to remove shadows and segment the hand and the background
![illuminated](https://github.com/Nader-Youhanna/Hand-Gesture-Recognition/assets/62957935/d64ac791-5a82-4e71-84de-258756b4d6ee)

# 3. Alignment of images
We detect each hand's orientation and orient all images in the same direction

![aligned](https://github.com/Nader-Youhanna/Hand-Gesture-Recognition/assets/62957935/d709fcd1-a0bc-4b41-9e3d-92e304cb51a5)

# 4. Edge Detection
We perform edge detection
![edge detected](https://github.com/Nader-Youhanna/Hand-Gesture-Recognition/assets/62957935/64aaecc7-ae7d-4079-9e73-f506ba9191c9)

## Model Training
## Model Evaluation

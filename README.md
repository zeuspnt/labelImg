# labelImg
:metal: LabelImg is a graphical image annotation tool and label human pose in images


## Requierment:
### OpenPose: https://github.com/CMU-Perceptual-Computing-Lab/openpose

## Quick Start:

1. Install lib for labelImg
Python3 and Qt5
```
sudo apt-get install pyqt5-dev-tools
sudo pip3 install lxml
make qt5py3
```

2. Install OpenPose

https://github.com/CMU-Perceptual-Computing-Lab/openpose/blob/master/doc/installation.md

Run ```make install``` after build successfully.

3. Edit some information

Open file ```labelImgOpenPose.py``` and edit at line 78
```
# Ensure you point to the correct path where models are located
params["default_model_folder"] = "folder/path/to/models/in/openpose"
```

4. Run
```
python3 labelImgOpenPose.py
```

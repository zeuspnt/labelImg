# labelImg
:metal: LabelImg is a graphical image annotation tool and label human pose in images


## Requierment:
### OpenPose: https://github.com/CMU-Perceptual-Computing-Lab/openpose

## Quick Start:
1. Clone source
```
git clone https://github.com/zeuspnt/labelImg.git
```

2. Checkout branch to ```labelimgwithpose```
```
 git checkout labelimgwithpose
```

3. Install lib for labelImg
Python3 and Qt5
```
sudo apt-get install pyqt5-dev-tools
sudo pip3 install lxml
make qt5py3
```

4. Install OpenPose

https://github.com/CMU-Perceptual-Computing-Lab/openpose/blob/master/doc/installation.md

Run ```make install``` after build successfully.

5. Edit some information

Open file ```labelImgOpenPose.py``` and edit at line 78
```
# Ensure you point to the correct path where models are located
params["default_model_folder"] = "folder/path/to/models/in/openpose"
```
usually, it will at ```.../openpose/models/```

6. Run
```
python3 labelImgOpenPose.py
```
## Extract keypoints from OpenPose to txt file (extractKeypointsWithOpenPose.py)

### Run with argument

```
python extractKeypointsWithOpenPose.py --imagedir=/home/ai/cuda-workspace/labelImg/examples/images/
```

Get all images in path at parameter ```--imagedir``` to pass into Openpose and save keypoints in txt file in keypoints directory with structure:
```
examples
|
---- images
|  |
|   ---- COCO_val2014_000000000474.jpg
---- keypoints
   |
    ---- COCO_val2014_000000000474.txt
```

## Review result be extracted (labelImgOpenPoseTXT.py)

```
python labelImgOpenPoseTXT.py
```

Click on ```Open dir``` to open folder images, the app will automate load txt files in keypoints folder and draw that pose on images.

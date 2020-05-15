# High Power Rocketry tracker with Python

## Description
Rocket launches are of great interest and many efforts have been made to automate the capturing process of close-up the take offs on camera. The capturing automation can be achieved by either object tracking, frame-by-frame object detection or combinations, depending on the problem limitations.
The main aim of this project is to offer a robust detector/tracker, capable to operate at almost real time with limited hardware resources, for the automated recording of the rocket launches. The algorithm will be combined with the single-board computer Raspberry which will be moving the camera. The hardware set-up of the camera motion is not part of this projects.
Implementation plan
The project consists of two components:

The rocket detection model.
The core component of most modern trackers is a discriminative classifier, tasked with distinguishing between the target and the surrounding environment. To cope with natural image changes, this classifier is typically trained with translated and scaled sample patches.
A model will be created using TensorFlow and Keras on Python3. It will be trained on multiple images containing rockets of different sizes, colors and orientations and it will output a bounding box when a rocket is detected.
The rocket tracking algorithm.
Once the object is identified, the tracking algorithm is applied. That way the information of past frames is considered and position of the object is predicted, allowing us to follow the flight trajectory. In case that the track algorithm fails (i.e. cannot track correctly the object), we rerun the detection model.
The tracking algorithm will be running on the Raspberry PI, which will be moving the camera in order to track and record the rocket the whole time. The OpenCV library will be used.

## Features

The model has been trained from scratch using the rocket image dataset I created from Google's OID/v4. I put the components of the whole project in different repositories.
- I built a web scrapper to download custom dataset 
   - [My Tool Link](https://github.com/sunn-e/Google-Image-Downloader-Rocket-Dataset)
   - You can reuse it to download other images too.
- Built a tool to convert annottions type from OID Label to Yolov3 format.
   - [My Tool Link](https://github.com/sunn-e/OIDLabelToTFRecords)
   - This helps to train model. We do this before actual training instead of during training as it may create bottleneck.
- Created detailed guide on how to setup and train the model.
   - [My Tool Link](https://github.com/sunn-e/RocketModelTrainer)
   - The model used is TinyYolo v3 as it can be deploed on raspberry pi too. It can be trained using Yolov3 as well with few tweaks in parameters section.

### Todo

- [x] Setup yolov3
- [x] Convert dataset to yolov3 format. Check [this](C:\Users\Helios\Desktop\Google Image Downloader + Rocket Dataset\converter-scripts) out to know how to do that.
- [x] Train the yolov3 model on custom dataset
- [x] Upload weights and share here via Mega or GDrive
- [x] Added webcam mode with realtime rocket detection
- [x] Added video file mode with realtime object detection
- [x] Upload demo video online. Link coming soon.

## How to use

### Run on your PC with provided weights
- `git clone https://github.com/sunn-e/OpenCV-Yolov3-CPU/`
- `cd OpenCV-Yolov3-CPU`
- download weights and configuration file from [here](https://pjreddie.com/darknet/yolo/)
- download coco.names from [here](https://github.com/pjreddie/darknet/blob/master/data/coco.names)
- run the main notebook using jupiter notebook
- Give input/objects when prompt opens.
- Custom folder name is supported, may have to change script a little
- Wait for pictres to get displayed
- Open `TinyYolov3-Prototype-custom-rocket.ipynb` in jupyter notebook
- Enter 1 for webcam mode and 2 for custom video mode. 

### Run with your custom weights


- [Visit my other repository.](https://github.com/sunn-e/RocketModelTrainer)
- Read my article on medium about how to install tensorflow on your NVidia CUDA GPU systm [here](https://medium.com/@sunnydhoke22)
- I built a web scrapper to download custom dataset 
   - [My Tool Link](https://github.com/sunn-e/Google-Image-Downloader-Rocket-Dataset)
   - You can reuse it to download other images too.
- Built a tool to convert annottions type from OID Label to Yolov3 format.
   - [My Tool Link](https://github.com/sunn-e/OIDLabelToTFRecords)
   - This helps to train model. We do this before actual training instead of during training as it may create bottleneck.
- Created detailed guide on how to setup and train the model.
   - [My Tool Link](https://github.com/sunn-e/RocketModelTrainer)
   - The model used is TinyYolo v3 as it can be deploed on raspberry pi too. It can be trained using Yolov3 as well with few tweaks in parameters section.
   
## Contribute

Feel free to fork it and create your own versions. Make sure you have installed all the dependencies.
Check out my other [repo](https://github.com/sunn-e/RocketModelTrainer) to learn how to train your own models from scratch.

## Getting Started

simply clone the repository to acquire the dataset.

## Dependencies

### Prerequisites

- Python 3.x+
- OpenCV 2
- numpy
- jupyter notebook

#### specially for opencv

```
pip install opencv-contrib-python
```

#### For weights

- I have provided the one I trained using google collab for 5000 epochs. Vrious models are under the custom weights model. Feel free to use them.


## Built With

- [Python 3.x+](https://www.python.org/download/releases/3.0/)
- [opencv](https://opencv.org/)
- [Yolo v3](https://pjreddie.com/darknet/yolo/)

## Contributing

Clone and see if you find anything to improve upon. You can also create issues using that tiny issue button.

## Versioning

Git

## Dataset

The dataset(coming soon) is inside data folder with image folder names corresponding the search term used to download those images.
Meanwhile check [this](https://github.com/sunn-e/Google-Image-Downloader-Rocket-Dataset) out!

## Notice

The images(if any), videos have been provided for educational purpose and are owned by their respective owners. Dataset is custom variant of Open Image Dataset v4.

## Authors

* **Sunny Dhoke** - *Initial work* - [sunn-e](https://github.com/sunn-e)

## License

[LICENSE.md](LICENSE.md) file for details

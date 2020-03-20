# OpenCV-TinyYolov3-CPU

## Description

 A setup to run open cv with tiny yolov3 on CPU.

## Features

- Basic setup to see how opencv deep neural network works in practice

## How to use

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

## Contribute

Feel free to fork it and create your own versions. Make sure you have installed all the dependencies

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

- You may copy paste the image folders to your intended location or simply copy past the path to out machine learning/deep learning model script.


## Built With

- [Python 3.x+](https://www.python.org/download/releases/3.0/)
- [opencv](https://opencv.org/)
- [Yolo v3](https://pjreddie.com/darknet/yolo/)

## Contributing

Clone and see if you find anything to improve upon. You can also create issues using that tiny issue button.

## Versioning

GitHub

## Todo

- [x] Setup yolov3
- [x] Convert dataset to yolov3 format. Check [this](C:\Users\Helios\Desktop\Google Image Downloader + Rocket Dataset\converter-scripts) out to know how to do that.
- [x] Train the yolov3 model on custom dataset
- [x] Upload weights and share here via Mega or GDrive
- [x] Added webcam mode with realtime rocket detection
- [x] Added video file mode with realtime object detection
- [x] Upload demo video online. Link coming soon.

## Dataset

The dataset(coming soon) is inside data folder with image folder names corresponding the search term used to download those images.
Meanwhile check [this](https://github.com/sunn-e/Google-Image-Downloader-Rocket-Dataset) out!

## Notice

The images(if any), videos have been provided for educational purpose and are owned by their respective owners.

## Authors

* **Sunny Dhoke** - *Initial work* - [sunn-e](https://github.com/sunn-e)

## License

[LICENSE.md](LICENSE.md) file for details

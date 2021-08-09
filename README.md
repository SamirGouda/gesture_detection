<!--
*** This README markdown is built from the following repo
*** https://github.com/othneildrew/Best-README-Template
-->



<!-- PROJECT SHIELDS -->
<!--
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->

[![LinkedIn][linkedin-shield]][linkedin-url]



<!-- PROJECT LOGO -->
<br />

  <h3 align="center">Gesture Detection</h3>

  <p align="center">
    Detects different hand gestures using tensorflow object detection
    <br />
    
  </p>
</p>



<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

[![Product Name Screen Shot][product-screenshot]]

The project consists of the following tasks

* installing tensorflow object detection package
* downloading pretrained mobnet model from tensorflow zoo detection models
* creating label-map and tf records
* updating pipeline config for the gesture detection task
* collecting images for gesture detection (thumbs_up, thumbs_down, live_long, thank_you) using `OpenCV` and webcam
* label the images using `labelimg` library 
* fine tuning the model
* evaluating the model


### Built With

main frameworks and packages used in building this project

* [Tensorflow](https://www.tensorflow.org)
* [OpenCV](https://opencv.org)
* [labelimg](https://github.com/tzutalin/labelImg)

<!-- GETTING STARTED -->
## Getting Started

There are some dependencies you have to install, and you may create virtual environment

### Prerequisites

Install the following packages.
* pip
  ```sh
  pip install opencv-python
  ```

### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/SamirGouda/gesture_detection.git
   ```
2. Optionally create virtual environment and activate it
```sh
    python -m venv {environment_name}
    .{environment_name}\Scripts\activate
```
if you created a virtual environment you should install the following dependencies
```sh
    python -m pip install --upgrade pip
    pip install ipykernal
```
add the virtual environment to the python kernal and install jupyter notebook
```sh
    python -m install ipykernal --user --name={environment_name}
    pip install jupyter notebook
```
3. Install the following python packages
* opencv for image capturing and processing
   ```sh
   pip install OpenCV
   ```
* install pyqt5 and lxml to be able to install labelimg package
```sh
    pip install --upgrade pyqt5 lxml
```
* install wget to download protoc and be able to install tensorflow object detection
```sh
    pip install wget
```



<!-- USAGE EXAMPLES -->
## Usage

* collect images and label them using img_collection notebook and then manually split your data to train and test folders
* train the model using training_and_detection notebook, note that training takes a long time (30min-2hrs), its preferable to copy the train_command and run in terminal to see progress
* once training is complete you can evaluate your model using tensorboard
```sh
    tensorboard --logdir=Tensorflow/workspace/models/ssd_mobnet_model/eval/
```

then training and detection

[![thumbs up][screenshot-1]]
[![thumbs down][screenshot-2]]



<!-- CONTACT -->
## Contact

Samir Gouda - [https://www.linkedin.com/in/samirgouda](https://www.linkedin.com/in/samirgouda) 

email: [samiir.ahmedd@gmail.com](mailto:samiir.ahmedd@gmail.com)

Project Link: [https://github.com/SamirGouda/gesture_detection](https://github.com/SamirGouda/gesture_detection)



<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements

* [nicknochnack](https://github.com/nicknochnack/TFODCourse) for his youtube tutorials and his TFODCourse which this project is built on 

* [tzutalin](https://github.com/tzutalin/labelImg) for his labelimg package

* [tensorflow object detection api](https://github.com/tensorflow/models/tree/master/research/object_detection)




<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/samirgouda/
[product-screenshot]: images/1.jpg
[screenshot-1]: images/2.jpg
[screenshot-2]: images/3.jpg
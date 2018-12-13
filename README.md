# :rocket: A Starter Guide to Face Detection & Recognition in Python :snake:

[![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/)
[![MIT license](https://img.shields.io/badge/License-MIT-blue.svg)](https://lbesson.mit-license.org/)

## How to Use this repo
1. Clone this repo:
```
$ git clone https://github.com/ohjho/starter_guide_img_recog.git
$ cd start_guide_img_recog
```
2. install the requirements. We **highly recommend** doing this inside a [virtualenv](https://virtualenvwrapper.readthedocs.io/en/latest/):
```
$ pip install -r _text_files/requirements.txt
```
and just check and resolve any packages dependency issues if any show up under `pip check`. It should say `No broken requirements found.`

3. Start Jupyter notebook
```
$ cd _templates
$ jupyter notebook
```
4. Have fun and go build some awesome projects! :surfer:
---
## :camera: What is Face Detection and Recognition
### A Brief History
### Face Detection & Recognition Now

#### OpenCV
Standing for Open Source Computer Vision, written originally in C/C++ but now with binding for Python.

The algorithm breaks the task of identifying a face into thousands of **classification** tasks. For a face, that's about 6000 classifier so for computational speed OpenCV uses a **cascade** model. The **cascade** model breaks the task of thousands of **classifications** into multiple stages. Doing rough and quick test at the earlier stages and only drilling down into the details, at later stages, if an image made it pass the early stages.

In practice, the **cascades** are a bunch of XML files pre-trained to identify specific features from faces to eyes to hands to even non-human things.

### Installing the Required Packages
#### openCV
`requirements.txt` will install `opencv-contrib-python` for you. For more details, read this [installation guide](https://www.pyimagesearch.com/2018/09/19/pip-install-opencv/).
#### face_detection/dlib
[`dlib`][url_dlib] is written in **C++**, so in order to use it we need to clone the [`dlib` repo][url_dlib] and compile it in python per this [instruction][url_dlib_installnote](make sure you satisfy the [pre-requisit](#dlib-pre-requisit) ):
```
$ cd to/your/git/dir
$ git clone https://github.com/davisking/dlib.git
$ cd dlib
$ mkdir build; cd build; cmake ..; cmake --build .
$ cd ..
$ python3 setup.py install
```
##### dlib Pre-requisit
* you need to have **Python3** installed. To check, type `which python3` in your command-line
* you need to have [**Homebrew**](https://brew.sh/). To install:
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
* you need to have `cmake`. To install: `brew install cmake`
#### yolo3

---
## :clipboard: Boilerplates
What to start working on an Image Recognition project?!

Here are some **templates** to get yous started:
* [OpenCV](_templates/opencv_facedetection.ipynb)
* [YOLO3]()

---
## References

### Tutorials
* An Intro [video by YoutTube star Siraj Raval](https://www.youtube.com/watch?v=4eIBisqx9_g&amp=&t=1116s)
* [Face Detection for Beginners](https://towardsdatascience.com/face-detection-for-beginners-e58e8f21aad9)
* [Methods for Face Detection and Face Recognition - A Review](https://medium.com/beesightsoft/methods-for-face-detection-and-face-recognition-a-review-57e73af1d67)
* [Building a Face Detection Model from Video using Deep Learning](https://www.analyticsvidhya.com/blog/2018/12/introduction-face-detection-video-deep-learning-python/)
#### Open CV
* [Face Recognition with Python, in Under 25 Lines of Code](https://realpython.com/face-recognition-with-python/)
* [Using OpenCV to play "Where's Waldo?"](https://machinelearningmastery.com/using-opencv-python-and-template-matching-to-play-wheres-waldo/)
* [OpenCV Face Recognition](https://www.pyimagesearch.com/2018/09/24/opencv-face-recognition/)
#### YOLO
* [YOLO: Real-time Object Detection](https://pjreddie.com/darknet/yolo/)

### Libraries
* [dlib][url_dlib]
* [face_recognition][url_facerecog]

### Documentations
* [dlib](http://dlib.net/)
* [OpenCV](https://docs.opencv.org/3.4.3/de/d27/tutorial_table_of_content_face.html)

---
## :black_nib: License
The content of this project is licensed under the [MIT license](_text_files/LICENSE)

[url_dlib]: https://github.com/davisking/dlib/
[url_dlib_installnote]: https://gist.github.com/ageitgey/629d75c1baac34dfa5ca2a1928a7aeaf
[url_facerecog]: https://github.com/ageitgey/face_recognition

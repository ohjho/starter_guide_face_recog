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
[Placeholder: write something on history to give some context to how awesome it is to have these recognition tools right in python]

### Face Detection
Detecting a face is generally easier than recognising a face of a specific person. The structure of a human face usually contains noses, eyes, foreheads, chins and mouths. All of these compose the general structure of a face.

Given an image, tell whether there is any human face, if there is, where is it (or where they are).

#### Face Detection Methods
* Viola-Jones Method (aka Haar Cascades)  
This is a over-simplified description of the Haar Cascades. 
Please refer to https://opencv-python-tutroals.readthedocs.io/en/latest/py_tutorials/py_objdetect/py_face_detection/py_face_detection.html#haar-cascade-detection-in-opencv for a details. 

![harr-cascades](https://docs.opencv.org/3.4/haar.png)

In short, the Haar Cascades 
The following figures shows how Harr Cascades identify features from a human face.
<img src='http://eyalarubas.com/images/face-detection-and-recognition/features-eyebrows.jpg' height='100'>
<img src='http://eyalarubas.com/images/face-detection-and-recognition/features-nose.jpg' height='100'>
<img src='http://eyalarubas.com/images/face-detection-and-recognition/haar-eyes.jpg' height='100'>
<img src='http://eyalarubas.com/images/face-detection-and-recognition/features-mouth.jpg' height='100'>
<img src='http://eyalarubas.com/images/face-detection-and-recognition/features-chin.jpg' height='100'>
Each of these figures represents a general feature of a human face. Combining all the features together we receive a  minecraft-like resemble of a human face.
<img src='http://eyalarubas.com/images/face-detection-and-recognition/haar-all.jpg' height = '100'>

In order for this process be quick, it is designed it in such a way that we first check the coarse features which represent the coarse structure of a face; and only if these features match, we continue to the next iteration and use finer features. 
In each such iteration we can quickly reject areas of the picture which do not match a face, and keep checking those which we are not sure about. 
In every iteration we increase the certainty that the checked area is indeed a face, until finally we stop and make our determination.

The cascading process accelerates the face detection process by quickly eliminates images that does not contain a face rather than focusing in determining if the image does contain a face. 


* Histogram of Oriented Gradients (HOG)  
<img src='https://cdn-images-1.medium.com/max/800/1*6xgev0r-qn4oR88FrW6fiA.png' height='300'>

* Facial Landmark Detection  
<p>
<img src='https://www.pyimagesearch.com/wp-content/uploads/2017/04/facial_landmarks_68markup-768x619.jpg' width='250' />
<img src='https://www.pyimagesearch.com/wp-content/uploads/2017/04/facial_landmarks_dlib_example.jpg' width= '250' />
</p>  

* Deep Learning

### Face Recognition
A set of two task:
* Face Identification: Given a face image that belongs to a person in a database, tell whose image it is.
* Face Verification: Given a face image that might not belong to the database, verify whether it is from the person it is claimed to be in the database.  

### Difference between Face Detection and Recognition
Detection – two-class classification
* Face vs. Non-face  
Recognition – multi-class classification
* One person vs. all the others

### Face Recognition Applications
* Facial Authentication
* Customer Service
* Retail, Marketing
* Security, Criminal Identification  
etc...

### Face Detection & Recognition Now
#### OpenCV
Standing for Open Source Computer Vision, written originally in C/C++ but now with binding for Python.

The algorithm breaks the task of identifying a face into thousands of **classification** tasks. For a face, that's about 6000 classifier so for computational speed OpenCV uses a **cascade** model. The **cascade** model breaks the task of thousands of **classifications** into multiple stages. Doing rough and quick test at the earlier stages and only drilling down into the details, at later stages, if an image made it pass the early stages.

In practice, the **cascades** are a bunch of XML files pre-trained to identify specific features from faces to eyes to hands to even non-human things.
#### YOLO
[Placeholder: write a high-level summary of what YOLO is]
#### DLIB
[Placeholder: write a high-level summary of what DLIB is]

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

# :camera: What is Face Detection and Recognition
## A Brief History [(ref)](https://www.facefirst.com/blog/brief-history-of-face-recognition-software/)
* 1960s: Woodrow Wilson Bledsoe invented the **RAND tablet**
* 1970s: Goldstein, Harmon, and Lesk proposed **21 Facial Markers**
* 1988: Sirovich and Kirby applied linear algebra to facial recognition creating **Eigenfaces**
* 1991: Turk and Pentland applied Eigenface within images to do the **first automatic face recognition**
* 1990s: **FERET program** created by the US government to encourage commercial face recognition technology to develop. The project create a dataset of 2000+ facial images
* 2002: law enforcement tested facial recognition at **Supe bowl XXXV** with limited success.
* 2000s: **FRVT program** formed by the US government to evaluate commercial facial recognition systems, mainly to help law enforcement agencies when selecting which technology to use.
* 2009: the Pinellas County Sherriff's Office created a **forensic database** which by 2011 aided in many arrest by deputies outfitted with cameras.
* 2010: **Facebook** launched the feature to suggest photo tag
* 2011: Panama, with the backing of US's Homeland Security, launched **FaceFirst**, the first major installation of face recognition in an airport. The system was successful in helping catch various drug traffickers.
* 2011: facial recognition technology was used to confirm the identity of **Osama Bin Laden** in the successful raid by US Navy Seals.
* 2014: US law enforcement agencies adopt mobile face recognition at scale.
* 2017: **iPhone X** uses facial recognition for device security and payment
* 2017: FaceFirst launched **Watchlist as a service** to help retail clients prevent shoplifting and violent crime.

## Face Detection vs Face Recognition
**Detection** is a two-class classification: Face vs. Non-face  

In contrast, **Recognition** is a multi-class classification: One-face vs. All Faces

## Face Detection
Detecting a face is generally easier than recognising the face of a specific person. The structure of a human face usually contains noses, eyes, foreheads, chins and mouths. All of these compose the general structure of a face.

### Face Detection Methods
#### Viola-Jones Method (aka Haar Cascades), 2001  
![harr-cascades](https://docs.opencv.org/3.4/haar.png)  

The following figures shows how Harr Cascades identify features from a human face.  
<p>
<img src='http://eyalarubas.com/images/face-detection-and-recognition/features-eyebrows.jpg' height='100'>
<img src='http://eyalarubas.com/images/face-detection-and-recognition/features-nose.jpg' height='100'>
<img src='http://eyalarubas.com/images/face-detection-and-recognition/haar-eyes.jpg' height='100'>
<img src='http://eyalarubas.com/images/face-detection-and-recognition/features-mouth.jpg' height='100'>
<img src='http://eyalarubas.com/images/face-detection-and-recognition/features-chin.jpg' height='100'>
</p>

Each of these figures represents a general feature of a human face. Combining all the features together we receive a  minecraft-like resemble of a human face.  
<img src='http://eyalarubas.com/images/face-detection-and-recognition/haar-all.jpg' height = '100'>  

In order for this process be quick, it is designed it in such a way that we first check the coarse features which represent the coarse structure of a face; and only if these features match, we continue to the next iteration and use finer features. In each such iteration we can quickly reject areas of the picture which do not match a face, and keep checking those which we are not sure about. In every iteration we increase the certainty that the checked area is indeed a face, until finally we stop and make our determination.  

The cascading process accelerates the face detection process by quickly eliminates images that does not contain a face rather than focusing in determining if the image does contain a face.  

For details, please refer to [this documentation](https://opencv-python-tutroals.readthedocs.io/en/latest/py_tutorials/py_objdetect/py_face_detection/py_face_detection.html#haar-cascade-detection-in-opencv).

#### Histogram of Oriented Gradients (HOG), 2005  
<img src='https://cdn-images-1.medium.com/max/800/1*6xgev0r-qn4oR88FrW6fiA.png' height='300'>

#### Facial Landmark Detection  
<p>
<img src='https://www.pyimagesearch.com/wp-content/uploads/2017/04/facial_landmarks_68markup-768x619.jpg' width='250' />
<img src='https://www.pyimagesearch.com/wp-content/uploads/2017/04/facial_landmarks_dlib_example.jpg' width= '250' />
</p>  

#### Deep Learning, 2012
Using pre-trained Convolutional Neural Networks (CNN) like **VGG** or **Inception** classifier and running it on a small sliding window across the given image. At each step we get a prediction of what's within the window. And at a given threshold, we only keep the classified objects with high predictive values.

![CNN Sliding Windown](https://cv-tricks.com/wp-content/uploads/2016/12/3.png.pagespeed.ce.nvAm4I5IA0.png)

#### R-CNN
An improvement on basic CNN, it split the task of image detection into **region proposal** and **classification**. The **region proposal** uses **selective search**.

**Selective search** [(ref)](https://www.learnopencv.com/selective-search-for-object-detection-cpp-python/) starts by over-segmenting the image based on intensity of the pixels using a segmentation method.
<p>
<img src='https://www.learnopencv.com/wp-content/uploads/2017/09/breakfast.jpg' width='250' />
<img src='https://www.learnopencv.com/wp-content/uploads/2017/09/breakfast_fnh.jpg' width= '250' />
</p>  

Then it...
1. Add bounding boxes corresponding to the segmented parts to the list of regional proposals
2. Group adjacent segments based on similarity (color, texture, size, and shape)
3. repeat step 1 with bigger bounding boxes for bigger segments

![selective search](https://www.learnopencv.com/wp-content/uploads/2017/09/hierarchical-segmentation-1.jpg)

## Face Recognition
Face Recognition is a two step process:
1. Face Identification: Given a face image that belongs to a person in a database, tell whose image it is.
2. Face Verification: Given a face image that might not belong to the database, verify whether it is from the person it is claimed to be in the database.  

### Applications
* Facial Authentication (e.g. mobile phone lock)
* Law enforcement
* Airport security
* Customer Service (e.g. Smile to Pay)
* Retail (e.g. Loss Prevention)
* and more!

## Face Detection & Recognition Now
This section discuss the most commonly used algorithm today.
### OpenCV
Standing for Open Source Computer Vision, written originally in C/C++ but now with binding for Python.

The algorithm breaks the task of identifying a face into thousands of **classification** tasks. For a face, that's about 6000 classifier so for computational speed OpenCV uses a **cascade** model. The **cascade** model breaks the task of thousands of **classifications** into multiple stages. Doing rough and quick test at the earlier stages and only drilling down into the details, at later stages, if an image made it pass the early stages.

In practice, the **cascades** are a bunch of XML files pre-trained to identify specific features from faces to eyes to hands to even non-human things.
### YOLO
[Placeholder: write a high-level summary of what YOLO is]
### DLIB
[Placeholder: write a high-level summary of what DLIB is]

## Installing the Required Packages
### openCV
`requirements.txt` will install `opencv-contrib-python` for you. For more details, read this [installation guide](https://www.pyimagesearch.com/2018/09/19/pip-install-opencv/).
### face_detection/dlib
[`dlib`][url_dlib] is written in **C++**, so in order to use it we need to clone the [`dlib` repo][url_dlib] and compile it in python per this [instruction][url_dlib_installnote](make sure you satisfy the [pre-requisit](#dlib-pre-requisit) ):
```
$ cd to/your/git/dir
$ git clone https://github.com/davisking/dlib.git
$ cd dlib
$ mkdir build; cd build; cmake ..; cmake --build .
$ cd ..
$ python3 setup.py install
```
#### dlib Pre-requisit
* you need to have **Python3** installed. To check, type `which python3` in your command-line
* you need to have [**Homebrew**](https://brew.sh/). To install:
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
* you need to have `cmake`. To install: `brew install cmake`
### yolo3

[url_dlib]: https://github.com/davisking/dlib/
[url_dlib_installnote]: https://gist.github.com/ageitgey/629d75c1baac34dfa5ca2a1928a7aeaf

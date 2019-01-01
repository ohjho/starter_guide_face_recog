# :camera: What is Face Detection and Recognition
## A Brief History
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

---

## Face Detection vs Face Recognition
**Detection** is a two-class classification: Face vs. Non-face  

In contrast, **Recognition** is a multi-class classification: One-face vs. All Faces

## Face Detection
Face detection is the process of finding faces in pictures or videos (recorded or real time). It has already been implemented to areas such as auto focusing camera.

Detecting a face is generally easier than recognising the face of a specific person. All human faces shares some universal properties. For example, the eyes region is relatively darker than its neighbour pixels; and the nose and forehead region is brighter.  

Therefore face detection algorithm searches general human face features as segments in the whole image.

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

Each of these figures represents a general feature of a human face. Combining all the features together we receive a  Minecraft-like resemble of a human face.  

<img src='http://eyalarubas.com/images/face-detection-and-recognition/haar-all.jpg' height = '100'>  

In order for this process be quick, it is designed in such a way that we first check the coarse features which represent the structure of a face; and only if these features match, we continue to the next iteration and use finer features. In each iteration we can quickly reject areas of the picture which do not match a face, and keep checking those which we are not sure about. In every iteration we increase the certainty that the checked area is indeed a face, until finally we stop and make our determination.  

<img src='https://www.bogotobogo.com/python/OpenCV_Python/images/FaceDetection/stages.png' height = '300'>

The cascading process accelerates the face detection process by quickly eliminates images that does not contain a face rather than focusing in determining if the image does contain a face.  

For details, please refer to [this documentation](https://opencv-python-tutroals.readthedocs.io/en/latest/py_tutorials/py_objdetect/py_face_detection/py_face_detection.html#haar-cascade-detection-in-opencv).

#### Histogram of Oriented Gradients (HOG), 2005  
Histogram of Oriented Gradients is a **feature descriptor** used in image processing, mainly for **object detection**. It was invented by [Navneet Dalal and Bill Triggs](https://lear.inrialpes.fr/people/triggs/pubs/Dalal-cvpr05.pdf) and was originally used for **detecting pedestrian**.

The goal of HOG is to create a feature descriptor, that is a representation of an image or an image patch that simplifies the image by extracting useful information and throwing away extraneous information. We can later compare two descriptors to see if they depict the same object. It usually takes the form of a **vector**.

**The advantage of analyzing gradients over pixels**  
If we analyze pixels directly, the **pixel values** for dim images and bright images of the same person will be totally different. But by only considering the direction that brightness changes(**gradients**), both bright and dim images will end up with the same exact representation.

To find faces in an image, photo is first converted to **black and white** as colour data is not needed. For every single pixel, we want to look at the pixels that directly surrounding it.  

<img src = 'https://cdn-images-1.medium.com/max/800/1*RZS05e_5XXQdofdRx1GvPA.gif' height='200'>

Then we compare the darkness of current pixels with those directly surrounding it. We will then draw an arrow showing in which direction the image is **getting darker**.  

<img src = 'https://cdn-images-1.medium.com/max/800/1*WF54tQnH1Hgpoqk-Vtf9Lg.gif' height='200'>

By repeat that process for every single pixel in the image, we replace every pixel by an arrow. These arrows are called **gradients** and they show the flow from light to dark across the entire image.  

<img src='https://bit.ly/2Lusa3r' height='200'>

The image is splitted into small squares of 16x16 pixels. In each square, we’ll count up how many gradients point in each major direction and the square is replaced by the arrow directions that are the strongest. The original image is converted into simple representation that captures **basic structure** of a face in a simple way. Detecting faces means find the part of our image that looks the most similar to a known HOG pattern that was extracted from a bunch of other training faces:  
<img src='https://cdn-images-1.medium.com/max/800/1*6xgev0r-qn4oR88FrW6fiA.png' height='300'>

#### Facial Landmark Detection, 2014
After we can isolate the faces in an image, we will need to handle the problem that **faces turned sideways** as they look totally different to a computer. Facial Landmark Detection was introduced for the task. There are lots of ways to do face landmark estimation but we are going to use the approach invented by [Vahid Kazemi and Josephine Sullivan](http://www.csc.kth.se/~vahidk/papers/KazemiCVPR14.pdf).

The approach proposed to use **68** specific points (called **landmarks**) to map with the face features. Then a model is built by machine learning (Regression Trees) to find these 68 specific points on any face.  
<p>
<img src='https://www.pyimagesearch.com/wp-content/uploads/2017/04/facial_landmarks_68markup-768x619.jpg' width='200' />
<img src='https://www.pyimagesearch.com/wp-content/uploads/2017/04/facial_landmarks_dlib_example.jpg' width= '200' />
</p>

After we know where the face features are, we can simply rotate, scale and shear the image so that the eyes and mouths are **centered** as best as possible. Hence, now no matter how the face is turned, we are able to transform the face features in the roughly same position in an image.  
<img src='https://cdn-images-1.medium.com/max/800/1*igEzGcFn-tjZb94j15tCNA.png' height='200'>

This enable us to compare and proceed next step much easier, including face recongition, face morphing and replacement, virtual makeover, etc. You can find more detail from article [here](https://www.learnopencv.com/facial-landmark-detection/).

#### Deep Learning, 2012
Using pre-trained Convolutional Neural Networks (CNN) like **VGG** or **Inception** classifier and running it on a small **sliding window** across the given image. At each step we get a prediction of what's within the window. And at a given threshold, we only keep the classified objects with high predictive values.

![CNN Sliding Windown](https://cv-tricks.com/wp-content/uploads/2016/12/3.png.pagespeed.ce.nvAm4I5IA0.png)

#### R-CNN
An improvement on basic CNN, it split the task of image detection into **region proposal** and **classification**. The **region proposal** uses **selective search**.

[**Selective search**](https://www.learnopencv.com/selective-search-for-object-detection-cpp-python/) starts by over-segmenting the image based on intensity of the pixels using a segmentation method.
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

Face Recognition takes one step further than face detection as it recognise the identity of a person given that the algorithm has been on that particular person's face.

A single face should be given as input, and the output will be a name, or class name or unknown face. [PCA, LDA]
One popular recognition algorithm is PCA using eigenfaces.

<img src='http://eyalarubas.com/images/face-detection-and-recognition/eigenfaces.jpg' width='250' />

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

---

## Face Detection & Recognition Now
This section discuss the most commonly used algorithms today.
### OpenCV
OpenCV stands for Open Source Computer Vision, written originally in C/C++ but now with binding for Python.

The algorithm breaks the task of identifying a face into thousands of **classification** tasks. For a face, that's about 6000 classifier so for the sake of computational speed, OpenCV uses a **cascade** model. The **cascade** model breaks the task of thousands of **classifications** into multiple stages. Doing rough and quick test at the earlier stages and only drilling down into the details, at later stages, if an image made it pass the early stages.

In practice, the **cascades** are a bunch of XML files pre-trained to identify specific features from faces to eyes to hands to even non-human things.

### YOLO (v1: 2015, v2: 2016, v3: 2018)
A advance deep learning model for facial detection. It's main advantage is on speed because the algorithm actually only look at the image once. Therefore, it's name: **You Only Look Once**.

A single **trained neural network** that can take the whole image and output all the predictions in a single pass.

YOLO algorithm lay a grid over the image and each cell in the grid does the following:
1. predict some number of bounding boxes and it's confidence level of having an object inside  
<img src='https://cdn-images-1.medium.com/max/800/1*4Y1PaY3ZgxKt5w84_0pNxw.jpeg' width='350' />

2. predict a class probability  
<img src='https://sandipanweb.files.wordpress.com/2018/03/proba_map.png?w=676' width='400' />

Then with a given threshold, YOLO only keeps the bounding boxes with the highest probability  
![yolo combining 1 and 2](https://i.stack.imgur.com/zlhvo.png)

The parameterization fixes the output size for detection. So we have a output tensor which we try to predict in one pass through our neural network.  
![yolo output tensor prediction](https://www.renom.jp/notebooks/tutorial/image_processing/yolo/yolo010.png)  

### DLIB
DLib is a C++ library/toolkit that contains machine learning algorithms, including computer vision, however, you can use a number of its tools from python applications.

Dlib is commonly used for **face detection** and **facial landmark detection**. The face detection works by computing **HOG features** and classifiying them with a **linear SVM**, while facial landmark detection uses **random forests**. Popular face recognition libraries such as [face_recognition](https://github.com/ageitgey/face_recognition) and [openface](https://github.com/cmusatyalab/openface) use dlib underneath.

Dlib also has deep neural network (**DNN**) support to do face recognition. [Example](http://blog.dlib.net/2017/02/high-quality-face-recognition-with-deep.html) shows that the pretrained dlib_face_recognition_resnet_model_v1 model has a 99.38% accuracy on the [Labeled Faces in the Wild](http://vis-www.cs.umass.edu/lfw/).

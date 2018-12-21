---?image=https://source.unsplash.com/ptA_7ODacAk/
@snap[north-east]
### @color[black](A Gentle Introduction to Facial Detention and Recognition)
@snapend
+++?image=https://source.unsplash.com/PR9fXnVzfzw/
@snap[west]
### @color[white](Overview)
@ul
* The Story
* Methods
* Current Landscape
* A gift!
@ulend
@snapend

---?image=https://source.unsplash.com/9pw4TKvT3po/
@snap[north]
### The Story
@snapend
+++
@snap[north-east]
#### 1960s: RAND Tablet
@snapend
+++
@snap[north-east]
#### 1970s: 21 Facial Markers
@snapend
+++
@snap[north-east]
#### 1988: Eigenfaces
@snapend
+++
@snap[north-east]
#### 1991: Turk and Pentland applied Eigenface within images
@snapend
+++
@snap[north-east]
#### 2002: Supe bowl XXXV
@snapend
+++
@snap[north-east]
#### 2010: Facebook
@snapend
+++
@snap[north-east]
#### 2011: Panama
@snapend
+++
@snap[north-east]
#### 2011: Osama Bin Laden
@snapend
+++
@snap[north-east]
#### 2017: iPhone X
@snapend
---?image=https://source.unsplash.com/FRQUz7W1SvI/
@snap[north]
### Methods
@snapend
+++
@snap[north-east]
### Face Detection vs Face Recognition
@snapend

![An awesome image of face detection vs recognition]()
+++
@snap[north-east]
### Face Detection
@snapend
![an awesome face detection image]()
+++
@snap[north-east]
#### Viola-Jones (Haar Cascades) Method, 2001
@snapend
![pictures for haar cascades]()
+++
@snap[north-east]
#### Histogram of Oriented Gradients (HOG), 2005
@snapend
@div[top-50 fragment]
<img src = 'https://cdn-images-1.medium.com/max/800/1*RZS05e_5XXQdofdRx1GvPA.gif' height='200'>
@divend
@div[bottom-50 fragment]
<img src='https://camo.githubusercontent.com/1b13edb3d9be904abce434c7019b7139374604dc/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a5746353474516e48314867706f716b2d567466394c672e676966' height='200'>
@divend
+++
@snap[north-east]
#### Histogram of Oriented Gradients (HOG), 2005
@snapend
<img src='https://cdn-images-1.medium.com/max/800/1*6xgev0r-qn4oR88FrW6fiA.png' height='400'>
+++
@snap[north-east]
#### Facial Landmark Detection, 2014
@snapend
<img src='https://www.pyimagesearch.com/wp-content/uploads/2017/04/facial_landmarks_68markup-768x619.jpg' width='500'>
+++
@snap[north-east]
#### Facial Landmark Detection, 2014
@snapend
![facial landmarks transformation](https://cdn-images-1.medium.com/max/800/1*igEzGcFn-tjZb94j15tCNA.png)
+++
@snap[north-east]
#### Deep Learning, 2012
CNN, Sliding Window
@snapend
@div[bottom-70]
![picture of sliding window](_text_files/pitch_assets/slidingwindow.jpg)
@divend
+++
@snap[north-east]
#### Deep Learning, 2012
R-CNN
@snapend

@div[left-50 fragment]
![picture before segementation](https://camo.githubusercontent.com/41d5328f14cc6b04b6d69e594db6158d59bf8b37/68747470733a2f2f7777772e6c6561726e6f70656e63762e636f6d2f77702d636f6e74656e742f75706c6f6164732f323031372f30392f627265616b666173742e6a7067)
@divend
@div[right-50 fragment]
![picture after segementation](https://camo.githubusercontent.com/79f34d7af94849b6487e8b416a07150a80829b6b/68747470733a2f2f7777772e6c6561726e6f70656e63762e636f6d2f77702d636f6e74656e742f75706c6f6164732f323031372f30392f627265616b666173745f666e682e6a7067)
@divend
+++
@snap[north-east]
#### Deep Learning, 2012
R-CNN
@snapend
![rcnn region proposal](https://camo.githubusercontent.com/2acccab6babe00d58154424a4daabb2e40cd4a10/68747470733a2f2f7777772e6c6561726e6f70656e63762e636f6d2f77702d636f6e74656e742f75706c6f6164732f323031372f30392f68696572617263686963616c2d7365676d656e746174696f6e2d312e6a7067)
+++
@snap[north-east]
### Face Recognition
@snapend
Say something about face recognition

---?image=https://source.unsplash.com/jG1z5o7NCq4/
### Current Landscape
+++
### OpenCV
![An image to explain OpenCV]()
+++
### DLIB
![An image to explain DLIB]()
+++
@snap[north-east]
### YOLO
(v1: 2015, v2: 2016, v3: 2018)
@snapend
@snap[midpoint]
![pic of grid predict boxes](https://camo.githubusercontent.com/fe90ad70fac9bdc955b83d2c02ea7a131bbb9fe7/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a345931506159335a67784b74357738345f30704e78772e6a706567)
@snapend
+++
@snap[north-east]
### YOLO
@snapend
@snap[midpoint]
![pic of grid predict classes](https://camo.githubusercontent.com/9d03c472f9125137829bcd59b26894c1020dc392/68747470733a2f2f73616e646970616e7765622e66696c65732e776f726470726573732e636f6d2f323031382f30332f70726f62615f6d61702e706e673f773d363736)
@snapend
+++
@snap[north-east]
### YOLO
@snapend
@snap[midpoint]
![pic of box + class](https://camo.githubusercontent.com/03122da4a67ccc0ec7902d248895f09cc96e2158/68747470733a2f2f692e737461636b2e696d6775722e636f6d2f7a6c68766f2e706e67)
@snapend
+++
@snap[north-east]
### YOLO
@snapend
@snap[midpoint]
![pic of tensor](https://camo.githubusercontent.com/274fd1443201e847aa67c7c2e01366fa83ceb362/68747470733a2f2f7777772e72656e6f6d2e6a702f6e6f7465626f6f6b732f7475746f7269616c2f696d6167655f70726f63657373696e672f796f6c6f2f796f6c6f3031302e706e67)
@snapend
---?image=https://source.unsplash.com/SBdmQcW8qag/
@snap[north]
### A Gift!
@snapend
[A Starter Guide to Face Detection & Recognition in Python](https://github.com/ohjho/starter_guide_face_recog)

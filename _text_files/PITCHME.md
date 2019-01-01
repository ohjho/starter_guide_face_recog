---?image=https://source.unsplash.com/ptA_7ODacAk/
<!-- Welcome stack
_       __     __                                  __             __  
| |     / /__  / /________  ____ ___  ___     _____/ /_____ ______/ /__
| | /| / / _ \/ / ___/ __ \/ __ `__ \/ _ \   / ___/ __/ __ `/ ___/ //_/
| |/ |/ /  __/ / /__/ /_/ / / / / / /  __/  (__  ) /_/ /_/ / /__/ ,<   
|__/|__/\___/_/\___/\____/_/ /_/ /_/\___/  /____/\__/\__,_/\___/_/|_|  

-->
@snap[north-east]
### @color[black](A Gentle Introduction to Facial Detection and Recognition)
@snapend
+++?image=https://source.unsplash.com/PR9fXnVzfzw/
@snap[west]
### @color[white](Overview)
@ul
* The Story
* Methods
* Current Landscape
* @fa[gift fa-1x]
@ulend
@snapend

---?image=https://source.unsplash.com/9pw4TKvT3po/
<!-- History stack


    __  ___      __                           __             __  
   / / / (_)____/ /_____  _______  __   _____/ /_____ ______/ /__
  / /_/ / / ___/ __/ __ \/ ___/ / / /  / ___/ __/ __ `/ ___/ //_/
 / __  / (__  ) /_/ /_/ / /  / /_/ /  (__  ) /_/ /_/ / /__/ ,<   
/_/ /_/_/____/\__/\____/_/   \__, /  /____/\__/\__,_/\___/_/|_|  
                            /____/                               


-->
@snap[north]
### The Story
@snapend
+++
@snap[north-east]
#### 1960s: RAND Tablet
@snapend
<br /><br />
<img src='https://wwwassets.rand.org/content/rand/blog/rand-review/2018/09/the-rand-tablet-ipad-predecessor/jcr:content/par/blogpost.aspectcrop.868x455.lm.jpg/x1536275788752.jpg.pagespeed.ic.CPtrA8fIFT.jpg' height='450' />
+++
@snap[north-east]
#### 1970s: 21 Facial Markers
@snapend
<br />
<img src='https://cdn-images-1.medium.com/max/600/0*IuKHrWCDkC8baWsD.png' height='450' />
+++
@snap[north-east]
#### 1988: Eigenfaces
@snapend
<br />
![pic of eigenfaces](https://cdn-images-1.medium.com/max/600/0*FmfgrEtBOB6slWiH.jpg)
+++
@snap[north-east]
#### 1991: Turk and Pentland applied Eigenface within images
@snapend
<br /><br />
<img src='https://image.slidesharecdn.com/eigenfaces-140124151754-phpapp01/95/eigenfaces-2-638.jpg?cb=1390576732' height = '450' />
+++
@snap[north-east]
#### 2002: Super bowl XXXV
@snapend
<br />
<img src='https://www.tampabay.com/storyimage/HI/20180430/ARTICLE/304309783/AR/0/AR-304309783.jpg&MaxW=1200&Q=66' height = '450' />
+++
@snap[north-east]
#### 2010: Facebook
@snapend
<br />
<img src='https://cdn-images-1.medium.com/max/600/0*ty_lPs0wP35t1XxH' height='350'/>
+++
@snap[north-east]
#### 2011: Panama
@snapend
<br/>
![pic of pananma airport](http://pty.life/wp-content/uploads/2015/01/tocumen_airport.jpg)
+++
@snap[north-east]
#### 2011: Osama Bin Laden
@snapend
<br/>
<img src='https://www.moviequotesandmore.com/wp-content/uploads/zero-dark-thirty-15.jpg' height='450' />
+++
@snap[north-east]
#### 2017: iPhone X
@snapend
<br />
![pic of iphone x](https://support.apple.com/library/content/dam/edam/applecare/images/en_US/iOS/ios12-iphone-x-face-id-hero.jpg)

---?image=https://source.unsplash.com/FRQUz7W1SvI/
<!-- Method stack


    __  ___     __  __              __        __             __  
   /  |/  /__  / /_/ /_  ____  ____/ /  _____/ /_____ ______/ /__
  / /|_/ / _ \/ __/ __ \/ __ \/ __  /  / ___/ __/ __ `/ ___/ //_/
 / /  / /  __/ /_/ / / / /_/ / /_/ /  (__  ) /_/ /_/ / /__/ ,<   
/_/  /_/\___/\__/_/ /_/\____/\__,_/  /____/\__/\__,_/\___/_/|_|  



-->
@snap[north]
### Methods
@snapend
+++
@snap[north-east]
### Face Detection vs Face Recognition
@snapend
<br />
@div[left-50 fragment]
<img src = 'https://www.mantra.ai/wp-content/uploads/2018/09/Face-detection.png' width = '500' />
@divend
@div[right-50 fragment]
<img src = 'https://www.mantra.ai/wp-content/uploads/2017/06/faceRecognition.jpg' width = '500' />
@divend
+++
@snap[north-east]
### Face Detection
@snapend
<br />
<img src = 'https://www.mantra.ai/wp-content/uploads/2018/09/Face-detection.png' height = '400' />
+++
@snap[north-east]
#### Viola-Jones (Haar Cascades) Method, 2001
@snapend
<img src = 'https://docs.opencv.org/3.4/haar.png' height = '300' />
+++
@snap[north-east]
#### Viola-Jones (Haar Cascades) Method, 2001
@snapend
@div[left-20 fragment]
<img src='http://eyalarubas.com/images/face-detection-and-recognition/features-eyebrows.jpg' height='250'>
@divend
@div[left-20 fragment]
<img src='http://eyalarubas.com/images/face-detection-and-recognition/features-nose.jpg' height='250'>
@divend
@div[left-20 fragment]
<img src='http://eyalarubas.com/images/face-detection-and-recognition/haar-eyes.jpg' height='250'>
@divend
@div[left-20 fragment]
<img src='http://eyalarubas.com/images/face-detection-and-recognition/features-mouth.jpg' height='250'>
@divend
@div[left-20 fragment]
<img src='http://eyalarubas.com/images/face-detection-and-recognition/features-chin.jpg' height='250'>
@divend
+++
@snap[north-east]
#### Viola-Jones (Haar Cascades) Method, 2001
@snapend
<img src='http://eyalarubas.com/images/face-detection-and-recognition/haar-all.jpg' height = '250'>  
+++
@snap[north-east]
#### Viola-Jones (Haar Cascades) Method, 2001
@snapend
<br />
<img src='https://www.bogotobogo.com/python/OpenCV_Python/images/FaceDetection/stages.png' height = '400'>
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

<br/><br/>
![picture of sliding window](_text_files/pitch_assets/slidingwindow.jpg)
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
<br />
<img src = 'https://www.mantra.ai/wp-content/uploads/2017/06/faceRecognition.jpg' height = '350' />

---?image=https://source.unsplash.com/jG1z5o7NCq4/
<!-- Algo stack


    ___    __                    __             __  
   /   |  / /___ _____     _____/ /_____ ______/ /__
  / /| | / / __ `/ __ \   / ___/ __/ __ `/ ___/ //_/
 / ___ |/ / /_/ / /_/ /  (__  ) /_/ /_/ / /__/ ,<   
/_/  |_/_/\__, /\____/  /____/\__/\__,_/\___/_/|_|  
         /____/                                     

-->
### Current Landscape
+++
@snap[north-east]
### OpenCV
@snapend
@div[left-50 fragment]
<img src = 'https://www.superdatascience.com/wp-content/uploads/2017/07/False-Positive-1.png' width = '500' />
@divend
@div[right-50 fragment]
<img src = 'https://www.superdatascience.com/wp-content/uploads/2017/07/False-Positive-Fix.png' width = '500' />
@divend
+++
@snap[north-east]
### DLIB
@snapend
<br /><br />
<img src = 'http://dlib.net/ml_guide.svg' height = '500'>
+++
@snap[north-east]
### DLIB
@snapend
@div[left-50 fragment]
<img src='http://1.bp.blogspot.com/-pPgDErLVJ_k/UvBGZk22ZXI/AAAAAAAAALs/c0mJmAVZnQE/s1600/face_fhog_filters.png' height = '300'>
@divend
@div[right-50 fragment]
<img src='https://i.stack.imgur.com/9bUgR.png' height = '300'>
@divend
+++
@snap[north-east]
### YOLO
@size[0.5em](v1: 2015, v2: 2016, v3: 2018)
@snapend
<br/><br/><br/>
<img src='https://camo.githubusercontent.com/fe90ad70fac9bdc955b83d2c02ea7a131bbb9fe7/68747470733a2f2f63646e2d696d616765732d312e6d656469756d2e636f6d2f6d61782f3830302f312a345931506159335a67784b74357738345f30704e78772e6a706567' height = '450' />
+++
@snap[north-east]
### YOLO
@snapend
<br/><br/>
<img src='https://camo.githubusercontent.com/9d03c472f9125137829bcd59b26894c1020dc392/68747470733a2f2f73616e646970616e7765622e66696c65732e776f726470726573732e636f6d2f323031382f30332f70726f62615f6d61702e706e673f773d363736' width = '600' />
+++
@snap[north-east]
### YOLO
@snapend
<br/><br/>
<img src='https://camo.githubusercontent.com/03122da4a67ccc0ec7902d248895f09cc96e2158/68747470733a2f2f692e737461636b2e696d6775722e636f6d2f7a6c68766f2e706e67' width = '700' />
+++
@snap[north-east]
### YOLO
@snapend
<br/><br/>
<img src='https://camo.githubusercontent.com/274fd1443201e847aa67c7c2e01366fa83ceb362/68747470733a2f2f7777772e72656e6f6d2e6a702f6e6f7465626f6f6b732f7475746f7269616c2f696d6167655f70726f63657373696e672f796f6c6f2f796f6c6f3031302e706e67' width = '700' />
---?image=https://source.unsplash.com/SBdmQcW8qag/
<!-- Outro


   ____        __           
  / __ \__  __/ /__________
 / / / / / / / __/ ___/ __ \
/ /_/ / /_/ / /_/ /  / /_/ /
\____/\__,_/\__/_/   \____/


-->
@snap[north]
### A Gift!
@snapend
@fa[gift fa-3x]( &#8594; ) [@fa[github fa-3x]](https://github.com/ohjho/starter_guide_face_recog)

# :rocket: A Starter Guide to Face Detection & Recognition in Python :snake:

[![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/)
[![MIT license](https://img.shields.io/badge/License-MIT-blue.svg)](https://lbesson.mit-license.org/)

## Intro
To understand what is Facial Detection and/or recognition, you can read our [primer](_text_files/primer.md) or checkout a [the slides]() we made for our data science bootcamp presentation.

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
and just check and resolve any packages dependency issues if they show up under `pip check`. It should say `No broken requirements found.`

3. Start Jupyter notebook
```
$ cd _templates
$ jupyter notebook
```
4. Have fun and go build some awesome projects! :surfer:

## :clipboard: Boilerplates
Want to start working on an Image Recognition project?!

Here are some **templates** to get yous started:
* [OpenCV](_templates/opencv_facedetection.ipynb)
* [YOLO3]()

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

## :pray: Credits
This project's main contributors are [@youonf](https://github.com/youonf) and [@agsl0905](https://github.com/agsl0905).

Special Thanks to [@samoshaughnessy](https://github.com/samoshaughnessy) for showing us how to use Git.  

## :black_nib: License
The content of this project is licensed under the [MIT license](_text_files/LICENSE)

[url_dlib]: https://github.com/davisking/dlib/
[url_dlib_installnote]: https://gist.github.com/ageitgey/629d75c1baac34dfa5ca2a1928a7aeaf
[url_facerecog]: https://github.com/ageitgey/face_recognition

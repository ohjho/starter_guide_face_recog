# :rocket: A Starter Guide to Image Recognition in Python :snake:

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
3. Start Jupyter notebook
```
$ cd _templates
$ jupyter notebook
```
4. Have fun and go build some awesome projects! :surfer:
---
## :camera: What is Image Recognition
### A Brief History
### Image Recognition Now
### Installing the Required Packages
#### openCV
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
* [YOLO3]()
* [OpenCV]()
---
## References
* An Intro [video by Youttube star Siraj Raval](https://www.youtube.com/watch?v=4eIBisqx9_g&amp=&t=1116s)

---
## :black_nib: License
The content of this project is licensed under the [MIT license](_text_files/LICENSE)

[url_dlib]: https://github.com/davisking/dlib/
[url_dlib_installnote]: https://gist.github.com/ageitgey/629d75c1baac34dfa5ca2a1928a7aeaf

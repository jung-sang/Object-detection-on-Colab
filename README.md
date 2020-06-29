# Object detection on Colab

## 1. Mount your account on Google

import os
import pathlib
from google.colab import drive
drive.mount('/content/drive')

#### for local computer using Jupyter notebook, need to build virtual environment

conda create -n topyoo pip python=3.6

## 2. Downgrade Tensorflow and Numpy

pip install --upgrade tensorflow==1.14
pip install numpy==1.17.4

#### To check tensorflow version

import tensorflow as tf
print(tf.__version__)

## 3. Install packages

apt-get install protobuf-compiler python-pil python-lxml python-tk
pip install Cython
pip install jupyter
pip install matplotlib
pip install pandas
pip install opencv-python
pip install tf_slim

## 4. upload a folder in directory, content, and then unzip it

cd /content
unzip {your file name}.zip

## 5. Compiling protobuf

cd /content/models/research
protoc object_detection/protos/*.proto --python_out=.*
python setup.py build
python setup.py install


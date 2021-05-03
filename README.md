## Intro

[![Build Status](https://travis-ci.org/thtrieu/darkflow.svg?branch=master)](https://travis-ci.org/thtrieu/darkflow) [![codecov](https://codecov.io/gh/thtrieu/darkflow/branch/master/graph/badge.svg)](https://codecov.io/gh/thtrieu/darkflow)

Real-time object detection and classification. Paper: [version 1](https://arxiv.org/pdf/1506.02640.pdf), [version 2](https://arxiv.org/pdf/1612.08242.pdf).

Read more about YOLO (in darknet) and download weight files [here](http://pjreddie.com/darknet/yolo/). In case the weight file cannot be found, I uploaded some of mine [here](https://drive.google.com/drive/folders/0B1tW_VtY7onidEwyQ2FtQVplWEU), which include `yolo-full` and `yolo-tiny` of v1.0, `tiny-yolo-v1.1` of v1.1 and `yolo`, `tiny-yolo-voc` of v2.


See demo below or see on [this imgur](http://i.imgur.com/EyZZKAA.gif)

<p align="center"> <img src="demo.gif"/> </p>

## Dependencies

Python3, tensorflow 1.0, numpy, opencv 3.

## Citation

```
@article{trieu2018darkflow,
  title={Darkflow},
  author={Trieu, Trinh Hoang},
  journal={GitHub Repository. Available online: https://github. com/thtrieu/darkflow (accessed on 14 February 2019)},
  year={2018}
}
```

### Getting started

You can choose _one_ of the following three ways to get started with darkflow.

1. Just build the Cython extensions in place. NOTE: If installing this way you will have to use `./flow` in the cloned darkflow directory instead of `flow` as darkflow is not installed globally.
    ```
    python3 setup.py build_ext --inplace
    ```

2. Let pip install darkflow globally in dev mode (still globally accessible, but changes to the code immediately take effect)
    ```
    pip install -e .
    ```

3. Install with pip globally
    ```
    pip install .
    ```
### Real Time Automated Number Plate Recognition

Once the cython extensions are in place and built using one of the above commands. 

Please make sure to download the weights from [this link](https://pjreddie.com/media/files/yolov2-tiny.weights) which is taken from the official [yolo webiste](https://pjreddie.com/darknet/yolo/)

Run the ipynb files. I had some dependency issues while running it on my personal machine, but it runs perfectly on Google Colab. 

I suggest you do the same. Upload the file to your google drive and link it to the notebook. 

This system uses darknet and tiny yolo for object detection and tessaract to perform OCR. I have found that on initial training of 24000 iterations, it has performed well enough for a demo. 

This could be used with yolo for commericial applications instead of tiny yolo and with a lot more training. 

That is all

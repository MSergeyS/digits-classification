# __DigitsClassification__
__Handwritten Digits Classification__ : An OpenCV
---

Based on materials from [this tutorial](https://learnopencv.com/handwritten-digits-classification-an-opencv-c-python-tutorial/#disqus_thread).
The inspiration and data for that post comes from the OpenCV tutorial [here](https://docs.opencv.org/3.4/dd/d3b/tutorial_py_svm_opencv.html).
In this tutorial, we will build a simple handwritten digit classifier using [OpenCV](https://opencv.org/).

In that code, a pipeline involved in most traditional computer vision image classification algorithms is implemented.

## __Image Classification Pipeline__

![as](/images/image-classification-pipeline.jpg)

The image above shows that pipeline. In this code, we will use Histogram of Oriented Gradients as the feature descriptor and Support Vector Machine (SVM) as the machine learning algorithm for classification.
This example with code to demonstrated Image Classification use [Histogram of Oriented Gradients (HOG)](https://waksoft.susu.ru/2021/11/01/histogram-of-oriented-gradients/) + [Support Vector Machine (SVM)](https://waksoft.susu.ru/2021/05/27/image-recognition-and-object-detection-part1/).


## __Build application__ (release)
- For build can be used [cmake](https://cmake.org/).

- Install OpenCV](https://docs.opencv.org/4.x/df/d65/tutorial_table_of_content_introduction.html).

- In the terminal you should enter:
```cmd
cd <path/to/your/project>
mkdir build
mkdir results
cd build
cmake -DCMAKE_BUILD_TYPE=Release ..
cmake --build . --config Release
```

## __Run application__ (release)
```cmd
Release/digits-classification.exe
```

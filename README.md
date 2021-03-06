# What is TDY Project? (Tattoo-detector-yolo)
This project uses <a href="https://github.com/pjreddie/darknet">Darknet</a> to blur the tattoos of people in photographs and videos. 

# Requirement
<ul>
    <li> <a href="opencv.org">openCV (4.2.0)</a> </li>
    <li> <a href="python.org">Python (3.8.1)</a> </li>
</ul>

# How to use?
Code Requires some filtering for the execution

# How it works?
The first thing we need is data about a person's tattoo. Data on this is currently available on Instagram and Pinterest. Then labeling with <a href="https://github.com/AlexeyAB/Yolo_mark">Yolo_mark.</a> <br>

In the labeling process, tattoos are divided into human arms, legs, chest, abdomen and neck. The labeling was done with the exception of a few photos that I think are too many and difficult to distinguish. Then you get weights through Colab. <br> <br> 
Some error weights are detected through openCV + Python code. openCV extracts the tattoo and blurs the pixels. After that, the final extraction project through synthesis. <br> <br>
This project is still in progress! So it may not be perfect yet. <br><br>
This document will continue to be updated :)

# Tell me what this file is
x64 is a folder that mainly contains data about AI in Yolo_mark.
<pre>
.
├── LICENSE.fuck
├── README.md
├── detector.py
├── notebook
│   └── tattoo_detector.ipynb
└── x64
    └── Release
        ├── data
        │   ├── img
        │   │   ├── {SKIP - SO MANY FILES ON THIS DIRECTORY...}
        │   ├── obj.data
        │   ├── obj.names
        │   └── train.txt
        ├── train_obj.cmd
        ├── yolo-obj.cfg
        └── yolo_mark.cmd

5 directories, 629 files
</pre>
The data was made, with Yolo_mark where he wanted to judge the authenticity of the label people. , Install Yolo_mark to see the labeling deleted x64 from Yolo_mark. Put it in the x64 folder. <br> <br>
Since it has not been released yet, we will post a download link after all Colab weight calculations have been completed.

# How many Classes?
First we have seven classes. The first thing we did was to go through one class and one "tattoo" class. The result was not good. To compensate for this, we tried to add half. The types of classes are listed below.
<ul>
    <li> chest_tattoo </li>
    <li> leg_tattoo </li>
    <li> arm_tattoo </li>
    <li> back_tattoo </li>
    <li> neck_tattoo </li>
    <li> stomach_tattoo </li>
    <li> etc_tattoo </li>
</ul>
The order of classes should be as above. This can cause errors in the labeled data.

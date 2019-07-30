# Computer Vision - COMS4036A
Lectures and Course Content by [Dr Richard Klein](https://www.wits.ac.za/staff/academic-a-z-listing/k/richardkleinwitsacza/)

# To Do
* [ ] Proofs For Distributions
* [ ] Chapter 3, Conjugacy Questions
* [ ] Distribution Sliders

# Getting Started
To run any of the code in this repository, install the necessary requirements with `conda` by running the following command:
```
conda create --name coms4036 --file requirements.txt 
```
Then run the command `conda activate coms4036` to activate the environment.

To run jupyter notebooks you will have to add the necessary environment's kernel to ipykernel. Ensure that you are within the `coms4036` env, and run the following command:
```
ipython kernel install --user --name=coms4036
```

# Course Outline
This course will provide an introduction to computer vision, with topics including image formation, feature detection, motion estimation, image mosaics, 3D shape reconstruction, and object and face detection and recognition. 

Applications of these techniques include building 3D maps, creating virtual characters, organizing photo and video databases, human computer interaction, video surveillance, automatic vehicle navigation, and mobile
computer vision.
## Textbook
The following book is prescribed. Although a PDF of the book, as well as other resources are available [on the
author’s website](http://www.computervisionmodels.com/).

* S.J.D. Prince, “Computer Vision: Models, Learning, and Inference.” Cambridge University Press, 2012.
* Bibtex:
```bibtex
@book{CV,
    author = {Prince, S.J.D.},
    title= {{Computer Vision: Models Learning and Inference}},
    publisher = {{Cambridge University Press}},
    year = 2012,
}
```
## Objectives
1. Recall, define and discuss the fundamental issues and challenges of computer vision
2. Discuss the strengths and weaknesses of various popular computer vision methods and contrast their efficacy in different situations
3. Demonstrate, discuss, prove and apply the underlying mathematical techniques within the computer vision algorithms
4. Apply practical experience of designing and implementing computer vision systems in real-world applications
5. Consider the issues related to data and labelling problems in computer vision

## Grading
* Projects - 30% - 2 Projects
* Class Tests - 30% - 2 Class Tests incorporating both practical and theoretical aspects
* Exam - 40% - Final exam incorporating both practical and theoretical aspects

## Test Dates
* Class Test 1: 28 August 2019
* Project 1: 11 September 2019
* Project 2: 09 October 2019
* Class Test 2: 16 October 2019
* Exam: TBC
## Syllabus
1. Probability and Distributions
2. Maximum Likelihood, Maximum a Posteriori, Bayesian Inference
3. Modelling Visual Data
4. Image Processing and Feature Extraction
5. The Pinhole Camera
6. Geometric Transformations
7. Shape Models
8. Convolutional Neural Networks
# Computer Vision: models, learning and inference
* Read through Chapter 1, 2 and 3 up to Conjugancy


Complete the following questions:
Chapter 2: 1,2,3,4,6,7,8,9,10 - everything except 5
Chapter 3: 1,2,3,6,8,9,10,11 - 4 if you feel like it, 12 will make you sad

# Chapter 1
Introduction, not that important.

* The goal of computer vision is to extract useful information from images. 


Here is the textbook structure:
![Tex](tex.png)

* Almost all models for computer vision can be interpreted in a probabilistic context.
* Why is probability a suitable language to describe CV problems?
  * The 3D world is projected onto a 2D set of measurements. However, it is not exact and there is noise. This noise must be described, and probability is used for that.
  * The relationship between world and measurements is generally many to one: there are many real-world configurations that are compatible with the same measurements. The chance that each of these possible worlds is present can also be described using probability.

# Chapter 2
Introduction to probability

## Random Variables
* Random variable $x$ denotes a quantity that is uncertain.
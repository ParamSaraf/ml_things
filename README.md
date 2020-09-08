<h3 align="center">
<p>Machine Learning Things
</h3>


<p align="center">
    <br>
    <img src="https://previews.123rf.com/images/djvstock/djvstock1609/djvstock160900168/62105361-laptop-gear-tools-developer-web-responsive-development-website-programming-icon-set-colorful-design-.jpg" width="300"/>
    <br>
<p>

[![Generic badge](https://img.shields.io/badge/Working-Progress-red.svg)]()
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Generic badge](https://img.shields.io/badge/Updated-Sep_2020-yellow.svg)]()
[![Generic badge](https://img.shields.io/badge/Website-Online-green.svg)]()

**Machine Learning Things (ml_things)** is a lightweight python library that contains functions and code snippets that 
I use in my everyday research with Machine Learning, Deep Learning, NLP.

I created this repo because I was tired of always looking up same code from older projects. 
By making this available to everyone it gives me easy access to some code I use frequently but also make it available for others in my situation. 
If you find any issues please feel free to open an issue.

This library also contains Python code snippets that can speed up Machine Learning workflow.

## Installation

I tested this repo with Python 3.6+.

It's always good practice to install `ml_things` in a [virtual environment](https://docs.python.org/3/library/venv.html). If you guidance on using Python's virtual environments you can check out the user guide [here](https://packaging.python.org/guides/installing-using-pip-and-virtual-environments/).

You can install `ml_things` with pip from GitHub:

```bash
pip install git+https://github.com/gmihaila/ml_things
```

## Functions

### pad_array

`def pad_array(variable_length_array, fixed_length=None, axis=1)` [[source]](https://github.com/gmihaila/ml_things/blob/6a4e345a5d26b9c8caeb76f5cca30d42c1a1b2a4/src/ml_things/padding.py#L20)


Pad variable length array to a fixed numpy array.
It can handle single arrays [1,2,3] or nested arrays [[1,2],[3]].

Parameters:
  variable_length_array: Single arrays [1,2,3] or nested arrays [[1,2],[3]].

  fixed_length: max length of rows for numpy.

  axis: directions along rows: 1 or columns: 0
:return:
  numpy_array:  axis=1: fixed numpy array shape [len of array, fixed_length].
                axis=0: fixed numpy array shape [fixed_length, len of array].

```python
>>> from ml_things import pad_array

>>> pad_array(variable_length_array=[[1,2],[3],[4,5,6]], fixed_length=5)

array([[1., 2., 0., 0., 0.],
       [3., 0., 0., 0., 0.],
       [4., 5., 6., 0., 0.]])
```
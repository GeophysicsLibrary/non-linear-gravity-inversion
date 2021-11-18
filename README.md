# Practical non-linear gravity inversion

**Author:** [Leonardo Uieda](https://www.leouieda.com/)<sup>1</sup>

> <sup>1</sup> Department of Earth, Ocean and Ecological Sciences,
> School of Environmental Sciences, University of Liverpool, UK

## About

Inverse problems abound in geophysics.
It is the primary way in which we investigate the subsurface of the Earth,
which is largely inaccessible to us beyond the first dozen or so kilometers.
From measurements acquired on land, sea, air, and from space, geophysicists
tease out the inner structure of the Earth - from a few meters to thousands of
kilometers deep in the inner core.
Observations of disturbances in the Earth's gravity field are one of the key
elements used by geophysicists to investigate the crust-mantle interface, the
large-scale structure of sedimentary basins (which are reservoirs for water and
hydrocarbons), and even the mass balance of the world's ice sheets.
However, the gravity inverse problem is particularly challenging due to the
physics of potential fields.
Unique solutions are difficult to come by and only exist under strict
assumptions, which often don't hold for real world scenarios.
For these problems, regularization plays a critical role and has been the focus
of much research in the past 20 years.

In this tutorial, we will work together to solve a 2D gravity inverse problem
in Python.
Our code will estimate the shape of a sedimentary basin from gravity
observations.
This non-linear inverse problem will allow us to visually explore the effects
of different types of regularization from a geometric perspective (smoothness,
equality constraints, and more).
We will discuss the challenges involved in real world applications and the
difficulties of quantifying the uncertainty in the solutions.
The main goal of this tutorial is to impart theoretical and practical
skills that can be easily transferred to other domains.

## Learning objectives

This course is designed to empower you to:

* Learn/revise the mathematics of non-linear inverse problems
* Translate mathematical knowledge into code
* Apply non-linear inversion theory to a real geophysical problem
* Analyze the effects of regularization on geophysical models

## Prerequisites

I will assume that you:

* Are comfortable with linear algebra (matrix and vector operations,
  norms, inverses, linear systems, etc)
* Have an understanding of basic calculus (partial derivatives, gradients,
  Taylor series expansions)
* Are able to program a computer to build and manipulate matrices and
  vectors, solve linear systems, and make graphs/plots (in any language
  but Python or Matlab would be best)

## Computer setup

Since there is large component of live coding, participants will
have to set up their computers **before the workshop**. It's
extremely important that everyone has a working Python environment
ahead of time as there will not be enough time to sort out
individual problems during the workshop.

1. **Download and install the Anaconda Python Distribution**.
   Please follow the instructions here:
   https://carpentries.github.io/workshop-template/#python
1. Make sure your installation works by opening JupyterLab through
   the Anaconda Navigator app (on Windows) or by running
   `jupyter lab` in a terminal (Mac/Linux). You browser should
   open with JupyterLab.
1. Brush up on your coding skills with [Software Carpentry's
   Introduction to Python](https://swcarpentry.github.io/python-novice-inflammation/)
   lesson.

We will be using [Jupyter Notebooks](https://jupyter.org/) to run our
Python code and the libraries [numpy](https://numpy.org/),
[scipy](https://www.scipy.org/), and [matplotlib](https://matplotlib.org/).
Anaconda already comes with all of these installed.

## Workshop material

All of the code and notes for this workshop are (or will be) uploaded
to this repository. In here, you'll find:

* `cheatcodes.py`: The ready-made Python functions for forward modelling and
  plotting.
* `gravity-inversion.ipynb`: Jupyter notebook with the code that I wrote live
  in the workshop (not including solutions to exercises).
* `gravity-inversion-solution.ipynb`: Same as the above but with the exercise
  solutions.
* `gravity-inverse-problems-notes.pdf`: Notes and mathematical derivations.

## License

All Python source code in this repository is free software: you can
redistribute it and/or modify it under the terms of the MIT License. A copy of
this license is provided in [LICENSE.txt](LICENSE.txt).

All other materials, including text and images, are distributed under the
[CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/)
license (except where otherwise noted).

Originally developed for a
[short course on geophysical inversion at RWTH Aachen University graduate school IRTG-2379 Modern Inverse Problems](https://github.com/compgeolab/2020-aachen-inverse-problems).

# Minimal monte carlo pi

This is a Monte Carlo simulation estimating Pi - with as little code as possible. It uses NumPy array operations for speed and to keep this code concise.

## Basic concept

In the notebook, the function inside_unit_circle will return true for all points that are inside the unit circle, using Pythagoras to check this.

We then set up a population of random guesses. This is used to create two uniform distributed arrays, x and y, with values between -1 and 1. Each with the same length as the population.

We then use the function inside_unit_circle to check if each point is inside the unit circle, creating two binary arrays, inside and outside.

These arrays can be used with NumPy to address x and y, so we can plot those inside and outside as scatter plots for a simple matplotlib visualisation.

Finally, we take the sum of the inside array, and divide by the total population size. This gives us an estimate of the ratio of points inside the unit circle to the total number of points. Multiplying this by 4 gives us an estimate of Pi.

## Usage

This code is designed to be run in a Jupyter notebook.
The simplest way is to install the requirements in a python interpreter (using a virtual env perhaps?), and load the notebook into VSCode.

A larger population size will give a more accurate estimate of Pi, but will take longer to run.

## Inspiration

I've been working on Monte Carlo simulations with robot localisation and using Ulab, a version of Numpy for CircuitPython for the book [Robotics at Home with Raspberry Pi Pico](https://amzn.eu/d/71zbNBQ).

A mentor at my coder Dojo has created a sheet with a [Monte Carlo simulation estimating Pi](https://github.com/jonathancychow/Monte_Carlo_Simulation_for_Estimating_pi/blob/master/src/estimate_pi_notebook_edu.ipynb). The idea stuck with me.

The code in this repo is not a copy of the code in that workbook, but it is inspired by the ideas from it.

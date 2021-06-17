## package-distributions

### Introduction
In this package, I build a python package which deals with probability distributions. More specifically, I build a class Distribution, then let two classes Gaussian (distribution) and Binomial (distribution) inherit from Distribution. Methods include the following:
* For all distributions:
  * `read_data_file`: read in data from a txt file
  * `calculate_mean`: calculate the mean of the distribution given parameters
  * `calculate_stdev`: calculate the standard deviation of the distribution given parameters
  * `pdf`: return the probability density function of the distribution given parameters
  * `__add__`: add together two distributions (Gaussian + Gaussian, or Binomial + Binomial)
  * `__repr__`: print the characteristics of the distribution
* For Gaussian distributions: 
  * `plot_histogram`: plot a histogram of the data
  * `plot_histogram_pdf`: plot the normalized histogram of the data and probability density function along the same range
* For Binomial distributions:
  * `replace_stats_with_data`: calculate the parameters n and p from data set
  * `plot_bar`: plot a bar chart of the data set
  * `plot_bar_pdf`: plot a bar chart of the probability density function

### Documents
This package includes the following documents:
* `setup.py`: to set up the package
* `test.py`: a test file to see if the code runs without error
* `numbers.txt`: test cases for Gaussian distribution
* `numbers_binomial.txt`: test cases for Binomial distribution
* `distributions`: a directory containing the following:
  * `__init__.py`: to initialize, import Gaussian and Binomial classes
  * `Generaldistribution.py`: containing the class Distribution
  * `Gaussiandistribution.py`: containing the class Gaussian
  * `Binomialdistribution.py`: containing the class Binomial
### Installation
This should run with Python 3.*.

To avoid installing extra package on your local environment, please create a virtual environment to run this package. After this step, you can follow the steps as below:
1. Make sure that you are in the directory where setup.py is.
2. Type `pip install .`.
3. You are now ready to go. To check, you can type `python -m unittest test` to see if the code does run without error.

### Limitation
For simplicity, I assume that the data set for Binomial distribution only contains 0 and 1. The code does not work for other cases.

### Source
This package is an exercise in Udacity Data Scientist Nanodegree Program. The general structure, the test files, and the todo instructions are written by their instructors. I completed the codes.


# NumPy package


![numpy](pic1.png)


My investigation into the numpy random package as a part of Programming for Data analysis, 2019 at Galway - Mayo Institute of Technology. 


# Created by:

Doris Zdravkovic


# Installing NumPy library

In most use cases the best way to install NumPy on your system is by using a pre-built package for your operating system. Please see https://scipy.org/install.html for links to available options.



# Running Jupyter notebook 


1. Enter the startup folder by typing cd /folder_name .
2. Run jupyter notebook command to launch the Jupyter Notebook App. The notebook interface will appear in a new browser window or tab.
3. In the top right corner press New, Python 3 to open new file in jupyter
4. Click ESC and key shortcut m to markdown or double click the text in the cell if you want to edit. 
5. You can run the notebook document step-by-step (one cell a time) by pressing shift + enter.
6. You can run the whole notebook in a single step by clicking on the menu Cell -> Run All.
7. Closing the browser (or the tab) will not close the Jupyter Notebook App. To completely shut it down you need to close the associated terminal.


# Downloading and updating the repository

1. Go to GitHub.
2. Navigate to the main page of the repository: https://github.com/doriszd/numpy-random_new
3. Under the repository name, click Clone or download
4. Save the repository to a local folder location on your computer.
5. Navigate to your target directory in the command line
6. To add new content on gitHub type add .
7. Type git commit -m "Write a message here"
8. To send it to gitHub type git push


# About Matplotlib

Matplotlib is a Python 2D plotting library which produces figures in a variety of hardcopy formats and interactive environments across platforms. Matplotlib can be used in Python scripts, the Python and IPython shells, the Jupyter notebook, web application servers, and four graphical user interface toolkits.You can generate plots, histograms, power spectra, bar charts, errorcharts, scatterplots, etc., with just a few lines of code. find more information about maplotlib here: https://matplotlib.org/



# About Numpy

NumPy (Numerical Python) is a linear algebra library in Python. It is a very important library on which almost every data science or machine learning Python packages such as SciPy (Scientific Python), Matplotlib (plotting library), Scikit-learn, etc depends on to a reasonable extent. NumPy is very useful for performing mathematical and logical operations on Arrays. It provides an abundance of useful features for operations on n-arrays and matrices in Python. Find more information about numpy here: https://docs.scipy.org/doc/numpy-1.15.0/user/index.html



# About Assignment

The aim of this assignment is to: 

1. Explain the overall purpose of the Numpy package.
2. Explain the use of the “Simple random data” and “Permutations” functions. 
3. Explain the use and purpose of at least ﬁve “Distributions” functions. 
4. Explain the use of seeds in generating pseudorandom numbers.


### 1. Purpose of the Numpy package

The focus of this project is to focus on pseudorandom numbers as they are a sample of numbers that look close to true random numbers but are generated using some deterministic process. As computers can not produce random numbers itself, they need packages and algorithms that would deal with it. Numpy.random package is one of the libraries in Python that generates pseudorandom data.

Within the package there are many different functions and distributions. You can find more information about numpy.random package and its features here: https://docs.scipy.org/doc/numpy-1.15.0/reference/routines.random.html#

Some of more important attributes of an ndarray object:

- ndarray.ndim:
This function returns the number of axes or dimensions of the array.
- ndarray.shape:
This function returns the dimensions of the array
- ndarray.size:
This function shows the total number of elements in the array
- ndarray.dtype:
This function describes the type of elements in the array. It tells us if the element is for example integer or float.
- ndarray.itemsize:
This function shows the size in bytes of each element of the array. 


Numpy.random package consists of 4 parts:

1. Simple random data
2. Permutations
3. Distributions
4. Random generator


### 2. “Simple random data” and “Permutations” functions

These are simple random data function that are explained in the notebook in more details. 

1. rand(d0, d1,....dn)  - Random values in a given shape.
2. randn(d0, d1, …, dn) - Return a sample (or samples) from the “standard normal” distribution.
3. randint - Return random integers from low (inclusive) to high (exclusive).
4. random_integers - Random integers of type np.int between low and high, inclusive.
5. random_sample([size]) - Return random floats in the half-open interval [0.0, 1.0).
6. random([size]) - Return random floats in the half-open interval [0.0, 1.0).
7. ranf([size]) - Return random floats in the half-open interval [0.0, 1.0).
8. sample([size]) - Return random floats in the half-open interval [0.0, 1.0).
9. choice(a[, size, replace, p]) - Generates a random sample from a given 1-D array
10. bytes(length) - Return random bytes.

Permutations: there are only 2 functions

1. shuffle(x) - Modify a sequence in-place by shuffling its contents.
2. permutation(x) - Randomly permute a sequence, or return a permuted range.

### 3. Distribution functions

There are many probability distributions, but in this work I will focus on 5 distributions that data scientists find most useful (https://towardsdatascience.com/).

1. Poisson distribution

Poisson Distribution is applicable in situations where events occur at random points of time and space wherein our interest lies only in the number of occurrences of the event. It gives us the probability of a given number of events happening in a fixed interval of time. https://www.statisticshowto.datasciencecentral.com/poisson-distribution/

2. Uniform distribution

The probabilities of getting outcomes from example 1-10 are equally likely and that is the basis of a uniform distribution. The shape of the Uniform distribution curve is rectangular, the reason why Uniform distribution is also called rectangular distribution. 

3. Binominal distribution

A distribution where only two outcomes are possible, such as success or failure, gain or loss, win or lose and where the probability of success and failure is same for all the trials is called a Binomial Distribution. Each trial is independent since the outcome of the previous toss doesn’t determine or affect the outcome of the current toss. 

4. Normal distribution

It represents the behaviour of most of the situations in the universe. That is why it’s called a “normal” distribution. The large sum of (small) random variables often turns out to be normally distributed, contributing to its widespread application. Any distribution is known as Normal distribution if it has the following characteristics:

The mean, median and mode of the distribution coincide.
The curve of the distribution is bell-shaped and symmetrical about the line x=μ.
The total area under the curve is 1.
Exactly half of the values are to the left of the centre and the other half to the right.

5. Exponential distribution

Exponential Distribution is used to model the time taken between the occurrence of different events. We should use exponential distribution when:

You have a lot of events going.
They happen at a certain rate (which does not change over time).
Just because one happened the chances of another one happening don’t change.
https://www.kdnuggets.com/2019/07/5-probability-distributions-every-data-scientist-should-know.html


### 4. Use of seeds in generating pseudorandom numbers

Computers can't produce random numbers itself, they need human help. That is the reason why random numberes are deterministic which means that they operate by a set of rules, and we call them pseudorandom numbers. The pseudorandom number generator is a mathematical function that generates a sequence of nearly random numbers. It takes a parameter to start off the sequence, called the seed.

- Syntax of random.seed()

If the seed=None, then by default, current system time is used. If seed value is in the form of an integer it is used as it is. This method is called when RandomState is initialized. It can be called again to re-seed the generator. RandomState exposes a number of methods for generating random numbers drawn from a variety of probability distributions. In addition to the distribution-specific arguments, each method takes a keyword argument size that defaults to None.

- If size is None, then a single value is generated and returned.
- If size is an integer, then a 1-D array filled with generated values is returned.
- If size is a tuple, then an array with that shape is filled and returned.

https://docs.scipy.org/doc/numpy-1.16.0/reference/generated/numpy.random.RandomState.html#numpy.random.RandomState

# Table of content:

- What are random numbers 
- Numpy package 
  * ndarray.ndim
  * ndarray.shape
  * ndarray.size
  * ndarray.itemsize
  * arange
  
-

# References

https://scipy.org/install.html
https://towardsdatascience.com/lets-talk-about-numpy-for-datascience-beginners-b8088722309f

https://jupyter-notebook.readthedocs.io/en/stable/examples/Notebook/Notebook%20Basics.html
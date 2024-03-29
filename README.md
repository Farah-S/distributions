# fsc-distributions package
Package that contains classes for binomial and gaussian distributions, created while taking the AI Programming with Python - Bertelsmann course on Udacity

## Installation instructions

```sh
pip install fsc_distributions
```

## Gaussian class
Gaussian distribution class for calculating and visualizing a Gaussian distribution.

Attributes:

	mean (float) representing the mean value of the distribution

	stdev (float) representing the standard deviation of the distribution

	data_list (list of floats) a list of floats extracted from the data file


Methods:

	read_data_file(file_name) Function to read in data from a txt file. The txt file should have one number (float) per line. The numbers are stored in the data attribute.
		Args:
			file_name (string): name of a file to read from

		Returns:
			None

	calculate_mean() Function to calculate the mean of the data set.
		Args: 
			None

		Returns: 
			float: mean of the data set

	calculate_stdev(sample=True) Function to calculate the standard deviation of the data set.
		Args: 
			sample (bool): whether the data represents a sample or population

		Returns: 
			float: standard deviation of the data set
			
	plot_histogram() Function to output a histogram of the instance variable data using matplotlib pyplot library.
		Args:
			None
		
		Returns:
			None

	pdf(x) Probability density function calculator for the gaussian distribution.
		Args:
			x (float): point for calculating the probability density function
		
		Returns:
			float: probability density function output
	
	plot_histogram_pdf(n_spaces = 50) Function to plot the normalized histogram of the data and a plot of the probability density function along the same range
		Args:
			n_spaces (int): number of data points 
		
		Returns:
			list: x values for the pdf plot
			list: y values for the pdf plot
	
```python
from fsc_distributions import Gaussian

gaussian1 = Gaussian(25,2) #create a new Gaussian object and initialize the mean with 25 and stdev with 2

gaussian2 = Gaussian(35,8) #create a new Gaussian object and initialize the mean with 25 and stdev with 8

gaussian3 = gaussian1 + gaussian2 #sum the two distributions with an overloaded add operator
```

## Binomial class
Binomial distribution class for calculating and visualizing a Binomial distribution.

Attributes:

	mean (float) representing the mean value of the distribution
	
	stdev (float) representing the standard deviation of the distribution
	
	data_list (list of floats) a list of floats to be extracted from the data file
	
	p (float) representing the probability of an event occurring
	
	n (int) number of trials
    
Methods:

	read_data_file(file_name) Function to read in data from a txt file. The txt file should have one number (float) per line. The numbers are stored in the data attribute.
		Args:
			file_name (string): name of a file to read from
	
		Returns:
			None
	
	calculate_mean() Function to calculate the mean from p and n
        Args: 
            None
    
	    Returns: 
            float: mean of the data set
	
	calculate_stdev(sample=True) Function to calculate the standard deviation from p and n.
        Args: 
            None
    
	    Returns: 
            float: standard deviation of the data set
	
	replace_stats_with_data() Function to calculate p and n from the data set
        Args: 
            None
    
	    Returns: 
            float: the p value
            float: the n value
	
	plot_bar() Function to output a histogram of the instance variable data using matplotlib pyplot library.
        Args:
            None
    
	    Returns:
            None
	
	pdf(k) Probability density function calculator for the binomial distribution.
		Args:
			k (float): point for calculating the probability density function
	
		Returns:
			float: probability density function output
	
	plot_bar_pdf()Function to plot the pdf of the binomial distribution
        Args:
            None
    
	    Returns:
            list: x values for the pdf plot
            list: y values for the pdf plot
	

```python
from fsc_distributions import Binomial

binomial1 = Binomial(0.5,20) #create a new Binomial object and initialize the prob with 0.5 and size with 20

binomial2 = Binomial(0.5,30) #create a new Binomial object and initialize the prob with 0.5 and size with 30

binomial3 = binomial1 + binomial2 #sum the two distributions with an overloaded add operator (only sums binomials with the same p)
```


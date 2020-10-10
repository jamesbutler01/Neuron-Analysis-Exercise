# Example prefrontal cortex neuronal data from an economic decision-making task

A subset of processed data from one of our recent experiments featured in Nature Neuroscience ([link](https://pubmed.ncbi.nlm.nih.gov/30258238/)). The full dataset (unprocessed) is publicly available [here](https://crcns.org/data-sets/pfc/pfc-7/about-pfc-7). 

The neurons (all recorded from ACC) showcase a range of different response profiles, such as this beautiful positive value coder:
![Example neuron](https://github.com/jamesbutler01/Example-Neuronal-Analysis/blob/main/ExampleNeuron.png?raw=true)



#### Data consists of the following files: 
- x.npy
	- [neurons x trials] matrix of the value of the attended cue
	- Cue is one of 5 different values (0.1, 0.3, 0.5, 0.7, 0.9), sampled with a uniform distribution

- y.npy 
 	- [neurons x trials x time] matrix of neural activity during each trial.
		- The first dimension of the matrix will be each neuron (i.e. length 10 as there are 10 neurons)
		- The second dimension will be trials (length 342, the number of trials per session)
		- The third dimension will be each time point (length 250 as it is a 2500 ms window sampled at 10 ms intervals)
	- Cue onset is at 400 ms (i.e. point 40)
	- The firing rate has been smoothed, which is why it's not a binary variable (as raw spike data would be)

- xy.mat
	- As above but in a Matlab compatible file

#### Exercise
This is an introduction to the basics of neural data analysis/visualisation. Exploring how individual cells in the primate brain alter their firing rates in response to cues of different value. 
- Load the data
- For each neuron (i.e. with a for loop)
	- Plot the average firing rate across time for each of the 5 cues (like above)
	- On the same plot, plot the standard error for each cue (don't worry about the fancy shading, or making pretty plots!)
- Do all neurons have higher firing rates for higher value cues (like in the plot above), or do some do the opposite?

#### Further questions of interest
If you want, further things you can look for in the data:
- Quantify each neurons value response by doing a linear regression at each time point
- Overall, do the population respond positively or negatively to the value of the cue?

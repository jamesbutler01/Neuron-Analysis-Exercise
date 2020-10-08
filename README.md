# Example prefrontal cortex neuronal data from an economic decision-making task

A subset of processed data from one of our recent experiments featured in Nature Neuroscience ([link](https://pubmed.ncbi.nlm.nih.gov/30258238/)). The full dataset (unprocessed) is publicly available [here](https://crcns.org/data-sets/pfc/pfc-7/about-pfc-7). 

The neurons (all recorded from ACC) showcase a range of different response profiles, such as this beautiful positive value coder:
![Example neuron](https://github.com/jamesbutler01/Example-Neuronal-Analysis/blob/main/ExampleNeuron.png?raw=true)



#### Data consists of the following files: 
- x.npy
	- [neurons x trials] matrix of the value of the attended cue
	- Cue is one of 5 different values (0.1, 0.3, 0.5, 0.7, 0.9), sampled with a uniform distribution

- y.npy 
 	- [neurons x trials x time] matrix of neural activity during each trial
	- Time is sampled every 10 ms
	- Cue onset is at 500 ms (i.e. point 50)

- xy.mat
	- As above but in a Matlab compatible file

#### Notes
- Neurons are from different sessions, and so have different X properties

- Due to this uneven number of trials between neurons, the end of each array is padded with NaNs to allow the use of a matrix

- These NaNs should be removed/handled appropriately before any analysis takes place

#### Exercise
- Load the data
- For each neuron (i.e. with a for loop)
	- Remove/account for the NaNs in its data
	- Plot the average firing rate for each of the 5 cues
	- On the same plot, plot the standard error for each cue

#### Further questions of interest
If you want, further things you can look for in the data:
- Quantify each neurons value response by doing a linear regression at each time point
- Overall, do the population respond positively or negatively to the value of the cue?

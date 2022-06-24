# bayes-neuropixel

This activity was carried out as a part of the Bristol Bayes for the Brain 2022 workshop. The objective was to conduct a Bayesian analysis of electrophysiological data collected from a mouse brain via a Neuropixel probe. The data originates from a [dataset](https://figshare.com/articles/dataset/Dataset_from_Steinmetz_et_al_2019/9598406) used in a paper titled [Distributed coding of choice, action and engagement across the mouse brain](https://www.nature.com/articles/s41586-019-1787-x).

## Importing the Dataset

1. The entire dataset can be downloaded as a singe file 'spikeAndBehavioralData.zip' from this [link](https://figshare.com/ndownloader/files/17387882), which can also be found on the dataset website. 
2. Place 'spikeAndBehavioralData.zip' into the same directory as this repository and extract it. 
3. Within the now extracted folder there is a compressed folder called 'allData.tar'. Extract this as well.
4. Within the folder 'allData.tar' there is a file called Cori_2016-12-14.tar. Extract this as well.  

## Models

1. [Exponential Model](exponential-model.ipynb) is a first attempt at getting a working model using [Turing](turing.ml), it is therefore a really simple model. The assumption is that the spike counts for each cluster can be modelled using an exponential distribution which is fit to the data. 
2. [Linear Regression Model](linear-regression-model.ipynb) uses the theory that increased pupil size is an indicator of increased neural activity. This model finds the linear relationship between the two data.
3. [Poisson Process Model](poisson-process-model.ipynb) builds upon the second model to use the pupil area to model the parameter of a Poisson model for the spike counts for each cluster. 

(These models are a work in progress)

## Saved Results

Saved plots and chains can be found in the 'results' folder. Each saved result is held in a directory named with the time that it was recorded. This timestamp corresponds to the name of a tag, so that the code that produced that result can be identified.
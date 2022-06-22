# bayes-neuropixel

This activity was carried out as a part of the Bristol Bayes for the Brain 2022 workshop. The objective was to conduct a Bayesian analysis of electrophysiological data collected from a mouse brain via a Neuropixel probe. The data originates from a [dataset](https://figshare.com/articles/dataset/Dataset_from_Steinmetz_et_al_2019/9598406) used in a paper titled [Distributed coding of choice, action and engagement across the mouse brain](https://www.nature.com/articles/s41586-019-1787-x).


## Models

1. [Exponential Model](exponential-model.ipynb) is a first attempt at getting a working model using [Turing](turing.ml), it is therefore a really simple model. The assumption is that the spike counts for each cluster can be modelled using an exponential distribution which is fit to the data. 
2. [Linear Regression Model](linear-regression-model.ipynb) uses the theory that increased pupil size is an indicator of increased neural activity. This model finds the linear relationship between the two data.
3. [Poisson Process Model](poisson-process-model.ipynb) builds upon the second model to use the pupil area to model the parameter of a Poisson model for the spike counts for each cluster. (This model is a work in progress)
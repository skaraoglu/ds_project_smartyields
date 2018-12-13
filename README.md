# Experimental Analysis on Smartyields' Monitoring Dataset
## Abstract
This project focuses on the analysis of a sensor measurements data provided by the Smartyields company. We explored this dataset by exploring the attributes, looking meaningful relations in the data, further grouping and experimenting on attributes, clustering by real distance and comparative approach to datapoints with common attributes. After these experiments, we share our comments and possible future work on the data.

## Introduction
As the technology getting deeper into our lives everyday, one of the areas that benefit from that development is agriculture. Smart Yields use of data combined into hardware and software components as wireless sensors solutions for farmers in areas stricken by cold frost to improve the farmers yield of crops impress us enough to take on the project. By this purpose, Smartyields collected the data from these sensors and provided a small portion of that dataset for us to explore [1].  
To make this analysis, first we come up with some questions. We tried to provide answers to these questions - these questions were developed without having any experience with Agriculture or farming;
* How can crop monitoring ensure the health of the crop, at different levels of growth stages?
* How accurate are the wireless sensors? 
* How many sensors are needed to provide relatively accurate data?
* What conditions of the crops before and after monitoring?
* Could our findings provide a visualize assessment of data accuracy?
* How do we account for the unknowns?
* Provide data sharing within regions to minimize the number of sensors deployed?
  
This analysis first provide general information about the data provided. Looking at the dataset and the attributes led us to deeper explorations, we looked for correlations, data distributions and discover the deeper aspects of the dataset with some experimental work. Further, we applied clustering to the data by distance, using latitude and longitude values to observe the local differences. Following clustering, we plotted the locally clustered data on real world images provided by satellites. Finally we grouped the datapoints by their attributes to prepare the time based plots. We created time based temperature and humidity measurements for each sensor on the field and questioned the abnormalities. We conclude the analysis by presenting our observations.
## Background
In this project, we looked at the data on the aspect of "What this data is?" rather than "What we can do with this data?". The main reason is we couldn't use the data without knowing what it is, so we analysed the dataset with experiments. Looking deeper on the dataset bring us more questions to answer. We developed a series of python based code to dig the dataset, therefore there are some necessary background information we need to provide to have some clarity on the work we have done.  
We build this project based on a conda environment running on python 3.6. Here are some libraries needs to be installed to run the code;
* Numpy, Scipy: NumPy is the fundamental package provided by SciPy for scientific computing with Python. SciPy is a Python-based ecosystem of open-source software for mathematics, science, and engineering [2]. 
* Pandas: Pandas is an open source library providing high-performance, easy-to-use data structures and data analysis tools for the Python programming language [3].
* Matplotlib: Matplotlib is a Python 2D plotting library which produces publication quality figures in a variety of hardcopy formats and interactive environments across platforms [4].
* Basemap: The matplotlib basemap toolkit is a library for plotting 2D data on maps in Python [5].
* Scikit-Learn MiniBatch K-Means Clustering: The MiniBatchKMeans is a variant of the KMeans algorithm which uses mini-batches to reduce the computation time, while still attempting to optimise the same objective function. Mini-batches are subsets of the input data, randomly sampled in each training iteration. These mini-batches drastically reduce the amount of computation required to converge to a local solution [6].

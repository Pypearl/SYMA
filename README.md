# Syma [![Profile][title-img]][profile]

[title-img]:https://img.shields.io/badge/-SCIA--PRIME-red
[profile]:https://github.com/bictole

## Objective

The goal of this project is to apply and demonstrate the use of different **machine learning** methods to real datasets.

## Dataset

We had to choose two **datasets** within the following constraints :
* several hundreds of lines
* at least 6 attributes (columns), the first being a unique id, separated by commas
* we may use some categorical (non quantitative) features.
* some fields should be correlated

Obvously, we had to tweak the datasets in order to artificially make it possible to apply **analysis** and **visualization** techniques on them.


## Supervised learning

In a first part, we had to work on a dataset and perform **supervised learning** on it. We decided to work on mobile price **classification**, and try to find some relation between features of a mobile phone (RAM, number of cores, internal memory...) and its selling price. 

We found a dataset that instead of giving the actual price of each phone give a price range indicating how high the price is.

We could perform different analysis ont this dataset and try to visualize our data.

<img src="https://github.com/Pypearl/PTML/blob/main/readme_images/supervised_vis.png" alt="Supervised_Visualization">

We decided to test several algorithms with the **sklearn** and **xgboost** library.
First, we split our data to obtain a train dataset and a test dataset, then we iterate on the **classifier** to fit them and test them. The scoring is here a `R2 score`, which is evaluated by **cross validation**.

The results are the following :

<img src="https://github.com/Pypearl/PTML/blob/main/readme_images/supervised_res.png" alt="Supervised_Visualization">

## Unsupervised learning

In this section, we decided to work on a dataset containing information about 167 **countries**, like the inflation, the net income by person and other **economical parameters**.

After loading the data we checked that there were no missing and duplicated data. And we decided to visualize it with **seaborn** library.

Our objectives in this unsupervised learning is to decide whether or not a country should receive a **Funding** for Development Aid.

For this **machine learning** part, we decided to use the **K-Means** algorithm from the **sklearn** library. The objective was to apply a **clustering** technique on our data to classify them and to know which one of them should receive a Funding for Development Aid.

We applied the algorithm on two datasets, the first one which was the result of a **PCA**, and the second one which was the result of a **MinMax Scaling**. The most optimized number of cluster is 3, we used the elbow method and the silouhette method from the sklearn library to find it.


<img src="https://github.com/Pypearl/PTML/blob/main/readme_images/unsupervised_map.png" alt="Supervised_Visualization">

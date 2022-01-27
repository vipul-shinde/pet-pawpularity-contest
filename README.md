[![forthebadge](https://forthebadge.com/images/badges/powered-by-coffee.svg)]()
[![forthebadge](https://forthebadge.com/images/badges/made-with-python.svg)]()
[![forthebadge](images/badges/uses-deep-learning.svg)]()

<h1 align="center">Pawpularity Contest: Predict the popularity of shelter pet photos</h1>

<div align="center">

  [![Status](https://img.shields.io/badge/status-active-success.svg)]()
  [![License](https://img.shields.io/badge/license-MIT-blue.svg)]()
  ![GitHub repo size](https://img.shields.io/github/repo-size/vipul-shinde/pet-pawpularity-contest)

</div>

---

<p align="center"> In this project, we have build a deep learning model to predict the pawpularity score of a pet's profile based on the photograph for that profile.
    <br>
</p>

## 📝 Table of Contents

- [🧐 About](#about)
- [📊 Dataset Overview](#data-overview)
- [🧹 Data Cleaning](#data-cleaning)
- [🧠 Model Building](#neural-network-model)
- [🎯 Model Performance](#model-performance)
- [🏅 Model Evaluation](#model-evaluation)

## 🧐 About <a name = "about"></a>

Millions of stray animals suffer on the streets or are euthanized in shelters every day around the world. We can expect pets with attractive photos to generate more interest and be adopted faster. But what makes a good picture?

With the help of data science, we can accurately determine a pet photo’s appeal and even suggest improvements to give these rescue animals a higher chance of loving homes.

## 📊 Dataset Overview <a name="data-overview"></a>

The dataset was collected from Malaysia’s leading animal welfare platform, PetFinder.my. It is available to us as a kaggle competition and the dataset can be found at https://www.kaggle.com/c/petfinder-pawpularity-score/data.

The Pawpularity Score is derived from each pet profile's page view statistics at the listing pages, using an algorithm that normalizes the traffic data across different pages, platforms (web & mobile) and various metrics. 

The dataset contains around 10.000 cat and dog images in different resolutions. The training, test, and validation separation is 80%, 10%, and 10%, respectively. 

The training are images named with their uniques IDs, which can be used to find their corresponding pawpopularity score.

## 🧹 Data Cleaning <a name="data-cleaning"></a>

In order to check if the dataset contain any duplicate images with different scores, we used a combination of hashes to find the similar images. 

We used a list of hash functions such as Average Hashing, Perceptual Hashing, Difference hashing and Wavelet Hashing.

In the end, we removed all the duplicate images that had a similarity score of more than 90%.

### Click to view 👇:

[![forthebadge](images/badges/solution-exploratory-data-analysis.svg)](https://github.com/vipul-shinde/pet-pawpularity-contest/blob/main/notebooks/01-eda-data-cleaning.ipynb)

## 🧠 Model Building <a name="neural-network-model">

We started by building a Convolutional Neural Network with the following architecture and let it run for 30 epochs. But due to no further improvement and because of the callback functions we used it stopped training after 15 epochs and the model with best weights was stored.

<p align="center">
    <img src="images\cnn-architecture.png" alt="cnn-architecture">
</p>

Later on, we used pretrained models such as Xception, Resnet50 and Efficientnet50 as the bottom layers and fine tuned the top custom layers to build a model able to predict the pawpularity score.

### Click to view 👇:

[![forthebadge](solution-cnn-and-transfer-learning-models.svg)](https://github.com/vipul-shinde/pet-pawpularity-contest/blob/main/notebooks/02-cnn-and-transfer-learning.ipynb)


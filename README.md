# Plagiarism Project, Machine Learning Deployment

This repository contains code and associated files for deploying a plagiarism detector using AWS SageMaker.

## Project Overview

In this project I built a plagiarism detector that examines a text file and performs binary classification, labeling that file as either *plagiarized* or *not*, depending on how similar that text file is to a provided source text. Detecting plagiarism is an active area of research; the task is non-trivial and the differences between paraphrased answers and original work are often not so obvious.

This project is broken down into three main parts:

**Data Exploration**
* Load in the corpus of plagiarism text data.
* Explore the existing data features and the data distribution.

**Feature Engineering**

* Clean and pre-process the text data.
* Define features for comparing the similarity of an answer text and a source text, and extract similarity features.
* Select "good" features, by analyzing the correlations between different features.
* Create train/test `.csv` files that hold the relevant features and class labels for train/test data points.

**Train and Deploy Model in SageMaker**

* Upload train/test feature data to S3 buckets.
* Define a binary classification model and a training script.
* Train model and deploy it using SageMaker.
* Evaluate deployed classifier.

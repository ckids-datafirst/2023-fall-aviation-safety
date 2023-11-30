---
title: Approach
summary: Data science methodology used to address the problem, including data preprocessing steps, exploratory data analysis, feature engineering techniques, machine learning models, and evaluation metrics.
date: "2018-06-28T00:00:00Z"
editable: true
share: false
---

This page contains key sections of the **Final Report** for the project focused on the data science methodology used to approach the problem.  It should be no more than 3 pages long.  It should be done after or in combination with the Requirements document.  It should have an initial release after no more than eight weeks into the project, and can serve as an interim project report.  It can be refined as the project progresses and the problem is better understood.  

## Data Quality

The data initially sourced from ASRS contains more than 46,000 rows and 120 columns of data. Upon visual and statistical analysis it is realised that the data contains multiple duplicate columns and many columns contain negligible data these have to be cleaned. The narrative wherein the anonymous reporter explains an incident doe not use aviation english always. For instance flight, aircraft, and airplane is used to describe the same object. Therefore the model has to be trained in accordance with varying parameters or the dataset has to be cleaned substantially. 

## Data Preprocessing

The data preprocessing involved the following tasks conversion of all characters to lowercase, stop word removal : specific stops words for aviation ( like aircraft), lemmatization/ stemming/ Tokenization, expand contractions.

## Exploratory Data Analysis (EDA)

We used python libraries pandas, numpy and matplotlib for exploratory data analysis of the ASRS dataset.

![Number of incidents regarding light](https://raw.githubusercontent.com/ckids-datafirst/2023-fall-aviation-safety/main/content/images/noofincidents.png)

![Number of primary problems](https://raw.githubusercontent.com/ckids-datafirst/2023-fall-aviation-safety/main/content/images/numberofproblems.png)

![Top 50 airports with most cases](https://raw.githubusercontent.com/ckids-datafirst/2023-fall-aviation-safety/main/content/images/noofcases.png)

## Model Development

![Method Architecture](https://raw.githubusercontent.com/ckids-datafirst/2023-fall-aviation-safety/main/content/images/methodarchdiagram.png)
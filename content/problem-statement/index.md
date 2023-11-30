---
title: Problem and Requirements
summary: Problem and Requirements document that will drive the work to be done in the project
date: "2018-06-28T00:00:00Z"
editable: true
share: false
---

## Introduction
1. The New York Times article [‘Air disasters are rare in the US, close calls are a different story’](https://www.nytimes.com/2023/10/11/business/air-traffic-control-austin-airport-fedex-southwest.html) highlights a trend of incursions and near misses in the United States aviation industry. 
While there haven't been major plane crashes for over a decade, close calls involving commercial airlines are occurring frequently, often due to human error and a shortage of air traffic controllers.

2. The number of near misses has doubled in the last decade, raising questions about the safety of the U.S. air travel system.
3. The concerned governmental authorities are analysing this issue currently.

4. Through this project, our team plans to take direct action and contribute as researchers on how to improve the situation of runway incursions.


## Motivation

The United States alone has an annual passenger traffic of 666 million passengers (in 2021). In recent years aviation safety reporting system has received a record number of incident reports which points to a major question whether the safety standards have been degrading or the number of reports has been increasing. Whatever may be the case there are millions of passengers who travel in these aircraft and therefore it becomes necessary to find out the root causes of these faults. 


## Problem for the Semester

1. To analyze aviation incursion reports and determine the primary safety concerns and system fracture points leading to such situations with compelling data.
To improve aviation safety through the analysis of NASA’s ASRS data. 
2. To use Machine Learning and Natural Language Processing models to process data and extract useful statistics from (45000, 126) records that can be used to make suggestions to the concerned authorities and effectively alleviate the ongoing crisis.
3. Setup preliminary foundation for development of an encompassing artificial intelligence model that can dynamically read new reports and provide valuable insights.


## State of the Art

Post-air crash-related incidents usually investigation teams have a flight manifest and black box data to uncover the root cause of the incident. Unlike crashes, near misses do not have black box access therefore problem solving completely relies on anonymous reports. Therefore analysis of these reports becomes the only way to solve this problem.


## Design and Approach

If we treat the data as supervised data and divide it into train and test. The primary problem can be treated as a label. Post this divide we intend to run correlation analysis and feature extraction algorithms like principle component analysis, and linear discriminant analysis. Word2vec or term frequency-inverse document frequency (tf-idf) to make narratives into features. Train data over a neural network and test it over a sample set to gauge the accuracy.

## Use Case Scenario

The end user for this system could be the Federal Aviation Administration, this system could help them in policy framing. After certain modifications, airlines could use it internally for incident report generation and problem-solving.

![Use case diagram](https://raw.githubusercontent.com/ckids-datafirst/2023-fall-aviation-safety/main/content/images/usecasediagram.png)

## Desired Outcomes and Benefits

Given the timeframe of one semester, we find it realistic to focus on a particular type of incident and study it in detail, therefore we intend to focus on runway incursions and identify the fracture points in the system.
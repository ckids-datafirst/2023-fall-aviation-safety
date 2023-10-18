---
title: Data Assessment
summary: Data Assessment Document that gives an overview of the data used for the project.

date: "2018-06-28T00:00:00Z"
editable: true
share: false
---

## Introduction

The dataset used in this project is sourced from the Aviation safety reporting system. The original ASRS dataset has more than 300 thousand rows of information from the year 1988. Since we are specifically interested in runway incursion we applied a filter while downloading the dataset and received a subset of 46,000 rows and 126 columns. The rudimentary goal is to analyse this dataset to identify fracture points in safety regulations.

## Data Overview and Examples

The ASRS data is anonymised reports collected from individuals working in the aviation sector. The dataset contains the credentials of the reporting person (excluding personally identifiable content), time and date of the incident, name of the airport, state, altitude, visibility, narrative etc. We intend to use a subset of the 127 features already present with us. The reason is that there are multiple features with a negligible amount of data making analysis unfavourable. Therefore we intend to drop those features completely before further processing. ASRS is the largest data repository available for aviation safety incidents therefore any other dataset which is publicly available may either be a subset of ASRS or might not be reliable since ASRS is a government-backed dataset.

## Data Accessibility

The dataset is accessible through a web portal. There are multiple filters that a user could use to extract the data based on time, type of incident, reporting agency etc. Since we are interested in runway incursions we used word filters like runway, ramp and taxiway. The major constraint for downloading the dataset is at a time only 10,000 rows can be downloaded. Therefore we had to download 5 reports and collate them together.

## Data Formats

The dataset can be downloaded in Excel, CSV, pdf, word and HTML formats from the ASRS portal. For ease of use with Python, we preferred the usage of csv format.

## Data Challenges

The most challenging part of the dataset is the narrative. The narrative is a description of the incident from a reporter/observer’s point of view. All the reports available in the dataset are not written in aviation English. For instance, airplane, aircraft and flight may essentially point towards the same object but are written in diverse ways. Similarly, the runway is often time written as rwy. All the reports are not written in a professional manner, for instance in a report pilot makes an attempt to humor by mentioning “spilling coffee in the cockpit”. This information is futile as far as the algorithm is concerned.

## Data Visualizations and Highlights

Including a visualization is a simple way to show something interesting about the data.  Perhaps the visualizations could simply highlight the size, distribution, and other simple statistical characteristics of the data.

![Number of incidents regarding light](https://imgur.com/YUerqmA)

![Number of primary problems](https://imgur.com/2QSREdQ)

![Top 50 airports with most cases](https://imgur.com/mh9Q15O)
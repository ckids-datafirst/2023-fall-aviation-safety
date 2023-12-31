## Objectives: 
what we can achieve
(Everyone contributes atleast 3 points)

Chahita : These are the areas that I explored. Some of them are pretty heavy. We can brainstorm and reduce them into components on which we can work. 
1. Pattern analysis on ASRS data to understand common factors such as specific airports r aircraft type or weather conditions or time of day other than human factors. We have human factor report from NTSB. How many of them can be fixed? And we know what latest technology should be used to reduce these human factors issue. We want to find which airports have installed or are using those technologies to prevent it. And if they are using it, did it decrease the number of incursions? Also can look at the budget to use these technologies.
2. Can create a virtual ATC to handle the problem of shortage of ATC staff.
3. Can create a model which when given an airport design and std airport design, can point out if it is following all rules and also if its complex or not or might cause issues?
4. Creating a model that use cnn to Detect and Identify Airport Signs during low visibility.

Shreyas :
1. Data analysis for Aviation safety recommendations:  Create categories of technical failures extracted from report narratives and assign them to the airport where the incident happened. Let’s say after analysis we realize maximum braking-related incidents happen in JFK. It suggests that something is wrong with maintenance in that department.
2. Identify airlines with maximum safety incidents and launch an inquiry for these incidents
3. Representation of incidents with respect to carrier, type of fault, type of aircraft etc on an interactive US map. [Example of interactive maps](https://www.tableau.com/learn/articles/interactive-map-and-data-visualization-examples) 

Abhinav:
1. Finding correlation between the relevant attributes to create scenarios leading to runway incursions. For example, bad weather leads to more clouds and less visiblity. Use correlation matrix and other methods to create a pattern analysis: x, y, z together lead to w
2. Create an easy to understand document for non-technical layman to read and understand the problem/cause/solution.
4. Interactive Dashboard with the dataset:  
&ensp;a. Display sample report (for viewer to understand the data) - from a particular month (because we don't have date wise, only month wise)  
&ensp;b. State wise report count vs number of flights vs number of towered/untowered airports  
&ensp;c. Incursions taking place at 0 to x altitude filter - number  
&ensp;d. Flight phase when incursion takes place - including overlapping cases like taxi;parked and Landing;Taxi 

Atharva:
1. Convert the Narrative feature into different categories by NTSB and create new features out of them using one hot encoding. Easier to create a classification model or a report for the Narrative section.
2. Make a report consisting of preventive measures and solutions for the most common human factors causing the incursions.
3. Create a model that can predict the chance or probability of an incursion to happen given some live features like visibility, weather conditions, etc.

## Filtered Objectives:
1. Interactive Dashboard
2. Replicate NTSB model for processing Narrative column + Can also use supervised learning (categories predited in NTSB report) to categorize all the reports of incursions (Priority - 1)
3. Predictive model - given a few attriutes predicts likelylood of incursion taking place 

## Aproaches to discuss with Prof. Ulf:
(Based on objectives)

## Fix dataset to match NTSB 2017 report and replicate graphs:
(Shreyas puts up full dataset)
Chahita : put up collab scripts  - done

NTSB report work: (one suggestive approach : altitude 0-1000 ft for runway incursion)
1. NLP related : Chahita
2. Concurrent human factors: Abhinav
3. Contributing factors: Ravneet
4. Top 20 Airports by year: Shreyas
5. Top 15 concurrent anomalies: Likhit
6. Bar graphs on ASRS intake and runway incursion: Atharva
7. Runway incursion reported: Mino

## Interactive Dashbard that runs python scripts behind:
(Mino checks with Najm/Daniel if this is needed/makes sense for our project)

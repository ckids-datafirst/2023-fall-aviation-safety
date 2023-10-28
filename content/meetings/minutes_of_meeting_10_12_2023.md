## Questions
1. Are we supposed to make a new project or build upon existing work done by the last team? From the report, we can study that they have taken a lot of the same steps we are working on. 
2. Can we get access to get their project?
3. Do we need to make a poster or ppt? What is the Mid-term presentation format? Is poster necessary?
4. Data Doubts:  
&emsp;a. ‘Weather Element/Visibility’ Numeric Value Meaning  
&emsp;b. ‘Ceiling’ value meaning and usefulness? 0- completely fogged  
&emsp;c. ‘Flight Phase’ with multiple phases, eg: Parked; Landing; Landing, etc  
&emsp;d. ‘Operating Under FAR Part’ meaning?  
&emsp;e. How should we handle the same columns for different aircrafts and persons?  
&emsp;f. Need some direction for where to proceed  
&emsp;g. The dataset description says that this dataset cannot be used for actual implementation since it is not approved by the FAA.

## Points discussed in the meeting:

1. Upload data and other useful materials to the github repository for the professors to review
2. Focus of Incursions - A classifier model for human errors like confusion, fatigue, etc can be designed which can then be tackled by the Federal Aviation Administration. Hint: To classify the data, we can check for keywords like fatigue, extra hours etc. which are related to "overtime" in the Narrative column of the ASRS dataset.
3. Data Doubts:
   * 'Weather Element/Visibility' Numeric Value Meaning
     Ans: The numeric value denotes visibility in miles.
   * 'Ceiling' value meaning and usefulness? 0- completely fogged.
     Ans: More the ceiling (height of the clouds), the better is the visibility.
   * 'Flight Phase' with multiple phases, eg: Parked; Landing; Landing, etc
     Ans: They represent the different stages that the plane went through in during the incident. Some cells have redundant stages.
   * 'Operating Under FAR Part' meaning?
     Ans: The Federal Aviation Regulations (FARs) are rules prescribed by the Federal Aviation Administration (FAA) governing all aviation activities in the United States.
4. Check out the power point presentation that was presented at an ASRS meeting and has 4 factors to identify the incursions. It was shared to us by Prof. Najmedin earlier in the emails.
5. The team can get an award if everyone does a good job and wins the International Society of Air Safety Investigators (ISASI) conference. This year it will be held at Lisbon, Portugal.
6. Update the project website with the current work done.

## Ideas:
1. Classifier model for human errors like confusion, fatigue, etc which can then be tackled by the FAA.
2. Incursion Predictor model that takes some features as inputs like weather, crew size, etc and gives the chance or probability of an incursion happening.

## Important Links:

1. ASRS General Report Form: [https://asrs.arc.nasa.gov/docs/general.pdf]()
2. ATSAP Resources: [https://www.atsapsafety.org/]()
3. DataFirst Website: [https://ckids-datafirst.github.io/website/editions/2023-fall/]()
4. GitHub Austin incident: [https://github.com/ckids-datafirst/2023-fall-aviation-safety/blob/main/content/data/news_articles.md]()
5. GitHub Aviation Safety GitHub Repository: [https://github.com/ckids-datafirst/2023-fall-aviation-safety]()

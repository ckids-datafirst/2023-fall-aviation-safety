## Requirements:

1. Introduction/Motivation (why should people be interested in this project?)
2. Aims (what is your goal?)
3. Methods (what did you do? A schematic may look good here)
4. Results (what have you found? Figures will look great here)
5. Conclusion (if someone asked you what you discovered in a sentence, what would you tell them?)

## INTRODUCTION

‘Air disasters are rare in the US, close calls are a different story’
- The New York Times (Front Page) - 23rd August 2023

1. The article highlights a concerning trend of safety incidents and near misses in the United States' aviation industry. 
2. While there haven't been major plane crashes for over a decade, close calls involving commercial airlines are occurring frequently, often due to human error and a shortage of air traffic controllers. 
3. The number of near misses has doubled in the last decade, raising questions about the safety of the U.S. air travel system.
4. Direct action is needed to improve the situation. NASA maintains a database - ‘Aviation Safety Reporting System’ - that records incident reports of all runway/taxiway incursions since 1988. A treasure trove of untapped potential.

## AIMS

1. To analyze aviation incursion reports and determine the primary safety concerns and system fracture points leading to such situations with compelling data.
2. To improve aviation safety through the analysis of NASA’s ASRS data. 
3. To use Machine Learning and Natural Language Processing models to process data and extract useful statistics from (45000, 126) records that can be used to make suggestions to the concerned authorities and effectively alleviate the ongoing crisis.
4. Setup preliminary foundation for development of an encompassing artificial intelligence model that can dynamically read new reports and provide valuable insights.

## METHODS

EDA of ASRS Dataset using Numpy, Pandas, Matplotlib
Pre-processing
TF-IDF Vectorization
Lemmatization using spaCy, NLTK
Wordcloud ?

## PROPOSED MODEL

1. If we treat data as supervised data and divide the data into train and test. Primary Problem can be treated as our label.
2. Run correlation analysis and feature extraction algos like PCA, LDA to find relevant features from all attributes and word2vec/ Glove or tf-idf to make narrative and synopsis into features. 
3. Then train a NN model on this data.
4. Test it over a testing set and see if the model is figuring out the label correctly.
5. For human factors specifically, take out rows which have primary problems as HumanFactors. That is a dataset. Use topics created by previous work to further categorize data using narrative columns. 
6. Steps to be taken:
  a. Data preprocessing: Convert to lower case
  b. Stop word removal : specific stops words for aviation ( like aircraft)
  c. lemmatization/ stemming/ Tokenization
  d. Expand contractions - Try using abbreviations pdf 
  e. EDA :  distribution of words/ phrases. Find common terms and patterns. Word clouds and plots
  f. Keyword extraction: find most significant words (tf-idf can be used)
  g. Topic modeling : LDA ( use previous work as base to get good topics)
  h. Runway incursion identification : use topics to find narratives which are runway incursions.
  i. Context analysis: analyze context for narrative. Factors, people involved, series of events lead to that incident 

Collect data. Identify examples . what want to extract. 10-20 cases 


Questions:
Are we supposed to make a new project or build upon existing work done by the last team? From the report, we can study that they have taken a lot of the same steps we are working on. 
Can we get access to get their project?
Do we need to make a poster or ppt? What is the Mid-term presentation format? Is poster necessary?
Data Doubts:
‘Weather Element/Visibility’ Numeric Value Meaning
‘Ceiling’ value meaning and usefulness? 0- completely fogged.
‘Flight Phase’ with multiple phases, eg: Parked; Landing; Landing, etc
‘Operating Under FAR Part’ meaning?
How should we handle the same columns for different aircrafts and persons?
Need some direction for where to proceed.
The dataset description says that this dataset cannot be used for actual implementation since it is not approved by the FAA.

Minutes of Meeting:

Upload data and other useful materials to github for the profs to review
Focus of incursions 
Get better results than absurd or ridiculous
Visibility in miles
More the ceiling, the better (height of the clouds) - 0 ceiling: full fog
Different stages the plane went through in Flight Phase
FAR: Part 91 - general, part 121 - airlines, etc
Power point presentation at ASRS meeting has 4 factors to identify the incursions 
https://asrs.arc.nasa.gov/docs/general.pdf
https://www.atsapsafety.org/
https://ckids-datafirst.github.io/website/editions/2023-fall/
Midterm presentation Friday, October 20, 5-7pm SAL 101 (not Wednesday)
GitHub Austin incident: https://github.com/ckids-datafirst/2023-fall-aviation-safety/blob/main/content/data/news_articles.md
GitHub aviation safety: https://github.com/ckids-datafirst/2023-fall-aviation-safety
Check for fatigue keywords like overtime in the ASRS data
You can get an award if you do a good job
International conference for air safety investigation - annual conference
The next ISASI conference is in Lisbon, Portugal
Update the project website!!!

Ideas:
1. Classifier model for human errors like confusion, fatigue, etc which can then be tackled by the FAA.
2. Incursion Predictor model that takes some features as inputs like weather, crew size, etc and gives the chance or probability of an incursion happening.


Content needed for the website
Approach
Data Quality
The data initially sourced from ASRS contains more than 46,000 rows and 120 columns of data. Upon visual and statistical analysis it is realised that the data contains multiple duplicate columns and many columns contain negligible data these have to be cleaned. The narrative wherein the anonymous reporter explains an incident doe not use aviation english always. For instance flight, aircraft, and airplane is used to describe the same object. Therefore the model has to be trained in accordance with varying parameters or the dataset has to be cleaned substantially.


Data Pre processing
The data preprocessing involved the following tasks conversion of all characters to lowercase, stop word removal : specific stops words for aviation ( like aircraft), lemmatization/ stemming/ Tokenization, expand contractions.


EDA
We used python libraries pandas, numpy and matplotlib for exploratory data analysis of the ASRS dataset.






Model Development
Describe the algorithms, methodology, and architectures used to generate models. Discuss how models were generated, seeded, and improved. Show the libraries and frameworks used for model development, as well as the rationale behind those choices.
Model Evaluation
Discuss the evaluation metrics used to assess model performance, and justify those choices based on the problem that the project is addressing. Describe the evaluation techniques used, such as cross-validation, and how undesirable model behaviors, such as overfitting, were avoided.
Data
Introduction
The dataset used in this project is sourced from the Aviation safety reporting system. The original ASRS dataset has more than 300 thousand rows of information from the year 1988. Since we are specifically interested in runway incursion we applied a filter while downloading the dataset and received a subset of 46,000 rows and 126 columns. The rudimentary goal is to analyse this dataset to identify fracture points in safety regulations.
Data overview and examples
The ASRS data is anonymised reports collected from individuals working in the aviation sector. The dataset contains the credentials of the reporting person (excluding personally identifiable content), time and date of the incident, name of the airport, state, altitude, visibility, narrative etc. We intend to use a subset of the 127 features already present with us. The reason is that there are multiple features with a negligible amount of data making analysis unfavourable. Therefore we intend to drop those features completely before further processing. ASRS is the largest data repository available for aviation safety incidents therefore any other dataset which is publicly available may either be a subset of ASRS or might not be reliable since ASRS is a government-backed dataset.
Data Accessibility
The dataset is accessible through a web portal. There are multiple filters that a user could use to extract the data based on time, type of incident, reporting agency etc. Since we are interested in runway incursions we used word filters like runway, ramp and taxiway. The major constraint for downloading the dataset is at a time only 10,000 rows can be downloaded. Therefore we had to download 5 reports and collate them together.
Data formats
The dataset can be downloaded in Excel, CSV, pdf, word and HTML formats from the ASRS portal. For ease of use with Python, we preferred the usage of csv format.
Data challenges
The most challenging part of the dataset is the narrative. The narrative is a description of the incident from a reporter/observer’s point of view. All the reports available in the dataset are not written in aviation English. For instance, airplane, aircraft and flight may essentially point towards the same object but are written in diverse ways. Similarly, the runway is often time written as rwy. All the reports are not written in a professional manner, for instance in a report pilot makes an attempt to humor by mentioning “spilling coffee in the cockpit”. This information is futile as far as the algorithm is concerned.
Data Visualization and Highlights







Problem
Motivation
The United States alone has an annual passenger traffic of 666 million passengers (in 2021). In recent years aviation safety reporting system has received a record number of incident reports which points to a major question whether the safety standards have been degrading or the number of reports has been increasing. Whatever may be the case there are millions of passengers who travel in these aircraft and therefore it becomes necessary to find out the root causes of these faults. 
State of art
Post-air crash-related incidents usually investigation teams have a flight manifest and black box data to uncover the root cause of the incident. Unlike crashes, near misses do not have black box access therefore problem solving completely relies on anonymous reports. Therefore analysis of these reports becomes the only way to solve this problem.
Design and approach
If we treat the data as supervised data and divide it into train and test. The primary problem can be treated as a label. Post this divide we intend to run correlation analysis and feature extraction algorithms like principle component analysis, and linear discriminant analysis. Word2vec or term frequency-inverse document frequency (tf-idf) to make narratives into features. Train data over a neural network and test it over a sample set to gauge the accuracy.


Use case scenarios
The end user for this system could be the Federal Aviation Administration, this system could help them in policy framing. After certain modifications, airlines could use it internally for incident report generation and problem-solving.
Desired outcomes and benefits
Given the timeframe of one semester, we find it realistic to focus on a particular type of incident and study it in detail, therefore we intend to focus on runway incursions and identify the fracture points in the system.



Results
System and performance model
Show the performance of the best system and model(s) developed, showing clearly the performance metrics and improvements over the baseline system as appropriate. Create visualizations that show clearly these results.
Discussion of findings
Words such as aircraft, runway, approach, landing, light, taxi, etc. occur more frequently
Incursion accidents mostly happen on-ground during taxi, initial approach or landing
CA, TX and FL have very high number of incursions
Human Factors and Aircraft Issues are the leading primary causes of most incursions


Limitations and future work
Discuss any limitations of the work to date, how these limitations could be addressed in future work. Discuss what lines of work are most promising given the understanding of the problem and the data gained throughout the project.




EDA Results:
The bar chart of Years vs Incidents will help us to analyze and visualize the distribution of incidents over different years, showing how many incidents occurred in each year. This can be useful for gaining insights into trends, patterns, or changes in incidents over time. The highest number of incidents were reported in the year 2019.
The horizontal bar chart of Flight Conditions vs Incidents helps us analyze and visualize the distribution of different flight conditions in the dataset, showing how many incidents are associated with each type of flight condition. This analysis could be valuable for understanding the relationship between flight conditions and incidents or events and making it easier to compare the frequencies of different flight conditions. The flight condition VMC is responsible for most of the incidents as per the graph.
After analyzing the environmental weather conditions, rain is responsible for a lot of events followed by turbulence.
By examining the 50 airports with the highest number of reported cases, we discovered that the largest number of incidents were documented at the ORD airport.
By visually representing the distribution of reported cases across different states we were able to analyze the states that have the highest number of reported cases. The chart provided a clear visual representation of this information, making it easier to identify which states have the most incidents. California had the highest number of reported cases.
Through an analysis of incident counts relative to environmental lighting conditions, we discovered that the majority of incidents occurred during daylight hours.
The predominant factor contributing to the majority of incidents was identified as the human factor, with issues related to the aircraft following as the second most significant contributor.
A map is styled with boundaries, colour-coded data, legends, and a title to provide a clear and visually appealing representation, enhancing our understanding of the distribution of incidents across states.
By displaying a word cloud visualization based on the text contained in the narrative we could visually represent the frequency of words in the text, with larger words indicating higher frequency. This type of visualization is often used to gain insights into the most common terms or words in a given text or dataset. The common terms used were time, first officer, aircraft and so on.

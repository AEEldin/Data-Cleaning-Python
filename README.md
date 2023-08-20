# Data Cleaning using Python

Data is a valuable asset in any application and field (e.g., healthcare, tourism, business), and -by understanding and analyzing such data- we can reach important insights and information that guide the decision-making process. However, there is a meaningful repeated saying in data analysis: "Garbage in, Garbage out"! Corrupted, inaccurate, or "garbage" data may result in misleading, inaccurate, or "garbage" insights. Such insights are not only untrustworthy but also may be harmful. The more accurate and "clean" your data, the more meaningful and precise your insights will be. Consider the field of Machine Learning as an example, the models and algorithms perform well only if they are trained well, and they are trained well only if they are provided with accurate and clean data. Thus it is important to keep the data accurate and up-to-date.

Data cleaning -also known as _**data cleansing and data scrubbing**_- is considered one of the most essential and initial steps towards generating quality data suitable to understand the data, gain insights, and for the decision-making process. With data coming from a single source or multiple sources, there is a wide range of opportunities for such data to be corrupted, incorrect, missing parts, duplicated, mislabeled, incorrectly formatted, irrelevant, incomplete, or human errors during the data entry process. Data cleaning is simply the process of detecting and then fixing these problems to provide clean data. The fixing process can be done by modifying the content, replacing data, or deleting some data records according to the nature of the data and the application. Data cleaning is a core step in any data-oriented activities, including data management, data analysis, machine learning, data mining, and data visualization. On the other hand, eliminating unnecessary data and duplication in data records helps to reduce data storage requirements and the required amount of data processing.


## Essential Keywords
As we discuss the data-cleaning process, we will come across some essential keywords and terms that we would like to discuss.

+ _**Missing values**_ are the gaps in the data or empty (e.g., blank, null) data points. These data points can be detected and have their values either replaced with fixed values, filled with data from another data source, or estimated using other related data points in the data set.

+ _**Outliers**_ are the data points that are relatively far away -in value or behavior- from the other data points in the same data set. Detecting and removing such anomalies and Irrelevant data points provide high-quality data and correct overall results.

+ _**Irrelevant data**_ are considered data points or observations that you may not need in your data set and that aren’t relevant to your downstream needs a need to be filtered. Further added structural info may also be filtered; this includes hashtags, URLs, emojis, HTML tags, etc., unless they are necessarily a part of your analysis. 

+ _**Data formatting**_ refers to the type of data point and the structure of the data set. Data records that do not follow the expected format require special handling, including changing the data from one type to another (e.g., you expect the phone numbers data field to have numbers only).

+ _**Consistency**_ refers to the differences between data points pulled from more than one source (e.g., employees' phone numbers received from different data sets are different) and may lead to a wide range of errors and problems.

+ _**Data transformation**_ is the process of converting data points from one format or domain into another as required. Data transformation is also referred to as data wrangling, munging, and mapping and is usually part of an Extract-Transform-Load (ETL) function to align the data with a specific structure.

+ _**Data visualization**_ in the context of data cleaning can be used to spot errors in the data set, especially the outliers.



## Main Data Cleaning Steps and Techniques

The data-cleaning process is usually composed of the following steps:

+ _**Step1 - Profiling**_: where the data is inspected to identify issues and problems to be fixed, and data profiling is about understanding the data, finding any links between the data points, and collecting statistics on the data sets.

+ _**Step2 - Scrubbing**_: This is the actual cleaning process on incorrect, inconsistent, duplicate, and redundancy in data, along with other issues and problems detected from the first step.

+ _**Step3 - Verification**_: where the processed data is inspected to verify its cleanliness and readiness with respect to the application, requirements, and standards. This is usually done by data professionals to check data integrity and ensure the data is accurate and valid for downstream processes. Data wrangling techniques and tools can be utilized to automate the process.

+ _**Step4 - Reporting**_: where the verified data set is reported to business users and other teams for further tasks like data analysis and machine learning.
    

With a focus on step 2, the data cleaning, there is a wide range of techniques that vary from one data set to another, and there is no exact and specific sequence of techniques that can be taken to clean a data set. In this subsection, we would like to mention some of the commonly used techniques for data cleaning:

### Remove Duplicates:
Remove unwanted observations from your dataset, including duplicate observations or irrelevant observations. Duplicate observations will happen most often during data collection. When you combine data sets from multiple places, scrape data, or receive data from clients or multiple departments, there are opportunities to create duplicate data. If you train a machine learning model on a dataset with duplicate results, the model will likely give more weight to the duplicates, depending on how many times they’ve been duplicated. So they need to be removed for well-balanced results. De-duplication is one of the largest areas to be considered in this process. This is usually the first technique used to clean data.

### Fix structural errors:
Structural errors include things like misspellings, strange naming conventions, improper capitalization, typos, incorrect word use, etc.  These inconsistencies can cause mislabeled categories or classes.  For example, you may find “N/A” and “Not Applicable” both appear, but they should be analyzed as the same category. 

Another example is if you’re analyzing different data sets and find that the gender values are Woman, Female, woman, w, female - you would have to standardize these to ensure consistency throughout the dataset. Similarly, things like dates (e.g., YYYY-MM-DD or MM-DD-YYYY), addresses, phone numbers, etc. need to be standardized so that computers can understand them.

The same applies to the names, and to avoid confusion and maintain uniformity, we should follow a standardized way of providing the column names. The most preferred code case is the snake case or cobra case. Cobra case is a writing style in which the first letter of each word is written in uppercase, and each space is substituted by the underscore character. While in the snake case, the first letter of each word is written in lowercase, and each space is substituted by the underscore. Therefore, the column name “Total Sales” can be written as “Total_Sales” in the cobra case and “Total Sales” in the snake case. Along with the column names, the capitalization of the data points should also be fixed.

Also, to avoid duplicate entries, ensure that values in the same columns follow the same naming standard. For example, email Id's ‘myemail@hostname.com’ and ‘MYEMAIL@HOSTNAME.COM’ can be interpreted as different email IDs, so making all the email ID values in the field lowercase is better. Similarly, we can follow the title case where all words are capitalized. 


### Handle missing data:
Since many algorithms will not accept missing values, ignoring missing data points or unanswered survey responses is not a solution for most applications. There are different options to handle this issue; each has some drawbacks. One option is to drop the observation that contains missing values; however, this will lead to losing information. Another option is to fill in the missing values based on other related observations or use some statistical techniques (e.g., Mean or Median values); however, this may lead to losing the integrity of the data where your data set now contains no actual observations. Another option is to change how the data will be used to navigate the missing values effectively; however, this limits the possible analysis and processing you can run on the data.


### Handle Outliers:

With data, there will be some off observations that do not appear to fit with the other data points you are analyzing or falls outside the norm. In some applications (e.g., security-related applications), identifying outliers is the core of the data analysis task.
However, in other applications, such outliers may significantly impact the overall statistics. Outliers can be removed if required. Another method to handle the outliers is to change their values (e.g., getting the average, getting the log value) to make them fit the normal distribution. 



## Data Cleaning Using Python
Python provides several libraries that can help data professionals clean and transform data. Pandas and NumPy are two of the commonly used libraries that provide wide range of methods and functions to deal with handling missing values, detecting and eliminating outliers, and translating data from one format to another.

+ [Pandas](https://pandas.pydata.org)
+ [NumPy](https://numpy.org)

dealing with missing values, eliminating outliers, and translating data into a model-friendly format. Additionally, eliminating redundant features or combining groups of highly correlated features into a single feature could lead to dimensionality reduction. 


In this repository, we will have a set of educational tutorials on using Python's Pandas and NumPy libraries to read and clean data. The tutorials covered in this repository are:

+ Locating and Handling Missing Data
+ Handling Duplicates
+ Detecting and Handling Outliers
+ [Visualize Data to detect Data Problems](https://github.com/AEEldin/Data-Visualization-Python)



More resources

# WeRateDogs - A Data Wrangling Project

The goal of this project is to wrangle a twitter account (@WeRateDogs) and to generate meaningful insight and visualization. WeRateDogs is a twitter account that rates people's dogs with a humorous comment. The data wrangling process involved 3 sections.

# Data Gathering
Three (3) different sources of datasets were used for this project. They are:

WeRateDogs TwitterArchive: This dataset was provided by udacity and downloaded manually as a csv format. It was read into a data frame using pandas read_csv method.

The Tweet Image Predictions: This is a tsv (tab separated file) dataset that was downloaded programmatically using the requests library. The dataset was saved locally to my computer and read into a pandas data frame.

Additional Data Using Twitter API: Twitter API (Tweepy) was used to collect additional data such as likes (favorite count) and retweet count using the tweet id in the enhanced twitter dataset. The Twitter API returned a JSON data which was saved into a text (.txt) file which was converted into a pandas dataframe.

## Assessing Data
After gathering all the dataset required, I assessed them visually and programmatically. The visual assessment was done in jupyter notebook and Microsoft Excel. For the programmatical assessment, different pandas functions/methods were used such as .info(), .head(), .isnull(), .duplicated(), and so on. I was able to identify 9 data quality issues and 2 tidness issues.


Quality Issues 
   
   `archive` table

* Timestamp column is an object data type
* There are some tweets with retweeted_id
* Null values are written as 'None' in all the dog stages columns
* Some of the values in the rating denominator column are not 10
* Source column contains html tags
* Some columns are not needed for the analysis
  
  `Image_prediction` table

* Duplicate values in jpg_url column
* Some images were not predicted as dog
* Some columns are not needed for the analysis

Tidiness Issues

* dog stages (doggo floofer pupper puppo) in 4 different columns in archive table
* all the 3 dataframes should be combined as one

## Cleaning Data
At this stage, I addressed the data quality and tidiness identified during the data assessment. I made a copy of the original dataframe before the cleaning process. I used the define-code-test framework, which was well documented. At the end, I created a master dataset, which was stored on my computer.

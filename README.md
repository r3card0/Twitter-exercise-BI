# Twitter - BI exercise 📊

[Tableau Dashboard](https://public.tableau.com/app/profile/ricardosaldivar/viz/ConferenceCandidates/Dashboard1?publish=yes)

![Candidates Viz](/img/CandidatesViz.png)

# Part A - Dashboard
It's required to:

1. Analyze and determine which Twitter user could be the best candidate creating the relevance KPI from the “retweets” and “favorites” measures.

2. Replicate the following dashboard where you can find 5 visualizations (3 graphs, 1 map, and 1 table) and 3 filters.

   - 1 Table with the top 20 Relevant candidates.
   - 1 bar chart with the distribution of the tweets by language.
   - 1 Map with the geographical tweets distribution by sentiment.
   - 1 Pie chart of tweets distribution by sentiment.
   - 1 open chart (as per your consideration) regarding tweets distribution by day on a weekly basis.

3. (Optional) Apply any additional features to enhance the user experience in the dashboard, such as drill-down capabilities, enabled search bar in filters, navigation buttons, custom tooltips or any other elements you want to propose.

This must be done in Power BI or Tableau. No other tool is accepted.

# Part B - Data modeling

PLEASE VERIFY WITH YOUR RECRUITER IF YOU ARE REQUIRED TO SOLVE THIS SECTION.

To facilitate further analysis of this data, the team has decided to design a data model to save the data coming from the csv file and then generate dashboards based on this model.

The team has defined that the grain in the fact table will be the tweet id (tweet_id column). From the  dataset provided you should be able to create a dimensional model abstracting all the involved concepts such as : User, Tweet, location, Etc.

We need you to:
Design a data warehouse logical model. It’s up to you if you use a star or a snowflake model or both.

In this model, please consider the following:

1. Add the fields you feel necessary to implement best practices and maximize the analysis of the data for the business.

2. We need to keep historical changes. At least, for the User dimension, we must keep track of the historical change of the User attributes. For example, an user may change its display name,  but it remains the same user. 

3. (Bonus Question) Besides a transactional fact table, propose a fact that facilitates the snapshot of total tweets count in a weekly basis.

# Outline
## Introduction
As a data analyst, D&AI Studio requires to analyze and determine which Twitter user could be the best candidate creating the relevance KPI from the "retweets" and "favorites" measures. Then, replicate the reference dashboard described on [Part A](/README.md#part-a---dashboard)
## Workflow
The process to accomplish this assigment will be as this after download the dataset: 
- Read the data set with Jupyter notebooks to perform data gathering and transformation process
- Then start a preliminary data analysis and create some charts related to reference dashboard
- Iterate serverals scenarios to figure out what is the best one for this solution
## Data Gathering & Transformation
In this step it was implemented the notebook [Data Gathering & Transformation](/Data_Gathering-Transformation.ipynb).

It's required to install the pandas and matplotlib libraries
```
conda install pandas
```

To visualice the distribution of the tweets geographically, it's required to install geopandas library to display the location geometry

```
conda install geopandas
```
Once installed, it can be calculated the geometry from coordinates data such as latitude and longitude

## Dashboard
Once the data set was normalized, it was loaded to Tableau to create the required dashboard and it can be visualized clicking on: [Tableau Dashboard](https://public.tableau.com/app/profile/ricardosaldivar/viz/ConferenceCandidates/Dashboard1?publish=yes)

## Data Analysis

The data analysis comes with the next outcomes and it can be reviewed on the next notebook:[Data Analysis](/DataAnalysis.ipynb)

* This data set contians 1726 tweets, created by 1516 users
* 1073 tweets are retweets and they represent the 62% of the total
* 653 are not retweets and they represent the 38% of the total
* Time period of time is from August 1, 2021 to August, 31 2021. Tweets of 31 days
* There were created 55 tweets in average by day
* 79 tweets were created at 2021-08-20. This is the maximum by day
* 43 tweets were created at 2021-08-07. This is the minimum by day
* The most languages used on the tweets are: English(491), Spanish(479), Italian(442) and French(312), and there is one tweet in Portuguese and one tweet in Wales
* The tweets are coming from 41 countries, where Philipines, contributed with 222 tweets and representing the 12% of the total.
* The tweets are comming from two sources, users and bots and 1636 tweets (94.79%), coming from users and 90 tweets (5.21%), coming from bots 




## Data Modeling
![modeling](/img/dataModeling.png)

For data modeling was proposed the model of the image.

The object TWEET was taken as a fact table, because around this object are relationships betweet the tweet and the other attributes contained on the CSV file, such as User, Sentiment, Source, Language, Counts, etc. **This is a snowflake schema ❄️** . For me, this schema helps to track the historical changes of the User attributes and also the location attributes can be mapped correctly, such as latitutde and longitude coordinates, that both belong to a city and a city belongs to a country. This location data coming from the CSV file.

## Conclusion
### Part A
* There is a data set of 1726 tweets in a period of time from August 1st to 31. There were unvolved 1516 users from 41 countries and for four languages. The most of tweets came from users, because there are bots too. The attributes retweets and favorite, showed the relevance of the tweets. 

### Part B
* A snowflake schema it's more effective to track the attributes from the Tweet, User and locations.

* The object Tweet was defined as a fact table
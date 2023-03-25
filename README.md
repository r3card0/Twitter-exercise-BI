# Twitter - BI exercise 📊

![Reference Dashboard](/img/referencedashboard.png)

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

## Part B - Data modeling

PLEASE VERIFY WITH YOUR RECRUITER IF YOU ARE REQUIRED TO SOLVE THIS SECTION.

To facilitate further analysis of this data, the team has decided to design a data model to save the data coming from the csv file and then generate dashboards based on this model.

The team has defined that the grain in the fact table will be the tweet id (tweet_id column). From the  dataset provided you should be able to create a dimensional model abstracting all the involved concepts such as : User, Tweet, location, Etc.

We need you to:
Design a data warehouse logical model. It’s up to you if you use a star or a snowflake model or both.

In this model, please consider the following:

1. Add the fields you feel necessary to implement best practices and maximize the analysis of the data for the business.

2. We need to keep historical changes. At least, for the User dimension, we must keep track of the historical change of the User attributes. For example, an user may change its display name,  but it remains the same user. 

3. (Bonus Question) Besides a transactional fact table, propose a fact that facilitates the snapshot of total tweets count in a weekly basis.
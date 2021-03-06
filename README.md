# Analysis of Kickstarter Campaigns

## Overview of Project
This project is an analysis of Theater Kickstarter campaign data relative to launch dates and funding goals. The data is taken from a set of various Kickstarters with differing goal funds and success, failure, and cancellation outcomes.  

### Purpose
The purpose of this project is to better understand the relationship between Theater Kickstarter launch dates relative to funding goals based on an exisiting Kickstarter dataset. The aim is to understand if there is an association with any particular launch month and the success or failure of reaching the Kickstarter's goals. Doing so will better inform the client of potential factors of Theater Kickstarter success and provide insight for future fundraisers.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

To begin, outcomes based on launch date were analyzed by first isolating the data that the client may find most useful from the larger Kickstarter set. First, the Year was isolated from the Kickstarter's launch date using the =YEAR function based on the date the Kickstarted was created (launch date):

![image](https://user-images.githubusercontent.com/103383489/172029692-259c4cf1-03e6-453a-821d-68db59808bec.png)

![image](https://user-images.githubusercontent.com/103383489/172029759-c0688e59-c681-45b7-a01e-a3e6858f8455.png)

Once the year of the launch date was isolated, a pivot table was created to view outcomes based on date created and using filters by "theater" and "years." All years were viewed for this analysis purpose and the dataset was filtered exclusively for the theater Parent Subcategory. This is so the client can easily view the number of campaigns based on outcome by certain months of the year (factoring in every single year on the Kickstarter data set), as well as totals for each outcome relative to the grand total of theater Kickstarters.

![image](https://user-images.githubusercontent.com/103383489/172029838-0c1618df-8501-485f-b837-fca4dc545ec5.png)

![image](https://user-images.githubusercontent.com/103383489/172029850-88da48fb-02e0-4d49-8400-a18e855d0091.png)

From this pivot table information, a line chart was considered to be the most useful in visualizing the percentage rate of success, failure, and cancellation of Kickstarters over a year's period as it takes into consideration the total number of campaigns under each outcome and is easily readable for a data set extending over twelve months. 

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/103383489/172030112-528f406d-05ab-4240-8182-cee9dc18a512.png)

Based on these two visualizations, it can be noted that the majority of the successful campaigns started in May, June, July, and August (out of 839, May: 111, June: 100, July: 87, and August: 72) and the highest number of failed campaigns were in May, July, and October (out of 493, May: 52, July: 50, October: 50). 

May marginally is the highest rate of successful campaign months (representing 13.2% of the total successful campaigns), whereas June is the second highest rate (representing 11.9% of total successful campaigns). Failure outcomes of Kickstarters were highest in the months of May, July, and October, with May representing the highest amount of failure rates for total failed campaigns (10.5% of the total failed campaigns).  


### Analysis of Outcomes Based on Goals
Next, outcomes based on goals were considered by means of dollar-amount range and percentage of specific outcome. The COUNTIF function was used to detect the goal amount number ranges based on whether or not they were successful, failed, or cancelled. Based off the number of goal amount number ranges, percentages of successful, failed, and cancelled campaigns were calculated. 

![image](https://user-images.githubusercontent.com/103383489/172031241-e2e2e78a-d35a-42cc-a1fc-b92aa7af69f6.png)

![image](https://user-images.githubusercontent.com/103383489/172031249-990f13a2-41cd-4110-9477-1705444b063b.png)

Based on these percentages, a line chart was created to visualize the percentage of outcome rate based on goal ranges. Percentage cancelled was found to be a rate of 0 notwithstanding goal data. 

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/103383489/172031376-7f7cc1db-e9a0-4ef6-bf4a-31f4247bbc8c.png)

Kickstarters were most successful with a goal with less than $1000 at a 76% success rate, however it does not seem that having a higher goal set impacts success rates as goals between $35,000 to $44,999 were both at 67% success rates. 


### Challenges and Difficulties Encountered
Possible challenges or difficulties that could be encountered could be data that has inaccurate outliers in donation amount, thus skewing pledged numbers or errors in date conversions from the Unix timestamps conversion (unreadable format). When using the VLOOKUP function, there may not be a comparable campaign in the current dataset with searchable verbiage to one that the client may want to investigate. None of these challenges or difficulties impacted this instance of data research.  

## Results
Regarding theater outcomes by launch date, it should be considered that launch dates in May, June, July, our August are most successful based on the analysis of this data set, as their ratio to failed campaigns had the highest differences. May could be considered as a month to begin the campaign as the ratio of highest success rate to lowest failure rate was in May with successful campaigns representing 67% of the total overall campaigns and failed campaigns representing 31%. 

December had the lowest rate of Kickstarters and also the closest ratio between successful and failed Kickstarters, so it may be more advisable to consider a campaign with a Start Date in the months of May or June and not consider a campaign start date in December.

When considering outcomes based on goals, it may be advisable to set a goal between the range of $35,000-$44,999 as the ratio between percentage successful and percentage failed were 67:33. However, it should be considered that there were 9 total projects for the ranges of $35,000-$44,999 and 186 total projects for the ranges under $1,000, so the ratios may be skewed inaccurately and may require further data collection. There was the most data at 534 projects for the goal range of $1,000 to $4,999 with a success to failure ratio of 73:27, making this a candidate for a target goal range, dependent on the client's project budget.

While no major challenges or difficulties arose when isolating data for outcomes based on goals and launch dates, there are a few considerations that came up during the analysis process. First, it may be useful to isolate most recent years of Kickstarters, as success/failure outcomes may be more accurate for our new campaign when considering more recent years. 

It may be helpful to outcomes based on goals but isolated by the most recent years' launch date. This can easily be filtered by the client with the pivot table created for outcomes based on launch date. The dataset ends in 2017, so more finding a data set with more recent information would prove beneficial to further analysis. Something else to consider may be Kickstarter length relative to outcome. When did the Kickstarter end and compared to when it began and how did that affect its success? 

It may also be helpful to create a box and whisker plot demonstrating pledged amounts relative to goal amounts, to see if any outliers played a role in whether or not a campaign was successful (and perhaps gather information on where and why those outliers were happening). Variance of failed campaigns may be useful to look at relative to outcomes by launch date as there was not much variability between months. This is where the dataset was limited: it may be useful to have qualitative survey comments or quantitative (Likert scale, etc.) backer feedback to see why they contributed the amount they did and why they did not contribute more/less. The data gathered on backer feedback may have more insight as to how best market for this new Kickstarter.

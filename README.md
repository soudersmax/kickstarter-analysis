# Kickstarting with Excel

## Overview of Project

### Purpose

​	Client intends to create a Kickstarter campaign to fund the production of her new play *Fever*, but needs guidance on how best to plan said campaign. To accomplish this, aggregate data was pulled from Kickstarter, including date launched and closed, goal amounts, pledged amounts, campaign outcome, country of origin, number of backers, and categories for the type of campaign.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

​	To capture the best time of year to begin the client's campaign, the aggregate data was filtered to include only those campaigns in the "Theater" parent category. The data was then further delineated by the year created, and displayed as a table and chart based on the month it was initialized and the outcome (Successful, Failed, or Canceled). This information was then plotted on a line chart by displaying the number of campaigns on the Y-axis, Month Created on the X-Axis, and outcomes as value series.  



<p align="center">
  <img src="Resources\theater_outcomes_vs_launch.png" style="zoom: 67%;" />
    Figure 1: Outcomes vs Launch Date
</p>




### Analysis of Outcomes Based on Goals

​	To capture the landscape of campaigns based on their fundraising goal amounts, a new table was created to include quantitative categories for the goal amount (less than $1000, $1001 - $4999, $5000 - $9999, $10000 - $14999, $15000 - $19999, $20000 - $24999, $30000 - $34999, $35000 - $39999, $40000 - $44999, $45000 - $49999, and greater than $50000).  The campaign data was then sorted into columns displaying the raw number successful, failed, and canceled. To standardize the data, the raw information was converted into a percentage of the campaigns in a given goal category for each outcome. This information was then plotted on a line chart, with Percentage of Campaigns on the Y-Axis, Fundraising Goal on the X-Axis, and outcomes as value series.



<p align="center">
  <img src="Resources\Outcomes_vs_Goals.png" style="zoom: 67%;" />
    Figure 2: Outcomes Based on Goal
</p>




### Challenges and Difficulties Encountered

​	While there were no significant challenges encountered regarding the processes used to clean and analyze the data set, it is worth noting that someone unfamiliar with Unix time stamps would likely encounter a challenge converting the "deadline" and "launched_at" columns to usable form. In addition, further analysis based on columns such as "spotlight" and "staff_pick" isn't necessarily viable, as they are not contextualized unless you're familiar with Kickstarter as a platform.

​	Additionally, one major issue I found with the prescribed analysis for the project is that neither "country" nor "currency" were normalized or converted for the "Outcomes Based on Goals" deliverable. This part of the project needs additional filtering and standardization before indicating truly applicable information. For example, even though "Daemon's  scale up - Brieuc Le Meur _ Berlin" had a goal of 50 Euros and was successful, this is not necessarily comparable to "Industry  Success Project (Canceled)," a US based project with a goal of 50 USD. While the difference at the 50 unit level is small in this case (50 EUR = 56.61 USD on the date of launch), that may not be the case for each currency or around each date. Thus, it is probable that the data in the "Outcomes Based on Goals" deliverable is skewed in some way. In fact, filtering based on country to US Only, the most efficient (though limiting) way to create standardized currency data, mostly affects those data points from the "$15000 - $19999" category through to the "$35000 - $39999" category. While overall trends remain comparable, the differential between the percentage successful and percentage failed greatly decreases, making any conclusions from the original chart slightly less significant. It is likely that true standardization of currency would provide a more insightful view into real differences between goal amounts.



## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
  - Conclusion 1: Summer (May and June) is the most popular time to launch a campaign in the "theater" category, and it maintains the highest percentage of successful campaigns throughout the year. 
  - Conclusion 2: Launching a "theater" campaign in the winter months (November, December) has the lowest chance of success, with the number failed and number succeeded essentially equal. 
- What can you conclude about the Outcomes based on Goals?
  - Conclusion: Overall, the lower the goal amount, the more likely a campaign will succeed. However, the limited number of projects in the $40,000 to $49,999 categories showed approximately 67% success rates, indicating that there may be some other factors influencing the success of campaigns with  much larger goal amounts. 
- What are some limitations of this dataset?
  - This data set does not fully encompass potential factors of successful campaigns. For example, many Kickstarter campaigns include reward and incentive tiers, which could influence the number of backers, the average pledged amount, and the eventual success of the campaign. An additional limitation is the number of records in the "plays" subcategory. While there are enough points to create an acceptable analysis, it could be much stronger  with additional support. This in itself does create an interesting point of analysis, though: there are other platforms similar to Kickstarter - are plays more highly represented on any of those?
  - As mentioned above there are some analytical limitations regarding the currency/country of production. This could be overcome through additional calculations and/or filtering.
- What are some other possible tables and/or graphs that we could create?
  - A table or chart plotting "staff_pick" vs "outcome" could provide insight regarding how effective Kickstarter's additional publicity is. While this is mostly something out of control of the client, taking a deeper look at those projects that are selected by Kickstarter staff and comparing it to the project page and specs of *Fever* 's landing page could prove helpful. 

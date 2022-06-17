# Kickstarting with Excel

## Overview of Project

### Purpose
Louise's play *Fever* came close to completing it's fundraising goal. She is curious about other theatre kickstarters and how they did based on their launch date and fundraising goals. Given the dataset of kickstarter campaigns by Louise (available to download [here](/Kickstarter_Challenge.xlsx)), we are going to create new columns, pivot tables, and charts to help visualize the kickstarters to her liking. In doing so we will sharpen our Microsoft Excel data management and visualization skills. 

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

To analyze the theater outcomes based on the launch date we need only theater, outcomes, and date launched data. I created a pivot tabel in excel by highlighting all the data and inserting pivot table. The strength of a pivot table is I am able to filter my data based on the columns. I added a "Parent Category" filter and only selected "theater" and added launch date to the rows and outcomes to the columns. It gave me a pivot table that looked like this:

![](/Resources/Theater_Outcomes_vs_Launch_PivotTable.png) ![](/Resources/Theater_Outcomes_vs_Launch_PivotTableFields.png)
>*Pivot Table and Fields*

For duration of time, a good visualization method is the line chart. Using our newly filtered data I inserted a line chart that you see below: 

![](/Resources/Theater_Outcomes_vs_Launch.png)
>*Figure 1*

### Analysis of Outcomes Based on Goals
For the analysis of outcomes based on goals a table was created to show the number of successful, failed, and cancelled kickstarters there were based on what their goal amounts were. We needed to use the `countifs()` formula in excel to gather the total number of projects by each outcome. Countifs() takes an array of data as the first parameter and a condition to filter the data as the second. This can be performed multiple times and so we can effectively total the number of successful theater kickstarters for various goal amounts. The functions looks like: 
```
= COUNTIFS(Kickstarter!$D:$D,"<1000",Kickstarter!$F:$F,"successful",Kickstarter!$R:$R,"plays")
```
Here we are looking at only play kickstarters that are successful with a goal less than $1,000. We are then able to generate percentages using `(Number of projects filtered/total projects)` and changing the format to percentage. The table generated is below as *table 1*. Finally we created another line chart to show the relationship between outcomes and goal amounts that is below:

![](/Resources/Outcomes_vs_Goals_Table.PNG)
>*Table 1*

![](/Resources/Outcomes_vs_Goals.png)
>*Figure 2*

### Challenges and Difficulties Encountered
In order to create the outcomes vs goals graph, we needed to grab the total number of successful, failed, and cancelled projects from out kickstarter dataset sheet. The `= countifs()` formula was particularly confusing to me. At first, I thought you needed a bunch of nested formulas to search each column with a differing condition. The `countifs()` formula takes a set of data and a condition, which you could enter as many times as you wanted. Conceptually it was confusing how the set of data was different each time. And so I kept getting an incorrect figure for *Figure 2*. After working for some time I realize the first "data" condition that is passed must match the size of every subsequent set of "data". I see how this makes the countifs() formula so powerful!

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
    1. The number of failed or cancelled theater kickstarters does not change with month of the year started.
        - If you look at *Figure 1* you can see the red and yellow lines, labelled failed and cancelled respectively, do not change drastically depending on the month. If you are trying to figure out why your theater kickstarter failed, the time of year you launch it does not seem to matter. There might be another factor as to why theater kickstarters fail or get cancelled.
    2. Successful theater kickstarters are more common in May through July than any other month.
        - Continuing to look at *Figure 1*,  the green line or Successful theater kickstarters, shows a spike during May through July. More specifically, the number of successful kickstarters increases from the start of the year until May and then decreases until the end of the year. Based on *Figure 1*, we can say launching a theater kickstarter in May through July would be a smart idea given how many successful theater kickstarters started in those months.

- What can you conclude about the Outcomes based on Goals?
    - When looking at *Figure 2* we see the percentage of successful vs failed theater kickstarters based on their funding goals. It seems the percentages fluxuate rapidly for kickstarter goals greater than $30,000. Thus, looking at kickstarter goals less than $30,000 we notice the higher the goal amount is, the lower the percent success is. This intuitively makes sense as the higher the goal, the more money needed to fund it. For kickstarters less than $1,000, there is almost a 80 percent success rate, whereas kickstarters between $25,000 and $29,999 only have roughly a 20 percent success rate.

- What are some limitations of this dataset?
    - The main limitation of this dataset is the raw number of kickstarters. The more data we have, the stronger our analysis can be. As mentioned previously, there are very few kickstarter campaigans above $30000 for their goals, and thus it is hard to develop good analysis of outcomes based on goals past that amount. Another limitation is the time these kickstarters took place. It looks like we have kickstarters from 2009 - 2017. What if this was a good/bad period for kickstarters? What if kickstarters are not funded as well now in 2022? The last limitation I will talk about is regions. The only data we have for location of the kickstarter is country. In the US for example, there might be a large difference if the kickstarter was being funded in California vs Missouri. Or maybe west coast cities are more likely to fund kickstarters than east coast due to their proximity to Los Angeles.
- What are some other possible tables and/or graphs that we could create?
     1.  We could filter our outcomes based on launch date by country and create a pivot table/chart that only shows theaters in the United States. This would more closely relate to Louise's play.
     2.  Instead of looking at percentages for outcomes based on goals, we can use the total number of projects. When working with lower numbers of projects it is hard to see the effect using percentages. We could create a clustered column chart using the number of successfull, failed, and cancelled projects. This would allow us to see most of the theater kickstarts have between $1000 and $4999 goals and more than two-thirds are successful!

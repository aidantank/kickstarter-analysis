# Kickstarting with Excel

## Overview of Project

### Purpose
Louise's play *Fever* came close to completing it's fundraising goal. She is curious about other theatre kickstarters and how they did based on their launch date and fundraising goals. Given the dataset of kickstarter campaigns by Louise (available to download [here](/Kickstarter_Challenge.xlsx)), we are going to create new columns, pivot tables, and charts to help visualize the kickstarters to her liking. In doing so we will sharpen our Microsoft Excel data management and visualization skills. 

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date  

![](/Resources/Theater_Outcomes_vs_Launch.png)
>*Figure 1*

### Analysis of Outcomes Based on Goals

![](/Resources/Outcomes_vs_Goals.png)
>*Figure 2*

### Challenges and Difficulties Encountered

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
    1. The number of failed or cancelled theater kickstarters does not change with month of the year started.
    2. Successful theater kickstarters are more common in May through July than any other month.
    

- What can you conclude about the Outcomes based on Goals?
    1.  Below $30000, where you see most of the projects, the lower the goal is, the higher the percent successful. After $30000, due to the low number of projects, it is hard to develop any sort of conclusion.

- What are some limitations of this dataset?
  - The main limitation of this dataset is number of kickstarters. The more data we have, the stronger our analysis can be. As mentioned previously, there are very few kickstarter campaigans above $30000 for their goals, and thus it is hard to develop good analysis of outcomes based on goals past that amount. Another limitation is the time these kickstarters took place. It looks like we have kickstarters from 2009 - 2017. What if this was a good/bad period for kickstarters? What if kickstarters are not funded as well now in 2022? The last limitation I will talk about is regions. The only data we have for location of the kickstarter is Country. In the US for example, there might be a large difference if the kickstarter was being funded in California vs Missouri. Or maybe west coast cities are more likely to fund kickstarters than east coast due to their proximity to Los Angeles.  

- What are some other possible tables and/or graphs that we could create?
  1.  We could filter our outcomes based on launch date by country and create a pivot table/chart that only shows theaters in the United States. This would more closley relate to Louise's play.
  2.  Instead of looking at percentages for Outcomes based on goals, we can use the total number of projects. When working with lower numbers of projects it is hard to see the effect using percentages. We could create a clustered column chart using the number of successfull, failed, and cancelled projects. This would allow us to see most of the theater kickstarts have between $1000 and $4999 goals and more than two-thirds are successful!
  3.  Maybe we need more time to get backers, so we could look at number of backers 

# Kickstarting with Excel

## Overview of Project

### Purpose
Louise's play *Fever* took only a short amount of time to come close to her goal. As a result, she is requesting an analysis of how other campaigns fared in relation to their launch dates and funding goals.
    
## Analysis and Challenges
### Analysis of Outcomes Based on Launch Date
![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/100883212/159586001-d80a11a4-e4dd-4bf3-b4b7-59b59fb76264.png)
  
For this chart, I narrowed down the sample data by creating a pivot table filtered for "Parent Category" and "Years" and removed the live campaigns from the data. From here, I narrowed down our data set to only include campaigns with a Parent Category of "theater." In order to provide an easily-digestible visual for Louise, I created a line chart from the pivot table, pictured above.
    
### Analysis of Outcomes Based on Goals
![Outcomes_vs_Goals](https://user-images.githubusercontent.com/100883212/159398548-500388d9-fb67-4390-87c9-4bfca859fd4b.png)

For our Goals analysis, I divided the goals into twelve categories and used a COUNTIFS() formula to sort each campaign into their respective category. I separated the data further by creating two columns - one for successful campaigns and another for failed campaigns. We then divided the number of successful campaigns in each category by the total number of campaigns in that category (calculated using a SUM() equation) to calculate the percentage of successful campaigns per category, and then repeated this process to find the percentage of failed campaigns. Finally, I used this data to create a line chart so Louise can easily see where the campaign outcomes lie based on their goal amounts.

### Challenges and Difficulties Encountered
The biggest diffuculty I encountered with the analysis was ensuring the COUNTIFS() formulas were correct for the Outcomes Based on Goals chart. While it's easy to copy and paste the formula into all of the needed cells, I had to pay great attention to ensure I was typing in the different information for each category correctly. Because there were 12 categories, all of the numbers started to run together after a bit.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
  - Statistically, the best month to launch a campaign is May due to the large spike in the line chart. The worst month to launch a campaign is December as 49% of campaigns launched in December failed to meet their goal, likely due to the holidays.

- What can you conclude about the Outcomes based on Goals?
  - Overall, Kickstarter campaigns with goals less than $14,999 statistically had a higher chance of being fully funded than campaigns with higher goals. There were 24 total campaigns with goals between $15000 and $19999, and these campaigns had an equal percentage of successes vs. failures. Starting at the $20000 goal mark, the majority of the campaigns failed, with the exception of campaigns with goals between $35000 and $44999. This grouping saw a greater number of successful campaigns than it did failures.

- What are some limitations of this dataset?
  - One limitation of this dataset is that it represents a sample of campaigns created in Kickstarter, not the entire population. The sample also contains quite a few obvious outliers for their goals that skew the analysis. An example of this is that every campaign with a goal of $1,000,000 or higher either failed or was canceled. Since Louise's campaign had a much smaller goal than that, the sample could have been reduced to only include campaigns with a more reasonable range of goals for a more accurate comparison.

- What are some other possible tables and/or graphs that we could create?
  - A helpful chart to create for this study would be a line chart showing the outcome based on average donation to see if projects with larger average donations from fewer patrons had a better chance of being fully funded over those with lesser average donations from more patrons. 

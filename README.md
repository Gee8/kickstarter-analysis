# Kickstarting with Excel

## Overview of Project
We looked at a data set consisting of kickstarter campaigns, whether or not they were successful, their goals for funding, the amount they recieved, and the date they launched.

### Purpose
    The purpose of the analysis was to see the theater kickstarters outcomes based on their launch date and the funding goals of the campaigns within the plays subcategory. 

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
For our analysis of outcomes based on launch date we created a pivot table and pivot chart to visualize our data. The pivot table can be filtered by both parent category and years, with the rows being the months of the year and the columns as their outcomes. With this data we created a line chart to show the number of each successful, failed, and cancelled theater outcomes throughout each month. Shown below are the pivot table and chart for our theater outcomes based on launch date.

![2021-03-18-15-47-22](https://user-images.githubusercontent.com/78509850/111724447-7d74bc00-8822-11eb-9386-be0f520bf305.png)


### Analysis of Outcomes Based on Goals
Each kickstarter campaign had a goal for funding. To see the relationship between goal amount and success, we created a table with rows of goals in about $5,000 increments, and the columns with the count of successful, failed, cancelled, total and their percentages, respectfully. To find these counts, we used the COUNTIFs function. Because we are finding data to draw conclusions with respect to a play, we only counted kickstarters within the play subcategory. For example, to find the number of successful kickstarters for plays who had a goal of $5,000 to $9,999, we used `=COUNTIFS(Kickstarter!D:D,">=5000",Kickstarter!F:F,"successful",Kickstarter!R:R,"plays",Kickstarter!D:D,"<=9999")` to find that there were 93. Shown below is the populated table and line start for outcomes based on goal.

![2021-03-18-15-50-25](https://user-images.githubusercontent.com/78509850/111724402-66ce6500-8822-11eb-84c0-179b17a3a3b3.png)


### Challenges and Difficulties Encountered
A challenge I faced while making the pivot table for the theater outcomes based on launch date was figuring out how to organize the columns. I first overlooked the filter because it said decending order and I was trying to organize words, but after trying out the filters I was able to organize the columns correctly.

A difficulty I faced while finding the outcomes based on goals was populating the table itself. If I tried to copy one function and enter it into the next line, it would also change the range it was looking at to count. To overcome this I just found the first manually then populated the rest of the column automatically. This solved the range issue, but I still had to change each of the values for each row manually. Since it was a small table it wasn't too time consuming, but after learning about VBA, I would have tried to write a macro to populate the cells instead of doing most of each manually.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
    - Regardless of the month for the launch, there were more successful theater launchs than failed ones. 
    - We can also see that the months of May, June, and July have many more successful launches than the rest of the months.

- What can you conclude about the Outcomes based on Goals?
    - With a lower goal, play kickstarters seem to have a higher chance of succeeding. Other than the few who had goals between 35000-45000, the play kickstarers succeeded more than failed when their goal was less than 20000.

- What are some limitations of this dataset?
    - When we are just looking at goals or launch date, we ignored the amount that was pledged to the kickstarter. The kickstarters who had small goals and succeeded doesn't tell us that they succeeded because of their small goal or because of the amount that they recieved.

- What are some other possible tables and/or graphs that we could create?
    - To adress the limitation above, we could make another chart similar to the one we made about goals, but instead of goals we looked at amount pledged. This could give us an idea about how successful kickstarters based on the amount pledged. We could then make another line chart to see if the more money pledged led to a higher success rate.

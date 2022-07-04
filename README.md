# An analysis of kickstarters campaign
Analysis of kickstarters data
[data-1-1-3-StarterBook.xlsx](https://github.com/sirjanashrestha/kickstarter-analysis/files/9013234/data-1-1-3-StarterBook.xlsx)

# **Kickstarting with Excel**
## Overview of Project
Louise is an upcoming Playwright who wants to start a crowdfunding campaign to fund her play "Fever". She has an estimated budget of over $10,000 and she is reluctant to jump into crowd funding campaign without prior study and analysis. This project entails use of excel to analyze various project campaigns launched between 2009 and 2017 in 21 different countries.

### Purpose
The purpose of this analysis is to organize, sort and analyze the crowdfunding data to determine whether there are specific factors that make a project's campaign successful which will help Louise plan her campaign for successful outcome. 

## Analysis and Challenges
Here, we are going to use Excel to perform the analysis of crowdfunding data. First we will look at the data of theater to analyze the campaign outcome based on launch date and then we will look at the data of Plays to analyze the campaign outcome based on goal.

### Analysis of Outcomes Based on Launch Date
The main tools used for this analysis are PIVOT table and Charts.

Step 1: We have to convert the column (J) launched_at which is in UNIX timestamp format to date.  A detailed information on timestamp can be found on this link; 
https://websiteseochecker.com/blog/what-is-timestamp/

![image](https://user-images.githubusercontent.com/107566776/177178053-0df612b4-21d8-4143-af11-6f8029813171.png)

R2=(((J2/60)/60)/24) +DATE (1970,1,1)

Launch date(T2) =YEAR(R2)

Launch MonthU2) =TEXT(R2,"mmm")

Step 2: Parent Category and Subcategory is created from Category and Subcategory column using Text to Column.

Step 3: Pivot Table is formed for Theater launch outcomes as "Successful", "Failed" or "Canceled" based on launch date. Parent Category is filtered for Theater.

 ![image](https://user-images.githubusercontent.com/107566776/177178316-bf3e47b2-ebd1-48d3-96e4-d80a2a3833c8.png)

The Pivot field input as above generates following pivot table which shows theater outcomes launched by month.
 ![image](https://user-images.githubusercontent.com/107566776/177178487-915bfa09-1cb8-423d-8a3f-0a77688acfe7.png)

Step 4: Finally, we will use line chart to generate a visualization of above table, which provides theater outcome based on launch month as below.

 ![image](https://user-images.githubusercontent.com/107566776/177178516-65128408-f68a-40d4-b7ed-2ebe331ea0cb.png)

### Analysis of Outcomes Based on Goals
Now we will look at Plays to analyze the campaign outcome based on goal. The main tools used for this analysis are COUNTIFS and line chart.
Step 1: First, we will categorize Goal into 12 groups so that we can have a better understanding of our dataset.

Step 2: Then we will count the total number of projects in each group based on three outcomes "Successful", "Failed" and "Canceled" using COUNTIFS function.

Based on these data, we will calculate percentage successful, percentage failed and percentage canceled for each category.
Our final table should look like this;

![image](https://user-images.githubusercontent.com/107566776/177178586-a2a2f89f-427d-4fcd-bd87-ac1b64698d90.png)

Step 3: Finally, with the help of line chart, we will see what percentage of project campaign under different goal category succeeded or failed based on their set goal as below.

![image](https://user-images.githubusercontent.com/107566776/177178663-d0a4c23e-6b54-4618-a3f5-5732f92dde82.png)

### Challenges and Difficulties Encountered
The main challenges that I encountered during the analysis were;
1.	Creation of Parent category and subcategory: I had trouble creating parent category and subcategory. So, I could not filter my data set based on theater or plays at the beginning. To overcome this challenge, I went through modules and asked for a session with instructor during office hours.
2.	Use of COUNTIFS function: I had difficulty using COUNTIFS function for different parameters. For this, I referred to hint on Excel provided on module and this YouTube video
https://www.youtube.com/watch?v=if4i55JB58M


## Results

- Outcomes based on Launch Date

1.Theater projects launched during May were more successful. February, May and October were the peak season for theater project with successful outcomes. 
2.No Projects were cancelled during October.

- Outcomes based on Goals
1. No Projects were cancelled in Plays Subcategory.
2. Projects with goal below 15,000 or between 32,000 and 42,000 were successful. 

- Limitations of dataset
Some of the limitations of dataset are;
1.	The number of live projects are not considered for the analysis.
2.	Theater outcome based on launch date is analyzed based on launch month than years.
3.	For some goal categories, the no. of project is few. For instance, for goal category of 45,000 to 49,999, total no. of project is 1.

- Other possible tables and/or graphs

We can analyze how theater project fared based on launch year. We can observe from the line chart that most of the campaigns were launched between year 2014 and 2016, with most successful campaign being launched in the year 2015.
 ![image](https://user-images.githubusercontent.com/107566776/177178703-e3beddc3-bb84-4f85-86cb-b6a5aa4e86a6.png)


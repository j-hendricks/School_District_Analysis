# School_District_Analysis

## Overview
In this project, we are tasked with analyzing standardized test data for several schools in the same school district, the goal being to find performance trends and patterns. This data will be used by the local school board to make decisions on school funding in the school district. The school board has provided us with school funding data and standardized test scores, which were separated into csv files containing ![school data](Resources/schools_complete.csv) and ![student data](Resources/students_complete.csv). The ![analysis](jupyter_notebook/PyCitySchools_Challenge.ipynb) was performed using Python and Jupyter Notebook.

Two problems arose when analyzing the student data: 1) several student names contained incorrect prefixes and suffixes, such as MD or PhD. These misnomers were cleaned using basic string manipulation. 2) There were reports of cheating in the ninth grade class at Thomas High School (THS). As a result, standardized test scores had to be removed for these students, which only slightly altered the resulting statistics for THS.

## Results

After removing the 9th grade scores at THS, the rankings of each school remained the same. Rankings were determined by calculating the percentage of students who passed both the reading and math tests for each school. The top 5 schools are as follows:

* Cabrera 
* Thomas 
* Griffin 
* Wilson
* Pena

The bottom 5 school are as follows:

* Rodriguez
* Figueroa
* Huang
* Hernandez
* Johnson

As seen above, Thomas High School maintains its ranking as the 2nd top-scoring school. Since these ranking remained the same, removing the 9th grade scores at THS does not alter the overall analysis and therefore should not be included in the data presented to the school board. 

Even when looking at the scores and passing percentages of THS exclusively, there appears to be no significant difference before or after removing 9th grade scores. 

![Before](analysis/THS_Initial.png)
![After](analysis/THS_Final.png)

The differences in percent-passing are all 0.3% or less, and do not effect the school ranking for THS. 

In addition, the average score and percentages remain the same for:

* the spending bins
* the size bins
* between charter and district

When analyzing the spending bins, it is evident that spending more money per student does not translate to higher achievement on standardized testing. In fact, schools with a budget of less than $586 per student achieved the highest overall passing rate compared to all other spending brackets, and those in the highest bracket ($646-675) score the lowest. Therefore, the school board must consider other factors besides funding when deciding how to improve test scores. 

One such factor is the type of institution conducting the education. As seen below, charter schools have an overall passing percentage that is 40% higher than that of the district schools. Therefore, there must be differences between these two school types that are causing the discrepnacy. Perhaps it is the way the material is taught, or perhaps there are differences between the type of students who attend charter versus district schools. These are only speculations and cannot be verified with this data. In the school size summary table, there is a sharp difference in overall passing rates between large schools and medium or small schools. School with less than 2,000 students perform far better, but again we can only speculate why from this data. 

![Spending Bins Summary](analysis/Spending_Bins_Summary.png)
![School Type Summary](analysis/School_Type_Summary.png)
![School Size Summary](analysis/School_Size_Summary.png)


## Summary

The schools achieving the lowest overall passing rates are those that either: 1) are district 2) spend more money on average per student 3) have a student population of 2,000 or more. These are important observations that must be reported to the school board. However, it is difficult to say with certainty why these discrepancies have occured - we can only speculate given only this data. 

Despite having to remove the 9th grade scores for THS, the average test scores and passing percentages remained the almost exactly the same. Therefore, the cleaned data should be presented to the school board, though the removal of data should be noted during the presentation. 

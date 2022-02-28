# School District Analysis

## Project Overview

> The school board has notified Maria that the students_complete.csv file shows evidence of academic dishonesty; specifically, reading and math grades for Thomas High School ninth graders appear to have been altered. Although the school board does not know the full extent of the academic dishonesty, they want to uphold state-testing standards and have turned to Maria for help. We have been asked to replace the math and reading scores for Thomas High School with NaNs while keeping the rest of the data intact. Once the math and reading scores have been replaced, we will then need to repeat the school district analysis and write up a report to describe the impact of these changes on the overall analysis.
## Resources
* Data source: schools_complete.csv, students_complete.csv
* Software: Python 3.7.10, Anaconda, Jupyter Notebook

## Results

### District Summary Impact


* New District Summary excluding Thomas High School 9th Grade reading and math scores
 ![](https://github.com/timbialek/PyCity_School_District_Analysis/blob/main/Resources/District_Summary_Original.png)

* Original District Summary including Thomas High School 9th Grade reading and math scores
 ![](https://github.com/timbialek/PyCity_School_District_Analysis/blob/main/Resources/District_Summary_New.png)

 	
* The impact to the district summary is minimal and as you can see in the above two images can only be noticed when looking summary at the one-hundredth decimal place.   
	* Average Math score increasing by .01, 
	* Average Reading score staying the same
	* % Passing Math increasing by .02
	* % Passing Reading increased by .01
	* % Overall passing increasing by .03

* What is not seen in the district summary images is that the number of students used to perform the calculation went from 39,170 to 38,709 once the 9th grade students from Thomas high school are removed.  This decrease of 461 is only 1.18% of the total student population so it is not surprising that there was a virtually no impact to scores.  


----------


### School Summary Impact
* When viewing the school summary, the only the line for Thomas high school was impacted since as no other schools had their data modified for the potential academic dishonesty.  Below is the before and after summaries for Thomas High School and the complete school summary for the new and original can be found by clicking on the following links: [New School Summary](https://github.com/timbialek/PyCity_School_District_Analysis/blob/main/Resources/School_Summary_New.png) and [Original School Summary](https://github.com/timbialek/PyCity_School_District_Analysis/blob/main/Resources/School_Summary_Original.png)
* As you can see in the below two images for Thomas High School there are some impacts to the scores as follows:
	* Average math score decreased by  -0.067412  (-0.08%)
	* Average Reading Score increased by +0.047152  (+0.06%)
	* Passing Math decreased by -0.086481  (-0.09%)
	* Passing Reading decreased by -0.29013  (0.30%)
	* Overall Passing decreased by -0.317688 (-0.35%)


New School Summary for Thomas High School excluding 9th Grade reading and math scores
![](https://github.com/timbialek/PyCity_School_District_Analysis/blob/main/Resources/Thomas_High_School_New.png)

Original School Summary Thomas High School including 9th Grade reading and math scores
![](https://github.com/timbialek/PyCity_School_District_Analysis/blob/main/Resources/Thomas_High_School_Original.png)


----------


### Ranking Impact
•	Replacing the 9th grade scores for Thomas High School had no impact on the school ranking as it places 2nd overall in the top 5 in both the new and original rankings as seen in the below images. 


Original Top #5 % Overall Passing
![](https://github.com/timbialek/PyCity_School_District_Analysis/blob/main/Resources/School_Ranking_Original.png)

 
New School Rankings Rankings:
![](https://github.com/timbialek/PyCity_School_District_Analysis/blob/main/Resources/School_Ranking_New.png)


----------

### Impact of Replacing the 9th Grade Scores

* **Impact of Replacing the Math and Reading scores by grade**

	* The impact to replacing the 9th grade scores for Thomas High School is that they are no longer taken into account in the calculation of the scores and are reflected as null values in the data or nan when viewing the dataframe as in the below image.

New Math and Reading Scores by Grade
![](https://github.com/timbialek/PyCity_School_District_Analysis/blob/main/Resources/Math_and_Reading_Scores_New.png)

Original Math and Reading Scores
![](https://github.com/timbialek/PyCity_School_District_Analysis/blob/main/Resources/Math_and_Reading_Scores_Original.png)

----------


* **Impact on Scores by School Spending**

	* There is no impact on the spending per student because we did not adjust the number of students for the spending calculation.

New Scores by School Spending
![](https://github.com/timbialek/PyCity_School_District_Analysis/blob/main/Resources/Scores_by_Spending_New.png)

Original Scores by School Spending
![](https://github.com/timbialek/PyCity_School_District_Analysis/blob/main/Resources/Scores_by_Spending_Original.png)


----------


* **Impact on Scores by School Size**
	* When looking at high level summaries of the data by School Size there is no impact from removing the Thomas High school 9th graders from summary.  Since we did not remove the 9th grade students from the population there is no impact to the calculation of the school size and there is not enough of a change in the avg scores or passing metrics to impact the results.   

New Scores by School Size
![](https://github.com/timbialek/PyCity_School_District_Analysis/blob/main/Resources/Scores_by_Size_New.png)

Original Scores by School Size
![](https://github.com/timbialek/PyCity_School_District_Analysis/blob/main/Resources/Scores_by_Size_Original.png)

---------


* **Impact on Scores by School Type**
	* There is no impact on the scores when summarized at this high of a level

New Scores by School Type 
![](https://github.com/timbialek/PyCity_School_District_Analysis/blob/main/Resources/Scores_by_Type_New.png)


Original Scores by School Type
![](https://github.com/timbialek/PyCity_School_District_Analysis/blob/main/Resources/Scores_by_Type_New.png)


---------

## Summary:
After changing the Thomas High School 9th graders scores to 'NaN' (not a number) in the student dataframe and recalculating the scores below are the notable changes can be seen when comparing the new and original scores for Thomas High School:

* The most significant change for the high school is the decrease in their Overall passing percentage from 90.95 to 90.63 which is a 0.35% decrease.  
* The second notable decrease was in the Reading passing percentage from 97.3 to 97.0 which is a 0.30% decrease in the score.  
* The math score and passing math percentage also went down but those changes are only seen when you go out the hundredth decimal point which implies that the change is not overly significant.  
* Lastly regarding Thomas High school their avg reading score did go up, which was the only number to increase, but even that was only by a small amount from 83.845 to 83.896 which is a 0.06% increase.  

None of the modifications made impacted the high-level summaries by District, School Spending, School Size or School Type.  Prior to formatting those summaries, you can see some changes in the data when looking at the one-hundredth decimal place but the differences are not noticeable.  With a 9th grade population of 461 students that is only 1.18% of the 39,170 total students in the analysis and there would have to have been some significant manipulation of the data to impact the high-level summaries.  In conclusion there does not appear to be enough information to definitively say if there was academic dishonesty with regards to the 9th grade reading and math scores at Thomas High School.
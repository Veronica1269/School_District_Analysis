# School District Analysis



# Overview

Thomas High School ninth-graders' reading and math grades appear to have been altered in the students_complete.csv file according to the school board. Even though the school board is unaware of the entire scope of the cheating, they are looking for assistance in upholding state testing requirements. 

In this project, Thomas High School's math and reading test scores would be replaced with NaN values while keeping the rest of the data intact. The school board wants to repeat the school district analysis conducted previously and receive a report about how these adjustments influenced the overall study once the reading and math scores have been replaced.




# Results


- How is the district summary affected?


As the district summary tables for initial analysis and the challenge analysis shown below, after changing to NaN the math and reading scores of all the 9th grade students at Thomas High School, there is not too much difference between the two summaries at district level. The Average Math Score changed by 0.1 points, while the Average Reading Score keeps the same in both cases. The total number of 9th Grade students at Thomas High School is 461, which represents 1.18% of the total students (39170). This percentage is too low to make a big difference on the results for the total school district.


## Initial Distrct Summary:

district_summary_initial](Resources/district_summary_initial.png)



### Challenge Distrct Summary:

district_summary_challenge](Resources/district_summary_challenge.png)




- How is the school summary affected?


Since only the math and reading scores of all the 9th grade students at Thomas High School are changed while the rest of the data is untouched, the results stayed the same for all the schools, except Thomas High School itself. The The school summary tables for Thomas High School in both analysis are shown below:


### Initial School Summary for Thomas High School:

school_summary_initial](Resources/school_summary_initial.png)



### Challenge School Summary for Thomas High School:

school_summary_challenge](Resources/school_summary_challenge.png)



The values for "Average Reading Score" and "Average Math Score" remained pretty much unchanged because the .mean() function in Pandas ignores the NaN values. However, the value for "% Passing Reading", "% Passing Math" and "% Overall Passing" for Thomas High School are decreased significantly. The reason is that the passing percentage is calculated using the number of students counted by the count() function. 

The functions for the passing percentage are:
  per_school_passing_math = per_school_passing_math / per_school_counts * 100
  per_school_passing_reading = per_school_passing_reading / per_school_counts * 100
  per_overall_passing_percentage = per_passing_math_reading / per_school_counts * 100




- How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?








How does replacing the ninth-grade scores affect the following:
Math and reading scores by grade
Scores by school spending
Scores by school size
Scores by school type

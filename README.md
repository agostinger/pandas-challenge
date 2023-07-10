# pandas-challenge
-Background:
Assist the school board and mayor to provide analysis for them to make strategic decisions regarding future school budgets and priorities. 
The analyst is based on district-wide standardized test, which includes the student's math and reading scores, as well as various information 
on the schools they attend. The analyst below is aggregating data to showcase trends in school performances based on school budget, school size 
and school type.

-Summary of analysis:

The first analysis performed was to summarize district-wide data including the total students, total school budget, average test scores in math
and reading, and percentages of students passing in math, reading and overall (based on a score of 70% or higher). District-wide there are a total 
of 39,170 students, total school budget of $ 24,649,428, average math score is 79, average reading score is 82, and percent of students passing 
math is 75 percent, reading is 85.8 percent and overall passing is 65 percent. 

The second analysis performed was to summarize the district-wide data by the individual schools. This was performed by using a "groupby" operation 
in Pandas code in order to calculate the total students, budget, average test scores in math and reading, and percentage passing by individual school 
name. Furthermore, this was used to calculate the schools budget spend per student. This summary allowed for more analysis as to which schools are 
performing well and compare to the individual school's budget amounts and total students.  

The groupby school name analysis allowed for showing the top performing schools, worst performing schools and calculated passing percentages by grade 
in each school to look for correlations. The bins operation was used on the summarized by school data in order to display a summary by school budget 
per student and a summary based on school size with the resulting students' passing percentage. The groupings for school budget per student were less 
than 585 dollars, 585 to 630 dollars, 630 to 645 dollars and 645 dollars to 680 dollars. The groupings for school size small (less than 1,000 students), 
medium (1,000 to 2,000 students) and large (greater than 2,000 students). Lastly, a summary was created to display passing student percentages based on 
school type being either a district or charter school. 

-Conclusion:

The data provided insight into school size and performance. Based on the analysis, the percentage of student's passing in larger size schools was lower
than in small or medium size schools, particularly in math. The overall passing rate in large schools was only 58.3 percent vs. 89.8 percent and 90.6 
percent in small and middle size schools respectively. This could suggest more personal attention is given to students in smaller schools, with smaller 
class sizes, that is increasing the test scores. 

In addition, there is a correlation between school type (district or charter) and passing rate of students. The overall passing rate for district schools 
is only 53.67 percent vs. 90.43 percent in charter schools. This could be due to a variety of social-economic factors, but it does suggest students test 
scores are much higher in charter schools than district schools.

Lastly, a few interesting observations were made. Based on the analysis performed, the per student budget spend had an inverse effect on the passing rates
of students. The lower spend per student showed a higher passing rate than the schools spending more per student. This is hard to draw a conclusion from 
as there are a variety of factors that could influence this. The other observation made was students in different grades at the same school had very
consistent grades. Thus, a student's grade level appeared to not be a factor in passing test scores.

Citations: Peer collaboration with Ryan Himes and Juliet Hamilton.
AskBCS learning assistant (MBush) assisted with code on school types below, which was used to group the school name and type.
    school_types = school_data.set_index(["school_name"])["type"].
ChatGPT utilized to code a conversion of an object to a float data type. This reversed the formatting of the field in order to perform calculations.
    school_spending_df["Per Student Budget"] = school_spending_df["Per Student Budget"].replace({'\$': '', ',': ''}, regex=True).astype(float).

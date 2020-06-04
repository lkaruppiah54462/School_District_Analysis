# School_District_Analysis
Given the task of Analyzing Math and Reading results by school, district and overall. 
Also analyze data after suppresing some of the scores related to some incidence
Relevant data - student data and school data

1)  Clean up the student data for prefixes and suffixes 
    ["Dr. ", "Mr. ","Ms. ", "Mrs. ", "Miss ", " MD", " DDS", " DVM", " PhD"]
    Challenge Overview
2)  Locate Thomas High School and replace all 9th grade math and reading scores with 
    numpy.nan
3)  Merge the cleaned student data with school data using school name as index
4)  Analyze the summary reports for district , school and compare it prior to supressing thescores.
5)  How is Thomas high School's performance affected by the suppressing of 9th grade scores?
6)  How is the school ranking changed by suppressing the score?
7)  How is replacing 9th grade score affect a)Math and reading score by Grade b)Scores by School spending
    c) Scores by School Size d) Scores by School Type

##Resources
1.  school_summary.csv, students_complete.csv
2.  Anaconda python 3.7.8, 
3.  created pthondata environment
4.  Jupyter notebook for python/pandas analysis

##Challenge Sumary
1.  District Summary
    a. Average Math Score fell by 0.1% from 79% to 78.9% and AverageReading score stayed the same at 81.9%
       - the mean calculation drops the rows with NaN, the divisor drops as well as the accumulated score, so the change is minimal
    b. % Passing for Math, Reading and overall fell by 1 % to 74%,85% and 64% respectively. Based on count which was reduced, 
       and the total student count remained the same, thus the rate dropped across the board.
2. School Summary
    a. Since this is by school, only Thomas High school metrics changed. Also only the average and passing rates changes as the 
       numbers for these calculations were changed by dropping the 9th grade scores. The remaining metrics did not change.
3. Thomas High School Summary
    a. Before dropping (461 students) the scores, Thomas High School was amongst the top school (2nd) in the ranking
       After dropping the score,Thomas High School was 8th in the ranking 
    b. Metrics only affected Thomas high Scool. Average Math and Reading scores dropped a little, but %passing Math, reading and overall changed
       from 93.3,97.3,90.5 to 66.9,69.7,65.1% respectively. These changes are due to how the averages and passing rates were calculted. 
       Averages does not include the dropped rows in the numerator or denominator. % passing rates only the numerator changed.
4. Impact of removing the 9th grade score of Thomas High School
   a. Math and Reading Score : Only Thomas High School 9th grade metric changed to NaN
   b. Scores by School Spending : Thomas High School Average spending is $638. So the spending range$630 to $644 metrics changed, the rest were not changed.
      Averages dropped a little, passing rates dropped by about ~6-7%
   c. Scores by School Size : Thomas High School total student count is 1635. So the bin (Medium : 1000 to 2000) metrics changed. No significant change in the avergage
      but the passing rate dropped ~6%.
   d. Scores by School Type : Thomas High School is of charter type. So the metrics for this category changed. Averages did not change significantly, but passing rate dropped by about 4%


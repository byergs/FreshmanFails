# Freshman Failure Prediction Model

### Excel | Python | Power BI 

### How can we quickly identify and predict which incoming freshmen will struggle academically? Can we use demographic, assessment, course placement, and grade data to predict freshmen who will need additional support?

For school leaders and teachers, it is crucial to identify incoming freshmen who will struggle academically and to do so early, quickly, and accurately. Research clearly shows that one's freshman year is critical in the overall high school experience. This project seeks to use historical data to develop a model that uses over 20 freshman characteristics to rank the likelihood that students will struggle in their first semester of high school. If a specific set of data points are strongly related to how past year's freshman have performed, it could be used to predict how this year's freshmen will do, with additional fine-tuning year after year to make the prediction more accurate.

 - Assessment and demographic data of the previous year's 8th graders was merged with their grades as freshmen the next year.
 - Numerical data points were checked for correlation to students' GPAs and the number of Ds and Fs in their first high school semester.
![image](https://github.com/byergs/byergs.github.io/blob/main/images/Heatmap.png)

### What numerical test data points are most strongly correlated with Freshman Ds and Fs?
There's no significance for our purposes the degree to which Fastbridge scores are correlated with IAR scores. There are a lot of relationships I could look at, but only a few that serve the purpose of predicting freshman failures. From the heatmap below, the Winter aMath and aReading scores show the strongest correlation to Ds and Fs, but clearly aren't a perfect picture of freshman failures. The prediction of freshman failures will require a combination of metrics with different weights.  
<img width="1062" height="623" alt="NumVars Corr with Grades" src="https://github.com/user-attachments/assets/a2758f56-377a-48ad-bc30-1ef5c1cb4ab7" />

### What categorical data points are most strongly correlated with Freshman Ds and Fs?
Categorical data was plotted in numerous ways to view relationships between GPA, Ds and Fs, and categorical data. The strongest related categories were the students' grades in their 8th grade math and science classes. Understanding business context is key in a case like this. Teachers at middle school levels grade students very differently than teachers at the high school level. Fs are quite rare in middle school classes - it is not at all uncommon for students that are behind in content knowledge will still be able to earn a D in middle school courses.

 ![image](https://github.com/byergs/byergs.github.io/blob/main/images/Code%20for%20Box%20Plots.png)
<img width="336" height="274" alt="Math Grade vs DF" src="https://github.com/user-attachments/assets/e2287ed5-e9df-40dd-ab92-fe47c92f4899" /> <img width="327" height="270" alt="Sci Grade vs DF" src="https://github.com/user-attachments/assets/02cc4227-821c-495a-becc-d246430b6f52" />

## Creating a "Risk Rating" based on all the variables and their correspondence to freshman Ds and Fs.
 - Criteria were given a set of weight values to create a risk rating. Once created, they were checked for correlation with Ds and Fs.
 ![image](https://github.com/byergs/byergs.github.io/blob/main/images/Risk%20Rating%20Tally.png)

 Here's the first attempt at correlating the Risk Rating to GPAs. An algorithm was created to find the best set of weights for the Risk Rating that created the strongest overall correlation.
 
 ![image](https://github.com/byergs/byergs.github.io/blob/main/images/Rating%20vs%20GPA.png)

An algorithm was created to find the best set of weights for the Risk Rating that created the strongest overall correlation. 
![image](https://github.com/byergs/byergs.github.io/blob/main/images/Code%20for%20Correlation%20Checker.png)

After running through millions of combinations of risk rating weights, the best correlation value was 0.6934. The scatterplot below shows that with the rating weights, all but one student with 0 Ds and Fs had a risk rating below 20 while all students with 3 or more Ds and Fs had a risk rating above 10. The visual appearance of the plot says so much - on the one hand, there is clearly a relationship, but on the other, it is nowhere close to airtight. Some students ended up with 4 Ds and Fs, and the rating system only gave them a rating of about 13-15. Meanwhile, there were a few students who got a higher risk rating and ended up with no Ds or Fs. 
<img width="501" height="315" alt="Rating vs DFs" src="https://github.com/user-attachments/assets/b3973733-4781-4e78-bbe4-37ed2cbdfe0e" />



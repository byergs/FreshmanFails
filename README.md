# Freshman Failure Prediction Model

### Excel | Python | Power BI 

### How can we quickly identify and predict which incoming freshmen will struggle academically? Can we use demographic, assessment, course placement, and grade data to predict freshmen who will need additional support?

For school leaders and teachers, it is crucial to identify incoming freshmen who will struggle academically and to do so early, quickly, and accurately. Research clearly shows that one's freshman year is critical in the overall high school experience. This project seeks to use historical data to develop a model that uses over 20 freshman characteristics to rank the likelihood that students will struggle in their first semester of high school. If a specific set of data points are strongly related to how past year's freshman have performed, it could be used to predict how this year's freshmen will do, with additional fine-tuning year after year to make the prediction more accurate.

 - Assessment and demographic data of the previous year's 8th graders was merged with their grades as freshmen the next year.
 - Numerical data points were checked for correlation to students' GPAs and the number of Ds and Fs in their first high school semester.
![image](https://github.com/byergs/byergs.github.io/blob/main/images/Heatmap.png)

### What numerical test data points are most strongly correlated with Freshman Ds and Fs?
There's no significance for our purposes the degree to which Fastbridge scores are correlated with IAR scores. There are a lot of relationships I could look at, but only a few that serve the purpose of predicting freshman failures. 

 - Categorical data was plotted in numerous ways to view relationships between GPA, Ds and Fs, and categorical data.
 ![image](https://github.com/byergs/byergs.github.io/blob/main/images/Code%20for%20Box%20Plots.png)
 ![image](https://github.com/byergs/byergs.github.io/blob/main/images/Box%20Plots.png)

 - Criteria were given a set of weight values to create a risk rating, which was checked for correlation with GPA and Ds and Fs.
 ![image](https://github.com/byergs/byergs.github.io/blob/main/images/Risk%20Rating%20Tally.png)

 Here's the first attempt at correlating the Risk Rating to GPAs.
 
 ![image](https://github.com/byergs/byergs.github.io/blob/main/images/Rating%20vs%20GPA.png)

More details will be added soon, as I am still in the middle of this project. Here's a little preview of where it's headed:
![image](https://github.com/byergs/byergs.github.io/blob/main/images/Code%20for%20Correlation%20Checker.png)

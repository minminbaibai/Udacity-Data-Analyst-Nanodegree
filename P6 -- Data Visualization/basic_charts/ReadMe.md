# P5--Data Visualization: Prospor Loan Data Visualization
by Min Lu

### Summary

Prosper is a P2P marketplace providing person-to-person lending utilizing alisting and bidding process to get competitive rates for loans. The dataset has 88 variables and 84854 oberservations.And the loans cover the period from 2009 to 2014. The dataset contains classes int,numeric,data and factor. We will explore the relationship between different main Variables. This project contains a bar chart with three most variables LoanRating vs. LoanAmount vs. Loan Term vs. Different Years. We can choose different years to get more detail information for each year and see how these numbers changed from time to time.

## Design

#### Exploratory Data Analysis and Cleaning (R)

I downloaded the data from [ProsperLoanData](https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv). I first use tableau to do data anlysis and cleaning. There are some NA data in Loanrating sections. Then I tried to find most important varaiables in the dataset and figure on the relationship between them. There are 88 different varaiables. While exploring the data. I believed that loan ratings, interest rates, and loan term will be most important factors to estimate Prosper Company business model. So I finally chose loan ratings, loan amount. loan term and years to do data visualization. 

#### Data Visualization (dimple.js)

I decided to use **d3.js** and **dimple.js** together to complete my data visualization.

I considered using mutiple chart types, like scatter chart, line chart, bubble chart, bar chart,etc. I also thought about color to separately each variables to test how to arange to show the best numbers and visualization on one chart. I first chose bubble chart. I selected loan ratings, loan amount, number of investors and loan term to make my first chart. Here's a link for my first chart [Index1](https://github.com/minminbaibai/Udacity-Data-Analyst-Nanodegree/blob/master/P6%20--%20Data%20Visualization/basic_charts/index1.html). After I viewed my chart few times, I think I can make a better one. And I am interested to add Years to this chart. Next day, I invited three friends to my home and showed them my chart. I asked for some feedback.

### Feedback

Here are three feedbacks:

#### Interview #1

> Your chart was nice, but too simple. If there are more explanation about these variables, it will looks better. You used size of bubble to show number of investors in different loan rating, but it's not easy to tell the diffence of the size since there are too many simiplar bubble.

#### Interview #2

> The chart is interactive, that's nice. But why some bubble are extrmely small on the bottom of chart. I suggest you change variable arrangements or chart type which can better show the relationship and figures in these varaiables. How about try bar chart?

#### Interview #3

> I agreed that chart is a little bit too simple. How about add another variable like Years and do an animation? I will also consider change the chart type since some 12 months term bubbles are too small on the bottom of chart.

### Post-feedback Design

Following the feedback from the 3 interviews, I implemented the following changes:

- I deleted number of investors variable and add Years variable
- I added animation with Years.
- I changed chart type from bubble chart to bar chart.
- I added legend to better explained my chart.

My final Edition of Data Visualization [Index_final](https://github.com/minminbaibai/Udacity-Data-Analyst-Nanodegree/blob/master/P6%20--%20Data%20Visualization/basic_charts/index_final.html)

### Outcome
From this chart, we could see that loans with rating A, B, C always has a higher demand, almost doubled other ratings. And loans with terms 36 months and 60 months are more popular than loans with 12 months.

### Resources

- [dimple.js Documentation](http://dimplejs.org/)
- [Data Visualization and D3.js (Udacity)](https://www.udacity.com/course/viewer#!/c-ud507-nd)


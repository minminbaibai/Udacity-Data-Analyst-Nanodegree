## Data Visualization: Prospor Loan Data Visualization
by Min Lu

### Summary

Prosper is a P2P marketplace providing person-to-person lending utilizing alisting and bidding process to get competitive rates for loans. The dataset has 88 variables and 84854 oberservations.And the loans cover the period from 2009 to 2014. The dataset contains classes int,numeric,data and factor. We will explore the relationship between different main Variables. This project contains a bar chart with three most variables LoanRating vs. LoanAmount vs. Loan Term vs. Different Years. We can choose different years to get more detail information for each year and see how these numbers changed from time to time.

### Design

#### Exploratory Data Analysis and Cleaning (R)

I downloaded the data from [ProsperLoanData](https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv). I first use tableau to do data anlysis and cleaning. There are some NA data in Loanrating sections. Then I tried to find most important varaiables in the dataset and figure on the relationship between them. There are 88 different varaiables. While exploring the data. I believed that loan ratings, interest rates, and loan term will be most important factors to estimate Prosper Company business model. So I finally chose loan ratings, loan amount. loan term and years to do data visualization. 

#### Data Visualization (dimple.js)

I decided to use **d3.js** and **dimple.js** together to complete my data visualization.

I considered using mutiple chart types, like scatter chart, line chart, bubble chart, bar chart,etc. I also thought about color to separately each variables to test how to arange to show the best numbers and visualization on one chart. I first chose bubble chart. I selected loan ratings, loan amount, number of investors and loan term to make my first chart. Here's a link for my first chart[Index1](https://github.com/minminbaibai/Udacity-Data-Analyst-Nanodegree/blob/master/P6%20--%20Data%20Visualization/basic_charts/index1.html)

### Feedback

I gathered feedback from 3 different people people and tried to follow Udacity questions guideline and here is the abridged responses. 

#### Interview #1

> Your chart was a bit messy & no clear headlines & legend. If there is some explanation like a bold headline then these charts would make sense. The insights is not so much of a surprise and if you just create a small tweak in the legend, x-axis & y-axis then this would looks good. The data clearly favors your initial hypothesis, women children & elders are prioritized to board the baot first. 

#### Interview #2

> The chart is interactive, that's nice. But why the second chart is revert and not in-line with the other chart. Switch x-axis & y-axis with each other and I think the chart will looks much better. By the way, the first chart to split between classes is cool but I think you can make it even better by combining gender & classes to see if there's different behavior in different classes. Broadly speaking, the chart looks intuitive & only needs a few small tweak. 

#### Interview #3

> The second chart looks a bit weird and too much junk information, there's no need to include different age in different age bracket like that. There's not much information to show. And for the first chart, split the column into two, a stacked-bar wouldn't be necessary. Also, you also needs to clean up the headline & make clear of the axis, what is PClass? Can you makes it a bit clearer. Overall, this chart is straightforward.

### Post-feedback Design

Following the feedback from the 3 interviews, I implemented the following changes:

- I separate man & women from the first chart.
- I added careful chart title & clearly labeled axis title.
- I flipped the chart from horizontal bar chart to vertical bart chart.
- I remove the individual age & only shows aggergrate age group.
- I intended to add few special effect (highlight a chart when mouseover) but this would not be necessary.
- I switched from Number of Survival to Survival Rates since the amount of passengers in each class/ages group is not similar.

Final rendition of the data visualization is shown below:

![Final Chart](https://raw.githubusercontent.com/tommyly2010/Udacity-Data-Analyst-Nanodegree/master/p6 - Data Visualization/img/image-final.png)

### Resources

- [dimple.js Documentation](http://dimplejs.org/)
- [Data Visualization and D3.js (Udacity)](https://www.udacity.com/course/viewer#!/c-ud507-nd)
- [mbostock's blocks](http://bl.ocks.org/mbostock)
- [Dimple homepage](http://dimplejs.org/examples_viewer.html?id=bars_vertical_grouped)

### Data

- `train.csv`: original downloaded dataset with minor cleaning for dimple.js implementation.

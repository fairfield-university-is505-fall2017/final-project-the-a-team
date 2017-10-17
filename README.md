# The A-Team's Demographic Data Analysis
by Trang Vu, Vincent Rella, and Anthony Iorio

## Background
Using census-derived data, the purpose of our analysis is to analyze demographic and gender characteristics, and relate it to income and education levels to see current trends in our population. Additionally, we aimed to show immigrant settlement trends by cross-referencing the data with DHS statistics on the preferred areas where newcomers chose to settle down in the United States.

### What is ['adult.csv'](https://www.kaggle.com/uciml/adult-census-income)?
We're glad you asked! This is a comma-seperated value file containing the records of more than 32,500 individuals, all surveyed inside the United States taken from 1994 US Census data. When considering the data, keep in mind the following:

* The individuals surveyed currently reside in the 50 States, 18 Territories, or 1 District of the United States of America.
* The types of data collected were as follows, and constitute the `columns` of the data (note that only bolded entries were used in our analysis):
  * **Age (`age`)**
  * **Type of Employment (`workclass`)**<sup>1</sup>
  * Final Sampling Weight (`fnlwgt`)<sup>2</sup>
  * **Education (`education`)**
  * Education Number (`education.num`)<sup>3</sup>
  * **Marital Status (`marital.status`)**
  * **Occupation (`occupation`)**
  * **Relationship (`relationship`)**<sup>4</sup>
  * **Race (`race`)**
  * **Sex (`sex`)**
  * **Capital Gain (`capital.gain`)**<sup>5</sup>
  * **Capital Loss (`capital.loss`)**<sup>6</sup>
  * **Working Hours per Week (`hours.per.week`)**
  * **Native Country (`native.country`)**
  * **Income (`income`)**
  

<sup>1</sup> This refers to the class of employment that an individual's work activites are linked to; for example, "private sector", or "government (local)".

<sup>2</sup> This is a continuous attribute . For more information, see a similar study that also endeavored to explain the variable definitions either [here](http://mhahsler.github.io/arules/reference/Adult.html), or [here](http://webcache.googleusercontent.com/search?q=cache:XDAnLT7ItZIJ:mhahsler.github.io/arules/reference/Adult.html+&cd=1&hl=en&ct=clnk&gl=us) (as the last link appears to have been taken down).

<sup>3</sup> This is a numeric representation of the attribute `education`, determined based on the Census Bureau's conversion formula for academic levels. Since this relates to a formula that is not clearly defined and/or encompasses other datasets, we did not choose to utilize this varable.

<sup>4</sup> This is a descriptor that is highly related to the attribute `marital.status`, but expresses the status in the context of the individual being surveyed (for example, "husband" or "unmarried").

<sup>5</sup> A numeric vector used to chart possible positive variations (gains) in capital.

<sup>6</sup> A numeric vector used to chart possible negative variations (losses) in capital.

### How was the heatmap showing where new immigrants are settling created?
* The US Department of Homeland Security, which curated the collection *2015 Yearbook of Immigration Statistics*, is responsible for the data used to create that heatmap. The data can be found [here](https://www.dhs.gov/immigration-statistics/yearbook/2015/table4).

## Analysis
Having the data is one thing, but utilizing it to extract useful, informative trends is another. We performed an analysis centering on the following questions outlined below, with a brief description of what we found below them. For the full details, we encourage you to view the full report!

### Questions
We set out to perform the following operations with the data:
* V1. What is the distribution of income among various relationship types?
  * This was completed, and is reflected in the report. For the marital status category, married-civ-spouse (married, with civilian spouse) earns more than other statuses. 44.7% of married civ-spouse earn more than 50k per year.
* V2. We would like to know general information about the demographic composition and  age
  * This allowed us to see the demographic composition of the dataset at a glance. We found that the majority of the demograpic in this sample was described as White, at 85.54%. The next largest value was African American with 9.59%, Asian/Pacific Islander with 3.19%, then American-Indian .956%. The Other category consists of .83%.
  * The distribution of age was skewed to the right.
* T3. What is the relationship between the variables in this dataset? What is the correlation, if any?
  * Based on the heatmap and the correlation coefficient, there is no correlation between quantitative variables in the dataset. See the report for more information.
* T4. What is the relationship between the level of education and level of income, if any?
  * There is a connection between income and education level. Generally speaking, more education means more income. With few exceptions, people who got PhD or Masters' degrees earn more than 50k per year. 
* A5. Which gender earns higher income? 
  * Looking at the chart, we see an obvious trend that males earn higher incomes than females among the individuals surveyed in this dataset. To better understand why, view the full report.
* A6. Which occupation work more hours per week? If they work more, would they earn more income?
  * On average, people who are farm fishing work the most, 50 hours per week, but their income is low compared to other occupation. Exec-managerial and prof-specialty earn the most.
* Advanced Question: Which states in the United States have the largest immigrant groups?
  * This was completed, and we highly recommend you actually view the heatmap by viewing the report!
* Really Advanced Question: Which country has the largest immigrant groups that now reside within the United States?
  * This was completed, and we highly recommend you actually view the heatmap by viewing the report!* 

## Takeaways
There were a few key takeaways that really stuck out at us toward the end of this project, particularly with regard to the myriad of errors that we were forced to surmount in order to complete it! Here's our top 5 takeaways, as a group.
* **Error diagnosis is paramount.** Ideally, each group member should be equally skilled in diagnosing the errors that their code will invariably yield before it finally works. However, ff there is one group member who feels patrticularly comfortable being the diagnostician, use their expertise to better understand your own errors. It helps everyone get on!
* **Use unified references.** We created three workspaces, `workspace_trang`, `workspace_vin`, and `workspace_anthony` to write some code in our own silos, and planned to fuse that later on - which is what we did. However, we quickly realized that seperate development efforts meant our code had very little in common to reference, so we were stuck constantly redefining dataframes or performing redundant operations that one of us had already completed. That's why we took a break from coding, made sure our efforts aligned and used similar references, and then continued on our way. It would have been a headache if we didn't!
* **Google really is your friend.** There really is no error message so unique that literally nobody else has encountered it - we were heartened by the legions of other budding programmers who also ran into similar problems (or in many cases, the exact same ones) as us, as it helped us find a solution to our problems. Of course, Google also directed us to invaluable developer resources such as verbose documentation, which helped us understand neato modules like Matplotlib and Seaborn. (We're big fans.) Stackoverflow really is a blessing!
* **Lazy isn't necessarily a bad thing.** Yes, programmers are lazy, but in a good way - why reinvent the wheel if you've invented it already? Repurposing existing code (when done right, of course) frees up development resources, which enables you to find ways to make that code even better, or pursue the development of even more advanced functions that enhance the project more than stressing out about basic stuff ever could. This class has been a learning experience for us all, and building on the code we already created helped us maximize our learning even more!
* **Don't be afraid to ask a teammate for help.** There is no way we could have done this without asking each other for help. It can be quite intimidating asking for a hand, lest someone else think you're slow or lazy. But if you've really tried your best to solve a problem and you're not getting anywhere, blanking searing your retinas staring into the screen won't help anything! Ask for help, but most importantly, make sure you understand **how** that person was able to help resolve your issue. That way, you'll be better equipped to resolve the issue on your own, next time!

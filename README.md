# The A-Team's Demographic Data Analysis
by Trang Vu, Vincent Rella, and Anthony Iorio

## Background
We endeavor to analyze this data, and expand on this statement later. The purpose of our analysis is to analyze demographic and gender characteristics, and relate it to income and education levels to see current trends in our population.

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
  * Capital Gain (`capital.gain`)<sup>5</sup>
  * Capital Loss (`capital.loss`)<sup>6</sup>
  * **Working Hours per Week (`hours.per.week`)**
  * **Native Country (`native.country`)**
  * **Income (`income`)**
  

<sup>1</sup> This refers to the class of employment that an individual's work activites are linked to; for example, "private sector", or "government (local)".

<sup>2</sup> This is a continuous attribute . For more information, see a similar study that also endeavored to explain the variable definitions either [here](http://mhahsler.github.io/arules/reference/Adult.html), or [here](http://webcache.googleusercontent.com/search?q=cache:XDAnLT7ItZIJ:mhahsler.github.io/arules/reference/Adult.html+&cd=1&hl=en&ct=clnk&gl=us) (as the last link appears to have been taken down).

<sup>3</sup> This is a numeric representation of the attribute `education`, determined based on the Census Bureau's conversion formula for academic levels.

<sup>4</sup> This is a descriptor that is highly related to the attribute `marital.status`, but expresses the status in the context of the individual being surveyed (for example, "husband" or "unmarried").

<sup>5</sup> A numeric vector used to chart possible positive variations (gains) in capital. Since this relates to a timespan that is not clearly defined and/or encompasses other datasets, we did not choose to utilize this varable.

<sup>6</sup> A numeric vector used to chart possible negative variations (losses) in capital. Since this relates to a timespan that is not clearly defined and/or encompasses other datasets, we did not choose to utilize this varable.

### How was the heatmap showing where new immigrants are settling created?
* The US Department of Homeland Security, which curated the collection *2015 Yearbook of Immigration Statistics*, is responsible for the data used to create that heatmap. The data can be found [here](https://www.dhs.gov/immigration-statistics/yearbook/2015/table4).

## Analysis
### Questions
We set out to perform the following operations with the data:
* V1. Create a pie chart that reveals the distribution of income among various races.
* V2. Create a pie chart of demographic composition.
* T3. What is the relationship between the variables in this dataset? What is the correlation, if any?
* T4. What is the relationship between the level of education and level of income, if any?
* A5. Create a bar chart that shows the distribution of income among females and males.
* A6. Create a histogram that shows the distribution of age among respondents.
* Advanced Question: Create a heatmap of the United States displaying the largest immigrant groups by state and territory.
* Advanced Advanced Question: Create a heatmap of the world displaying the largest immigrant groups by country that now reside within the United States.

## The Takeaways
* Lesson Learned: here are the skill sets we created
* error finding
* Google is good
* stackoverflow
* seaborn
* repurposing existing code

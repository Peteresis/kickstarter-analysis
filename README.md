# Kickstarting with Excel

## Overview of Project

The objective of the project is to analyze different Kickstarter campaigns using their launch dates and their funding goals. The analysis focuses only on the "Theater" parent category and the "Plays" subcategory.

### Purpose

The purpose is to discover trends that allow to identify when is the best time of the year to launch a Kickstarter campaign and what is the range of financial goal that will have the probability of being more successful in getting the funds to produce a theathrical play.

## Analysis and Challenges

The analysis focuses on two variables: 

1- The time of the year on which similar campaigns have been launched.
2- The amount of money that such campaigns have asked from the public.

Several elements of the data used constituted a challenge.  First we have the large amount of data contained in the Excel sheet to be analyzed.  The total was 4115 Excel rows, belonging to different categories in different countries.  Secondly, the launch and completion dates of the various projects on Kickstarter are in a Unix date format, which needed to be converted to a date format in which the analysis could be done in Excel.  Finally, it was necessary to separate the Category and Subcategory into 2 parts in order to obtain the Parent Category and Subcategory.

Excel proved to be a very powerful tool to work with the data.  The software has many pre-programmed formulas that allow to analyze the data with minimal effort.  Its sorting and filtering capabilities are also very useful for the kind of work being done, as well as the charting capacity of the software.

### Analysis of Outcomes Based on Launch Date

Based on the data extracted from Kickstarter, the table contained in the Tab "Theather Outcomes by Launch Date" was elaborated.  It is a specific table for the Theather category.  From this table the graph of Successful, Failed and Canceled campaigns was generated.  This graph shows that, in general, there are more Successful campaigns than Failed or Canceled campaigns and that April to September is the best time of the year to launch a successful campaign.  On average, 61% of campaigns are successful, 36% of campaigns fail and 3% of campaigns are cancelled.

There is no clear trend indicating the months of the year when there is a greater chance of campaign failure.  The curve of failed campaigns has little fluctuation throughout the year and shows little seasonality.

With respect to cancelled campaigns, the number is insignificant and the curve is fairly flat throughout the year, so there is no particular time of year when more campaigns are cancelled.

### Analysis of Outcomes Based on Goals

With the data obtained from Kicstarter, the table included in the Tab "Outcomes Based on Goals" was elaborated.  This table shows the number of Successful, Failed and Canceled campaigns for the subcategory "Plays".  The table is divided into 12 ranges with the goals of money to be raised from the public.  The first rank is for goals under $1,000 and the following categories increase in steps of $5,000 until reaching the top category, which includes projects over $50,000.

The graph shows that the "plays" projects under $5,000 are the most successful (between 73% and 76% success) and then the curve begins to decline until it reaches 20% of successful projects, although there is an increase in the range between $35,000 and $45,000 where the success rate rises sharply to 67% and then falls back to 0%. Does this mean that it is better to launch only campaigns between $35,000 and $45,000?  The answer is, no.  Although the success rate in the indicated range is quite high, the number of campaigns is very small, just 6 campaigns in this range out of a total of 694 successful campaigns.

Based on the data analyzed, the range that offers the highest probability of success is "Less than $1,000" with 76%; however, in the "$1000 to $4999" range the success rate is only 3% lower, but the number of successful campaigns is more than twice as high as in the previous range.  On the other hand, little can be done in a "Play" with a budget of less than $1,000, so it is better to launch campaigns for "plays" with a budget between $1,000 and $4,999.


### Challenges and Difficulties Encountered

Analyzing Kickstarter campaign data has several aspects that may be of difficulty for those uninitiated in the use of Excel.  I list them below:

1- You have to be familiar with the use of Excel formulas, the use of cell references in relative and/or absolute form, as well as working with cells contained in different "Sheets" of an Excel workbook.
2- The data needs to be prepared before starting the analysis so that it can be used with greater facility when creating a Pivot Table.  In this case it was necessary to add two new columns to the data: "Years" and "Month" and that required the use of formulas with the functions "YEAR()" and "MONTH()".
3- The Pivot Table contained in the Sheet "Theather Outcomes by Launch Date" had some complexity since it was necessary to add two filters to the table and to group the campaigns by months so that the graph could be easier to analyze.
4- The table contained in the Tab "Outcomes Based on Goals" requires knowing how to use the function "COUNTIFS()".  In the study at hand, the function "COUNTIFS()" needs the ranges between which we are going to make the calculations.  Since the goal column contains these ranges expressed as a text string, there was the possibility to enter the ranges manually in each of the "COUNTIFS()" formulas, or to make a formula that extracts the limits of the ranges from the text string.  This second possibility was the one I chose since it seems to me that it is less error prone than entering the information manually in each formula.  However, I must admit that to do these nested functions correctly requires good practice with Excel.  In a limited set of ranges as in the analyzed case, the manual option can work well, but if the number of ranges would be 50 or 100 levels, definitely the use of nested functions is a more convenient way to work.  As an additional remark, I think that the table should have been built with two columns for the range (column for minimum value of the range and column for the maximum value of the range) instead of a single column and thus the use of the "COUNTIFS()" function would have been simpler, however the instructions received indicated the creation of the first column with text strings.
5- Finally I must say that in this type of analysis it is necessary to be very careful with the use of the filters as much in the base data, as in the Pivot Tables as well as within the formulas ("COUNTIFS()" and others) since a badly placed filter makes that the Pivot Table, the Table of Results or the charts come out totally altered with respect to the results that should have been obtained.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

1- It is better to launch a campaign between the months of April and September.
2- The number of successful campaigns is bigger than the number of failed campaign by a ratio of a little under 2:1.

- What can you conclude about the Outcomes based on Goals?

1- The "plays" projects under $5,000 are the most successful (between 73% and 76% success).
2- There is an increase in the success rate in the range between $35,000 and $45,000 where the success rate rises sharply to 67% but it has very few campaigns in it.
3- The sweetspot to launch campaigns is the range "$1000 to $4999".  In this range the number of successful campaigns is more than twice as high as in the previous range.

- What are some limitations of this dataset?

I believe that the main limitation is the fact that there are categories with very few "plays" but with a high sucess rate and that skews the data when you only look at the outcome based on financial goals.  If you look at the chart alone, you cold be deceived into thinking that it is a good idea to launch a campaign between $35,000 and $45,000, when in reality there are very few campaigns in this range.

Another limitation is that the parent category "Theater" only has 3 subcategories: musicals, plays and theathers.  Perhaps it would be more useful if it had more subcategories so that it could give more information about the type of "plays" that have more probability of success.  Also, the subcategory "spaces" needs to be discarded as it refers to the construction of repairs of theater halls and so it can skew the data if such subcategory is not discarded.

- What are some other possible tables and/or graphs that we could create?

I would include a chart that tracks successful "plays" by year to see whether there is a rising or decreasing trend and to see if the public's interest in plays is waning with time.

Another useful graphic would be to compare success rates across countries to see if there is a hotspot for theather plays.

It would also be interesting to compare the categories "Theather" with "Film & Video" Perhaps the public invests far more money in one category than the other, and both involve acting, one in front of the public and the other in front of a camera.

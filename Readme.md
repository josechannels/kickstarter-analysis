# Kickstarting with Excel

## Overview of Project

### Purpose

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
To analyze the relation between the outcome of a theater campaign and the date the campaign was launched I created a pivot table from the master data filtered to contain only data from theater campaigns for all years in the database.  The sum of the different outcomes were shown per month in rows.

![](resources/Table-theater-outcomes.PNG)

From this pivot table I produced a linechart with the sum of each of the possible outcomes on the y-axis and the month the campaign was launched on the x-axis:

![](resources/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals
To analyze the relation between the initial goal set and the outcome for a play I created a table with I broke the down the goal into 12 different levels (rows) and then in 3 additional columns counted the total number of plays that were successful, that failed and that were cancelled per goal range.  To accomplish this, I used a COUNTIFS statement with 3 or 4 different conditions that needed to be met: 

1. campaign was a "play" 
2. the goal was larger or equal to the lowest value in the goal range, 
3. the goal was smaller or equal to the highest value in the goal range,
4. the campaign outcome was defined

an example of a such statement: ```=COUNTIFS(Data!R:R,"plays",Data!$D:$D,">=25000",Data!$D:$D,"<=29999",Data!$F:$F,"Canceled")```

Here is what the table looked like:

Using this table I constructed a line graph whre on the y-axis i plotted the percent of the campaigns that were successfull, failed and were cancelled and on the x-axis i ploted the campaign goal ranges:

![](resources/Outcomes_vs_Goals.png)


### Challenges and Difficulties Encountered
One challenge that i encountered was that i could not figure out how to hide the Pivot Chart filters so as to obtain a clean image with only the data.
A google search took me to this [page](https://excellenttips.wordpress.com/2014/07/14/hide-pivot-chart-filters/) where i was shown how to do this.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
A first conclusion is that the largest number of successfull theater campaings were launched in May (111 successfull campaigns).  This number is three times higher than the number of successful campaigns launched in the month of December (lowest number of successfull campaings in a month).
A second conclusion is that the number of campaigns that were cancelled per month was small compared to the number of campaigns that suceeded or failed: With the exception of the month of January when 7 campaigns were cancelled, in the rest of the months of the year, the number of canceled campaigns ranged between 2 and 4.

- What can you conclude about the Outcomes based on Goals?

- What are some limitations of this dataset?

- What are some other possible tables and/or graphs that we could create?

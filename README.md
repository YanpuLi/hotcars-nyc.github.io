
Final Project: Hot Subway Cars in NYC
===

Team Member and Related Link
---

Azharuddin Priyotomo (apriyotomo)

Huan Ye (Leaf27)

Yanpu Li (yanpuli)





[demo link](http://hotcars-nyc.github.io/)<br>
[ video link ](https://www.youtube.com/watch?v=UrOkAUUkJqs#action=share)


Composition of Files
---
Process Book: CS573processbook.pdf

Data: folder "data" and "dataset"

CSS: folder "CSS"

Code: index.html,  coffee-wheel.html,  folder "js"

Background and Motivation
---

New York City (NYC) is the most populous city in the US and has been described as the cultural and financial capital of the world. As a metropolitan city, the public transportation plays a very important role for the convenience of the city's dwellers and visitors. The subway is considered as the favorite public transportation. However, during summer time where most people would visit the city, there has been a major issue occurred frequently over years, which is the hot cars problem.



The hot car problem is caused by the air-conditioning breakdowns in the subway cars which happened about 10 times a day during June, July and August between 2010 and 2014, according to analysis of Metropolitan Transportation Authority data obtained by The New York World through open records request. In total, there were nearly 6,500 “hot cars” over the five-year period covered by the data. Unsurprisingly, the vast majority of those incidents occurred during the hottest months of the year. This problem brings a very bad experience for the users, as they described that it was a horrendous to be stuck on an underground hot train.



The MTA has a complete data of the problem details such as the incident time, the repair time, the subway route and the car model, but there is no any complete guidance information yet to the users about this problem. So in this project, we are trying to provide a comprehensive visualization for the subway users so that they can avoid hot subway cars problem.

Project Objectives
---

We want to reduce occurrence of riders taking hot subway cars in New York City. In order to achieve that, we need to know what type of cars whose air condition breakdowns frequently and what factors will increase the repair frequency. After figuring out all of these, we can recommend passengers to take subway cars with least air condition breakdown possibilities. 

Data and Data Processing
---

Our dataset is about “Hot Cars” happening frequency in summer season in New York. We derived it from “data.βetaNYC” (http://data.beta.nyc)


As for our dataset, we care about two parts. One is which factor would be the most influential one that can increase the frequency of “hot cars”, the other is the distribution of these “hot cars”.
So the relating attributes would be car types, repair status, problem being addressed, in-use time, year, month, manufacturer, service line. The first step is about doing aggregation by the cars’ working month and year. As there are so many related attributes, we will only evaluate one at each time. For the tools, we will use python and excel.

Visualization Design
---

Shared by three prototypes:We add a calendar view to show repair frequency of each car type per month during 2010-14 period. And we use hue to differ frequency.  Also, we want to encode  repair frequency of different car types to a stacked bar chart, that means height of each bar is total number of repairs for each car type  and heights of portions in a bar representing number of repairs in one year. When users click on a cube in calendar view, the corresponding bar in stacked bar chart will be highlighted, as well as the associated arc in pie chart. We also draw a pie chart to show the percentages of hot car of different type. What’s more, we use a NYC subway map to show in each line what type of cars are easily being a hot car. 


Additional features for First prototype: when users want to check a certain line, click on the line in NYC subway map and a new pie chart will appear. This pie chart represents percentages of hot cars of types which are running in the given line. 


Additional features for Second prototype: users can click on a certain stop, zoom in it and a new pie chart will appear. Each arc in the pie chart represents number of hot cars of types which will stop in this station.


Additional features for third prototype: we will add a pie chart to show percentage of hot cars for different manufacturer. Also, we use a slope chart to encode car types as y axis and encode in-service year as the x axis. 

Must-have Features
---

For analysis aspect:


The attributes we must keep is shown below:


1.woid - Work order ID making each repair job unique.


2.repair - The nature of the repair. Most common are REPLACED (54,927), REPAIRED    (7,508), HDWE REPLACED (1,826), CLEANED (1,611), and RESET (1,560). Possibilities are ADDED, ADJUSTED, CHANGED FLUID, CHARGED, CLEAN & LUB, CLEANED, COMPLETED, HDWE INSTALLED, HDWE REPAIRED, HDWE REPLACED, HDWE TIGHTENED, HDWE TORQUED, INSTALLED, MONITOR, REINSTALLED, REMOVED, REPAIRED, REPLACED, REPLACED FUSE, REPROGRAMMED, RESET, SHOPPED, TIGHTENED, UPGRADED, VERIFIED, WASHED.


3.year - The year of the work order.


4.month - The month of the work order.


5.car type - The type of car. Possibilities are R142, R142A, R143, R160, R188, R32, R42, R46, R62, R62A, R68, and R68A.


6.car - The unique number of the car in which the work is taking place.


7.service - The lines that car type serves.


9.inservice - The years in which the car type was brought into service, for calculating the in-use time for each car.


For the visualization design aspect:


We will use stacked bar chart and pie chart to show the relationship between each factor (e.g. inservice time) and frequency of being a “hot car”. These two charts are used for finding the most influential factors of a car.
As for frequency distribution in summer (June, July, August), we will use a calendar view to display. This chart will be shown in multi-dimensions (e.g. car type, year, month).  
At last, a subway map is needed to show “hot car” distribution in service lines.


Optional Features
---

For analysis aspect:


We haven’t take these two attributes as must-have because these two might not be highly related to the frequency of “hot cars”. So after finishing must-have attributes analysis, we will go deep into these two.


1.component - The machinery being worked on.


2.manufacturer - The company that manufactured the car type. 


Project Schedule
---


![schedule](img/schedule.jpg)


Sketch
---

![Stacked Bar Chart](img/stackedBar.jpg)

![Calendar View](img/calendar.jpg)

![NYC Subway Map](img/map.jpg)

![Slope Chart](img/slope.jpg)

![Interaction 1](img/dashboard.png)

![Interaction 2](img/dashboard2.jpg)


References
---

Dataset: From NYC.beta (http://data.beta.nyc/dataset/subway-hot-cars-dataset/resource/bd1efb1b-326e-43fc-93f0-4f2e601c117b)


Web Design: This website design is using Agency theme. Agency is a free bootstrap theme created by Start Bootstrap(http://startbootstrap.com/).

Zoomable sunburst diagram: derived from Coffee Wheel by Jason Davies(https://github.com/amaunz/d3)


Parallel Set derived from Jason Davies repository(https://github.com/jasondavies/d3-parsets)


Parallel Coordinate derived from syntagmatic repository(https://syntagmatic.github.io/parallel-coordinates/)

Line Chart derived from C3 library(http://c3js.org/samples/simple_multiple.html)

NYC subway map derived from website(https://docs.google.com/spreadsheets/d/1idKvafTPqrr9dFDRy_KS5rvWors1ZirLUCassGLLP2c/pub?output=html)



# Call Centre Dashboard

## Problem Statement

This dashboard helps to understand the calls received by the call centres for the October 2020. The dataset consists of 32941 rows and 12 columns with names Id,CallTimestamp,Call-Centres City , Channel,City,Customer Name, Reason,Response Time,Sentiment,State ,Call Duration in Minutes,Csat Score.The data gives information of customers who called, from which city they called, the reason for their call,feedback of customers,call duration,customer satisfaction score for all the customers.  
###Steps Followed

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 :Check the columns .
- Step 4 : After transforming the data , clicked on close and apply from home tab.
- Step 5 :In the report view, under the view tab, theme was selected.
- Step 6 : As there is only one table, a new table named "Date" was created for measures so that a relation can be established between the given table and new table.
- Step 7 : In model view, a relation between date and the given table was created and it was one to many relationship.
- Step 8 : Measures were created.
- Step 9 : KPI's  were added for the measures created in above step : "Total Calls", "Total Call Duration(in hours),"Total Call Duration (in minutes)","Average time duration (in mins)","Response Time Percentage".
- Step 9 : Visual filters (Slicers) were added for three fields named "Date", "Channel", "City".
- Step 10 : A Column Chart was created representing Total Calls by Day. Formatting was done and the graph was not sorted according to the weekdays.For that a new column was created named "Day Number" using weekday function and then the grpah was sorted according to the Day Number and in ascending order.
- Step 11 : Shape Map was used to visualize Total Calls by State.Formatting was done accoridng to the number of calls.
- Step 12 : A tree map was created depicting the Total Calls by Reason.
- Step 13 - Donut Chart was created representing Total Calls by Channels.
- Step 14 - Column Chart was created for Total Calls by Sentiments.
- Step 15 - A Bar Chart was created representing Total Calls by Call Centre City.
- Step 16 -A Grid was created using Table which included Id,customer name ,channel, state ,reason,response time,city, total call duration (mins).

###DAX Expressions used for creating Measures for Card Visuals.
- 1)Total Calls = COUNT('Call Center_Call Center'[Id])
![total calls](https://github.com/Shreyavig/Call-Centre-Dashboard/assets/158707069/26f3f14b-87a6-46fd-b79a-75e90aa10655)

- 2)Total call duration (hours) = [Total Call duration (mins)]/60
Snap of Average Revenue :
![total duration(in hours)](https://github.com/Shreyavig/Call-Centre-Dashboard/assets/158707069/ca02d630-eab7-42d4-b98c-3144949b8321)
- 3) Total Call duration (mins) = SUM('Call Center_Call Center'[Call Duration In Minutes]).
Snap of Total Transaction : 
![total call duration (in mins)](https://github.com/Shreyavig/Call-Centre-Dashboard/assets/158707069/8517111e-c3ae-46f1-aca5-c67cd06aadd5)

-4)Avg call duration(mins) = AVERAGE('Call Center_Call Center'[Call Duration In Minutes])
Snap of Total Countries :
![average call duration(mins)](https://github.com/Shreyavig/Call-Centre-Dashboard/assets/158707069/4bd919bd-4532-4689-b8a4-3576d35ecdb4)
- 5) Response time percenatge = CALCULATE([Total Calls],'Call Center_Call Center'[Response Time]="Within SLA" || 'Call Center_Call Center'[Response Time]="Above SLA")/[Total Calls]
Snap of Response Time Percentage :
![response time percentage](https://github.com/Shreyavig/Call-Centre-Dashboard/assets/158707069/d633a835-e1f1-47b4-8a33-3da39aefb8d4)


### SNAP OF POWER BI DASHBOARD 
![call centre](https://github.com/Shreyavig/Call-Centre-Dashboard/assets/158707069/2eb61836-dbcd-4957-97fe-58a6408950af)

![call centre 2](https://github.com/Shreyavig/Call-Centre-Dashboard/assets/158707069/8f8ec83b-b3fb-4887-98a1-797aa3967538)







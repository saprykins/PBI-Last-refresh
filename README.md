# PBI-Last-refresh

Step 1: Open Power BI desktop, click on Transform Data option.


Step 2: From the Home ribbon, click in New Source option and select Blank Query.


Step 3: Once you have Blank Query table “Query1” in place under the Queries section, right click on it and rename it to “Last Refreshed Date”.


Step 4: Now, open the Advance Editor from the Home ribbon and paste the below M code.


M Code

let
Source = #table(type table[Date Last Refreshed=datetime], {{DateTime.LocalNow()}})
in
Source


Once you pasted the code, click on Done.

Now, the M code will create a column with name “Last Refreshed Date” which has current date and time. This date will get updated every time you refresh the dataset of the report.

Now, click on Close & Apply.

Link https://addendanalytics.com/blog/last-refresh-date-in-power-bi/  

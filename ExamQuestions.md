# DA-100: Analyzing Data with Microsoft Power BI



## CASE STUDY 1:
Overview -
Litware, Inc. is an online retailer that uses Microsoft Power BI dashboards and reports.
The company plans to leverage data from Microsoft SQL Server databases, Microsoft Excel files, text files, and several other data sources.
Litware uses Azure Active Directory (Azure AD) to authenticate users.

Existing Environment -

Sales Data -
Litware has online sales data that has the SQL schema shown in the following table.

![alt text](/img/casestudy1_img1.PNG) 

In the Date table, the date_id column has a format of yyyymmdd and the month column has a format of yyyymm.
The week column in the Date table and the week_id column in the Weekly_Returns table have a format of yyyyww.
The sales_id column in the Sales table represents a unique transaction.
The region_id column can be managed by only one sales manager.

Data Concerns -
You are concerned with the quality and completeness of the sales data. You plan to verify the sales data for negative sales amounts.

Reporting Requirements -
Litware identifies the following technical requirements:
Executives require a visual that shows sales by region.
Regional managers require a visual to analyze weekly sales and returns.
Sales managers must be able to see the sales data of their respective region only.
The sales managers require a visual to analyze sales performance versus sales targets.
The sale department requires reports that contain the number of sales transactions.
Users must be able to see the month in reports as shown in the following example: Feb 2020.
The customer service department requires a visual that can be filtered by both sales month and ship month independently.

You need to review the data for which there are concerns before creating the data model.
What should you do in Power Query Editor?

* A. Transform the sales_amount column to replace negative values with 0.
* B. Select Column distribution.
* C. Select the sales_amount column and apply a number filter.
* D. Select Column profile, and then select the sales_amount column.

## Answer A






## Q.1  You need to create a relationship between the Weekly_Returns table and the Date table to meet the reporting requirements of the regional managers. What should you do?

* A. In the Weekly.Returns table, create a new calculated column named date-id in a format of yyyymmdd and use the calculated column to create a relationship to
the Date table.
* B. Add the Weekly_Returns data to the Sales table by using related DAX functions.
* C. Create a new table based on the Date table where date-id is unique, and then create a many-to-many relationship to Weekly_Return.

## Answer: A

## Q.2 What should you create to meet the reporting requirements of the sales department?

* A. a calculated column that use a formula of couMTA(Sales[sales_id]>
* B. a calculated measure that uses a formula of couNTROws(Sales)
* C. a calculated column that uses a formula of suM(Sales[sales_id])
* D. a measure that uses a formula of sw-i(Sales[sales_id])

## Answer: B


## Q.3 You create a dashboard by using the Microsoft Power Bl Service. The dashboard contains a card visual that shows total sales from the current year. You grant users access to the dashboard by using the viewer role on the workspace. A user wants to receive daily notifications of the number shown on the card visual. You need to automate the notifications. What should you do?

* A. Share the dashboard to the user.
* B. Create a subscription.
* C. Create a data alert.
* D. Tag the user in a comment.

## Answer: B 

## Q.4 You build a report to analyze customer transactions from a database that contains the tables shown in the following table.

![alt text](/img/Q4_img1.PNG) 

You import the tables.
Which relationship should you use to link the tables?

* A. one-to-many from Customer to Transaction
* B. one-to-one between Customer and Transaction
* C. one-to-many from Transaction to Customer
* D. many-to-many between Customer and Transaction

## Answer: A


## Q.5 You use an R visual to produce a map of 500,000 customers. You include the values of CustomerID, Latitude, and Longitude in the fields sent to the visual. Each customer ID is unique.

In powerbi.com, when users load the visual, they only see some of the customers.
What is the cause of the issue?

* A The visual was built by using a different version of R.
* B The data comes from a Microsoft SQL Server source.
* C The data is deduplicated.
* D Too many records were sent to the visual.

#  Answer : D

## Q.6 You have a line chart that shows the number of employees in a department over time.

You need to see the total salary costs of the employees when you hover over a data point.

What is possible way to achieve this goal?

* A Add a salary to the tooltips.
* B Add a salary to the visual filters.
* C Add salary to the drillthrough fields.

## Answer A

## Q.7 you have a report that contains a bar chart and a column chart. The bar chart shows customer count by customer segment. The column chart shows sales by month.

You need to ensure that when a segment is selected in the bar chart, you see which portion of the total sales for the month belongs to the customer segment.

How should the visual interactions be set on the column chart when the bar chart is selected?

* A no impact
* B highlight
* C filter HIGHLIGHT as the question required us to 'you see which portion of the total sales for the month belongs to the customer segment' -- in order to see WHICH portion, you need to still see the whole visual, highlight is most appropriate. If the requirement stated to ONLY SEE THE PORTION IT RELATES TO then filter would be appropriate.

## Answer B

## Q.8 You have a dashboard that contains tiles pinned from a single report as shown in the Original Dashboard exhibit. (Click the Original Dashboard tab.)
![alt text](/img/Q8_img1.PNG) 
You need to modify the dashboard to appear as shown in the Modified Dashboard exhibit. (Click the Modified Dashboard tab.)

![alt text](/img/Q8_img2.PNG) 

What should you do?

* A Edit the details of each tile.
* B Change the report theme.
* C Change the dashboard theme.
* D Create a custom CSS file.

## Answer C

## Q.9 Note: This question is part of a series of questions that present the same scenario. Each question in the series contains a unique solution that might meet the stated goals. Some question sets might have more than one correct solution, while others might not have a correct solution.

After you answer a question in this section, you will NOT be able to return to it. As a result, these questions will not appear in the review screen.

    You are modeling data by using Microsoft Power BI. Part of the data model is a large Microsoft SQL Server table named Order that has more than 100 million records.

    During the development process, you need to import a sample of the data from the Order table.

Solution1 : From Power Query Editor, you import the table and then add a filter step to the query.

Does this meet the goal?
* A Yes
* B No

## Answer A

Solution 2: You add a WHERE clause to the SQL statement.

Does this meet the goal?

* A Yes
* B No
## Answer A

## Q.10 Note: This question is part of a series of questions that present the same scenario. Each question in the series contains a unique solution that might meet the stated goals. Some question sets might have more than one correct solution, while others might not have a correct solution.

After you answer a question in this section, you will NOT be able to return to it. As a result, these questions will not appear in the review screen.

    You create a parameter named DataSourceExcel that holds the file name and location of a Microsoft Excel data source.

    You need to update the query to reference the parameter instead of multiple hard-coded copies of the location within each query definition.

Solution 1: You modify the source step of the queries to use DataSourceExcel as the file path.

Does this meet the goal?

* A Yes
* B No
## Answer : A

## Q.11 You have a Microsoft SharePoint Online site that contain several document libraries.

One of the document libraries contains manufacturing reports saved as Microsoft Excel files. All the manufacturing reports have the same data structure.

You need to use Power BI Desktop to load only the manufacturing reports to a table for analysis.

What should you do?

* A. Get data from a SharePoint Online folder, enter the site URL, and then select Combine & Load.
* B. Get data from a SharePoint Online list and enter the site URL. Select Combine & Transform, then filter by the folder path to the manufacturing reports library.
* C. Get data from a SharePoint Online folder and enter the site URL. Select Combine & Transform, then filter by the folder path to the manufacturing reports library.
* D. Get data from a SharePoint Online list, enter the site URL, and then select Combine & Load.

## Answer C

## Q.12 You have a report page that contains the visuals shown in the following exhibit
![alt text](/img/Q12_img1.PNG) 

Use the drop-down menus to select the answer choice that completes each statement based on the information presented in the graphic.
NOTE: Each correct selection is worth one point.

![alt text](/img/Q12_img2.PNG) 

## Answer
![alt text](/img/Q12_img3.PNG)

## Q.13 you have a report that contains four pages. Each page contains slicers for the same four fields.Users report that when they select values in a slicer on one page, the selections are not persisted on other pages.

You need to recommend a solution to ensure that users can select a value once to filter the results on all the pages.

What are two possible recommendations to achieve this goal? Each correct answer presents a complete solution.

NOTE: Each correct selection is worth one point.
* A. Replace the slicers with report-level filters.
* B. Sync the slicers across the pages.
* C. Create a bookmark for each slicer value.
* D. Replace the slicers with page-level filters.
* E. Replace the slicers with visual-level filters.

## Answer A,B

## Q.14 You plan to create the chart shown in the following exhibit.
![alt text](/img/Q14_img1.PNG)

How should you create the dashed horizontal line denoting the 40th percentile of daily sales for the period shown?

* A. Add a measure to the visual that uses the following DAX expression. Measure1 = PERCENTILEX.INC (Sales,Sales[Total Sales],0.40)
* B. Add a new percentile line that uses Total Sales as the measure and 40% as the percentile.
* C. Create a horizontal line that has a fixed value of 24,000.
* D. Add a measure to the visual that uses the following DAX expression. Measure1 = PERCENTILEX.EXC (Sales,Sales[Total Sales],0.40)

## Answer B

## Q.15 You need to create a visual as shown in the following exhibit.

![alt text](/img/Q15_img1.PNG)
The indicator color for Total Sales will be based on % Growth to Last Year.
The solution must use the existing calculations only.
How should you configure the visual? To answer, select the appropriate options in the answer area.
NOTE: Each correct selection is worth one point.
Hot Area:
![alt text](/img/Q15_img2.PNG)

## Answer 
![alt text](/img/Q15_img3.PNG)

## Q.16 Note: This question is part of a series of questions that present the same scenario. Each question in the series contains a unique solution that might meet the stated goals. Some question sets might have more than one correct solution, while others might not have a correct solution. After you answer a question in this scenario, you will NOT be able to return to it. As a result, these questions will not appear in the review screen.

    You have a clustered bar chart that contains a measure named Salary as the value and a field named Employee as the axis. 

    Salary is present in the data as numerical amount representing US dollars.

    You need to create a reference line to show which employees are above the median salary.

Solution 1: You create a constant line and set the value to .5.

Does this meet the goal?

* A. Yes
* B. No

## Answer B

Solution 2: You create a median line by using the Salary measure.

Does this meet the goal?
A. Yes
B. No

## Answer A

## Q.17 You need to create a visualization that compares revenue and cost over time.
Which type of visualization should you use?

* A. stacked area chart
* B. donut chart
* C. line chart
* D. waterfall chart

## Answer C

## Q.18 You have a collection of reports for the HR department of your company. You need to create a visualization for the HR department that shows a historic employee counts and predicts trends during the next six months.

Which type of visualization should you use?

* A. key influencers
* B. ribbon chart
* C. line chart
* D. scatter chart

## Answer: C

## Q.19 You are developing a sales report that will have multiple pages. Each page will answer a different business question.

You plan to have a menu page that will show all the business questions.

You need to ensure that users can click each business question and be directed to the page where the question is answered. 

The solution must ensure that the menu page will work when deployed to any workspace.

What should you include on the menu page?
* A. Create a text box for each business question and insert a link.
* B. Create a button for each business question and set the action type to Bookmark.
* C. Create a Power Apps visual that contains a drop-down list. The drop-down list will contain the business questions.

## Answer C

## Q.20 You are developing a report page. Some users will navigate the report by using a keyboard, and some users will consume the report by using a screen reader.

You need to ensure that the users can consume the content on a report page in a logical order.

What should you configure in Microsoft Power BI Desktop?
A. the tab order
B. the layer order
C. the bookmark order
D. the X position

## Answer A

## Q.21 You have the Power BI data model shown in the following exhibit.
![alt text](/img/Q21_img1.PNG)

Use the drop-down menus to select the answer choice that completes each statement based on the information presented in the graphic.
NOTE: Each correct selection is worth one point.

![alt text](/img/Q21_img2.PNG)

## Answer
![alt text](/img/Q21_img3.PNG)

## Q.22 You have the line chart shown in the exhibit. (Click the Exhibit tab.)

![alt text](/img/Q22_img1.PNG)

You need to modify the chart to meet the following requirements:

✑ Identify months that have order counts above the mean.

✑ Display the mean monthly order count.

Which three actions should you perform in sequence? To answer, move the appropriate actions from the list of actions to the answer area and arrange them in the correct order.

Select and Place:
![alt text](/img/Q22_img2.PNG)

## Answer: 
![alt text](/img/Q22_img3.PNG)

## Q. 23 You have a query named Customer that imports CSV files from a data lake. The query contains 50,000 rows as shown in the exhibit. (Click the Exhibit tab.)

![alt text](/img/Q23_img1.PNG)

Each file contains deltas of any new or modified rows from each load to the data lake. Multiple files can have the same customer ID.

You need to keep only the last modified row for each customer ID.

Which three actions should you perform in sequence? 
To answer, move the appropriate actions from the list of actions to the answer area and arrange them in the correct order.
Select and Place:

![alt text](/img/Q23_img3.PNG)


## Q.24 Your company has training videos that are published to Microsoft Stream. You need to surface the videos directly in a Microsoft Power BI dashboard.

Which type of tile should you add?
* A. video
* B. custom streaming data
* C. text box
* D. web content

## Answer : B

## Q.25. You need to create a relationship between the Weekly_Returns table and the Date table to meet the reporting requirements of the regional managers. What should you do?

* A. In the Weekly.Returns table, create a new calculated column named date-id in a format of yyyymmdd and use the calculated column to create a relationship to
the Date table.
* B. Add the Weekly_Returns data to the Sales table by using related DAX functions.
* C. Create a new table based on the Date table where date-id is unique, and then create a many-to-many relationship to Weekly_Return.

## Answer: A

## Q.26 You have a Microsoft SharePoint Online site that contains several document libraries. One of the document libraries contains manufacturing reports saved as Microsoft Excel files. All the manufacturing reports have the same data structure. You need to load only the manufacturing reports to a table for analysis.

What should you do in Microsoft Power Bl Desktop?

* A. Get data from a SharePoint Online folder and enter the site URL. Edit the query and filter by the
path to the manufacturing reports library.
* B. Get data from a SharePoint Online list and enter the site URL. Edit the query and filter by the path
to the manufacturing reports library.
* C. Get data from a SharePoint Online list, enter the site URL, and then select Combine & Load.
* D. Get data from a SharePoint Online folder, enter the site URL, and then select Combine & Load.

## Answer: A

## Q.27 You need to create a visualization to meet the reporting requirements of the sales managers. How should you create the visualization? To answer, select the appropriate options in the answer area.

NOTE: Each correct selection is worth one point.

![alt text](/img/Q27_img1.PNG)

## Answer

![alt text](/img/Q27_img2.PNG)

## Q.28 Your company plans to completely separate development and production assets such as datasets, reports, and dashboards in Microsoft Power Bl.

You need to recommend an application lifecycle strategy. The solution must minimize maintenance to update access and prevent end users from viewing the
development assets.

What should you recommend?
* A. Create production reports in a separate workspace that uses a shared dataset from the development workspac
* B. Grant the end users access to the production workspace.
* C. In the same workspace, create separate copies of the assets and append DEV to the names of the copied asset
* D. Grant the end users access to the workspace.
* E. Create separate workspaces for development and productio
* F. Grant the end users access to the production workspace.
* G. Create one workspace for developmen
* H. From the workspace, publish an app for production.

## Answer: C

## Q.29 You have a report that contains four pages. Each page contains slicers for the same four fields. Users report dthat when they select values on a slicer on one page, the visuals are not updated on all the pages. You need to recommend a solution to ensure that users can select a value once to filter the results on all the pages. 

What are two possible recommendations to achieve this goal? Each correct answer presents a complete solution. NOTE: Each correct selection is worth
one point.

* A. Sync the slicers across the pages.
* B. Replace the slicers with page-level filters.
* C. Replace the slicers with visual-level filters.
* D. Create a bookmark for each slicer value.
* E. Replace the slicers with report-level filters.

## Answer: A,B

## Q.30  You have a collection of reports for the HR department of your company. The datasets use row-level security (RLS). The company has multiple sales regions that each has an HR manager. You need to ensure that the HR managers can interact with the data from their region only. The HR managers must be prevented from changing the layout of the reports. How should you provision access to the reports for the HR managers?

* A. Create a new workspace, copy the datasets and reports, and add the HR managers as members of the workspace.
* B. Publish the reports to a different workspace other than the one hosting the datasets.
* C. Publish the reports in an app and grant the HR managers access permission.
* D. Add the HR managers as members of the existing workspace that hosts the reports and the datasets.

## Answer: D

## Q.31 You have a data model that contains many complex DAX expressions. The expressions contain frequent references to the RELATED and RELATEDTABLE functions. You need to recommend a solution to minimize the use of the RELATED and RELATEDTABLE functions.

What should you recommend?

* A. Split the model into multiple models.
* B. Hide unused columns in the model.
* C. Merge tables by using Power Query.
* D. Transpose.

## Answer C
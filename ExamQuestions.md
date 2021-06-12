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

Solution3: You add a report-level filter that filters based on the order date.

Does this meet the goal?

* A. Yes
* B. No

## Answer: B

## Q.10 Note: This question is part of a series of questions that present the same scenario. Each question in the series contains a unique solution that might meet the stated goals. Some question sets might have more than one correct solution, while others might not have a correct solution.

After you answer a question in this section, you will NOT be able to return to it. As a result, these questions will not appear in the review screen.

    You create a parameter named DataSourceExcel that holds the file name and location of a Microsoft Excel data source.

    You need to update the query to reference the parameter instead of multiple hard-coded copies of the location within each query definition.

Solution 1: You modify the source step of the queries to use DataSourceExcel as the file path.

Does this meet the goal?

* A Yes
* B No
## Answer : A


Solution 2: Solution: In the Power Query M code, you replace references to the Excel file with DataSourceExcel. Does this meet the goal?
* A. Yes
* B. No
## Answer: B

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

## Q.20 You are developing a report page. Some users will navigate the report by using a keyboard, and some users will consume the report by using a screen reader.You need to ensure that the users can consume the content on a report page in a logical order.

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


## Q.32 You have a custom connector that returns ID, From, To, Subject, Body, and Has Attachments for every email sent during the past year. More than 10 million records are returned.
You build a report analyzing the internal networks of employees based on whom they send emails to.
You need to prevent report recipients from reading the analyzed emails. The solution must minimize the model size.
What should you do?

* A. Implement row-level security (RLS) so that the report recipients can only see results based on the emails they sent.
* B. Remove the Subject and Body columns during the import.
* C. From Model view, set the Subject and Body columns to Hidden.

Answer B

### Q.33 You have a prospective customer list that contains 1,500 rows of data. The list contains the following fields:
✑ First name
✑ Last name
✑ Email address
✑ State/Region
✑ Phone number
You import the list into Power Query Editor.
You need to ensure that the list contains records for each State/Region to which you want to target a marketing campaign.
Which two actions should you perform? Each correct answer presents part of the solution.
NOTE: Each correct selection is worth one point.
* A. Open the Advanced Editor.
* B. Select Column quality.
* C. Enable Column profiling based on entire dataset.
* D. Select Column distribution
* E. Select Column profile.

## Answer: C,E

## Q.34 You have an API that returns more than 100 columns. The following is a sample of column names.
✑ client_notified_timestamp
✑ client_notified_source
✑ client_notified_sourceid
✑ client_notified_value
✑ client_responded_timestamp
✑ client_responded_source
✑ client_responded_sourceid
✑ client_responded_value
You plan to include only a subset of the returned columns.
You need to remove any columns that have a suffix of sourceid.
How should you complete the Power Query M code? To answer, select the appropriate options in the answer area.

![alt text](/img/Q34_img1.PNG)

Answer

![alt text](/img/Q34_img2.PNG)

## 35: You build a report to help the sales team understand its performance and the drivers of sales. The team needs to have a single visualization to identify which factors affect success. Which type of visualization should you use?
* A. Key influences
* B. Funnel chart
* C. Q&A
* D. Line and clustered column chart

## Answer: A

## 36. You receive revenue data that must be included in Microsoft Power Bl reports. You perform an initial load of the data from a Microsoft Excel source as shown in the following exhibit


![alt text](/img/Q34_img1.PNG)


You plan to create several visuals from the data, including a visual that shows revenue split by year and product.
You need to transform the data to ensure that you can build the visuals. The solution must ensure that the columns are named appropriately for the data that they contain.


![alt text](/img/Q34_img2.PNG)

## Answer:

![alt text](/img/Q34_img2.PNG)


## Q.37 You have two Azure SQL databases that contain the same tables and columns. For each database, you create a query that retrieves data from a table named Customers.

You need to combine the Customer tables into a single table. The solution must minimize the size of the data model and support scheduled refresh in
powerbi.com.

What should you do? To answer, select the appropriate options in the answer area. NOTE: Each correct selection is worth one point.


![alt text](/img/Q37_img1.PNG)

## Answer
![alt text](/img/Q37_img2.PNG)


## Q.38 You have an Azure SQL database that contains sales transactions. The database is updated frequently. You need to generate reports from the data to detect fraudulent transactions. The data must be visible within five minutes of an update.

How should you configure the data connection?
* A. Add a SQL statement.
* B. Set Data Connectivity mode to DirectQuery.
* C. Set the Command timeout in minutes setting.
* D. Set Data Connectivity mode to Import

## Answer B


## Q.39 You publish a report to a workspace named Customer Services. The report identifies customers that have potential data quality issues that must be investigated by the customer services department of your company. You need to ensure that customer service managers can create task lists in Microsoft Excel based on the data. Which report setting should you configure?

* A. Don't allow end user to save filters on this report.
* B. Change default visual interaction from cross highlighting to cross filtering.
* C. Enable the updated filter pane, and show filters in the visual header for this report.
* D. Allow users to add comments to this report.
* E. Choose the type of data you allow your end users to export.

## Answer: A

## Q.40 You are creating a visual to show the ranking of product categories by sales revenue.Your company's security policy states that you cannot send data outside of your Microsoft Power Bl tenant Which approach provides the widest variety of visuals while adhering to the security policy?

* A. Use default visuals or custom visuals uploaded from a .pbiviz file.
* B. Use only default visuals.
* C. Use default or any custom visuals from the marketplace.
* D. Use default or certified custom visuals.

### Answer: C

## Q.41 You import a large dataset to Power Query Editor. You need to identify whether a column contains only unique values.
Which two Data Preview options can you use? Each correct answer presents a complete solution.

NOTE: Each correct selection is worth one point

* A. Show whitespace
* B. Column distribution
* C. Column profile
* D. Column quality
* E. Monospaced

## Answer: A,D

## Q.42 You have a Microsoft Power Bl report. The size of PBIX file is 550 MB. The report is accessed by using an App workspace in shared capacity of powerbi.com.

The report uses an imported dataset that contains one fact table. The fact table contains 12 million rows. The dataset is scheduled to refresh twice a day at 08:00 and 17:00.

The report is a single page that contains 15 custom visuals and 10 default visuals.
Users say that the report is slow to load the visuals when they access and interact with the report You need to recommend a solution to improve the performance
of the report.

What should you recommend?
* A. Split the visuals onto multiple pages.
* B. Implement row-level security (RLS).
* C. Replace the default visuals with custom visuals.
* D. Increase the number of times that the dataset is refreshed.

Answer: A

## Q.43 You have a Microsoft Power Bl dashboard. You need to ensure that consumers of the dashboard can give you feedback that will be visible to the other consumers of the dashboard.

What should you use?
* A. Feedback
* B. Subscribe
* C. Comments
* D. Mark as favorite

Answer: C

## Q.44 You have a Microsoft Excel workbook that contains two tables. From Power BI, you create a dashboard that displays data from the tables. You update the tables each day. You need to ensure that the visualizations in the dashboard are updated daily.

Which three actions should you perform in sequence? To answer, move the appropriate actions from the list of actions to the answer area and arrange them in the correct order

![alt text](/img/Q44_img1.PNG)

### Answer:
![alt text](/img/Q44_img2.PNG)


## Q.45 You manage a Power BI model that has two tables named Sales and Product. You need to ensure that a sales team can view only data that has a CountryRegionName value of Unites States and a ProductCategory value of Clothing.

What should you do from Power BI Desktop?

* A. Add the following filters to a report. CountryRegionName is United States ProductCategory is Clothing
* B. From Power BI Desktop, create a new role that has the following filters. [CountryRegionName] = "United States" [ProductCategory] = "Clothing"
* C. Add the following filters in Query Editor. CountryRegionName is United States ProductCategory is Clothing
* D. From Power BI Desktop, create a new role that has the following filter. [CountryRegionName] = "United States" && [ProductCategory] = "Clothing"
 
## Answer D

## Q.46 You have five sales regions. Each region is assigned a single salesperson. You have an imported dataset that has a dynamic row-level security (RLS) role named Sales. The Sales role filters sales transaction data by salesperson. Salespeople must see only the data from their region. You publish the dataset to powerbi.com, set RLS role membership, and distribute the dataset and related reports to the salespeople.A salesperson reports that she believes she should see more data. You need to verify what data the salesperson currently sees. 

What should you do?
* A. Use the Test as role option to view data as the salesperson's user account.
* B. Use the Test as role option to view data as the Sales role.
* C. Instruct the salesperson to open the report in Microsoft Power Bl Desktop.
* D. Filter the data in the reports to match the intended logic in the filter on the sales transaction table.

## Answer: B


## Q.47 You need to create the required relationship for the executive's visual. What should you do before you can create the relationship?

* A. Change the data type of Sales[region_id] to Whole Number.
* B. In the Sales table, add a measure for sum(sales_amount).
* C. Change the data type of sales[sales_id] to Text.
* D. Change the data type of sales [region_id] to Decimal Number.

## Answer: C

## Q.48 You have four sales regions. Each region has multiple sales managers. You implement row-level security (RLS) in a data model. You assign the relevant distribution lists to each role. You have sales reports that enable analysis by region. The sales managers can view the sales records of their region. The sales managers are prevented from viewing records from other regions.

A sales manager changes to a different region.
You need to ensure that the sales manager can see the correct sales data.
What should you do?

* A. Change the Microsoft Power BI license type of the sales manager.
* B. From Microsoft Power BI Desktop, edit the Row-Level Security setting for the reports.
* C. Request that the sales manager be added to the correct Azure Active Directory group.
* D. Manage the permissions of the underlying dataset.

## Anwser C



## Q. 49 You are developing a report page. Some users will navigate the report by using a keyboard, and some users will consume the report by using a screen reader.
You need to ensure that the users can consume the content on a report page in a logical order. What should you configure in Microsoft Power Bl Desktop?
* A. the bookmark order
* B. the layer order
* C. the tab order
* D. the X position

## Answer: B
Refference:  https://docs.microsoft.com/en-us/learn/modules/data-driven-story-power-bi/2-report-layout


## Q.50 You have multiple dashboards. You need to ensure that when users browse the available dashboards from powerbi.com. they can see which dashboards contain Personally Identifiable Information (Pll). The solution must minimize configuration effort and impact on the dashboard design.
What should you use?

* A. Active Directory groups
* B. tiles
* C. data classifications
* D. comments

## Answer: A




## Q.51 You are creating an analytics report that will consume data from the tables shown in the following table.

![alt text](/img/Q51_img1.PNG)

There is a relationship between the tables.
There are no reporting requirements on employeejd and employee_photo. You need to optimize the data model
What should you configure for employeejd and employee.photo? To answer, select the appropriate options in the answer area.
![alt text](/img/Q51_img2.PNG)

## Answer:  
![alt text](/img/Q51_img3.PNG)


## Q.52 You build a report about warehouse inventory data. The dataset has more than 10 million product records from 200 warehouses worldwide. You have a table named Products that contains the columns shown in the following table
![alt text](/img/Q52_img1.PNG)

Warehouse managers report that it is difficult to use the report because the report uses only the product name in tables and visuals. 
The product name is contained within the ProductDescription column and is always the fourth value.
You need to modify the report to support the warehouse managers requirement to explore inventory levels at different levels of the product hierarchy. The solution
must minimize the model size.

Which three actions should you perform in sequence? To answer, move the appropriate actions from the list of actions to the answer area and arrange them in the
correct order.

![alt text](/img/Q52_img2.PNG)

## ANswer
![alt text](/img/Q52_img3.PNG)


## Q.53 You create the following step by using Power Query Editor.

    = Table.ReplaceValue(SalesLT_Address,"1318","1319",Replacer.ReplaceText,{"AddressLine1"})

A row has a value of 21318 Lasalle Street in the AddressLine1 column. What will the value be when the step is applied?

* A. 1318
* B. 1319
* C. 21318 Lasalle Street
* D. 21319 Lasalle Street

## Answer: D



## Q.54 You have a Microsoft Power Bl workspace. You need to grant the user capabilities shown in the following table

![alt text](/img/Q54_img1.PNG)
The solution must use the principle of least privilege.
Which user role should you assign to each user? To answer, drag the appropriate roles to the correct users. Each role may be used once, more than once, or not
at all. You may need to drag the split bar between panes or scroll to view content.
NOTE: Each correct selection is worth one point.

![alt text](/img/Q54_img2.PNG)

## Answer
![alt text](/img/Q54_img3.PNG) 

## Q.55 You are creating a quick measure as shown in the following exhibit.

![alt text](/img/Q55_img1.PNG) 

You need to create a monthly rolling average measure for Sales over time-How should you configure the quick measure calculation? To answer, select the
appropriate options in the answer area.
NOTE: Each correct selection is worth one point.

![alt text](/img/Q55_img2.PNG) 

### Answer

![alt text](/img/Q55_img3.PNG) 

## Q.56 You are building a dataset from a JSON file that contains an array of documents. You need to import attributes as columns from all the documents in the JSON file. The solution must ensure that date attributes can be used as date hierarchies in Microsoft Power BI reports.

Which three actions should you perform in sequence? To answer, move the appropriate actions from the list of actions to the answer area and arrange them in the correct order.


![alt text](/img/Q56_img1.PNG) 

## Answer
Steps to follow in order
* Convert the list to table
* Expand the columns
* Add column that use data type Convesion

## Q.57 You import two Microsoft Excel tables named Customer and Address into Power Query. Customer contains the following columns:

    ✑ Customer ID
    ✑ Customer Name
    ✑ Phone
    ✑ Email Address
    ✑ Address ID
    Address contains the following columns:
    ✑ Address ID
    ✑ Address Line 1
    ✑ Address Line 2
    ✑ City
    ✑ State/Region
    ✑ Country
    ✑ Postal Code

The Customer ID and Address ID columns represent unique rows.

You need to create a query that has one row per customer. Each row must contain City, State/Region, and Country for each customer.

What should you do?
A. Merge the Customer and Address tables.
B. Transpose the Customer and Address tables.
C. Group the Customer and Address tables by the Address ID column.
D. Append the Customer and Address tables.

### Answer A


## Q.57 You are creating a column chart visualization. You configure groups as shown in the Groups exhibit. {Click the Groups tab.)

![alt text](/img/Q57_img1.PNG) 

The visualization appears as shown in the Chart exhibit. (Click the Chart tab.)

![alt text](/img/Q57_img2.PNG) 

For each of the following statements, select Yes if the statement is true. Otherwise, select No.
NOTE: Each correct selection is worth one point.

![alt text](/img/Q57_img3.PNG) 

## Answer 
![alt text](/img/Q57_img4.PNG) 

## Q.58 Your company has affiliates who help the company acquire customers. You build a report for the affiliate managers at the company to assist them in understanding affiliate performance.
The managers request a visual showing the total sales value of the latest 50 transactions for each affiliate. You have a data model that contains the following tables.

![alt text](/img/Q58_img1.PNG) 

The Affiliate table has a one-to-many relationship to the Transactions table based on the AffiliateID column.
You need to develop a measure to support the visual.
How should you complete the DAX expression? To answer, select the appropriate options in the answer area.
NOTE: Each correct selection is worth one point.
Hot Area:

![alt text](/img/Q58_img2.PNG) 

## Answer

![alt text](/img/Q58_img3.PNG) 

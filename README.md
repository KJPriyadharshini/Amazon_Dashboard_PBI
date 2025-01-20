# Amazon_Dashboard_PBI
## Problem Statement


This dashboard helps the Sales Excecutive understand the sales of product. It helps them to track and analyze sales performance based on the total sales amount and units sold across different categories, time periods, and regions. The goal is to provide actionable insights for identifying trends, top-performing products, and underperforming areas to improve decision-making and optimize sales strategies.

### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Find the category section, image, name, and description. Split the large image column to find just one image and remove extra parts. 
- Step 4 : In the category column, divide the text where it changes from lowercase to uppercase.
- Step 5 : Replace empty spaces in other columns with blank values. 
- Step 6 : Add a new custom column by merging information. Remove all columns that are not needed or are empty.
 Data is cleaned and ready for visualizations.

- Step 7 : Click on the new slicer and add the category field. To remove blank data, click on transform and filter out blanks from the large column.
- Step 8 : Next, click on format visual and select callout value. Turn the label on and add the product name in the field description.
- Step 9 : Add the 'large' field to the image section. Align it to the left and keep it normal. Next, go to layout, set the rows to 8 and columns to 1, and add a space of 5 between the cards. Turn off the title.
- Step 10 : Change the layout for each state, like hover and select button. To create a navigation bar, choose a shape, change its color, and add a shadow. Add a logo image with the correct size.
- Step 11 : Create new pages named Product and Product View. Copy the entire navigation bar and paste it into both new pages.
- Step 12 : Create new table for sale options. Use an uploaded Excel file. Use the first row as a header, add a slicer, select the status field, filter the tab, and remove any blanks. Format it the same way as before.
- Step 13 : Merge two queries to get item prices. Add a new column for total amount and a new measure for sale amount. Add a filter for sales as a new card and another slicer for sales and units.

          Tot_Amt = Amt * qty 
          Sale_amt = SUM(Amazon[Total_Amt])
          Sale_Units = SUM(Amazon[Total_Qty])

- Step 14 : Format every visual according to the theme. To connect the "Sales & Units" slicer and synchronize the dashboard, manage the relationships of the table in the data model tab using the primary key.

          All_overall_sale = CALCULATE([Filter_Sale], ALL('amazon_fashion'[Category]))

- Step 15 : For tooltip page, change the canvas settings to 'tooltip' -> custom change height and width. Sync the slicers for the overview and product page.
- Step 17 : In product page, turn on the tooltip in general settings and give name of product tooltip page.

- Step 18: Add KPI using card visuals for sale_amt, sale_unit, review.

          Review = var val = SUM('amazon_fashion_YT'[no_of_reviews]
          return if (val = Blank), "0", val)

- Step 19 : For the return & lost, select sale_amt and filter the status for returns and lost.
- Step 20 : Make the unit KPI as area chart with date in x-axis and format it according to the theme.
- Step 21 : Copy and paste the product view page to the tooltip and size it to fit.
- Step 23 : The report was then published to power BI service.

# Report Snapshots (Power BI DESKTOP)

Overview page:
![Image](https://github.com/user-attachments/assets/bcb94019-3ea0-4989-8635-07b35314b3b9)

Products page:
![Image](https://github.com/user-attachments/assets/41ee95d0-6877-4096-9714-e2bdc0e507c7)

Product View Page:
![Image](https://github.com/user-attachments/assets/27849262-5f26-45ed-a182-ff0b7d8630f5)

Product_Tooltip Page:
![Image](https://github.com/user-attachments/assets/c2f28d52-af8f-4071-bd26-ad8a7591b884)

# Insights

A single page report was created on Power BI Desktop & it was then published to Power BI Service.


Following inference can be drawn from the dashboard;

     Total Sales = 89 M
           
These values will change if different visual filters will be applied.  
  
# amazon_dashboard.md.txt
Displaying #amazon_dashboard.md.txt.

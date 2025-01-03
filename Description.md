# Sales Forecasting 



 Creating a Sales Dashboard and Forecasting in Power BI is straightforward without using Python, R, or any other external tools. Power BI provides built-in functionalities to design dashboards and forecast data. 


## Objective: 
To contribute to the success of a business by utilizing data analysis techniques, specifically focusing on Time Series Analysis , to provide valuable insights and accurate Sales Forecasting.





## Steps For creating the dashboard: 

 _1. Import and Transform Data_

- Import the dataset in Power BI.
- Clean the data using Power Query Editor.

_2. Designing the Dashboard Layout_

- Add an attractive background to enhance visual appeal.

_3. Create Visuals_

- Clustered Bar Chart:

     - Visual 1: Y-axis: Category, X-axis: Sum of Sales.
     - Visual 2: Y-axis: Sub-Category, apply Top N filter to show the top 3 values.
     - Visual 3: Y-axis: Ship Mode, X-axis: Sum of Sales.
- Area Charts:

     - Sales Comparison
X-axis: Order Date (month), Y-axis: Sum of Sales, Legend: Order Date (year).

     - Profit Comparison
 X-axis: Order Date (month), Y-axis: Sum of Profit, Legend: Order Date (year).

- Map Visualization:

  - Location: State, Bubble Size: Sum of Sales, Tooltips: Sum of Profit.

- Donut Charts:

    - Chart 1: Value: Sum of Sales, Legend: Segment.
    - Chart 2: Value: Sum of Sales, Legend: Payment Mode.

 _4. Add Filters_

   -  Use slicers to filter data by region.


_5. Add Headings and KPIs_

   - Use a text box for headings.
   - Add four KPIs using Card Visualization:
       - Sales, Quantity, Profit, and Avg Delivery Time.







## Steps for using DAX Queries:

1.	Create a New Column for Average Delivery Time
   
       - DAX Query:
         
            ***AvgDelivery = DATEDIFF('Sheet1'[Order Date], 'Sheet1'[Ship Date], DAY)***

2.	Summarize Data for Forecasting

       - DAX Query to create a new table:
         
  	        ***Forecasting = SUMMARIZE('Sheet1', 'Sheet1'[Order Date], "Total Sales", SUM('Sheet1'[Sales]))***








## Steps for creating or analyzing Forecasting:

1.	Create Line Chart for Forecasting.

       - X-axis: Order Date, Y-axis: Sum of Sales.
   
2.	Enable Forecasting.

       - Go to the Analytics Pane in the visualizations panel.
       - Add a forecast, set the forecast length and confidence interval, and apply.
  
3.	Zoom for Detail

       - Enable the Zoom Slider to inspect forecasted values.
    




  
## Important Points:

1. Handling Null Values

     - Check null values in the Column Quality section under View

2. Replace Values

     - For the Return column, replace values with 0.

3. Formatting Tips

     - Use the Format Painter to apply consistent formatting across visuals.
     - Ensure the Canvas Background is set correctly for uploading the dashboard.
  
4. Map Visuals

     - Enable map features under File → Options & Settings → Security → Map & Filled Map Visuals.

5. Data Preparation for Forecasting

      - Combine and sum repeated values in the dataset before forecasting for accuracy.
  




## Conclusion




Incorporated data analysis techniques, specializing in Time series analysis , to deliver valuable Insights , accurate Sales Forecasting , and Interactive Dashboard creation , driving business success.


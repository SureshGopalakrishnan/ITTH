This Power BI Dashboard (SkyTransportCorp_Dashboard.pbix) is designed to offer a comprehensive view of key business operations. It focuses on several critical areas, including
- Financial Performance (Tracking Revenue and Costs)
- Operational Efficiency (Comparing Loaded versus Total Miles)
- Geographic and Time-Based Trends

By visualizing data from various sources such as `TotalMiles`, `Revenue`, and `ShippingCost`, the dashboard enables users to analyze performance over time, identify Top-Performing Regions, and gain insights into Trip Distribution and Profitability.

**Analysis of Cost and Revenue**  
These charts are used to compare Financial Metrics and identify relationships between key variables.
- Bar Chart or Column Chart  
  Visualize `Revenue`, `ShippingCost`, or `LoadedMiles` broken down by `ShipperID`, `CategoryID`, or `TripType`. This is perfect for comparing values across different groups.
- Pie Chart or Treemap  
  Show the proportion of `Revenue` or `ShippingCost` contributed by each `OriginState` or `TripType`.
- Scatter Plot  
  Analyze the relationship between `TotalMiles` and `Revenue`. This helps identify if longer trips are more profitable. `ShippingCost` can be added to the size of the bubbles to create a bubble chart.

**Analysis of Trip Efficiency**  
These visuals focus on Operational Efficiency by comparing `LoadedMiles` to `TotalMiles`.
- Stacked Column Chart  
  Compare LoadedMiles (Revenue Generating) to TotalMiles for each trip or group (e.g., `TripType`). This visual makes it easy to see the percentage of total miles that were productive.
- Gauge Chart or KPI Card  
  Create a KPI (Key Performance Indicator) to track the overall "Load Factor" or "Efficiency," which can be a DAX measure like `SUM([LoadedMiles]) / SUM([TotalMiles])`.

**Time-Based Trends**  
These charts are perfect for understanding how key metrics change over time.
- Line Chart
  Use this to track `Revenue`, `ShippingCost` or `TotalMiles` against `ShipDate` or `DeliveryDate`. This will help identify seasonal trends, peaks in activity, or show the cumulative growth of metrics.
  A secondary axis can be added to show both `Revenue` and `ShippingCost` on the same chart.
- Area Chart
  Similar to a Line Chart, but it fills the area below the line, which is great for visualizing the total volume of something over time, such as Total Miles Shipped per Month.

**Geographic Analysis**  
These visuals are used to see where business is operating and to identify key shipping lanes.
- Map Visuals
  Use `OriginState` and `DestinationState` to create a map showing the density of Trips. You can color-code states by total `Revenue`, average `ShippingCost` or number of trips to quickly spot your most
  profitable or busiest regions.
- Slicer with City/State
  Add slicers for `DestinationState` and `DestinationCity` to allow users to filter the entire dashboard and drill down into specific routes.

**Distribution & Comparison**  
These visuals are great for understanding the composition and distribution of your data.
- Bar Chart or Pie Chart
  Show the count of trips by `TripType` or `CategoryID` to see the mix of services provided. A pie chart or donut chart can show the percentage breakdown of `Revenue` by `CategoryID`.
- Histogram
  Use this to show the distribution of numerical data like `ShipDays` or `TotalMiles` by creating Bins.
  This can help understand the typical duration or distance of your trips and identify any trips that fall outside the norm.

**Performance & Financial Insights** 
These visualizations are crucial for a business-focused dashboard, providing a quick look at operations.
- Card/KPI Visuals
  Create big, bold cards for top-level metrics like total `Revenue`, total `ShippingCost`, total `LoadedMiles`, and average `ShipDays`. This provides an immediate summary of business performance.
- Bar Chart or Clustered Column Chart
  Use these to compare `Revenue` or `ShippingCost` across different `ShipperID`, `CustomerID` or `CategoryID`. This helps you see who your top performers are and where your costs are going.
- Treemap
  This chart is excellent for visualizing a hierarchical breakdown. You could use it to show the percentage of `Revenue` by `CustomerID`, and then by `TripID` within each customer, providing a clear view of your biggest clients.
- Scatter Plot
  This can reveal relationships between two numerical values. For example, plot `ShippingCost` against `TotalMiles` to see if your costs are proportional to distance. Outliers might indicate inefficient trips.

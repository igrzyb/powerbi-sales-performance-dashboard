# Executive Sales & Performance Dashboard (Power BI)

![Dashboard Preview](dashboard_preview.png)

## Overview
An interactive executive BI dashboard built in Power BI Desktop analyzing sales volume ($2.3M), profitability, and YoY growth trends for a multi-regional retail business.

## Tech Stack
* **BI Tool:** Microsoft Power BI Desktop
* **Calculations:** DAX (Data Analysis Expressions)
* **Data Modeling:** Star Schema (Orders Fact & Calendar Dim)
* **ETL:** Power Query (M)

## Key Features
* **Executive KPIs:** Real-time tracking of *Total Sales*, *Total Profit*, *Profit Margin %*, and *YoY Sales Growth %*.
* **Time Intelligence:** Dynamic monthly seasonality trends comparing current sales with prior year (*Sales LY*).
* **Segment & Category Analysis:** Performance breakdowns across consumer segments and product categories.
* **Geographic Distribution:** Interactive regional and state-level map analytics.

## DAX Calculations
* `Total Sales = SUM('Superstore'[Sales])`
* `Total Profit = SUM('Superstore'[Profit])`
* `Profit Margin % = DIVIDE([Total Profit], [Total Sales], 0)`
* `Sales LY = CALCULATE([Total Sales], SAMEPERIODLASTYEAR('Calendar'[Date]))`
* `YoY Sales Growth % = DIVIDE([Total Sales] - [Sales LY], [Sales LY])`

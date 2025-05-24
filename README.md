🚲 London Bike Sharing Dashboard
This project explores bike sharing patterns in London using a data model built in Power BI. It includes analysis of seasonal, temporal, and weather-related factors that influence ride frequency.

📊 Data Modeling
At the start of the project, relevant variables were identified and the data model schema was designed. The main dimensions included:

Season

Date

Holiday

Weather

These were supported by a fact table: F_BIKE_SHARING.

A star schema was chosen to optimize performance and simplify analysis, avoiding unnecessary columns in the fact table.

<p align="center"> <img width="562" alt="Model Scheme" src="https://github.com/user-attachments/assets/45a4afb0-b6f7-4153-95f7-8f1bc00a69e6" /> </p>
📆 Date Table Generation
A custom Power Query function using M code was developed to create a flexible and reusable date table. This function includes various time segments—weeks, start of week, months, start of month, etc.—to support flexible time slicing.

<p align="center"> <img width="960" alt="Date function" src="https://github.com/user-attachments/assets/20c747bb-76da-490f-87f1-3ff3f4e15652" /> </p>
The D_DATE table calls this function with two inputs:

Start Date

Number of Projection Years

<p align="center"> <img width="954" alt="DATE Table" src="https://github.com/user-attachments/assets/94faf7cf-c9a0-4f44-b5f2-b1853742d59f" /> </p>
📁 Other Dimensions and Fact Table
Other dimensions were created manually, as they consisted of limited predefined values.

<p align="center"> <img width="952" alt="Other Tables" src="https://github.com/user-attachments/assets/a6eb9ee7-411b-4dc2-8855-3ae4a1284444" /> </p>
The transactions table F_BIKE_SHARING required minimal preparation and was integrated directly into the model.

<p align="center"> <img width="942" alt="Transactions Table" src="https://github.com/user-attachments/assets/4022e1df-6c65-4eb0-bc5b-766121fc3df8" /> </p>
🎨 Report Design
The design and storytelling phase was planned using Figma. The layout was structured in two pages:

Page 1: Overview by month, season, and time of day

Page 2: Detailed patterns influenced by weather and temperature

<p align="center"> <img width="960" alt="Canvas" src="https://github.com/user-attachments/assets/4dbe26bd-70dc-4783-8232-da3b2b67e2de" /> </p>
🧮 Metrics
Simple metrics were created to support the analysis. The example below includes the calculation of Average Rides on Non-Holidays, which was displayed on a KPI card.

<p align="center"> <img width="934" alt="Metrics" src="https://github.com/user-attachments/assets/dfe88c80-f24b-46e2-b5d2-00817959e756" /> </p>
📄 Report Page 1 – General Overview
The first page of the report provides a high-level summary of bike sharing activity in London for 2015 and 2016. Key metrics include:

Average rides on holidays: 770

Average rides on non-holidays: 1,152

A line chart displays monthly trends, peaking during summer and dipping in winter.

A seasonal breakdown shows summer as the most active season, followed by fall, spring, and winter. Hourly patterns by season show strong commuting peaks at 8 AM and 5 PM, especially in warmer months.

These findings suggest bike sharing is mostly used for commuting during weekdays and in favorable weather.

<p align="center"> <img width="673" alt="London Bike Sharing Dashboard Page 1" src="https://github.com/user-attachments/assets/4b29597e-3b68-472a-9ca5-9c8aa8ff958a" /> </p>
📄 Report Page 2 – Time & Weather Analysis
This page analyzes how temperature and weather influence bike usage.

The scatter plot shows a strong positive correlation between temperature and bike rides, with usage increasing notably between 20°C and 30°C. Dot size represents humidity, which has a smaller effect.

The bar chart reveals that the most bike shares occur under:

Scattered clouds

Broken clouds

Clear skies

Rides decrease under rain, thunderstorms, and snow.

The heatmap shows weekday peaks at 8 AM and 5–6 PM, typical of commuting behavior. On weekends, usage is more evenly distributed, indicating leisure-oriented use.

Overall, the data shows bike sharing in London is influenced by both weather and daily routines, peaking under mild conditions and during weekday commute hours.

<p align="center"> <img width="673" alt="London Bike Sharing Dashboard Page 2" src="https://github.com/user-attachments/assets/7d78b651-259c-4a29-b99c-8f79f82de7ac" /> </p>

# London Bike Sharing Dashboard: 👉 [View Report](https://app.powerbi.com/view?r=eyJrIjoiOTExYzdmZjktZThlYS00OTU5LTgwZjEtZTJlYjUyOWMzMDQ4IiwidCI6ImY2OTI5MWY5LTNkYTctNDJiMy05ZjEwLWYyZWFlMjU3ZDVhYiIsImMiOjR9)

At the start of the project, the relevant variables were analyzed, and once identified, the model schema was planned. The key dimensions identified were: Season, Date, Holiday, and Weather, along with a transaction table. A star schema was chosen, with the aim of avoiding additional columns in the transaction table to keep the model optimized.

<p align="center">
<img width="562" alt="Model Scheme" src="https://github.com/user-attachments/assets/45a4afb0-b6f7-4153-95f7-8f1bc00a69e6" />
</p>

To begin, a custom function was created in Power Query using M code to generate the date table. This function included various temporal breakdowns—such as weeks, start of the week, months, start of the month, and other time-based segments—to enable flexible time slicing in the analysis.

<p align="center">
<img width="960" alt="Date function" src="https://github.com/user-attachments/assets/20c747bb-76da-490f-87f1-3ff3f4e15652" />
</p>

Then, the D_DATE table was created, with its source calling the custom function to generate all the columns. The function takes two inputs: the start date and the number of projected years.

<p align="center">
<img width="956" alt="Date Table" src="https://github.com/user-attachments/assets/35ce13c5-4c5b-434b-a012-e074a256fcdf" />
</p>

The other dimensions were created by manually specifying the values, as they involved only a limited set of entries.

<p align="center">
<img width="952" alt="Other Tables" src="https://github.com/user-attachments/assets/a6eb9ee7-411b-4dc2-8855-3ae4a1284444" />
</p>

Finally, the transactions table, F_BIKE_SHARING, required minimal preparation, as illustrated in the following figure.

<p align="center">
<img width="942" alt="Transactions Table" src="https://github.com/user-attachments/assets/4022e1df-6c65-4eb0-bc5b-766121fc3df8" />
</p>

Once the model was ready, the design phase began with layout planning in Figma. The canvas was structured using a clean grid to organize visual elements clearly. Space was divided into top and bottom sections, allowing for a natural flow from summary metrics to detailed visuals. Equal-sized panels ensured balance, while reserved areas for filters and charts supported future interactivity. This spatial planning aimed to keep the report intuitive and visually coherent from the start.

<p align="center">
<img width="956" alt="London Bike Sharing Dashboard Cavas" src="https://github.com/user-attachments/assets/9d5d3f2e-a3b9-48de-b2d6-c44a82b99be8" />
</p>

Simple metrics were created for the report. The following figure shows the metrics used, including the calculation of the Average Rides on Non-Holidays metric, which was displayed in a KPI card.

<p align="center">
<img width="934" alt="Metrics" src="https://github.com/user-attachments/assets/dfe88c80-f24b-46e2-b5d2-00817959e756" />
</p>

The first page of the report shows a general overview of bike sharing activity in London during 2015 and 2016. It includes key metrics such as the average number of rides on holidays (770) and non-holidays (1,152), along with a monthly trend line that highlights seasonal variations—peaking in the summer and decreasing during the winter months.  
A bar chart summarizes total rides by season, showing that summer had the highest usage, followed by fall, spring, and winter. Additionally, a line chart displays bike usage by hour and season, revealing typical commuting patterns with peaks around 8 AM and 5 PM, particularly during warmer seasons.  
These findings suggest that bike sharing in London is primarily used for daily commuting, especially on weekdays and during favorable weather, with significantly lower activity during holidays and winter months.

<p align="center">
<img width="673" alt="London Bike Sharing Dashboard Page 1" src="https://github.com/user-attachments/assets/4b29597e-3b68-472a-9ca5-9c8aa8ff958a" />
</p>

The second page of the report explores how weather and time affect bike usage in London. The scatter plot in the center shows a positive correlation between temperature and average bike shares—usage increases notably between 20°C and 30°C. Dot size reflects humidity, which appears to have a secondary effect. This suggests that warmer, less humid conditions encourage more riding.  
To the right, a bar chart highlights that bike usage is highest under “scattered clouds,” “broken clouds,” and “clear” weather, while conditions like rain, thunderstorms, and snow reduce activity significantly.  
At the bottom, a heatmap reveals time-based patterns. On weekdays, there are clear commuting peaks at 8 AM and 5–6 PM, especially midweek. On weekends, usage starts later and is spread more evenly throughout the day, reflecting more recreational use.  
Overall, the data indicates that bike sharing in London is strongly influenced by both temperature and time of day, with usage rising in mild weather and aligning closely with workweek routines.

<p align="center">
<img width="673" alt="London Bike Sharing Dashboard Page 2" src="https://github.com/user-attachments/assets/7d78b651-259c-4a29-b99c-8f79f82de7ac" />
</p>

In summary, this report presents a full analysis of London bike sharing data, starting from data modeling to dashboard planning. A star schema was created with well-structured dimension tables and a dynamic date function to support flexible time analysis. The dashboard layout was carefully planned in Figma, focusing on clear space organization to guide future visual storytelling. The project combines data preparation, model optimization, and design planning to explore how time, season, and weather influence bike usage in a meaningful and accessible way.

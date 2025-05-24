# London-Bike-Sharing-Dashboard
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
<img width="954" alt="DATE Table" src="https://github.com/user-attachments/assets/94faf7cf-c9a0-4f44-b5f2-b1853742d59f" />
</p>


<p align="center">
  <img src="https://github.com/user-attachments/assets/49132faa-af97-4f4c-a5f3-bcdd9b76c116" alt="Dashboard Preview">
</p>
<p align="center">
  <a href="https://app.powerbi.com/view?r=eyJrIjoiOTExYzdmZjktZThlYS00OTU5LTgwZjEtZTJlYjUyOWMzMDQ4IiwidCI6ImY2OTI5MWY5LTNkYTctNDJiMy05ZjEwLWYyZWFlMjU3ZDVhYiIsImMiOjR9">
    View Report
  </a>
</p>

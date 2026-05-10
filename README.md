# Churn and Retention Dashboard
An Excel dashboard for analyzing customer retention and churn using synthetic data. Built with Power Query, Power Pivot, and dynamic DAX measures.

## What is this project about?
The main goal of this project is to analyze customer churn and retention patterns through an interactive Excel dashboard. The dataset used for this analysis was synthetically generated using Gemini to safely practice relational data modeling and advanced DAX calculations.

## Tools & Tech Stack
* **Power Query (M Code):** I imported raw data from `.txt` files. To make the project easily reproducible, I created dynamic Power Query Parameters for the folder and file paths. By modifying the source code to run on parameters, any user can smoothly update the data source location without digging into the M code.

<img width="1070" height="190" alt="image" src="https://github.com/user-attachments/assets/1761cb19-47af-483d-b52f-01f084f5ae2d" />
(Changed data source code)
<br>
<br>
<img width="513" height="138" alt="image" src="https://github.com/user-attachments/assets/f93c5716-334c-4326-aaa5-243fd781cbd8" />
(Parameter for folder path)
<br>
<br>

* **Power Pivot (Data Modeling):** After loading the data, I built a relational Data Model . I connected fact tables with dimension tables and created a dynamic Date Table to enable time-intelligence calculations.
* **DAX Measures:** The core logic is powered by custom DAX measures (which you can review in the `measures.dax` file in this repository). I heavily utilized variables (`VAR`), `SWITCH`, `MAX`, and `DISTINCTCOUNT` to optimize calculations. 
* **Dynamic KPI Parameters:** The "Risk status" and "Risk status KPI" metrics are fully dynamic. They are driven by disconnected parameter tables in the spreadsheet, allowing the user to easily adjust the day thresholds for "Churn", "Win-back", and "Active" statuses without touching the underlying code.

<img width="933" height="350" alt="image" src="https://github.com/user-attachments/assets/4e7fac4b-d3b9-4865-9ef3-9b54ce741c50" />
(Mentioned tables having its performance in "Risk status KPI" and "Risk status" columns)
<br>
<br>

## How to use this dashboard?
To run this project locally, simply update the `FolderPath` parameter in the spreadsheet to point to the location where you downloaded this repository.

**Key Insights & Scenario Analysis:**
By playing with the slicers, you can quickly spot interesting trends. For instance, the analysis reveals that Electronic products generate the highest average customer income while maintaining a relatively low churn rate. This is a clear signal that the Sales and Marketing departments could collaborate on a targeted promotional campaign to boost retention in other, higher-risk product categories. 

This dashboard is designed to be a straightforward, interactive tool for data-driven decision-making.

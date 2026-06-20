#  Airline Operations and Passengers Analysis — Power BI Dashboard

##  Overview

This project is an interactive Power BI dashboard built on the same U.S. domestic flights dataset used in the [Airport SQL Analysis project](./airport_sql_project.sql). While the SQL project answers specific business questions through queries, this dashboard provides a visual, explorable view of airline route performance, passenger volume, and seasonal trends — allowing stakeholders to filter and drill into the data interactively rather than read static query results.


##  Dataset

Same source data as the SQL project — flight-level records including origin/destination airports and cities, passenger counts, seats, flights, distance, fly date, and airport coordinates. See the SQL project README for the full column reference.

##  Tools Used

- **Power BI Desktop** — data modeling and report design
- **Visual types used:** KPI cards, maps, column (bar) charts, line chart, area chart, slicers
- **Interactivity:** bookmarks + action buttons for view toggling

##  Dashboard Features

The report consists of a single page, **"Airline Operations And Passengers Analysis Report,"** combining the following elements:

| Visual | Description |
|---|---|
| **KPI Card** | Headline totals — Total Passengers, Total Flights, Total Distance |
| **Origin / Destination Map Toggle** | Two geographic maps (origin airport locations and destination airport locations, sized by passenger volume), switchable via **Origin** / **Destination** toggle buttons |
| **Top 5 Airports Chart Toggle** | Two bar charts (Top 5 Origin Airports and Top 5 Destination Airports by total passengers), linked to the same toggle |
| **Quarterly Flight Count** | Line chart showing flight volume by quarter, highlighting seasonal patterns |
| **Total Passengers by Year** | Area chart showing year-over-year passenger trend |
| **Slicers** | Filter panel for Origin City, Destination City, and Fly Date — enabling on-the-fly filtering of all visuals on the page |

The **Origin/Destination toggle** is built using Power BI bookmarks paired with action buttons, so the map and bar chart pair swap context (origin view ↔ destination view) without needing a second page — keeping the report compact while still letting users explore both directions of travel.

##  Key Insights

- The **Top 5 origin and destination airports** by passenger volume highlight the busiest hubs in the network, consistent with the SQL "flight frequency" and "passenger volume" analyses.
- The **geographic maps** make hub concentration and route geography immediately visible in a way tabular SQL output can't.
- The **quarterly and yearly trend charts** surface seasonal and year-over-year demand patterns at a glance, supporting the same seasonality and growth questions explored in the SQL project's window-function queries.
- The **slicers** allow a viewer to isolate any specific city or date range and see all visuals update together, making the dashboard useful for ad hoc exploration beyond the fixed SQL queries.

##  How to View

1. Install **Power BI Desktop** (free from Microsoft).
2. Open `airport_powerbi_dashboard.pbix`.
3. Use the slicers (Origin City, Destination City, Fly Date) to filter the report.
4. Use the **Origin / Destination** buttons to toggle the map and Top 5 chart between origin and destination views.

##  Related

This dashboard is a companion to the [Airport SQL Analysis project](./airport_sql_project.sql), which performs the deeper analytical work (seat utilization, underutilized routes, year-over-year growth percentages) that this report's visuals are built on top of.

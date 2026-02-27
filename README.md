**Sales and Returns Data Pipeline & Visualization Workflow**

This project implements a comprehensive data pipeline in KNIME that transforms raw Excel data into a structured dimensional model (Star Schema) and provides an interactive visualization dashboard for business insights.
+1



**🚀 Project Overview**
The workflow consists of two main components:


Creating Dimension Tables: Data cleaning, transformation, and schema modeling.


Visualization: Interactive dashboarding with various KPIs and performance metrics.

**🛠️ Data Pipeline (ETL)**
The pipeline filters raw data to create 10 specific Dimension Tables:

Customer, Product, Ship Mode, Segment, City, State, Postal Code, Region, Category, and Subcategory.

Key Transformation Steps:

Duplicate Removal: Ensures data integrity across all dimensions.


Unique ID Generation: Created using the Expression node (excluding existing IDs for Customer and Product).


Fact Table Creation: Derived by filtering the Excel reader, removing string names, and using the Category to Number node to establish foreign keys.


Inner Joins: Connects all dimension tables to the fact table for comprehensive reporting.

**📊 Dashboard & Visualizations**
The visualization component is divided into five specialized modules:

1. Revenue and Profit based on Time

Functionality: Extracts year and month from order dates.


Interactivity: Features a "Multiple Selection Widget" for year-specific filtering.


Display: Bar charts for monthly profit/revenue and table views for annual totals.

2. Revenue based on Region and Categories (with Sorting)

Functionality: Uses "Column Selection" and "Single Selection" widgets to allow users to choose grouping variables and sort results in ascending or descending order.


Display: Results are rendered in dynamic bar charts.

3. Top or Bottom 10 Performing City and Products

Functionality: Users can select specific columns to identify the top or bottom 10 performers (cities or products) based on custom choices.

4. Total Records of Everything (KPIs)

Functionality: Utilizes a Cross Joiner to aggregate all totals into a single table.


Display: Provides essential business KPIs through a consolidated table view.

5. Returns Based on Products, Region, or State

Functionality: Joins the fact table with returns data using Order IDs, followed by duplicate removal and column filtering.


Interactivity: Users can toggle between Product, Region, or State views.


Display: Aggregated return counts displayed in a Pie Chart.

⚙️ Requirements

KNIME Analytics Platform (Latest Version).


Input data: Excel source file containing Sales and Returns worksheets.

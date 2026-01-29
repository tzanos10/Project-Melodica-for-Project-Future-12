--Project Overview

This project implements a complete Data Engineering and Business Intelligence pipeline using the Chinook OLTP database.

--The architecture follows the flow:

OLTP → Staging → Data Warehouse → Power BI

The final Power BI report is named Melodica.

--Execution Order

1. Staging Layer

Run the staging script to create and load the MelodicaStaging database.

Raw copies of OLTP tables are created without complex joins.

2. Data Warehouse

Run the DW script to create and load the MelodicaDW database.

Dimension tables are loaded first, followed by the fact table (FactSales).

3. Power BI

Open the Melodica.pbix file.

The report connects directly to the ChinookDW database.

Data is analyzed using a star schema model.

--Notes

All transformations and joins are performed outside the OLTP system.

A design issue was identified with the initial DimDate implementation and was resolved by enriching it with additional date attributes.

The solution focuses on simplicity and clarity, as required by the project scope.

--Deliverables

SQL scripts (Staging, DW, ETL)

MelodicaDW database backup

Power BI report (Melodica.pbix)

Project report (.docx)

Presentation (.pptx)

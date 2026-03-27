# COVID-19 Data Analysis & Vaccination Tracking 🦠📊

## Overview
This project analyzes global COVID-19 data to derive insights on infection rates, mortality, and vaccination progress. Using SQL, the project explores patterns across countries, continents, and the United States specifically, helping understand the pandemic's impact on populations and effectiveness of vaccination efforts.

---

## 📋 Project Objectives
- Analyze COVID-19 total cases, new cases, and deaths globally.
- Calculate death probability for COVID-19 patients in the United States.
- Assess the percentage of population infected in different countries.
- Identify countries and continents with the highest infection and death rates.
- Track vaccination progress relative to population over time.
- Create reusable views and temporary tables for visualization and reporting.

---

## 🗄️ Data Sources
The project uses two primary datasets:

1. **CovidDeaths** – Contains daily records of COVID-19 cases and deaths across countries and continents.
   - Columns include: `location`, `date`, `total_cases`, `new_cases`, `total_deaths`, `population`, `continent` etc.

2. **CovidVaccinations** – Contains vaccination rollout data globally.
   - Columns include: `location`, `date`, `new_vaccinations`, `people_vaccinated` etc.

Both datasets are stored in the `PortfolioProject` SQL database.

---

## 💡 Key SQL Concepts Used
- **Filtering & Sorting** – Using `WHERE` and `ORDER BY` to refine datasets.
- **Aggregations** – `SUM()`, `MAX()` for population-level and country-level analysis.
- **Calculated Columns** – Compute death percentages, infection percentages, and vaccination coverage.
- **CTEs (Common Table Expressions)** – To organize rolling vaccination calculations.
- **Temporary Tables** – For intermediate calculations of vaccination percentages.
- **Views** – `PercentPopulationVaccinated` created for reusable reporting and visualizations.
- **Window Functions** – `SUM() OVER (PARTITION BY...)` to calculate cumulative vaccinations.

---

## 📊 Project Structure
- **SQL Scripts**
  - `CovidAnalysis.sql` – Core queries for deaths, cases, and population impact.

- **Database Objects**
  - Temporary Tables: `#PercentPopulationVaccinated`
  - Views: `PercentPopulationVaccinated` (for downstream visualizations)

---

## 🚀 How to Use
1. Load the `CovidDeaths` and `CovidVaccinations` datasets into your SQL Server database under the `PortfolioProject` schema.
2. Run the SQL scripts in order:
   - Analyze deaths and infection percentages.
   - Calculate vaccination progress using CTEs or temporary tables.
   - Create the view `PercentPopulationVaccinated` for reporting.
3. Connect the view to BI tools (Power BI, Tableau) for dashboards and visualizations.

---

## 🔧 Technologies & Tools
- SQL Server (T-SQL)
- Window Functions & CTEs
- Temporary Tables & Views
- Data Analysis & Aggregation
- Integration-ready for BI Tools (Power BI, Tableau)

---

## 📈 Insights Generated
- Identified countries with highest infection and death rates relative to population.
- Calculated death probability for COVID-19 patients in the US.
- Determined percentage of population vaccinated over time by country.
- Prepared datasets for real-time visual dashboards on infection and vaccination trends.

---

## 📫 Contact
- **LinkedIn:** [Aditya Chettipalli](https://www.linkedin.com/in/adityachettipalli/)  
- **GitHub:** [github.com/YOUR_GITHUB_USERNAME](https://github.com/aditya-chettipalli)

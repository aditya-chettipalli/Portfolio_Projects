# Nashville Housing Data Cleaning using SQL 🏡📊

## Overview
This project focuses on cleaning and transforming the Nashville Housing dataset using SQL.  
The goal is to prepare raw real estate data for analysis by handling missing values, standardizing formats, splitting columns, removing duplicates, and improving data quality.

This project demonstrates practical data cleaning techniques commonly used in real-world analytics workflows.

---

## 📌 Project Objectives
- Standardize date formats for consistency
- Populate missing property addresses
- Split address fields into structured columns
- Normalize categorical values
- Remove duplicate records
- Drop unused columns
- Prepare dataset for analysis and visualization

---

## 🗂 Dataset
**Dataset Used:** `NashvilleHousing`

### Key Columns
- ParcelID
- PropertyAddress
- SaleDate
- SalePrice
- OwnerAddress
- SoldAsVacant
- Acreage
- LandValue
- BuildingValue
- TotalValue
- Bedrooms
- FullBath
- HalfBath

---

## 🧹 Data Cleaning Steps

### 1. Standardized Date Format
- Converted `SaleDate` to SQL `DATE` format
- Created a new column `SaleDateConverted`
- Updated records to maintain consistent date formatting

---

### 2. Populate Missing Property Address
- Identified null `PropertyAddress` values
- Used self-join on `ParcelID` to populate missing addresses
- Ensured data consistency across duplicate parcels

---

### 3. Split Property Address into Columns
- Extracted:
  - Property Address
  - City
- Created:
  - `PropertySplitAddress`
  - `PropertySplitCity`

---

### 4. Split Owner Address into Columns
- Used `PARSENAME()` to separate:
  - Owner Address
  - Owner City
  - Owner State
- Created:
  - `OwnerSplitAddress`
  - `OwnerSplitCity`
  - `OwnerSplitState`

---

### 5. Standardized SoldAsVacant Values
- Converted:
  - 'Y' → 'Yes'
  - 'N' → 'No'
- Improved categorical consistency

---

### 6. Remove Duplicate Records
- Used `ROW_NUMBER()` with CTE
- Identified duplicates based on:
  - ParcelID
  - PropertyAddress
  - SalePrice
  - SaleDate
  - LegalReference
- Deleted duplicate rows while keeping original records

---

### 7. Drop Unused Columns
Removed unnecessary columns:
- OwnerAddress
- TaxDistrict
- PropertyAddress
- SaleDate

This improves dataset efficiency and readability.

---

## 🛠 SQL Concepts Used
- Data Type Conversion
- Self Joins
- CTE (Common Table Expressions)
- Window Functions (ROW_NUMBER)
- String Functions (SUBSTRING, PARSENAME, CHARINDEX)
- CASE Statements
- NULL Handling (ISNULL)
- ALTER TABLE
- UPDATE Statements
- Data Deduplication

---

## 📈 Data Cleaning Workflow
1. Inspect raw data
2. Standardize date formats
3. Handle missing values
4. Split composite columns
5. Normalize categorical data
6. Remove duplicates
7. Drop unnecessary columns
8. Prepare for downstream analysis

---

## 🎯 Outcome
- Clean and structured dataset ready for analysis
- Improved data consistency and usability
- Reduced redundancy
- Enhanced analytical performance
- Prepared dataset for BI tools (Power BI / Tableau)

---

## 🔧 Technologies Used
- SQL Server
- T-SQL
- Data Cleaning Techniques
- Data Transformation
- Window Functions

---

## 📊 Potential Use Cases
- Real estate price analysis
- Market trend dashboards
- Property valuation modeling
- Geographic housing analysis
- Investment decision support

---

## 📫 Contact
**Aditya Chettipalli**  
💼 LinkedIn: https://www.linkedin.com/in/adityachettipalli/  
🐙 GitHub: https://github.com/aditya-chettipalli

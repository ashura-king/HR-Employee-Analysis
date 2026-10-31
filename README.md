# HR Employee Analysis (Excel)

## Business question
Where are employees leaving, and why? Which departments and
groups should HR focus on to reduce attrition?

## Dataset
HR Data Set (HRDataset_v14) from Kaggle, created by
Dr. Carla Patalano and Dr. Rich Huebner. This is a synthetic
(fictional) dataset created for learning, so no real employees
are represented. Source: [link to the Kaggle page]

## What I cleaned
- Removed hidden spaces: Department (209 rows), Sex (135),
  Employee_Name (70), Position (1) using TRIM
- Split Employee_Name into Last_Name and First_Name
- Converted text dates to real dates (DOB, DateofHire,
  DateofTermination, LastPerformanceReview_Date)
- Confirmed no duplicate employee IDs
- Kept the original sheet untouched as Raw Data

## What I added
- Age and Tenure_year, calculated as of 28 Feb 2019 (the end of the
  dataset's period) so results don't change with today's date
- Age_group (IF) and Salary_Band (XLOOKUP with a lookup table)

## Validation
15 automated checks on the Checks sheet: row counts, hidden spaces,
real dates, status vs. termination date, lookup errors. All pass.

## Key findings
1. Production has the highest attrition among the larger departments
   (39.7% vs. 33.4% overall) and accounts for 83 of the 104 departures.
2. Another position, unhappiness, and more money are the top reasons
   people leave (45 of 104).
3. Average pay differs between women (67,787) and men (70,629), but
   this does not account for job level.

## Notes
- Executive Office has one employee (0% attrition, 250,000 salary),
  so it is not a trend.
- KPI cards are company-wide and don't respond to slicers.

## Tools and skills
Excel Tables, TRIM, Text to Columns, DATEDIF, IF, XLOOKUP, COUNTIFS,
AVERAGEIFS, PivotTables, PivotCharts, slicers

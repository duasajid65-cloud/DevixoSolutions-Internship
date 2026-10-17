# Task 02 - Data Cleaning and Feature Engineering

Devixo Solutions - Data Science Internship | Dua Sajid

## About
This task turns the raw Sample Superstore sales data (9,994 records, 21 columns) into a clean, analysis-ready dataset of 9,993 rows. It also creates 8 new features and a reusable Scikit-learn preprocessing pipeline.

## What was done
- Checked and handled missing values (none found)
- Removed duplicate records (1 found and removed; it was identical except for Row ID)
- Capped outliers in Sales, Quantity and Profit at 1.5 x IQR
- Converted data types (dates to datetime, Postal Code to 5-digit text)
- Created 8 new features: Order Year, Order Month, Order Quarter, Order Weekday, Shipping Days, Profit Status, Profit Margin, Unit Price
- One-hot encoded Category, Segment, Region and Ship Mode
- Standardized Sales, Quantity, Discount and Profit
- Compared descriptive statistics before and after preprocessing
- Built a Scikit-learn Pipeline and ColumnTransformer (bonus)

## Files
| File | Description |
|------|-------------|
| `superstore_notebook.ipynb` | Full notebook with code, explanations and statistics |
| `Task02_Documentation.pdf` | Short report explaining each step |
| `superstore.csv` | Raw dataset (9,994 rows, 21 columns) |
| `cleaned_superstore.csv` | Final cleaned dataset (9,993 rows, 37 columns) |
| `requirements.txt` | Python libraries needed |

## How to run
1. Install the libraries: `pip install -r requirements.txt`
2. Keep `superstore.csv` in the same folder as the notebook.
3. Open `superstore_notebook.ipynb` and run all cells from top to bottom.
4. The cleaned data is saved as `cleaned_superstore.csv`.

## Notes
- The Scikit-learn pipeline is a separate modelling example fitted on the raw file, so its row counts differ by one from the cleaned CSV.
- When opening `cleaned_superstore.csv`, read Postal Code as text (`dtype={"Postal Code": str}` in pandas). Excel will drop the leading zeros on display.
- Profit Margin and Profit Status are derived from Profit, so drop them if Profit is the modelling target.

## Tools
Python, Pandas, NumPy, Matplotlib, Scikit-learn

Data-extraction-Introduction
ID: 672515
This Python script creates a small random sales dataset for learning and testing with pandas or SQLite.
It simulates daily transactions for 10 customers over 61 days (April–May 2025) and saves them to a CSV file.

# What it does

Imports standard data libraries (pandas, numpy, matplotlib, sqlite3, seaborn, datetime, random).

Generates 3–6 random sales per day.
Each sale includes:

id – random 4-digit number

customer – randomly chosen name

date – day of transaction

amount – value between 100 and 2000

Last_updated – random time on that date

Saves all rows to sales_data.csv (≈ 183–366 rows).

Reads the file back and shows a preview with head().

# Output

**sales_data.csv** with columns:
id, customer, date, amount, Last_updated.

# Requirements

Python 3.9+ with:

pip install pandas numpy matplotlib seaborn

# How to run

From file:

python generate_sales.py


From notebook:

import pandas as pd
df = pd.read_csv("sales_data.csv", parse_dates=["Last_updated"])
df.head()

# Notes

Optional reproducibility:

import random; random.seed(42)


IDs may repeat since they’re randomly generated.

Last_updated is parsed as a datetime colum

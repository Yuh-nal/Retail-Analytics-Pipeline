# Retail Sales Pipeline

A small Python program that reads a file of store sales, removes the bad
rows, and prints a sales report.

## What you need

- Python 3.10 or newer
- No extra packages

## How to run it

1. Open a terminal in this project folder.
2. (Optional) Create and turn on a virtual environment:

   ```console
   python3 -m venv .venv
   source .venv/bin/activate
   ```

   On Windows, use `.venv\Scripts\activate` instead of the second line.

3. Run the program:

   ```console
   python3 main.py
   ```

The program reads `data/sales.csv` and prints the report.

## How to run the tests

```console
python3 -m unittest
```

## Files

```text
main.py               Starts the program
requirements.txt      List of packages needed (none)
data/sales.csv        Sample sales data
pipeline/schema.py    TransactionRecord class (one sale)
pipeline/validator.py Checks and cleans each row
pipeline/transformer.py  Filters sales and calculates tax and margins
pipeline/reporter.py  SalesReport class (totals and printing)
tests/test_pipeline.py   Unit tests
```

## Using your own data

Replace `data/sales.csv` with your own file. It must have these columns:

`transaction_id, branch_id, date, region, customer_tier, items, revenue,
cost, status`

- `date` must look like `2026-03-01`
- `region` must be North, South, East or West
- `customer_tier` must be Bronze, Silver or Gold
- `status` must be active or refunded

# Supermarket Sales Data Cleaning & Preparation

## Project overview
This project demonstrates data cleaning and preparation using the supplied supermarket sales dataset (`SuperMarket Analysis.csv`). It is suitable for a beginner Data Analyst portfolio.

## Dataset
- Input file: `data/SuperMarket_Analysis_Raw.csv`
- Cleaned output: `data/SuperMarket_Analysis_Cleaned.csv`
- Original size: 1,000 rows × 17 columns

## Tools
- Python
- pandas
- NumPy
- Jupyter Notebook / Google Colab
- GitHub

## Data quality checks and changes
1. Checked all columns for missing values.
2. Checked for exact duplicate rows.
3. Trimmed leading/trailing whitespace in text fields.
4. Parsed mixed date strings into dates and exported them as `YYYY-MM-DD`.
5. Standardized time values to 24-hour `HH:MM:SS`.
6. Converted numeric fields to numeric data types.
7. Validated the sales calculation (`Unit price × Quantity × 1.05`), tax calculation (`cogs × 5%`) and gross income against tax.

## Results
- Original rows: 1,000
- Original columns: 17
- Missing cells in original file: 0
- Exact duplicate rows in original file: 0
- Rows removed: 0
- Invalid dates after parsing: 0
- Invalid times after parsing: 0
- Sales formula mismatches: 0
- Tax formula mismatches: 0
- Gross income vs. tax mismatches: 0
- Final rows: 1,000
- Final missing cells: 0

## Notes on decisions
No rows were deleted because no exact duplicates were found. The date column contained mixed string formats and was normalized. Category labels were inspected and no inconsistent category variants were found in the supplied data. No valid transactions were removed based on assumptions. In other datasets, negative quantities or unusual values should be investigated rather than automatically deleted.

## How to run
1. Open `notebook/data_cleaning.ipynb` in Jupyter Notebook or upload it to Google Colab.
2. Keep the raw CSV in the relative location `data/SuperMarket_Analysis_Raw.csv`, or update `input_path` in the notebook if you upload files separately.
3. Run the cells from top to bottom.
4. The notebook exports `data/SuperMarket_Analysis_Cleaned.csv`.

## Repository structure
```text
SuperMarket_Data_Cleaning_Task1/
├── data/
│   ├── SuperMarket_Analysis_Raw.csv
│   └── SuperMarket_Analysis_Cleaned.csv
├── notebook/
│   └── data_cleaning.ipynb
└── README.md
```

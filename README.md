Extract Tables from PDF and Save as Excel Files 

Overview
This project provides a Python script to extract tables from a PDF file and save them as separate Excel files. The script utilizes pdfplumber for table extraction and pandas for data processing.

Features
Extracts tables from each page of a PDF.
Converts extracted tables into Pandas DataFrames.
Saves each table as a separate Excel file.
Handles multiple tables across different pages.

Code Explanation
Open the PDF: Uses pdfplumber.open() to access the file.
Extract tables: Iterates through each page and extracts tables using page.extract_tables().
Convert to DataFrame: Each extracted table is converted to a Pandas DataFrame.
Save as Excel: The DataFrame is saved as an Excel file using to_excel().
Print Confirmation: Displays the filename of each saved table.
Output: Extracted tables will be saved as table_1.xlsx, table_2.xlsx, etc., in the same directory.

Alternative Methods
Camelot: pip install camelot-py
Tabula: pip install tabula-py (Requires Java)

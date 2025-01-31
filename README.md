# MARKET-ANALYSIS-REPORT
pip install pdfplumber pandas openpyxl


import pdfplumber
import pandas as pd

pdf_path= "/content/stock_market_dataset.pdf"

with pdfplumber.open(pdf_path) as pdf:
    table_count= 1
    for i,page in enumerate(pdf.pages):
        tables= page.extract_tables()
        for table in tables:
            df= pd.DataFrame(table)
            excel_filename= f"table_{table_count}.xlsx"
            df.to_excel(excel_filename,index= False,header= False)
            print(f"Saved:{excel_filename}")
            table_count+= 1

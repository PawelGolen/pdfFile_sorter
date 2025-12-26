# PDF Page Count Filter

## Overview
This script automates verification of PDF files based on the number of pages.  
PDF files that **do NOT match** the specified page count are automatically moved to a separate folder.

This is useful for:
- Document validation
- Batch quality checks
- Pre-processing documents before further automation or ETL workflows

## Features
- Scans all PDF files in a selected directory
- Checks number of pages using PyPDF2
- Moves invalid PDFs to another directory
- Automatically creates destination folder if missing

## Requirements
- Python 3.x
- PyPDF2

Install dependency:
```bash
pip install PyPDF2
```

## How It Works
1. User provides:
   - Source folder with PDFs
   - Destination folder for invalid PDFs
   - Expected page count
2. Script iterates through all PDF files
3. PDFs with a different number of pages are moved

## Usage
Run the script:
```bash
python pdf_page_filter.py
```

Example input:
```
Please enter the path to the folder containing PDF files to verify:
C:/documents/source

Please enter the path to the folder where you want to store PDF files with the selected number of pages:
C:/documents/invalid

Please enter the number of pages the PDF files should have:
2
```

## Output
- PDFs with incorrect page count are moved
- Correct PDFs remain untouched
- Console prints: `Done!`

## Use Cases
- Invoice validation
- Contract checks
- Document compliance automation
- Pre-ETL data cleansing

## Notes
- Script assumes all files in source folder are PDFs
- Files are moved (not copied)

## Author
Paweł Goleń

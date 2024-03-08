# Document-Reader

## Overview
Document-Reader is a Python project showcasing my skills in extracting data from insurance documents using the pdfplumber library. The primary focus is on processing "declarations pages" from a folder of insurance documents. The script extracts key information and organizes it into a structured Pandas DataFrame.

## Key Features
- **Text Extraction**: Utilizes pdfplumber to extract text from specific areas on the document.
- **Data Organization**: Parses extracted data and structures it into a Pandas DataFrame.
- **CSV Export**: Exports the DataFrame to a CSV file, with the ability to update an existing CSV file based on policy numbers.

## Usage
1. **Run the Script**: Execute the script by running the `main()` function.
2. **Input Directory**: Specify the directory containing insurance documents in the `flood_directory` variable.
3. **Data Extraction**: The script identifies the "declarations page" and extracts relevant information, such as policy details, insured parties, dates, insurer, and premium information.
4. **CSV Export**: The data is exported to a CSV file named `dir_data.csv`. If the file already exists, it updates existing records based on policy numbers.

## Code Walkthrough
- The code defines a function `extract_dir(dir_path)` that processes a directory of insurance documents, extracting information from the "declarations page."
- Bounding boxes are defined for different sections on the page, and pdfplumber is used to extract text within these regions.
- Extracted text is parsed to obtain policy details, insured parties, dates, insurer, and premium information.
- The script supports both individual and business names as insured parties.
- Extracted data is organized into a Pandas DataFrame, and a function `to_csv(df)` exports it to a CSV file.

## Example Data Columns
- **policy-number**: Policy number
- **primary-insured**: Primary insured party
- **secondary-insured**: Secondary insured party (if applicable)
- **mailing-address**: Mailing address
- **transaction-type**: Type of transaction (e.g., New Business)
- **insurer**: Insurance provider
- **effective-date**: Policy effective date
- **expiration-date**: Policy expiration date
- **premium**: Total annual premium
- **policy-fee**: Policy fee
- **sl-tax**: Surplus lines tax
- **stamping-fee**: Stamping fee
- **total-premium**: Total policy charges

## Notes
- This project serves as a demonstration of Python skills in data extraction and manipulation.
- The script assumes a specific format for the "declarations page" and may require adjustments for different document layouts.

Feel free to reach out for any further clarifications or information.
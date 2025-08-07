# Extract ITEM 1. to ITEM 1A. from SEC.gov Filings

This project automates the process of extracting the **"Item 1. Business"** section up to **"Item 1A. Risk Factors"** from 10-K filings downloaded from [SEC.gov](https://www.sec.gov/), for multiple symbols.

---

## 📦 Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone https://github.com/your-username/extract-sec-item1.git
   cd extract-sec-item1
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   pip install -r requirements.txt
   
🚀 Workflow
Step 1: Download Latest Filings
Run the following script to fetch the latest 10-K filings and download the corresponding .htm or .txt files for each company symbol:

python filings_link_extraction.py

This will create a downloads/ folder.

Each symbol will have its own subfolder containing its latest filing.

Step 2: Extract ITEM 1 to ITEM 1A Content
Once the files are downloaded, extract the content using:

python extract_content_htm_in_csv.py

This script scans all downloaded files.

It extracts content between "Item 1. Business" (or "Item 1. Description of Business") and "Item 1A. Risk Factors".

Extracted content is saved to final_updated_with_item1.csv.


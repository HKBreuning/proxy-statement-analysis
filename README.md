# proxy-statement-analysis

1. Proceed with the installation of the necessary libraries.
The necessary libraries are installed through pip and apt-get. The libraries in question are essential for performing OCR, processing PDFs, conducting NLP tasks, and implementing question answering with a BERT model.

2. Import the Necessary Modules
The necessary modules have been imported, and Google Drive has been mounted to facilitate access to the proxy statement PDFs.

3. Initialise the BERT Model for the purpose of Question Answering
The BERT model utilised for question answering is instantiated through the transformers library.

4. Method for Determining the Total Page Count in a PDF Document
The get_pdf_page_count function employs the PyPDF2 library to determine the total number of pages present in a PDF file.

5. Method for Identifying Pages with Relevant Keywords
The find_relevant_pages function systematically identifies pages that contain pertinent keywords associated with board information.

6. Function for Optical Character Recognition to Extract Text from the Relevant Pages
The extract_text_from_pdf function employs the pdf2image and pytesseract libraries to conduct OCR on the pertinent pages and retrieve the text.

7. Function for Extracting Entities in NLP
The extract_information function employs the spacy library to identify and extract entities, including the names of board members, from the text.

8. Method for Extracting Age, Tenure, and Gender Utilising the BERT Model
The extract_age_tenure_gender function employs the BERT model to systematically extract age, tenure, and gender information for each board member through targeted enquiries.

9. Method for Extracting Company and Year from the Text
The extract_company_and_year function utilises regular expressions to identify and retrieve the company name and year from the provided text.

10. Primary Function for Analysing Proxy Statement
The process_proxy_statement function serves as the primary mechanism for handling the proxy statement, utilising the aforementioned functions to extract necessary information and organise it within a DataFrame.

11. Execute the processing of all PDF files located in the Proxy_Statements folder in systematic batches.
The code systematically processes all PDF files located in the Proxy_Statements folder in batches, thereby optimising memory usage.

12. Integrate All DataFrames
The DataFrames are merged, and the resulting DataFrame is exported as a CSV file.

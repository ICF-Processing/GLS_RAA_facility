# GLS | RAA facility data
## Data preparation guide
### Step #1: Manual word processing
* PDF of the National Mental Health Facilities data is converted to Word
* The raw converted word document is subsetted by state and into individual paragraphs where each paragraph (2 line breaks) consist of indivual facilities' name, address, contact information and services offered, with the information being separated by single line breaks
  * 1st line contains name of respective facilities
  * 2nd, 3rd and 4th line include their address
  * 5th line contains respective phone numbers
  * service offering variables separated by "?" delimiters that starts after 2 line breaks subsequently
* Follow this guide to structure the texts containing information for each facility and save each Word document by state, which will then be converted back to PDFs for NLP via Python
### Step #2: Natural Language Processing (NLP)
* Upload cleaned PDF onto this repo under folder "Raw_PDF"
* Import relevant PDF into Python for NLP
* Run existing NLP code for each state or each PDF document that needs to be processed to tabulate and download final output as csv. This process is repeated for each new cleaned text files that becomes available.
* There should be 2 NLP output for each state- 1 for values that can be processed immediately and 1 for rows with missing values that are isolated, which needs to be cleaned in more detail, cross referencing raw PDFs
* Upload the new saved NLP code into this repo under folder "NLP" with today's date at the beginning of file name (e.g. 01312024_facility_NLP.ipynb)
* Upload NLP output produced into this repo under folder "NLP output"
### Step #3: Processing NLP output and maintaining workbook
* Place all NLP output (for both values and missing) in a single excel workbook and clean as needed
* Compile all values for all states in the sheet "Values Compilation"
* All rows with missing content to be further processed in detail and compiled in the sheet "Missing Compilation" for all states
* "Values Compilation" and "Missing Compilation" to be rbind later for data analysis in conjunction with other cleaned pieces
* Updated workbook to be uploaded into this repo under folder "Final"

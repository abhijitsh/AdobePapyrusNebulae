# Adobe_PDF_Extractor_Project
This project uses PDF Extract API by Adobe to read transaction bills given in .pdf format and store the extracted data in a .csv format.


# How to use it?

1: Install dependencies by running the following commands:
npm install @adobe/pdfservices-node-sdk;   
npm install adm-zip

2: Input the Test Data path location and the extracted zip files path location inside extract.js as the values of constants- Input and Zip_File, respectively. This algorithm would extract data from the PDFs into zip files and store them in the assigned path location as zip files.

3: InvoiceFormat.js contains the code for filtering the fields from the object array of all PDFs. It traverses over the respective object of each PDF and filters out the fields based on their order in the Object.

4: csvcreate.js contains the modules to create the CSV File. This file uses csv-writer and  has the detail about the columns Titles in the CSV File, and done!

# Files structure

TestDataSet contains all the test data in .pdf format.

ResultZipSet contains folders which contain all the .zip files obtained by extracting data from the test data using Adobe PDF Extract API.

ResultJSONSet contains all the .json files obtained by unzipping data from ResultZipSet.

The folder FinalData contain the master file- FinalData.csv which consists of all the extracted information from pdf in csv file format.

PS: The input and output file locations have been added such that all the data will be in the master folder. Feel free to change the locations as per your convenience. If some PDFs have already been extracted and if you run the code again, the extracted zip files will be deleted and new zip files will be created.



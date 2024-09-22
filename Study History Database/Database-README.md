# Study History Database

## Purpose and Rationale
The overall purpose of developing a study history database was to have an ordered, standardized collection of data related to previous research studies that would be searchable for future reports. 

## Overall Design Process
### Software
MS Access 2016

### Design Steps
1. Created initial dimension tables
2. Created fact tables with relationships to dimension tables
3. Tested entry on the form tables
4. Created subform for each tab
5. Created main form for data entry
6. Tested forms and revised as needed
7. Added embedded datasheet for additional information tabs
8. Tested forms and revised as needed
9. Entered information

## Database Schema
This database followed a simple star schema, with the main fact table called "Study Info." Three additional fact tables were tied to the Study Info table, but were linked as datasheets, as multiple records could be entered into each table. These datasheets were the Monitoring Visits, IRB Submissions, Study Contacts, and Tasks. 

![The relationship of the tables in the database are displayed in this image. The main fact table is titled "Study_Info", with related dimension tables Sponsor Info, Funding, Principal Investigator, IRB, Status, Focus, Reproductive Conditions, and Other Conditions.](https://github.com/liv4data/clinical_studies/blob/6f315887c3aedb49585a8937e70ef9cb486f7e80/Study%20History%20Database/relationships-in-database.png)

You can view the tables used in the database [here.](https://github.com/liv4data/clinical_studies/blob/6f315887c3aedb49585a8937e70ef9cb486f7e80/Study%20History%20Database/tables-used-in-database.md) 

## Preview Blank Database
You can view a blank preview of the study database [here.](https://github.com/liv4data/clinical_studies/blob/6f315887c3aedb49585a8937e70ef9cb486f7e80/Study%20History%20Database/preview-of-database.pdf) (_Please note: the pdf will open in the current browser window_)

## Next Steps
As this is an ongoing work-in-progress, the database itself is not complete. Due to staffing knowledge, it is not efficient to continue developing and maintaining the database through Microsoft Access. The next step is to create the database via REDCap, as staff members are familiar with the data entry steps there. 

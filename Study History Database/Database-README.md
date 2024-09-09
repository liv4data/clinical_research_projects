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

![The relationship of the tables in the database are displayed in this image. The main fact table is titled "Study_Info", with related dimension tables Sponsor Info, Funding, Principal Investigator, IRB, Status, Focus, Reproductive Conditions, and Other Conditions.](https://github.com/liv4data/clinical_studies/blob/25443886fed986ed5245fc797d7c91b857436697/DB%20Relationships.png)

You can view the tables used in the database here. 

## Preview Blank Database
You can view a blank preview of the study database [here.](https://github.com/liv4data/clinical_studies/blob/25443886fed986ed5245fc797d7c91b857436697/Study%20History%20DB%20-%20slides.pdf) (_Please note: the pdf will open in the current browser window_)

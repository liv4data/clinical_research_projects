# Study History Database Tables

## Single-Selection Dimension Tables
When the fact tables referenced any of the tables listed in this section, only one value could be selected. 

### CROs/Monitor Companies
| Field | Data Type |
| --- | --- |
| ID | AutoNumber |
| Organization Name | Short Text |

### Funding
| Field | Data Type |
|---|---|
|ID|AutoNumber|
|Funder Type| Short Text|

### IRB
| Field | Data Type |
|---|---|
|ID|AutoNumber|

### Principal Investigator
| Field | Data Type |
|---|---|
|ID|AutoNumber|
|Last Name|Short Text|
|First Name| Short Text|
|Credential|Short Text|

### Sponsor Info
| Field | Data Type |
|---|---|
|ID|AutoNumber|
|Sponsor Name|Short Text|
|Sponsor Abbreviation|Short Text|

### Status
| Field | Data Type |
|---|---|
|ID|AutoNumber|
|Status|Short Text|
|Status Description|Short Text|

## Multiple-Selection Dimension Tables
When the fact tables referenced any of the tables listed in this section, multiple values could be selected. 

### Focus
| Field | Data Type |
|---|---|
|ID|AutoNumber|
|Focus|Short Text|

### Reproductive Conditions
| Field | Data Type |
|---|---|
|ID|AutoNumber|
|Reproductive Condition|Short Text|

### Other Conditions
| Field | Data Type |
|---|---|
|ID|AutoNumber|
|Other Condition|Short Text|

## Fact Tables
### Study Info
| Field | Data Type | Description |Lookup Code|
|---|---|---|----|
|DB Protocol ID|AutoNumber|Database-assigned record number|N/A|
|Protocol ID|Short Text|Sponsor provided protocol ID for the study|N/A|
|Protocol Title|Long Text|Full protocol title of study provided by sponsor|N/A|
|CRC Nickname|Short Text|Shortened version of study name used for identification at the CRC|N/A|
|Study Name|Long Text|Additional short name for the study if sponsor provided one|N/A|
|Status|Number|Current Status of Study |SELECT [Status].[Status_ID], [Status].[Status] FROM Status ORDER BY [Status_ID];|
|Sponsor|Number|Sponsor of Study|SELECT [Sponsor Info].[Sponsor ID], [Sponsor Info].[Sponsor Name] FROM [Sponsor Info] ORDER BY [Sponsor Name];|
|Funding|Number|Type of funding used for the study|SELECT [Funding].[ID], [Funding].[Funder Type] FROM Funding ORDER BY [Funder Type];|
|Grant #|Short Text|Institution-assigned grant number for the study|N/A|
|PI|Number|Site Principal Investigator of the study|SELECT [Principal Investigator].[ID], [Principal Investigator].[Last Name] FROM [Principal Investigator] ORDER BY [Last Name];|
|IRB|Number|IRB of record for the study|SELECT [IRB].[ID], [IRB].[IRB Name] FROM IRB ORDER BY [IRB Name];|
|IRB Number|Short Text|Identification number for the study assigned by the IRB|N/A|
|Notes|Long Text|Additional Notes about the study|N/A|
|Goal|Number|Number of subjects expected to complete study|N/A|
|Screened|Number|Number of subjects who signed consent and screened for the study|N/A|
|SF|Number|Number of consented subjects who did not meet eligibility requirements|N/A|
|Enrolled|Number|Number of subjects who met eligibility criteria and enrolled in study|N/A|
|DC|Number|Number of subjects who left study prior to completion|N/A|
LTFU|Number|Number of subjects who could not be contacted after enrollment, deemed "lost to follow up"|N/A|
Completed|Number|Number of subjects who completed all study requirements|N/A|
Enrollment notes|Long Text|Additional notes discussing screening and enrollment statistics|N/A|
IRB Approval|Date/Time|Date IRB approved study|N/A|
SIV|Date/Time|Date of Site Initiation Visit|N/A|
Activation|Date/Time|Date sponsor activated site to begin study activities|N/A|
Enrollment Closed|Date/Time|Date sponsor ceased enrollment for study|N/A|
COV|Date/Time|Date of closeout visit|N/A|
IRB Termination|Date/Time|Date IRB acknowledged study closure|N/A|
Study Phase|Short Text|FDA-defined phase of clinical trial|"Pilot"; 1; 2; "2B"; 3; 4; "N/A"|
Study Endpoints|Short Text|Endpoints defined by study protocol|"Safety"; "Bleeding Patterns"; "Pain"; "PK"; "PD"; "No pregnancy"; "Ovulation"; "Treatment of condition"; "Microbiota"; "Sperm Count"|
Samples|Short Text|Samples collected for the study|"Biopsies"; "CVF"; "RF"; "Hormones"; "Cervical mucus"; "Semen"|
Procedures|Short Text|Procedures performed during the study|"Acceptability"; "DXA"; "Colposcopy"; "IDI"; "Mammogram"; "MRI"; "Partner required"; "PCT"; "Pelvic Floor Imaging"; "TVUS"|
Placebo?|Yes/No|Was a placebo used in the study?|N/A|
Product Type|Short Text|Product type used in the study|"Capsule"; "Condom"; "Cream"; "Emergency"; "Film"; "Gel"; "Implant"; "Injection”; "Insert"; "IUD"; "IUS"; "Patch"; "Permanent"; "Pill"; "Ring"; "Tablet"|
Product Route|Short Text|Route of product used in the study|"Intramuscular"; "Intrauterine"; "Oral"; "Subcutaneous"; "Subdermal"; "Topical"; "Transdermal"; "Vaginal"|
Hormonal Product?|Yes/No|Was a hormonal product used in the study?|N/A|
Additional Study Notes|Long Text|Additional notes about study protocol|N/A|
Investigational Product|Short Text|Name of investigational product used in study|N/A|
IND Study?|Yes/No|Was the study associated with an FDA Investigative New Drug?|N/A|
IND Number|Short Text|What was the IND number for the product?|N/A|
Focus|Number|What was the overall focus of the study?|SELECT [Focus].[ID], [Focus].[Focus] FROM Focus ORDER BY [Focus];|
Reproductive Condition(s)|Number|Reproductive condition(s) associated with the study|SELECT [Reproductive Conditions].[ID], [Reproductive Conditions].[Reproductive Condition] FROM [Reproductive Conditions] ORDER BY [Reproductive Condition];|
Other condition(s)|Number|Other conditions (non-reproductive) associated with the study|SELECT [Other Conditions].[ID], [Other Conditions].[Other Condition] FROM [Other Conditions] ORDER BY [Other Condition];|
IDE Study?|Yes/No|Was the study associated with an FDA Investigational Device Exemption?|N/A|
IDE Number|Short Text|What was the IDE number for the study?|N/A|
NCT Number|Short Text|What was the NCT number for the study?|N/A|

### Study Monitors
| Field | Data Type | Description |Lookup Code|
|---|---|---|----|
|ID|AutoNumber|
|Monitor Name|Short Text|First and last name of study monitor|
|Credentials|Short Text|Study monitor's credentials|
|Title|Short Text|Study monitor's title|
|Company|Number|Study monitor's organization|SELECT [CROs/Monitor Companies].[ID], [CROs/Monitor Companies].[Organization Name] FROM [CROs/Monitor Companies] ORDER BY [Organization Name];|
|Phone Number|Short Text|Study monitor's phone number|
|Email Address|Short Text|Study monitor's email address|
|Notes|Short Text|Any notes about monitor (e.g. if they changed companies)|

## Datasheets
These tables were enabled as datasheets on the study forms, so that multiple facts could be entered. Each table was linked to the Study Info table by the Protocol ID.

### IRB Submissions
|Field|Data Type|Lookup Code|
|---|---|---|
|ID|AutoNumber|
|Protocol ID|Number|SELECT [Study_Info].[DB Protocol ID], [Study_Info].[Protocol ID] FROM Study_Info ORDER BY [Protocol ID];|
|Submission Type|Short Text|"Initial Submission"; "Continuing Review"; "Protocol Amendment"; "Modification"; "Recruitment or Advertising"; "Subject-Facing Materials"; "Miscellaneous"; "Termination"|
Submitter|Short Text|"Site";"Sponsor or CRO"|
Date Submitted|Date/Time|
Date Approved|Date/Time|
Date Notified|Date/Time|
Notes|Long Text|

### Monitoring Visits
|Field|Data Type|Lookup Code|
|---|---|---|
|ID|AutoNumber|
|Protocol ID|Number|SELECT [Study_Info].[DB Protocol ID], [Study_Info].[Protocol ID] FROM Study_Info ORDER BY [Protocol ID];|
|Visit Name|Short Text	
Visit Date|Date/Time	
Monitor Name|Number|SELECT [Study Monitors].[ID], [Study Monitors].[Monitor Name] FROM [Study Monitors] ORDER BY [Monitor Name];
Confirmation Date|Date/Time	
Follow Up Date|Date/Time	
Notes|Long Text	

### Study Contacts
|Field|Data Type|Lookup Code|
|---|---|---|
|ID|AutoNumber|
|Protocol ID|Number|SELECT [Study_Info].[DB Protocol ID], [Study_Info].[Protocol ID] FROM Study_Info ORDER BY [Protocol ID];|
|Full Name|Short Text
|Company|Short Text|
Credentials|Short Text
Title|Short Text
Phone #|Short Test
Email|Short Text
Notes|Short Text

### Tasks
|Field|Data Type|Lookup Code|
|---|---|---|
|ID|AutoNumber|
|Protocol ID|Number|SELECT [Study_Info].[DB Protocol ID], [Study_Info].[Protocol ID] FROM Study_Info ORDER BY [Protocol ID];|
Task Type|Short Text|"Startup"; "Regulatory"; "Study Conduct"; "Recruiting"; "Correspondence"; "Institution"; "Other"
Task Date|Date/Time	
Comments|Long Text|

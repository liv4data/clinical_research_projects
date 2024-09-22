# Recruitment Report DAX
## About
Power BI utilizes Data Analysis Expressions (DAX) in its queries and calculations that are then used in data visualizations. The DAX expressions used in the recruitment report are listed below. 

## Measures
### Status
```
Active = COUNTROWS(FILTER(Contacts, Contacts[Status]="Active"))
Closed = COUNTROWS(FILTER(Contacts, Contacts[Status]="CLOSED"))
Completed = COUNTROWS(FILTER(Contacts, Contacts[Status]="Done"))
DC = COUNTROWS(FILTER(Contacts, Contacts[Status]="DC"))
DNQ = COUNTROWS(FILTER(Contacts, Contacts[Status]="DNQ"))
LTFU = COUNTROWS(FILTER(Contacts, Contacts[Status]="LTFU"))
NLI = COUNTROWS(FILTER(Contacts, Contacts[Status]="NLI"))
No = COUNTROWS(FILTER(Contacts, Contacts[Status]="No"))
NRTC = COUNTROWS(FILTER(Contacts, Contacts[Status]="NRTC"))
Other = COUNTROWS(FILTER(Contacts, Contacts[Status]="Other"))
SF = COUNTROWS(FILTER(Contacts, Contacts[Status]="SF"))
Unknown = COUNTROWS(FILTER(Contacts, Contacts[Status]="UNK"))
```
### Recruitment Funnel
```
Contacted = COUNTROWS(Contacts)
Responded = [Contacted] – [NRTC]
Phone Screened = [Screened] + [DNQ] + [No]
Screened = [Enrolled] + [SF] + [Screens]
Enrolled = [Completed] + [DC] + [LTFU] + [Active]
Complete = [Completed]
```
### Calculated Measures
```
Comp Rate = [Complete]/[Enrolled]
Cont: Scr Ratio = [Contacted]/[Screened]
S:E Ratio = [Screened]/[Enrolled]
SF Rate = [SF]/[Screened]
```
### Study Information Calculated Columns
#### Birth Control Efficacy
```
BC_efficacy = /*calculated column to check if birth control efficacy study*/
    IF(
        CONTAINSSTRING( -- condition for if statement
            [Study Endpoints], --column to look in 
            "No pregnancy"), -- text to look for, not case sensitive
        "Efficacy", --result if true/endpoint contains "no pregnancy"
        "Non-Efficacy" --result if false/endpoint does not contain "no pregnancy"
    )
```
#### Hormonal Product
```
Hormonal = SWITCH(
    [Hormonal Product?], 
      TRUE(), "Hormonal", 
      FALSE(), "Non-hormonal")
```


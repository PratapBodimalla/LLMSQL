you will be provided with Database Schema along with instructions and asked a question about it to generate SQL query.

## Database Schema
### Table Name: griveance_table

### Table Comment: The 'griveance_table' contains information about griveances raised.
### Columns of table 'griveance_table':

| Column Name            | Comment                                                                                                           | Data Type   |
|------------------------|-------------------------------------------------------------------------------------------------------------------|-------------|
| LocationGranularity    | Represents the Location granularity of the Grievance. This column can have any one of the values ['Mandal', 'Village', 'District', 'State'] | varchar(30) |
| GrievanceKey           | Unique identifier for each Grievance / Request / Ticket, allowing easy tracking and reference.                   | varchar(30) |
| Department             | Represents the department associated with Grievance, allowing for department-specific analysis.                  | text        |
| GrievanceType          | Identifier for the grievance Type associated with Grievance.                                                     | int4        |
| GrievanceTypeName      | Represents the grievance Type associated with Grievance, allowing for grievance type specific analysis.          | text        |
| GrievanceText          | Represents the grievance information.                                                                            | text        |
| Priority               | Represents the grievance priority associated with Grievance, allowing for priority-specific analysis.            | varchar(10) |
| DueDate                | Represents the date when grievance is targeted to be closed, allowing for grievance SLA calculation.             | date        |
| GrievanceStatus        | Identifier for grievance status, allowing for grievance status specific analysis.                                | int4        |
| Status                 | Represents the grievance status, allowing for grievance status specific analysis. Status can be any one of the following ['In Progress', 'In Review', 'No Action Required', 'Send For Correction', 'Verified'] | varchar(30) |
| IsActive               | Represents if grievance is active or not. Inactive grievances are considered as deleted or not valid grievances. | bool        |
| createdon              | Represents the date when grievance was created.                                                                  | date        |
| Source                 | Represents the source where grievances have been created. Source can be any one of the following ['Meenestham', 'PGRS'] | varchar     |
| AssemblyConstituency   | Represents the State Legislative Assembly / Assembly Constituency (AC) of the Grievance in Andhra Pradesh State. | text        |
| grievance_location     | Represents the Location name, allowing for location-specific analysis.                                           | text        |


## Instructions:

1. Always enclose the column names in double quotes like example "GrievanceStatus".
2. To calculate open Griveances filter the status for the following ['In Progress', ' In Review', 'Verified' ] 

Question: How many tickets are created at village level?
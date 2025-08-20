***3.4 Data Dictionary***

### ***3.4.1  Student Table***

| Field Name | Description | Data Type |
| ----- | ----- | ----- |
| Student\_ID | Unique identifier for the student. | Integer/String |
| Student\_Name | Name of the student. | String |
| Student\_Address | Residential address of the student. | String |
| Student\_Contact | Contact phone number or email address. | String |
| Courses\_Completed | List of completed courses. | Array of Strings |
| Courses\_Backlog | List of backlogged courses. | Array of Strings |
| Current\_GPA | GPA for the current semester. | Float |
| Cumulative\_GPA | Cumulative GPA across all semesters. | Float |

- [ ] 

### ***3.4.2 Course Table we***

| Field Name | Description | Data Type |
| ----- | ----- | ----- |
| Course\_ID | Unique identifier for the course. | Integer/String |
| Course\_Name | Name of the course. | String |
| Instructor\_Name | Name of the instructor for the course. | String |
| Credits | Number of credits awarded for completing the course. | Integer |
| Semester\_Offered | The semester when the course is offered. | String |
| Course\_Description | Description of the course content. | String |

### 

### ***3.4.3 Inventory Table***

| Field Name | Description | Data Type |
| ----- | ----- | ----- |
| Inventory\_ID | Unique identifier for the inventory item. | Integer/String |
| Item\_Name | Name of the inventory item (e.g., equipment). | String |
| Item\_Description | Description of the inventory item. | String |
| Quantity\_Available | Number of units available. | Integer |
| Item\_Price | Price of a single unit of the inventory item. | Float |
| Location | Physical location of the item. | String |

### ***3.4.4 Research & Publications Table***

| Field Name | Description | Data Type |
| ----- | ----- | ----- |
| Research\_Project\_ID | Unique identifier for the research project. | Integer/String |
| Project\_Name | Name of the research project. | String |
| Project\_Description | A brief description of the research project. | String |
| Faculty\_Name | Name of the faculty member(s) involved. | String |
| Publication\_Title | Title of the publication. | String |
| Publication\_Details | Additional publication details. | String |

### ***3.4.5 Financial Records Table***

| Field Name | Description | Data Type |
| ----- | ----- | ----- |
| Income\_Type | Type of income received (e.g., grant, consultancy). | String |
| Income\_Amount | Amount of income received. | Float |
| Expenditure\_Type | Type of expenditure (e.g., salaries, equipment). | String |
| Expenditure\_Amount | Amount of money spent. | Float |
| Balance | Remaining balance. | Float |
| Cash\_Book\_Report | Record of income, expenditure, and balance summary. | String |

### 

### 

### 

### ***3.4.6 Query System Table***

| Field Name | Description | Data Type |
| ----- | ----- | ----- |
| Query\_Type | Type of query (e.g., "Student", "Cash Book"). | String |
| Roll\_Number | Roll number used to query student details. | Integer/String |
| Query\_Result | Output generated from the query. | String |

***3.5 Data Flow Diagram(DFD)***

**Level 0:**

**Level 1:**

***3.6 Structure Chart***
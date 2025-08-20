[3.0.	Requirements Specification	17](#heading=h.xvir7l)  
[3.1	External Interface Requirements	17](#3.1-external-interface-requirements)  
[3.2	Functional Requirements	17](#heading=h.2u6wntf)  
[3.2.1	Item Management	17](#the-system-shall-provide-real-time-financial-reporting-for-department-heads.)  
[3.2.2	Billing and Payments	18](#heading=h.3tbugp1)  
[3.2.3	Inventory Management	18](#heading=h.nmf14n)  
[3.2.4	Sales Statistics and Reporting	19](#heading=h.37m2jsg)  
[3.2.5	Price Management	19](#heading=h.3hv69ve)  
[3.2.6	Update Article Status	20](#heading=h.46r0co2)  
[3.2.7	Enter Communication	20](#heading=h.2lwamvv)  
[3.2.8	Assign Reviewer	21](#heading=h.206ipza)  
[3.2.9	Check Status	21](#heading=h.2zbgiuw)  
[3.2.10	Send Communication	22](#heading=h.1egqt2p)  
[3.2.11	Publish Article	22](#heading=h.3ygebqi)  
[3.2.12	Remove Article	23](#heading=h.2dlolyb)  
[3.3	Detailed Non-Functional Requirements	23](#3.3-detailed-non-functional-requirements)  
[3.3.1	Logical Structure of the Data	23](#3.3-detailed-non-functional-requirements)  
[3.3.2	Security	25](#heading=h.2r0uhxc)  
[Index	26](#heading=h.1x0gk37)

# **List of Figures**

[Figure 1 \- System Environment	4](#heading=h.35nkun2)  
[Figure 2 \- Article Submission Process	6](#heading=h.z337ya)  
[Figure 3 \- Editor Use Cases	8](#heading=h.3whwml4)  
[Figure 4 \- Logical Structure of the Article Manager Data	23](#heading=h.4bvk7pj)

# **1.0. Introduction**

The University Department Information System (UDIS) is a web-based application designed to manage and streamline administrative tasks within university departments. It centralizes the management of student records, course registrations, grading, department inventory, financial transactions, and research activities. By automating processes, the system improves efficiency, accuracy, and accessibility for students, faculty, and administrative staff.

We will base this project on our college website, NITRIS, which offers secure login functionalities for both students and staff.

The system administrator will assign role-based credentials to each department member, controlling their access levels and permissions. These roles include the secretary, instructors, students, research assistants, and department heads, each with access to the features and information relevant to their responsibilities.

The system architecture follows a modern three-tier design, leveraging the MERN stack: a responsive front-end built with React.js for an enhanced user experience, an Express.js backend running on Node.js to handle business logic and API endpoints, and a MongoDB database for efficient data management.

## ***1.1. Purpose***

	This document provides a detailed overview of the University Department Information System (UDIS), covering its core functionalities, technical architecture, user interfaces, operational parameters, and response mechanisms for various use cases. It serves as a reference for developers, system administrators, end-users, and department leadership. The system requires approval from the Dean's office and the IT governance board before deployment.

## ***1.2. Scope of Project***  	The University Department Information System (UDIS) streamlines academic and administrative processes with the following functionalities:

### ***1.2.1 Student Management***

- ### Stores student details, including name, address, and registered courses.

- ### 8Tracks completed courses and backlogs.

- ### Allows the department secretary to register students for courses each semester.

- ### Displays student records when a roll number is entered.

- ### Computes semester GPA and cumulative GPA (CGPA).

- ### Generates and prints student grade sheets.

### 

  ### ***1.2.2 Inventory Management***

- ### Maintains records of department equipment, furniture, and their locations.

### ***1.2.3 Financial Management***

- ### Tracks annual grants from the university and expenditures on books, equipment, and stationery.

- ### Records income from consultancy services.

- ### Manages departmental accounts, including income, expenses, and balance.

  ### ***1.2.4 Research and Faculty Management***

- ### Documents ongoing research projects within the department.

- ### Maintains records of faculty publications.

### ***1.2.5 Query and Reporting System***

- ### Supports real-time queries for student details using roll numbers.

- ### Allows financial queries, displaying department income, expenditures, and balance.

This system ensures accuracy, efficiency, and transparency in managing departmental operations.

## ***1.3. Glossary***

| Term | Definition |
| ----- | ----- |
| **Student Record** | A database entry containing a student’s personal details, registered courses, completed courses, and backlogs. |
| **Semester GPA
(SGPA)** | The grade point average calculated for a specific semester based on course grades. |
| **Cumulative GPA
(CGPA)** | The overall grade point average calculated from all completed semesters. |
| **Backlog** | A course that a student has failed and needs to retake. |
| **Grade Sheet** | A document displaying a student’s grades for a semester. |
| **Department Inventory** | A record of equipment, furniture, and other assets within the department. |
| **Equipment Tracking** | The process of monitoring the location and status of departmental assets. |
| **Annual Grant** | Yearly funding provided by the university for departmental expenses. |
| **Departmental Accounts** | Financial records tracking income, expenses, and balances. |
| **Expenditure** | Money spent on books, equipment, stationery, and other departmental needs. |
| **Research Project** | A study or investigation conducted by faculty members or researchers within the department. |
| **Faculty Publications** | Research papers, books, and articles authored by department faculty members. |
| **Financial Query** | A function that provides details of departmental income, expenditure, and balance. |
| **Real-time Reporting** | Instant generation of reports based on up-to-date data. |

## 

## ***1.4. References*** {#1.4.-references}

IEEE. *IEEE Std 830-1998 IEEE Recommended Practice for Software Requirements Specifications.* IEEE Computer Society, 1998\.

## ***1.5. Overview of Document***

The next chapter, the **Overall Description** section, provides an overview of the functionality of the supermarket automation software. It outlines the informal requirements and serves to establish a context for the detailed technical requirements specified in the following chapter.

The third chapter, the **Requirements Specification** section, is primarily intended for developers and describes the system’s functionality in technical terms. It details how various components, such as inventory management, pricing updates, and point-of-sale operations, are implemented within the software.

Both sections describe the same supermarket automation system in its entirety but are tailored for different audiences, using different levels of technical language.

.

# **2.0.	Overall Description**

## ***2.1	Product Perspective*** {#2.1-product-perspective}

	The **University Department Information System (UDIS)** is designed as an integrated platform for managing academic and administrative operations within a university department. It serves as a digital transformation of traditional paper-based processes, ensuring efficiency, accuracy, and accessibility. The system will be a **web-based** solution leveraging the **MERN stack (MongoDB, Express.js, React.js, Node.js)**. It will be deployed on a secure cloud infrastructure, ensuring scalability and availability.

## ***2.2	Product Functions***

* **Student Management:** Capture and maintain student profiles, including personal information and academic records.  
* **Course Registration:** Facilitate course enrollment at the beginning of each semester.  
* **Grading System:** Allow faculty to input grades and generate automated grade sheets.  
* **Inventory Tracking:** Maintain a catalog of department assets, including equipment and furniture.  
* **Financial Management:** Track departmental budgets, expenses, and income sources.  
* **Research and Faculty Management:** Store research publications and ongoing projects.  
* **Query and Reporting:** Provide real-time analytics and reporting capabilities.


## ***2.3	User Characteristics***

* **Students:** Should be familiar with web navigation to access course registration, academic records, and grading information.  
* **Instructors:** Should have proficiency in using web-based systems to manage grades and student performance.  
* **Department Secretaries:** Should handle administrative tasks, including student registration, inventory management, and financial tracking.  
* **Department Heads:** Should have access to high-level reports and approve financial and academic decisions.  
* **Administrators:** Should maintain the system, manage user access, and ensure data security.

## ***2.4	Constraints***

	The system must comply with university data protection policies to ensure the confidentiality and integrity of sensitive information. It should be capable of efficiently handling at least 500 concurrent users, maintaining optimal performance under high loads. To guarantee reliability, the system must achieve 99.9% uptime, minimizing disruptions and ensuring continuous availability. Additionally, it should adhere to all relevant academic and financial governance policies, ensuring regulatory compliance and seamless integration within the university's operational framework.

## ***2.5	Assumptions and Dependencies***

	The system operates under the assumption that all users have internet access and possess basic familiarity with web applications, ensuring a smooth user experience. It relies on the university's authentication services to implement role-based access control, maintaining secure and restricted access as needed. To optimize cost efficiency, the system will be developed using open-source technologies, reducing licensing expenses. Additionally, the university IT department will be responsible for providing the necessary hardware and network support, ensuring stable infrastructure and seamless system deployment.

# **3.0.	Requirements Specification**

## ***3.1	External Interface Requirements*** {#3.1-external-interface-requirements}

	***3.1.1 User Interfaces***

* The system shall provide a web-based graphical user interface accessible via modern browsers.  
  * The user interface shall include dashboard views for different user roles.  
  * The system shall support responsive design, ensuring usability on desktops, tablets, and mobile devices.

  #### ***3.1.2 Hardware Interfaces***

* The system shall be compatible with standard desktop and mobile devices.  
* The system shall interface with barcode scanners and printers for record-keeping and report generation.

  #### ***3.1.3 Software Interfaces***

* The system shall integrate with university authentication systems (e.g., LDAP, OAuth).  
* The system shall interface with financial management software for budget tracking.

  #### ***3.1.4 Communication Interfaces***

* The system shall support email notifications for course registration, grades, and financial transactions.  
* The system shall enable API-based access for third-party applications to retrieve data securely.

## ***3.2	Functional Requirements***

### ***3.2.1 Student Management***

* The system shall allow department secretaries to **register new students**.  
* The system shall track **student records**, including personal details and academic history.  
* The system shall support **automatic course enrollment verification**.

  ### 

  ### 

  ### ***3.2.2 Course Registration***

* Students shall be able to **register for courses** at the beginning of each semester.  
* The system shall ensure that **prerequisite requirements** are met before allowing registration.

  ### ***3.2.3 Grading System***

* Instructors shall be able to **enter grades** for students.  
* The system shall **automatically compute GPA and CGPA** based on student performance.

  ### ***3.2.4 Inventory Management***

* The system shall track **departmental assets**, including lab equipment and furniture.  
* The system shall generate **inventory reports** for department administration.

  ### ***3.2.5 Financial Management***

* The system shall track **annual department funding** and expenses.  
* The system shall allow authorized users to **generate financial reports**.

  ### ***3.2.6 Research and Faculty Management***

* The system shall allow faculty to **record research projects and publications**.  
* The system shall provide **search functionality** to query faculty research records.

  ### ***3.2.7 Reporting and Queries***

* The system shall support **querying student details using roll numbers**.  
* The system shall provide **real-time financial reporting** for department heads.

## ***3.3	Detailed Non-Functional Requirements*** {#3.3-detailed-non-functional-requirements}

### ***3.3.1 Performance Requirements***

* ## The system shall support at least 500 concurrent users.

* ## The system shall process user queries within 2 seconds.

* ## Reports shall be generated within 5 seconds.

* ## The system uptime shall be maintained at 99.9%.

### ***3.3.2 Safety and Security Requirements***

* ## The system shall implement role-based access control (RBAC) to restrict access to authorized users.

* ## All data transmissions shall be encrypted using TLS 1.3.

* ## User authentication shall support multi-factor authentication (MFA) for administrative users.

* ## Automated backup mechanisms shall allow system recovery within 30 minutes.

* ## System logs shall be securely stored for audit compliance.

### ***3.3.3 Software Quality Attributes***

#### ***3.4.3.1 Reliability***

* ## The system shall provide automated error handling and fault recovery mechanisms.

* ## Database replication shall ensure data redundancy and failover support.

* ## Maximum allowable downtime shall not exceed 15 minutes per incident.

  #### ***3.3.3.2 Maintainability***

* ## The system shall be developed using modular architecture for easy updates.

* ## A logging and debugging system shall be in place for administrators.

* ## The system shall follow industry-standard version control for code management.

  #### ***3.3.3.3 Usability***

* ## The user interface shall be intuitive and accessible, requiring minimal training.

* ## The system shall include search functionality for quick access to records.

* ## The system shall comply with WCAG 2.1 standards to ensure accessibility for all users.

  #### ***3.3.3.4 Scalability***

* ## The system shall support scaling up to 5,000 users.

* ## It shall be optimized for distributed computing and cloud deployment.

* ## API endpoints shall handle large dataset queries efficiently.
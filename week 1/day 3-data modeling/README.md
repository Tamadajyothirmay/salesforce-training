# Day 3 - Data Modeling in Salesforce

## 1. Difference Between App, Object, Record, and Field

| Concept | Description | Example |
|----------|-------------|----------|
| App | A collection of related tabs, objects, and features used for a specific business process. | College Management App |
| Object | A database table that stores related information. | Student Object |
| Record | A single entry stored inside an object. | Student: Rahul Kumar |
| Field | A single piece of information inside a record. | Student Name, Roll Number |

---

# 2. Standard vs Custom Objects

| Standard Objects | Custom Objects |
|------------------|----------------|
| Already provided by Salesforce | Created by users |
| Used for common CRM processes | Used for business-specific requirements |
| Examples: Account, Contact, Opportunity | Examples: Student__c, Faculty__c |
| Cannot delete most standard objects | Can be modified or deleted |

---

# 3. College Data Model

## Objects Used

### Standard Objects
- Account
- Contact

### Custom Objects
- Student__c
- Faculty__c
- Course__c
- Department__c
- Attendance__c

---

## Relationships

| Parent Object | Child Object | Relationship Type |
|----------------|--------------|-------------------|
| Department__c | Course__c | Lookup |
| Course__c | Student__c | Lookup |
| Faculty__c | Course__c | Lookup |
| Student__c | Attendance__c | Master-Detail |

---

# College Management Data Flow

1. Departments manage multiple courses.
2. Faculty members teach courses.
3. Students enroll in courses.
4. Attendance records are maintained for students.

---

# Data Model Diagram

```text
Department__c
      |
      | Lookup
      v
Course__c -------- Faculty__c
      |
      | Lookup
      v
Student__c
      |
      | Master-Detail
      v
Attendance__c
4. Formula Fields
What is a Formula Field?

A Formula Field automatically calculates values based on other fields.

Example 1: Student Full Name
Formula:
First_Name__c & " " & Last_Name__c
Explanation:

This formula combines first name and last name into a single field.

Example 2: Attendance Percentage
Formula:
(Classes_Attended__c / Total_Classes__c) * 100
Explanation:

This formula calculates the attendance percentage of a student automatically.

Example 3: Course Duration Status
Formula:
IF(Duration_Months__c > 6, "Long Term", "Short Term")
Explanation:

If course duration is greater than 6 months, it shows "Long Term"; otherwise, it shows "Short Term".

5. Validation Rules
What is a Validation Rule?

Validation Rules prevent users from entering invalid data into Salesforce.

Example 1: Phone Number Validation
Rule:
LEN(Phone__c) <> 10
Error Message:

"Phone number must contain exactly 10 digits."

Explanation:

This rule prevents saving records with incorrect phone numbers.

Example 2: Attendance Cannot Exceed Total Classes
Rule:
Classes_Attended__c > Total_Classes__c
Error Message:

"Attended classes cannot be greater than total classes."

Explanation:

This rule ensures logical attendance data.

Example 3: Student Age Validation
Rule:
Age__c < 16
Error Message:

"Student age must be at least 16."

Explanation:

This prevents invalid student age entries.

6. Reflection - Why Structured Enterprise Data Matters

Structured enterprise data is important because it helps organizations store, manage, and analyze information efficiently. In Salesforce, proper data modeling improves accuracy, reduces duplicate records, and makes reporting easier.

For a college management system:

Student details can be tracked properly.
Attendance and course data remain organized.
Relationships between departments, faculty, and students become easy to manage.
Reports and dashboards provide better decision-making.

Good data structure improves scalability, automation, and overall business efficiency.

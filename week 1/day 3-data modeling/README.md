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

1. Difference Between App, Object, Record, and Field
App

An App in Salesforce is a collection of tabs, objects, and features designed for a specific business process.
Example: College Management App.

Object

An Object is like a database table that stores related data.
Example: Student Object.

Record

A Record is a single entry inside an object.
Example: A student named Rahul Kumar.

Field

A Field stores a specific piece of information in a record.
Example: Student Name, Roll Number, Phone Number.

2. Standard vs Custom Objects
Standard Objects

Standard objects are already provided by Salesforce for common business processes.
Examples include Account, Contact, Opportunity, and Lead.

Custom Objects

Custom objects are created by users according to business requirements.
Examples include Student__c, Faculty__c, Course__c, and Attendance__c.

Standard objects cannot be deleted easily, while custom objects can be modified according to business needs.

3. College Data Model
Objects Used
Standard Objects
Account
Contact
Custom Objects
Student__c
Faculty__c
Course__c
Department__c
Attendance__c
Relationships
One Department can have many Courses.
One Faculty member can teach many Courses.
Students enroll in Courses.
One Student can have many Attendance records.
College Data Model Diagram
Department__c
      |
      v
Course__c -------- Faculty__c
      |
      v
Student__c
      |
      v
Attendance__c
4. Formula Fields
What is a Formula Field?

A Formula Field automatically calculates values using other fields.

Example 1: Student Full Name

Formula:

First_Name__c & " " & Last_Name__c

Explanation:

This formula combines the first name and last name into one field.

Example 2: Attendance Percentage

Formula:

(Classes_Attended__c / Total_Classes__c) * 100

Explanation:

This formula calculates the attendance percentage automatically.

Example 3: Course Duration Status

Formula:

IF(Duration_Months__c > 6, "Long Term", "Short Term")

Explanation:

If the course duration is greater than 6 months, it displays "Long Term"; otherwise, it displays "Short Term".

5. Validation Rules
What is a Validation Rule?

Validation Rules prevent users from entering incorrect data.

Example 1: Phone Number Validation

Rule:

LEN(Phone__c) <> 10

Error Message:

Phone number must contain exactly 10 digits.

Explanation:

This rule prevents invalid phone numbers from being saved.

Example 2: Attendance Validation

Rule:

Classes_Attended__c > Total_Classes__c

Error Message:

Attended classes cannot be greater than total classes.

Explanation:

This rule ensures attendance values are valid.

Example 3: Student Age Validation

Rule:

Age__c < 16

Error Message:

Student age must be at least 16.

Explanation:

This rule prevents invalid student age entries.

6. Reflection - Why Structured Enterprise Data Matters

Structured enterprise data helps organizations manage information efficiently. In Salesforce, proper data modeling improves data accuracy, avoids duplicate records, and makes reporting easier.

In a college management system, structured data helps track students, courses, faculty, and attendance properly. Relationships between objects make the system organized and scalable.

Good data structure also improves automation, reporting, security, and decision-making in an organization.

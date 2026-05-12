# Day 4 - Flow Builder

## 1. What is Flow Builder?

Flow Builder is a declarative automation tool in Salesforce used to automate business processes without writing code. It helps users create workflows, update records, send notifications, and collect user input using drag-and-drop components.

### Advantages of Flow Builder
- Reduces manual work
- Saves time
- Improves accuracy
- Automates repetitive tasks
- Improves productivity

---

# 2. Types of Flows

## Screen Flow

Screen Flow is an interactive flow that collects information from users through screens.

### Example
A student registration form where users enter:
- Name
- Email
- Course
- Phone Number

The flow stores the data automatically in Salesforce.

### Uses
- Forms
- Surveys
- Step-by-step processes
- Customer support screens

---

## Record-Triggered Flow

Record-Triggered Flow runs automatically when a record is created, updated, or deleted.

### Example
When a new employee record is created:
- Welcome email is sent automatically
- Manager gets notified
- Employee status changes to "Active"

### Uses
- Automatic record updates
- Notifications
- Approval automation
- Background processes

---

# 3. Your Automation Ideas

## 1. Student Admission Automation
When a student application is submitted:
- Student record is created
- Confirmation email is sent
- Status updates automatically

---

## 2. Library Reminder System
Before the due date:
- Reminder email is automatically sent to students

---

## 3. Employee Leave Management
When an employee applies for leave:
- Manager receives approval request
- Leave balance updates automatically

---

## 4. E-Commerce Order Automation
When a customer places an order:
- Invoice is generated
- Confirmation email is sent
- Order status updates automatically

---

## 5. Hospital Appointment Automation
When a patient books an appointment:
- Doctor gets notified
- Appointment slot is reserved
- Patient receives confirmation message

---

# 4. Your Flow Diagram

## Student Registration Automation Flow

```text
Start
   ↓
User Fills Registration Form
   ↓
Create Student Record
   ↓
Send Confirmation Email
   ↓
Update Student Status
   ↓
End
# 5. Manual vs Automated Process
Manual Process
Requires human effort
Time consuming
More chances of errors
Difficult to manage repetitive tasks
Example

Admin manually sending emails to students.

Automated Process
Tasks run automatically
Faster processing
Reduces errors
Easy to monitor
Example

Salesforce Flow automatically sends confirmation emails after form submission.

# 6. Reflection - Why Automation Matters in Enterprise Systems

Automation is important in enterprise systems because organizations handle large amounts of data and repetitive tasks daily. Manual processes consume time and may lead to errors.

Using Salesforce Flow Builder helps companies:

Save time
Improve accuracy
Reduce operational costs
Improve customer service
Increase productivity

Automation allows employees to focus on important business activities instead of repetitive manual work. It improves overall efficiency and system reliability.

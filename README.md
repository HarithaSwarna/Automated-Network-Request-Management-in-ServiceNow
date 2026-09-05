# Automated Network Request Management

## Project Overview

**Automated Network Request Management** is a ServiceNow-based application designed to automate and streamline the complete lifecycle of network service requests.

The system allows users to submit network requests through the ServiceNow Service Portal. The submitted requests are automatically processed through approval, assignment, notification, tracking, and resolution stages.

The main objective is to reduce manual effort, minimize errors, speed up request processing, and provide better visibility into the request lifecycle.

---

## Problem Statement

Manual network request processing can lead to delays in submission, approval, assignment, tracking, and resolution.

Users may also have limited visibility into their request status, while IT and network teams may spend significant time performing repetitive manual activities.

Therefore, an automated ServiceNow-based solution is required to manage the complete network request lifecycle efficiently.

---

## Business Objective

The main objective of this project is to streamline and automate the end-to-end lifecycle of network-related service requests using ServiceNow.

The solution aims to:

- Reduce manual effort and human errors
- Accelerate request fulfilment
- Standardize approval and assignment processes
- Improve request visibility and tracking
- Provide timely notifications
- Improve end-user experience
- Maintain centralized request records
- Improve operational efficiency

---

## Key Features

### 1. Network Request Catalog

Users can submit network-related requests through a ServiceNow Service Portal Catalog Item.

The catalog item collects required information such as:

- Requested For
- Mobile Number
- Type of Connection
- Existing Connection ID
- Total Amount
- Mode of Payment
- Customer Address

---

### 2. Dynamic Request Form

The request form provides appropriate fields based on the user's selection.

For example:

- New Connection
- Existing Connection
- Upgrade Existing Connection

The system can display the **Existing Connection ID** field when an existing connection option is selected.

---

### 3. Request Validation

Mandatory fields and validation rules help prevent incomplete or incorrect submissions.

The system validates important information before the request is submitted.

---

### 4. Automatic Request Number

Each network request is assigned a unique request/database number.

Example:

`RITM0010020`

This number can be used to identify and track the request throughout its lifecycle.

---

### 5. Automated Approval

The system uses ServiceNow Flow Designer to automate the approval process.

Depending on the request, approval can be routed to the appropriate approver.

Possible approval states include:

- Requested
- Approved
- Rejected

Approval records are maintained for tracking and audit purposes.

---

### 6. Automatic Assignment

After approval, the request can be assigned to the appropriate IT or network fulfilment team.

This reduces manual assignment work and helps ensure requests reach the correct team.

---

### 7. Email Notifications

Automated notifications keep users and teams informed about important request events.

Notifications can be triggered for:

- Request submission
- Approval
- Rejection
- Assignment
- Completion

---

### 8. Request Tracking

Users and administrators can track the current status of network requests.

The request lifecycle can include:

`Submitted → Approval → Assignment → Processing → Resolution → Closure`

---

### 9. Flow Designer Automation

ServiceNow **Flow Designer** is used to automate the request lifecycle.

The flow can perform activities such as:

- Getting catalog variables
- Creating database records
- Requesting approval
- Updating approval status
- Assigning requests
- Sending email notifications
- Updating records after approval or rejection

---

## Request Lifecycle

```text
User
  |
  v
Network Request Catalog
  |
  v
Request Submission
  |
  v
Create Network Request Record
  |
  v
Approval
  |
  +---- Rejected ----> Update Status
  |
  v
Approved
  |
  v
Automatic Assignment
  |
  v
Notification
  |
  v
Request Processing
  |
  v
Resolution
  |
  v
Closure

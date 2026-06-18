# AI Client Onboarding Hub

## Overview

AI Client Onboarding Hub is an end-to-end workflow automation system built using **n8n** and **Airtable**. The system automates the complete client onboarding lifecycle, from receiving a client submission to creating projects, assigning team members, and generating activity logs.

The goal of this project is to eliminate manual data entry, reduce administrative effort, and ensure that projects are assigned to the right team member based on complexity and skill level.

---

## Features

### Client Intake Automation

* Receives client submissions through a webhook endpoint.
* Captures client details including:

  * Company Name
  * Contact Name
  * Email
  * Phone Number
  * Industry
  * Budget
  * Requested Service
  * Project Description

### Validation Engine

* Validates required fields before processing.
* Prevents incomplete submissions from entering the system.

### Duplicate Detection

* Checks for existing client records using email address.
* Prevents duplicate client creation.
* Logs duplicate submission attempts.

### Automatic Client Creation

* Generates unique Client IDs.
* Creates new records in Airtable Clients table.

### Automatic Project Creation

* Generates unique Project IDs.
* Creates linked project records.
* Associates projects with the correct client.

### Complexity Assessment

Projects are automatically categorized based on budget:

| Budget Range  | Complexity | Required Level |
| ------------- | ---------- | -------------- |
| Low Budget    | Low        | Junior         |
| Medium Budget | Medium     | Engineer       |
| High Budget   | High       | Senior         |

### Dynamic Team Assignment

Projects are automatically assigned based on complexity:

| Level    | Assigned Member |
| -------- | --------------- |
| Junior   | Ahmed           |
| Engineer | Ali             |
| Senior   | Sara            |

### Activity Tracking

Automatically creates activity records for:

* Client Intake
* Project Assignment
* Duplicate Detection Events

### Linked Database Architecture

The system maintains relationships between:

* Clients
* Projects
* Team Members
* Activities

---

## Workflow Architecture

Client Submission

↓

Validation

↓

Duplicate Check

↓

Client Creation

↓

Project Creation

↓

Complexity Analysis

↓

Team Member Selection

↓

Project Assignment

↓

Activity Logging

↓

Success Response

---

## Airtable Database Structure

### Clients Table

Stores:

* Client ID
* Company Information
* Contact Details
* Budget
* Requested Service
* Linked Projects
* Linked Activities

### Projects Table

Stores:

* Project ID
* Project Name
* Description
* Complexity
* Priority
* Risk Level
* Assigned Team Member
* Linked Client
* Linked Activities

### Team Members Table

Stores:

* Member Name
* Level
* Email
* Availability Status
* Assigned Projects

### Activities Table

Stores:

* Activity Type
* Notes
* Assigned Member
* Linked Project
* Linked Client
* Status

---

## Technology Stack

### Automation Platform

* n8n

### Database

* Airtable

### Logic Layer

* JavaScript

### Integration

* Webhooks
* Airtable API

---

## Business Rules

### Complexity Logic

Low Budget:

* Complexity = Low
* Priority = Low
* Risk Level = Low
* Assigned Level = Junior

Medium Budget:

* Complexity = Medium
* Priority = High
* Risk Level = Medium
* Assigned Level = Engineer

High Budget:

* Complexity = High
* Priority = Critical
* Risk Level = High
* Assigned Level = Senior

---

## Sample Workflow Results

### Low Complexity Project

* Assigned to Ahmed

### Medium Complexity Project

* Assigned to Ali

### High Complexity Project

* Assigned to Sara

---

## Key Learning Outcomes

This project demonstrates practical experience with:

* Workflow Automation
* Business Process Automation
* Airtable Relational Databases
* Linked Records
* Lookup Fields
* API Integrations
* Webhooks
* JavaScript Logic
* Error Handling
* Duplicate Prevention
* Dynamic Record Assignment
* Low-Code Development

---

## Future Improvements

* AI-based project complexity analysis
* AI team member recommendations
* Email notifications
* Slack integration
* Project status dashboards
* Automated follow-ups
* Reporting and analytics
* CRM integration

---

## Author

**Tasdiq Ayub**

Electrical Engineer | Technical Sales Engineer | Automation Engineer

Focused on workflow automation, AI-powered business systems, renewable energy technologies, and process optimization using low-code tools.

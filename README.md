# SLA-Tracking-Excel-Project
Excel-based SLA tracking,lead management,and billing workflow with automation and validations
# SLA Tracking & Lead Operations System (Excel)

## Executive Summary
This project is a **production-ready SLA Tracking and Lead Operations system** built using Microsoft Excel to manage high-volume telecalling workflows.

It is designed to **enforce SLA compliance, track lead lifecycle, monitor telecaller performance, and ensure sales/billing traceability** — all within a single automated Excel solution.

This system mirrors how SLA tracking is implemented in real sales operations where CRM access is limited or Excel remains the operational backbone.

---

## Business Context
In telecalling and sales operations:
- Delayed first calls directly impact conversion rates
- SLA breaches go unnoticed without automation
- Manual follow-ups cause lead leakage
- Performance reviews lack data consistency
- Billing and visit confirmations are hard to trace

This Excel system solves these issues by introducing **structured automation, rule-based logic, and visual accountability**.

---

## System Design Philosophy
The system is built with the following principles:
- **Automation over manual tracking**
- **Error-resistant data entry**
- **Visual SLA accountability**
- **Scalability across telecallers**
- **Reporting-ready structure (Power BI compatible)**

No VBA macros are required for core SLA logic — ensuring transparency and maintainability.

---

## End-to-End Workflow

### 1️⃣ Lead Intake
- Lead is received with timestamp
- Source, customer details, and telecaller are captured
- Data validation ensures clean entry

### 2️⃣ SLA Enforcement
- Lead received time is split into date & time
- First call time is captured
- SLA is calculated automatically
- Status updates instantly:
  - SLA MET
  - SLA BREACHED

### 3️⃣ Follow-up & Call Monitoring
- Call attempts are counted
- Last call date is tracked
- Next follow-up date is enforced

### 4️⃣ Lead Outcome Management
- Lead status updated via controlled drop-downs
- Secondary & branch feedback captured
- Conversion funnel is clearly visible

### 5️⃣ Visit, Sales & Billing Traceability
- Visit completion is marked
- Sales confirmation recorded
- Bill value, invoice number, and billing date stored
- Bill copy linked for audit proof

---

## Column Architecture (Logical Grouping)

### Lead Identity & Source
MONTH | DATE | LEAD NAME | MOBILE NUMBER | LEAD SOURCE | TELECALLER

### Customer & Product Context
CUSTOMER LOCATION | BRANCH CODE | PROPERTY | BRAND | PRODUCT SIZE

### SLA Core Logic
LEAD DATE & TIME  
LEAD DATE  
LEAD RECEIVED TIME  
FIRST CALL TIME  
SLA STATUS  

### Call & Follow-up Control
CALL TYPE  
CALL ATTEMPT COUNT  
LAST CALL DATE  
NEXT FOLLOW-UP DATE  

### Outcome & Feedback
LEAD STATUS  
2ND FEEDBACK  
BRANCH FEEDBACK  

### Sales & Billing
VISIT DONE  
SALES DONE  
FINAL BILL VALUE  
INVOICE NUMBER  
BILLING DATE  
BILL COPY  
REMARKS  

---

## Core Excel Logic Implemented

### SLA Calculation Logic
**Design:**
- SLA status is calculated by comparing:
  - Lead received time
  - First call time

**Outcome:**
- Removes subjective SLA interpretation
- Enforces objective compliance

---

### Error-Safe Conditional Logic
**Functions Used:**
- IF
- IFS
- AND
- IFERROR

**Why this matters:**
- Sheet never breaks on missing data
- Live operational use without formula failures

---

### Lookup & Standardization
**Approach:**
- Central master data sheet
- Controlled drop-downs via Data Validation

**Impact:**
- Zero spelling mismatch
- Clean reporting
- Power BI friendly structure

---

### Aggregation & Reporting Logic
**Functions Used:**
- COUNTIFS
- SUMIFS

**Usage:**
- Telecaller SLA performance
- Call attempt analysis
- Conversion and sales tracking

---

### Visual Intelligence (Conditional Formatting)
| Condition | Visual Cue |
|----------|-----------|
| SLA MET | Green |
| SLA BREACHED | Red |
| Closed-Converted | Green |
| Closed-Not Interested | Red |
| Call Back Required | Blue |

This enables **instant management review without filtering or pivot tables**.

---

## Screenshots
Key system areas are documented in the `screenshots/` folder:
- SLA status calculation
- Master data controls
- Billing & visit tracking

---

## Skills Demonstrated
- SLA automation design
- Business process modeling
- Advanced Excel logic
- Operational reporting
- Data validation architecture
- Audit-ready documentation
- Power BI integration readiness

---

## Why This Project Matters
This project demonstrates how Excel can be engineered as a **lightweight CRM-style system** when designed with discipline, structure, and business logic.

It reflects real operational constraints — not textbook examples.

---

## Author Note
This system was built, tested, and used in a live environment for daily SLA and telecaller performance reporting.

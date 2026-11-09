# Academic Dashboard & Document Processing System

## Overview
This repository contains the implementation and test cases for an automated **Student Academic Dashboard**. The system processes student information, course grades, examination schedules, attendance records, and announcements into formatted documents and structured layouts.

---

## Student Details Placeholder

```text
==================================================
STUDENT INFORMATION
==================================================
Full Name     : [INSERT STUDENT NAME]
Student ID    : [INSERT STUDENT ID]
Course/Major  : [INSERT PROGRAM / MAJOR]
Current Term  : [INSERT SEMESTER / TERM]
==================================================
```

---

## Test Cases Overview

### Case 1: Standard Academic Report Processing
* **Objective:** Verify correct rendering and parsing of core student academic metrics including grade tables, examination schedules, and attendance percentages.
* **Input Data:** Complete academic record including major details, 4 subject records, mid-term schedule, attendance percentages, and system announcements.
* **Expected Output:** Fully structured visual dashboard containing:
  * Course & Grade summary table (DBMS, Algorithms, Operating Systems, Organizational Behavior).
  * Exam schedule with timing and room allocations.
  * Attendance metrics accurately mapped per course code.
* **Validation Criteria:** All grades, room numbers, and percentages match input source without truncation or formatting errors.

---

### Case 2: Attendance Threshold & Flagging Logic
* **Objective:** Validate system alerts when student attendance falls below the mandatory minimum threshold (e.g., 75%).
* **Input Data:** Academic profile with attendance values varying across subjects (e.g., Operating Systems at 74%).
* **Expected Output:** 
  * Generation of low-attendance warning flags for subjects under the threshold.
  * Conditional formatting or notifications triggered for advising review.
* **Validation Criteria:** Flags trigger strictly for values $< 75\%$; compliant attendance percentages ($\ge 75\%$) remain unflagged.

---

### Case 3: Dynamic Announcement & System Alert Handler
* **Objective:** Test parsing and prioritized display of active system notices (e.g., project deadline extensions, fee reminders).
* **Input Data:** Unstructured text announcements and administrative alerts.
* **Expected Output:**
  * Categorization of alerts into high-priority (financial/hall ticket hold) and general notifications (academic updates).
  * Clear section rendering on the primary user dashboard view.
* **Validation Criteria:** Critical alerts are prominently displayed at the top of the announcement panel; obsolete or cleared notifications are omitted.

---

## Project Setup & Usage

### Prerequisites
* Markdown Viewer / PDF Rendering Engine
* Supported Runtime Environment (Node.js / Python 3.x, if executing parsing scripts)

### Running Test Cases
1. Populate student details in the provided placeholder format.
2. Execute the parsing suite against input test data files:
   ```bash
   # Example execution command
   python run_tests.py --case=all
   ```
3. Inspect output generated artifacts for accuracy against the validation criteria listed above.
---
title: "Test Scenario, Test Case, and Bug Report"
date: 2025-09-01
categories: [Software Testing]
author: Nancy Jiwono
layout: post
description: "Explain about Test Scenario, Test Case, and Bug Report"
image: /assets/software/testScenarioCaseBug.png
comments: true
---

## Overview

**Test scenario**, **test case**, and **bug report** are three essential elements in the software testing process that complement one another to ensure that applications work as expected and remain free from errors.

| Element | Description/Focus |
| --- | --- |
| **Test Scenario** | A general description of what is being tested to ensure the application functions as required. |
| **Test Case** | A detailed step-by-step test, including input, process, and expected output. |
| **Bug Report** | A formal report of application errors, containing details of the problem, reproduction steps, and actual results. |

---

## Simple Templates

### Template: Test Scenario

| Field | Description |
| --- | --- |
| Scenario ID | Unique number for the scenario |
| Description | Summary of the testing scenario |
| Module/Feature | The module or feature being tested |

### Template: Test Case

| Field | Description |
| --- | --- |
| Test Case ID | Unique number for the test case |
| Description | Brief summary of the test |
| Precondition | Initial conditions before testing |
| Test Steps | Detailed testing steps |
| Test Data | Data used for testing |
| Expected Result | Results expected based on requirements |
| Actual Result | Actual results after testing |
| Status | Pass/Fail |

---

## Example Application: BMI App

### Test Scenarios for BMI Application

| Scenario ID | Description | Module/Feature |
| --- | --- | --- |
| **TS001** | Verify slider input function | Slider for weight and height |
| **TS002** | Verify calculation and BMI classification | BMI calculation and classification |
| **TS003** | Verify BMI history saving function | BMI history |

### Example Test Cases Based on Scenarios

**Scenario TS001: Verify slider input function**

| Test Case ID | Description | Test Data | Expected Result |
| --- | --- | --- | --- |
| **TC001** | Verify weight slider input | Slider set to 60 kg | Weight label displays 60 kg according to slider |
| **TC002** | Verify height slider input | Slider set to 170 cm | Height label displays 170 cm according to slider |

**Scenario TS002: Verify BMI calculation and classification**

| Test Case ID | Description | Test Data | Expected Result |
| --- | --- | --- | --- |
| **TC003** | Verify BMI calculation using standard formula ($kg/m^2$) | Height = 170, Weight = 65 | BMI calculation result is 22.49 |
| **TC004** | Verify "Underweight" category | Height = 170, Weight = 45 | BMI = 15.6, displays "Underweight" |
| **TC005** | Verify "Normal" category | Height = 165, Weight = 60 | BMI ≈ 22.04, displays "Normal" |
| **TC006** | Verify "Overweight" category | Height = 170, Weight = 75 | BMI ≈ 25.95, displays "Overweight" |
| **TC007** | Verify "Obese" category | Height = 165, Weight = 90 | BMI ≈ 33.06, displays "Obese" |

**Scenario TS003: Verify BMI history saving function**

| Test Case ID | Description | Test Steps | Expected Result |
| --- | --- | --- | --- |
| **TC008** | Verify saving the latest BMI result into history | Adjust weight and height slider. Press Save History. | User is redirected to history page, and the latest BMI is stored. |
| **TC009** | Verify saving multiple history records without data loss | Save several BMI results sequentially. Open history page. | All BMI results are saved and displayed in order, without data loss. |

---

## Bug Report

### Definition

A **Bug Report** is a formal report of system errors or issues.

### Bug Classification

### 1. Bug Severity (Impact Level on Software Functionality)

- **Low**: Bug does not affect system functionality.
- **Minor (Medium)**: Bug does not impact core functions but may cause user inconvenience.
- **Major (High)**: Bug disrupts main functionality but does not crash the entire system.
- **Critical**: Bug causes total system failure or data corruption; application becomes unusable.

### 2. Bug Priority (Order of Bug Fixing Priority)

- **P1 – Urgent/Critical**: Must be fixed immediately.
- **P2 – High**: Important bug affecting many users; needs fast resolution but less urgent than P1.
- **P3 – Medium**: Can be fixed in the next release cycle; does not affect core functions.
- **P4 – Low**: Minor or cosmetic bugs, fixable anytime.

### Example Bug Report Format (BMI App)

| Field | Detail |
| --- | --- |
| **Bug Title** | Incorrect BMI calculation when input is 60kg and 170cm |
| **Bug ID** | BMI-001 |
| **Steps to Reproduce** | 1. Open BMI app. 2. Enter Weight = 60. 3. Enter Height = 170. 4. Click “Calculate.” |
| **Actual Result** | BMI = 12.5 |
| **Expected Result** | BMI should be 20.8 |
| **Build Number** | Version 1.0.0 |
| **Severity** | Major (High) |
| **Priority** | P2 – High |
| **Assignee** | Developer |
| **Reporter** | SQA (Software Quality Assurance) |
| **Reported On** | 31-08-2025 |
| **Testing On** | Android |

---

## How to Prevent Bugs

The best way to prevent bugs is by applying best practices throughout the development lifecycle, not only during testing.

1. **Understand Requirements**: Ensure all requirements are clearly understood by the whole team.
2. **Unit Testing**: Detect bugs early through unit tests.
3. **Code Review**: Have other developers review the code to catch mistakes.
4. **Testing Plan**: Create a comprehensive test plan.
5. **Automated Testing**: Use automation tools to speed up bug detection.
6. **Team Collaboration**: Improve communication and collaboration between developers and testers.

---

## Conclusion

Test scenarios, test cases, and bug reports are interconnected components that strengthen the software testing process. Test scenarios provide an overview of what to test, test cases give detailed execution steps, and bug reports formally document errors for resolution. By implementing proper testing practices and preventive measures such as unit testing, code review, and automation, software teams can minimize bugs, improve system quality, and deliver reliable applications to users.
---
title: "Testing Strategy"
date: 2025-08-25
categories: [Software Testing]
author: Nancy Jiwono
layout: post
description: "Explain about basic concept of testing"
image: /assets/software/testingStrategi.png
comments: true
---

### What is Testing?

**Testing** is the process of evaluating a software product to find defects (*bugs*) and to ensure that the product works according to both **functional** and **non-functional** requirements.

### Objectives of Testing

The main objective of *testing* is **to find errors or defects (*bugs*)** in the software or system and **to ensure quality** before the product is released.

Other objectives include:

- Verification and Validation
- Reducing risk of failure
- Increasing stakeholder confidence
- Ensuring security
- Cost efficiency
- Improving User Experience

---

## Software Testing Life Cycle (STLC)

### Definition

**Software Testing Life Cycle** is a systematic approach to testing software to ensure that the software meets requirements and is free from defects. This process ensures that the software has the **highest quality**, is **reliable**, and **meets end-user needs**.

### STLC Phases

1. **Test Planning**
    - Creating testing strategies
    - Identifying the testing environment
    - Identifying test cases
    - Estimating time and cost
2. **Test Design**
    - Identifying test cases
    - Writing test cases
    - Creating test data and scenarios
    - Identifying expected results
    - Updating the Requirement Traceability Matrix
3. **Test Execution**
    
    This phase includes multiple levels of testing:
    
    - **Component Testing (Unit Testing)**: Testing individual program components; usually carried out by the component developer (except for critical systems).
    - **Integration Testing**: Testing the interaction between subsystems, i.e., groups of integrated components forming a subsystem or system.
    - **System Testing**: Conducted by an independent testing team, based on system specifications.
    - **Acceptance Testing**: The final testing before the system is used by the user; involves testing with real user data.
4. **Testing Reporting & Analysis**
    - **Test summary results**: Presenting numbers of passed, failed, or pending test cases.
    - **Application quality evaluation**: Assessing whether the system meets functional and non-functional specifications.
    - **Bug and issue identification**: Recording errors found during testing, including severity level and fix status.
    - **Improvement recommendations**: Suggesting performance, security, or system stability enhancements.

---

## Classification of Software Testing

*Software Testing* can be classified based on several criteria:

### 1. Based on Abstraction

| Testing Type | Focus / Description | Objective | Example |
| --- | --- | --- | --- |
| **Unit Testing** | Testing the smallest software components (functions, methods, classes) individually. | Verifying individual code unit functionality. | Testing a discount calculation function to ensure accuracy. |
| **Integration Testing** | Testing interactions and communication between two or more previously tested units. | Ensuring that different modules or units work together correctly. | Testing interaction between *login* and user profile modules after successful login. |
| **System Testing** | Testing the entire software system as one integrated unit against all functional and non-functional requirements. | Testing the system holistically against specified requirements. | Testing an *e-commerce* app handling 1000 users simultaneously (*performance testing*). |
| **Acceptance Testing** | Testing from the perspective of **end-users or clients**. | Validating that the system is acceptable by users/clients and meets their business needs. | Client gives final approval before a mobile app is launched to the market. |

### 2. Based on Function

| Testing Type | Focus / Description | Objective | Example |
| --- | --- | --- | --- |
| **Functional Testing** | Testing whether the software works according to its **functional requirements**. | Verifying correct operation, bug-free behavior, and validating outputs as expected. | Testing successful *login* with valid credentials or validating a payment transaction. |
| **Non-Functional Testing** | Testing performance, security, reliability, and other aspects **not directly related to specific functions** (how the system works). | Ensuring the system can handle real-world demands and deliver smooth, high-quality user experience. | Testing a website to handle traffic spikes (e.g., during *flash sale*). |

### 3. Based on Domain

| Testing Type | Focus / Description | Objective | Example |
| --- | --- | --- | --- |
| **Performance Testing** | Testing performance in terms of speed, responsiveness, and stability **under specific loads**. | Ensuring the software can handle high workloads. | Testing a website’s ability to run smoothly under simultaneous user load. |
| **Security Testing** | Identifying security vulnerabilities and protecting data from internal and external threats. | Ensuring the system is secure and user data is protected from attacks. | Testing vulnerability to attacks such as SQL injection or XSS. |
| **Usability Testing** | Evaluating **ease of use** of the software by end-users. | Ensuring the software is easy to use and meets user needs. | Testing whether an app is intuitive, easy to navigate, and features are easily accessible. |

### 4. Based on Structure

| Testing Type | Focus / Description | Advantages | Disadvantages |
| --- | --- | --- | --- |
| **Black-Box Testing** | Tester **does not know internal structure or code**. Focuses on **system functions and output**. | * Relevant for testing from an *end-user* perspective. * Suitable for large functions. * No need for technical code knowledge. | * Not all code paths are tested. * Hard to detect hidden logic bugs. |
| **White-Box Testing** | Tester **knows internal structure and code**. Focuses on **logic flow, algorithms, and data structures**. | * Ensures broader code coverage. * Can find hidden bugs in code. * Helps optimize and improve code quality. | * Requires deep program knowledge. * Time-consuming for complex systems. * Not suitable for testing large user-facing functions. |

---

## Conclusion

**Software Testing** is an integral part of the **Software Development Life Cycle (SDLC)**. Testing is a **critical phase** in software development, to ensure delivery of **high-quality, bug-free software that is appreciated by users**.

---

Hope you enjoyed and learned something new! 🎉 

Thank youu!!! 
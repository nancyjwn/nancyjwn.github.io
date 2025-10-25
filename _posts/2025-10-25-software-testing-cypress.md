---
title: "Cypress"
date: 2025-09-15
categories: [Software Testing]
tags: [Cypress, Java]
author: Nancy Jiwono
layout: post
description: "Explain about Cypress"
image: /assets/software/cypress.png
comments: true
---

## What is Cypress?

**Cypress** is an **end-to-end testing framework** for modern web applications (such as React, Vue, Angular, etc.).

### Cypress in Testing Levels

Although primarily positioned as an **End-to-End testing tool**, Cypress can also be used for **Integration Testing** and **Unit Testing**.

---

## Cypress Setup and Basic Commands

### Cypress Setup

1. **Requirement**: Node.js is required.
2. **Installation**:
    
    ```bash
    npm init -y
    npm install cypress --save-dev
    
    ```
    
3. **Open Cypress**:
    
    ```bash
    npx cypress open
    
    ```
    
4. **Run with specific browser**:
    
    ```bash
    npx cypress run --browser chrome/firefox/edge
    
    ```
    

### Basic Cypress Commands

| Command | Function |
| --- | --- |
| `cy.visit('URL')` | Opens a web page |
| `cy.get('selector')` | Selects an element using a selector |
| `cy.contains('text')` | Selects an element based on text |
| `cy.click()` | Clicks a button or link |
| `cy.type('text')` | Types into an input field |
| `cy.url()` | Gets the current active URL |

---

## Advantages of Cypress

Cypress differs from Selenium or Playwright due to its modern architecture and several standout features:

- **Interactive Test Runner** – allows developers to see tests run live in the browser.
- **Time Travel** – provides snapshots of the application’s state at each step of the test.
- **Automatic Waits** – Cypress automatically waits for elements to appear and be ready before executing the next command, avoiding timing issues.

---

## Case Study and Conclusion

### Example Test Cases (SauceDemo.com)

| ID | Test Case | Steps | Expected Result |
| --- | --- | --- | --- |
| **TC01** | Login with valid username & password | Enter `standard_user`, enter `secret_sauce`, click Login | Successfully redirected to inventory page |
| **TC02** | Login with wrong password | Enter `standard_user`, enter `wrong_pass`, click Login | Error message: *"Username and password do not match"* |
| **TC03** | Login with empty username | Leave username blank, enter `secret_sauce`, click Login | Error message: *"Username is required"* |

---

## Conclusion

Cypress is a modern testing framework designed for end-to-end testing of web applications. With easy installation and advanced features such as an interactive test runner, time travel, and automatic waits, it simplifies UI-based testing and makes it faster and more efficient. Its clear test structure and intuitive commands allow developers to simulate real user behavior seamlessly. Overall, Cypress is a reliable tool for improving the quality and dependability of modern web applications.
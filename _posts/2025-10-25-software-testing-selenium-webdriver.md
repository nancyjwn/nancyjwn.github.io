---
title: "Selenium Webdriver"
date: 2025-09-15
categories: [Software Testing]
tags: [Python, Selenium]
author: Nancy Jiwono
layout: post
description: "Explain about Selenium Webdriver"
image: /assets/software/seleniumWebdriver.png
comments: true
---

## What is Selenium?

- **Selenium** is an open-source framework for **browser automation**.
- It is widely used to **test web applications** with different programming languages.
- Supports multiple browsers such as Chrome, Firefox, Edge, and Safari.

### Advantages of Selenium

Main reasons for using Selenium include:

- **Open-source and free**.
- **Multi-platform** support (Windows, macOS, Linux).
- Supports multiple programming languages (*Python, Java, C#, JavaScript*).
- Can **integrate with other testing frameworks** such as Pytest, JUnit, and TestNG.
- Large community support and comprehensive documentation.

---

## What is Selenium WebDriver?

- **WebDriver** is the **core component** of Selenium.
- Acts as a **bridge between test code and the browser**.
- Its role is to **control the browser** (e.g., clicks, text input, navigation, and validation).

### Selenium WebDriver Workflow

1. **Test Scripts** (written in Java, Python, PHP, C#, Perl, or Ruby).
2. The script is sent to **WebDriver**.
3. WebDriver controls the **browser** (Chrome, Firefox, Edge, Safari, etc.) to execute testing commands.

---

## Basic Automation Process with Python

The practical steps of web automation include:

- Installing Selenium with Python.
- Launching a browser using Selenium.
- Interacting with HTML elements (click, text input, etc.).

---

## Example Test Scenarios and Test Cases

Example scenarios demonstrated in the live coding session (likely using SauceDemo as the target application):

### Test Scenarios

- **TS-001**: Successful login on the SauceDemo page.
- **TS-002**: Failed login with incorrect credentials.
- **TS-003**: Adding a product to the cart.

### Test Cases

| ID | Description | Steps | Expected Result |
| --- | --- | --- | --- |
| **TC-001** | Successful login | Enter `standard_user` & `secret_sauce`. Click Login. | User is redirected to the *inventory* page. |
| **TC-002** | Failed login | Enter invalid credentials. Click Login. | Error message is displayed. |
| **TC-003** | Add product to cart | Successful login → Click "Add to cart". | Cart count increases by 1. |

Code Source visit the [GitHub](https://github.com/MQAFSI23/basic-of-selenium).  

---

## Conclusion

Selenium WebDriver is a powerful tool for automating browser interactions and testing web applications. Its open-source nature, cross-platform support, and compatibility with various languages and testing frameworks make it highly flexible. By mastering Selenium WebDriver, testers can create effective automated test scripts, reduce manual testing effort, and improve software quality and reliability.
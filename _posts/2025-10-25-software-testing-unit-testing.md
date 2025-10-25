---
title: "Unit Testing"
date: 2025-09-08
categories: [Software Testing]
tags: [Python, Java, JavaScript]
author: Nancy Jiwono
layout: post
description: "Explain about Unit Testing"
image: /assets/software/unitTesting.png
comments: true
---

## What is Unit Testing?

**Unit testing** is a type of software testing that focuses on testing the **smallest units** of a software system.

Typically, this includes testing **functions**, **methods**, and **classes**.

- Unit testing checks components independently, without depending on other systems, focusing only on function-by-function verification.
- It is usually the **earliest test** performed by developers before moving on to other tests, such as **integration tests**, **functional tests**, or **end-to-end tests**.

Based on the **Test Pyramid**, Unit Testing sits at the base layer, making it **faster and cheaper** compared to Integration and End-to-End (E2E) testing.

### Analogy

Unit testing can be compared to checking each car component individually before assembling the car.

If each component passes the test, the assembled car will be of good quality.

If a problem occurs later, developers know it does not come from the basic components.

---

## Why is Unit Testing Important?

Unit testing ensures the **reliability, quality, and maintainability** of the code being written.

1. **Early Bug Detection**: Catches bugs early in development, making them cheaper and easier to fix.
2. **Saves Time and Costs**: Reduces repair costs later in the development cycle.
3. **Improves Code Quality**: Encourages developers to write structured, modular, and testable code.
4. **Supports Refactoring**: Acts as a safety net during code changes, immediately identifying broken functionality.
5. **Living Documentation**: Serves as executable documentation, showing how functions or classes should be used.
6. **Boosts Confidence**: Gives developers assurance in their code before release.

---

## Arrange, Act, Assert (AAA) Pattern

**Arrange-Act-Assert (AAA)** is a widely used structure for writing unit tests.

1. **ARRANGE**: Prepare the test setup or initial conditions.
2. **ACT**: Execute the function or method to be tested.
3. **ASSERT**: Verify that the result matches expectations.

---

## Popular Frameworks

### JUnit 5 (Java)

- **Definition**: The de facto and pioneering unit testing framework for Java.
- **When to Use**: For Java or JVM-based languages like Kotlin or Scala.
- **Strengths**: Full integration, a mature ecosystem, annotation-based structure.

### Jest (JavaScript)

- **Definition**: A JavaScript testing framework developed by Meta, efficient and user-friendly.
- **When to Use**: With React, Node.js, TypeScript, or other modern front-end frameworks.
- **Strengths**: Zero configuration, batteries-included, snapshot testing support.

### Pytest (Python)

- **Definition**: Simple, readable, and powerful with advanced hidden features.
- **When to Use**: For any Python project — from scripts and web apps to data science and APIs.
- **Strengths**: Simple syntax, powerful fixtures, detailed error reporting.

---

## Live Coding Examples

### Using Pytest (Python)

Testing a `ShoppingCart` class with functions: `add`, `get_items`, `update`, and `delete`.

- Includes success cases (adding items) and failure cases (adding items beyond `max_size` raises `OverflowError`, or deleting non-existent items raises `ValueError`).
- Uses `pytest.raises()` to check for expected exceptions.

Here is code photo:
![Pytest](/assets/software/liveCodingUnitTestingPython.png)  

### Using JUnit 5 (Java)

Testing a `BankAccount` class with functions: `deposit` and `withdraw`.

| Method Tested | Test Case | Assertions |
| --- | --- | --- |
| `deposit(int amount)` | `testDeposit()`: Add 100 to balance | `assertEquals(100, account.getBalance())` verifies final balance is 100 |
| `withdraw(int amount)` | `testWithdrawSuccess()`: Withdraw 150 from initial balance of 200 | `assertEquals(50, account.getBalance())` verifies remaining balance is 50 |
| `withdraw(int amount)` | `testWithdrawInsufficientFunds()`: Attempt to withdraw more than available balance | `assertThrows(IllegalArgumentException.class, …)` ensures exception is thrown, with error message “Saldo tidak cukup!” |

Here is code photo: 
![Junit](/assets/software/liveCodingUnitTestingJava.png)  

---

## Conclusion

Unit testing is the **foundation of software testing** that ensures code reliability, maintainability, and confidence in releases.

By adopting the **AAA pattern** and leveraging popular frameworks such as JUnit, Jest, and Pytest, developers can:

- Catch bugs early,
- Reduce costs,
- Improve overall code quality,
- Safely perform code refactoring, and
- Build more robust, scalable, and maintainable software systems.

In short, **unit testing is not just about finding bugs — it’s about building better software from the start.**
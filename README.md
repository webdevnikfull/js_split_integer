# 🧪 QA Portfolio: Integer Splitting Algorithm & Unit Testing

> **About this repository:** This project focuses on the foundation of the Agile Testing Pyramid: **Unit Testing**. It demonstrates how to validate core mathematical and logical algorithms (splitting an integer into nearly equal parts) using automated unit tests, static analysis, and continuous integration.

![JavaScript](https://img.shields.io/badge/-JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Unit Testing](https://img.shields.io/badge/-Unit_Testing-C21325?style=for-the-badge&logo=jest&logoColor=white)
![ESLint](https://img.shields.io/badge/-Static_Analysis-4B32C3?style=for-the-badge&logo=eslint&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/-CI/CD-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)

## 🎯 Project Overview

This repository contains a specialized JavaScript utility function designed to split a given integer into a specified number of parts as evenly as possible (`src/splitInteger.js`). 

As a **QA Automation Engineer**, my objective in this project is to ensure the algorithmic logic behaves predictably by writing and maintaining comprehensive unit tests (`src/splitInteger.test.js`) that cover standard use cases, boundary values, and edge conditions directly at the code level.

## 🛠️ QA Tech Stack & Tools

* **Testing Level:** Unit Testing (White-Box Testing)
* **CI/CD Pipeline:** GitHub Actions (Automated test execution on every push/PR)
* **Static Code Analysis (Shift-Left QA):** ESLint
* **Core Language:** JavaScript (ES6+)

## 📊 Test Strategy & Coverage

The testing strategy is engineered to isolate and tightly validate the algorithmic business logic:

### 1. Unit Testing (Code Level Validation)
Located in `src/splitInteger.test.js`, the automated test suite verifies:
* Correct mathematical distribution of integers across a given number of parts.
* Robust handling of edge cases (e.g., splitting into 1 part, numbers smaller than parts, remainder distributions).
* Data integrity and deterministic array return formats.

### 2. Continuous Integration (CI/CD)
The project is seamlessly integrated with GitHub Actions (`.github/workflows/test.yml`). Every commit automatically triggers a pipeline that:
* Runs `ESLint` to catch syntax, logic, and style errors early in the development lifecycle.
* Executes the full unit test suite to prevent regressions from reaching production.

## 🚀 How to Run the Tests Locally

To evaluate the unit tests and static analysis tools on your local machine, follow these steps:

### 1. Environment Setup
Clone the repository and install the required Node.js dependencies:
```bash
npm install

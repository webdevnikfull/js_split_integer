# 🧮 QA: Split Integer - Algorithm Test Suite

> ### A precise unit testing suite built with **Jest** to validate mathematical algorithms and array distribution logic.

This repository demonstrates how to architect comprehensive automated tests for algorithmic functions. It focuses on validating the `splitInteger` function[cite: 4], ensuring it meets strict mathematical constraints, handles edge cases, and correctly processes Equivalence Classes (evenly divisible vs. indivisible numbers).

---

## 🎯 System Under Test (SUT)

The function `splitInteger(value, numberOfParts)` is responsible for dividing a given positive integer (`value`) into a specified number of parts (`numberOfParts`)[cite: 4]. 

**Core Business Rules to Validate:**
1. **Length Constraint:** The returned array must contain exactly `numberOfParts` elements[cite: 4].
2. **Distribution Constraint:** The difference between the maximum and minimum numbers in the resulting array must be `<= 1`[cite: 4].
3. **Ordering Constraint:** The array must be sorted in ascending order (from lowest to highest)[cite: 4].
4. **Implicit Integrity:** The sum of all elements in the returned array must exactly equal the original `value`.

**Examples of Expected Behavior:**
- `splitInteger(8, 1)` returns `[8]`[cite: 4]
- `splitInteger(6, 2)` returns `[3, 3]`[cite: 4]
- `splitInteger(17, 4)` returns `[4, 4, 4, 5]`[cite: 4]
- `splitInteger(32, 6)` returns `[5, 5, 5, 5, 6, 6]`[cite: 4]

*(Note: Input argument validation is deliberately out of scope as inputs are guaranteed to be valid positive integers)*[cite: 4].

---

## 🧪 QA Strategy & Test Design

To ensure total confidence in the algorithm, the test suite leverages **Jest expectations**[cite: 4] and is structured around the following test scenarios:

| Testing Technique | Scenario Covered | QA Focus |
| :--- | :--- | :--- |
| **Equivalence Class Partitioning** | Evenly divisible numbers (e.g., 6 into 2 parts)[cite: 4]. | Verifying that all elements in the array are identical. |
| **Equivalence Class Partitioning** | Numbers with remainders (e.g., 17 into 4 parts)[cite: 4]. | Validating the remainder distribution and the `max - min <= 1` rule[cite: 4]. |
| **Boundary Value Analysis (BVA)** | Splitting into exactly 1 part[cite: 4]. | Checking array structure when `numberOfParts === 1`. |
| **Implicit Requirement Validation** | Array summation. | Using `Array.prototype.reduce()` within tests to assert that no value was lost during the split. |
| **Order Validation** | Ascending sort check[cite: 4]. | Iterating through the result to assert `arr[i] <= arr[i+1]`. |

---

## 🧰 Tech Stack

- **Environment:** Node.js
- **Language:** JavaScript (ES6+)
- **Testing Framework:** [Jest](https://jestjs.io/) 

---

## ⚙️ How to Run the Tests

To execute the test suite locally:

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/webdevnikfull/js_split_integer.git](https://github.com/webdevnikfull/js_split_integer.git)
   cd js_split_integer

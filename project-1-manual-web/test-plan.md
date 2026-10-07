# Test Plan - Project 1: Sauce Demo Manual Testing

## 1. Introduction
This Test Plan describes the strategy, scope, resources, and schedule for manual testing of the Sauce Demo e-commerce web application (https://www.saucedemo.com).

## 2. Objectives
- Ensure critical workflows (login, product sorting, cart management, and checkout) function without blocker or high-severity defects.
- Validate cross-browser layout consistency and basic error handling across core user journeys.

## 3. Scope of Testing

### In-Scope
- **Authentication:** Standard login, locked-out login, invalid credentials, logout, and session state.
- **Product Catalog:** Product list display, sorting (A-Z, Z-A, Price Low-High, Price High-Low), product detail view.
- **Cart & Checkout:** Add/remove items, cart badge count updates, mandatory user detail input validation, payment overview calculation, order completion.

### Out-of-Scope
- Performance and load testing (handled in API/automation phases).
- Security penetration testing.
- Backend database schema verification (covered in Project 2).

## 4. Test Strategy & Approaches
- **Equivalence Partitioning (EP):** Applied to form fields and login scenarios.
- **Boundary Value Analysis (BVA):** Applied to text input lengths and cart item counts.
- **Exploratory Testing:** Focused on unexpected user behaviors and page navigation edge cases.

## 5. Pass / Fail Criteria
- **Pass:** 100% execution of high-priority test cases with zero open Critical or Blocker defects.
- **Fail:** Unresolved blocker issues preventing order placement or login workflows.

## 6. Deliverables
- Test Plan (`test-plan.md`)
- Test Cases (`test-cases.csv`)
- Requirements Traceability Matrix (`requirements-traceability-matrix.csv`)
- Bug Reports (`bugs/BUG-001.md` ... `BUG-010.md`)
- Test Summary Report (`test-summary-report.md`)

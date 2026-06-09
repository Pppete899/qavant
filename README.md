# Qavant.dev — Enterprise Employee Operations & QA Showcase Platform

Welcome to the official repository of **Qavant**, a production-ready B2B Employee Engagement & Operations platform. 

> 🎯 **Project Purpose:** This platform was fully designed, architected, and developed from scratch to serve as a live production showcase of my Full-Stack development and advanced **QA Automation / Test Engineering capabilities**.

---

## 🚀 Live Demo & Production
* **Production Link:** [qavant.dev](https://qavant.dev)
* **Target Audience:** B2B / Internal Communications & HR Tech

---

## 🏗️ Architecture & QA Strategy (Proof of Work)

This repository demonstrates industry-level best practices in Software Quality Assurance. Instead of manual testing, the entire ecosystem is built with **Automation-First** mindset.

### 1. End-to-End (E2E) Testing
* **Framework:** Playwright (TypeScript) / *[Prispôsob podľa tvojho stacku, napr. Cypress]*
* **Design Pattern:** **Page Object Model (POM)** for maximum test maintainability and clean code separation.
* **Coverage:** Complete automated coverage of critical user journeys (User Registration, Auth flows, Form Submissions, and Dynamic UI elements).

### 2. API & Integration Testing
* **Framework:** Playwright API / Supertest / *[Doplň svoj nástroj]*
* **Coverage:** Automated validation of REST/GraphQL endpoints, HTTP status codes, JSON payload schemas, and RBAC (Role-Based Access Control) security boundaries.

### 3. CI/CD & DevOps Pipeline
* **Tool:** GitHub Actions
* **Workflow:** Every Pull Request or Merge to `main` automatically triggers a headless test runner executing the E2E suite across multiple browsers (Chromium, Firefox, WebKit). Deployment to production is blocked if a single test fails.

---

## 🛠️ Tech Stack

* **Frontend:** React / Next.js / TypeScript *[Uprav podľa reality]*
* **Backend:** Node.js / Express / Python *[Uprav podľa reality]*
* **Testing:** Playwright, Axe-core (Accessibility), k6 (Performance)
* **CI/CD:** GitHub Actions / Docker

---

## ⚙️ How to Run the Automated Tests Locally

To clone the project and execute the automated test suite, run the following commands:

```bash
# Clone the repository
git clone [https://github.com/YOUR_GITHUB_USERNAME/qavant.git](https://github.com/YOUR_GITHUB_USERNAME/qavant.git)

# Install dependencies
npm install

# Run all automated E2E tests (Headless mode)
npx playwright test

# Open interactive test report
npx playwright show-report

# Qavant.dev — QA Automation & Test Engineering Showcase

Official repository of **Qavant** — a production portfolio site, designed, built and continuously tested from scratch as a live showcase of my **QA Automation / Test Engineering** work.

> 🎯 **Project Purpose:** qavant.dev is the *system under test*. The site is intentionally simple; the engineering is in the test infrastructure around it — three independent suites, three technologies, three CI pipelines, with live pass-rate metrics fed back onto the page. No claim without clickable proof.

---

## 🚀 Live Demo & Production

* **Production:** [qavant.dev](https://qavant.dev)
* **Languages:** Slovak / English / German (auto-detected, switchable, persisted)
* **Audience:** QA / SDET hiring · fintech & DACH

---

## 🏗️ Architecture & QA Strategy (Proof of Work)

The site itself is a single static `index.html` (inline CSS + vanilla JS, no framework, no backend) on Netlify, auto-deployed from `main`. Everything below tests *that* site, automation-first, from three separate repositories.

[![Playwright](https://github.com/peterolah-qa/qavant-tests/actions/workflows/playwright.yml/badge.svg)](https://github.com/peterolah-qa/qavant-tests/actions/workflows/playwright.yml)
[![Newman](https://github.com/peterolah-qa/qavant-api-tests/actions/workflows/api-tests.yml/badge.svg)](https://github.com/peterolah-qa/qavant-api-tests/actions/workflows/api-tests.yml)
[![Selenium](https://github.com/peterolah-qa/qavant-selenium/actions/workflows/selenium.yml/badge.svg)](https://github.com/peterolah-qa/qavant-selenium/actions/workflows/selenium.yml)

### 1. End-to-End (E2E) Testing
* **Frameworks:** Playwright (TypeScript) and Selenium 4 (Java / TestNG) — the same site covered by two stacks.
* **Design Pattern:** Page Object Model (POM); explicit waits only, no `sleep`.
* **Coverage:** Critical journeys — language switching (SK/EN/DE), contact form, responsive layout, accessibility (axe-core / WCAG 2 AA), live-metrics widget, ISTQB badge link contract. 145 Playwright tests across 5 browsers + 11 Selenium tests.

### 2. API & Integration Testing
* **Framework:** Postman / Newman.
* **Coverage:** REST CRUD, authentication, JSON schema and negative tests, plus an HTTP contract check on qavant.dev. 27 assertions.

### 3. CI/CD Pipeline
* **Tool:** GitHub Actions.
* **Workflow:** Each suite runs on every push to `main` and daily on a schedule, headless across Chromium, Firefox and WebKit. After each run it publishes a `status.json` (read by the site for live metrics) and an HTML / Allure report to GitHub Pages — including failed runs.

| Repository | Stack | Tests |
|---|---|---|
| [qavant-tests](https://github.com/peterolah-qa/qavant-tests) | Playwright / TypeScript | 145 (×5 browsers) |
| [qavant-api-tests](https://github.com/peterolah-qa/qavant-api-tests) | Postman / Newman | 27 assertions |
| [qavant-selenium](https://github.com/peterolah-qa/qavant-selenium) | Java 17 / Selenium 4 / TestNG / Maven | 11 |

---

## 🛠️ Tech Stack

* **Site:** HTML5, CSS3, vanilla JavaScript (single file, no bundler), trilingual i18n, JSON-LD, Netlify Forms.
* **Testing:** Playwright, Selenium, Postman/Newman, axe-core (accessibility).
* **CI/CD:** GitHub Actions, Allure & HTML reporting on GitHub Pages.
* **Hosting:** Netlify (auto-deploy from `main`).

---

## ⚙️ Run Locally

The site is static — no dependencies, no build:

```bash
git clone https://github.com/peterolah-qa/qavant.git
cd qavant
npx serve .
```

The automated suites live in their own repos. Example for the Playwright suite:

```bash
git clone https://github.com/peterolah-qa/qavant-tests.git
cd qavant-tests
npm install
npx playwright test
npx playwright show-report
```

---

## 📬 Contact

**Peter Oláh** — QA Automation Engineer · ISTQB® Certified Tester (CTFL v4)
[peterolah@qavant.dev](mailto:peterolah@qavant.dev) · [qavant.dev](https://qavant.dev) · [LinkedIn](https://www.linkedin.com/in/peter-olah-8ab858137/)

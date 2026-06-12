# 2. Test Strategy

**Project:** Vendor Invoice Management Portal — B2B Use Case

---

## 2.1 Project Overview

The Vendor Invoice Management Portal is a B2B web application enabling vendors to submit invoices against Purchase Orders, and allowing the internal Accounts Payable (AP) team to review, approve, or reject those invoices. It also supports payment forwarding, email notifications, reporting, and role-based access control across 7 functional requirements.

---

## 2.2 Test Objectives

- Verify all 7 functional requirements are correctly implemented
- Validate role-based access control prevents unauthorized operations
- Confirm multi-step approval workflows execute correctly with proper notifications
- Ensure the portal performs reliably under expected concurrent user load
- Validate data integrity across UI, API, and database layers
- Identify and document all defects with sufficient detail for developer resolution

---

## 2.3 Scope

### In Scope

- Vendor registration and authentication
- Invoice submission, validation, and file upload
- AP team approval and rejection workflows
- Payment forwarding integration
- Email notification triggers
- Monthly report generation and export
- Role-based access control and security
- API layer testing for all backend services
- Database integrity verification

### Out of Scope

- Third-party payment gateway internal logic
- ERP/SAP system testing (integration boundary only)
- Network infrastructure and server provisioning
- End-user device procurement

---

## 2.4 Test Approach by Phase

| Phase | Activities | Techniques |
|-------|-----------|------------|
| Requirements Analysis | Review BRD, identify ambiguities, define acceptance criteria | Checklist review, question sessions |
| Test Planning | Define scope, risks, approach, environments, entry/exit criteria | Risk-based prioritisation |
| Test Design | Write test scenarios and detailed test cases, prepare test data | EP, BVA, Decision Tables |
| Functional Testing | UI, API, and DB layer testing of all features | Manual + exploratory testing |
| Non-Functional Testing | Performance, security, accessibility, compatibility | JMeter, OWASP ZAP, axe |
| Integration Testing | Email service, ERP, payment gateway boundary tests | Contract testing, mocks |
| UAT | Business team validates against real-world scenarios | Scripted + exploratory UAT |
| Deploy Verification | Smoke tests, config checks, rollback readiness | Smoke test checklist |

---

## 2.5 Test Environments

| Environment | Purpose | Notes |
|-------------|---------|-------|
| DEV | Developer unit & integration testing | Not used by QA team; used by developers |
| QA / SIT | Functional, API, and regression testing | QA team primary environment; refreshed per sprint |
| Staging / UAT | User Acceptance Testing | Mirror of production; business team access |
| Production | Smoke test post-deployment only | No destructive testing; read-only verification |

---

## 2.6 Entry and Exit Criteria

### Entry Criteria (to begin testing)

- Approved and baselined requirements document available
- Test environment deployed and accessible
- Test data prepared and loaded
- Build deployed with release notes
- Test plan and test cases reviewed and approved

### Exit Criteria (to close testing)

- 100% of planned test cases executed
- All Critical and High severity defects resolved and re-tested
- Test coverage ≥ 90% of requirements
- Test Execution Report published and signed off
- No open blockers on agreed in-scope features

---

## 2.7 Tools

| Purpose | Tool | Usage |
|---------|------|-------|
| Test Management | Jira / Zephyr | Test case authoring, execution, defect tracking |
| API Testing | Postman | REST API contract and regression testing |
| UI Automation | Selenium / Cypress | Regression suite for high-frequency flows |
| Performance | JMeter / k6 | Load and stress testing of critical endpoints |
| Security | OWASP ZAP / Burp Suite | Vulnerability scanning, OWASP Top 10 checks |
| Accessibility | axe / Lighthouse | WCAG 2.1 AA compliance checks |
| Bug Tracking | Jira | Defect logging, triage, and resolution tracking |

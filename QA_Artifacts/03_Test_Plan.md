# 3. Test Plan

**Project:** Vendor Invoice Management Portal  
**Version:** 1.0 | **Date:** June 2026

---

## 3.1 Purpose

This Test Plan defines the scope, resources, schedule, risks, and detailed approach for testing the Vendor Invoice Management Portal. It serves as the authoritative reference for all QA activities during this project.

---

## 3.2 Features to Be Tested

| Req ID | Feature | Priority | Test Type | Risk |
|--------|---------|----------|-----------|------|
| REQ-01 | Vendor Registration & Login | High | Functional, Security | Medium |
| REQ-02 | Invoice Submission & Upload | Critical | Functional, API, DB | High |
| REQ-03 | AP Approval / Rejection Workflow | Critical | Functional, Workflow | High |
| REQ-04 | Payment Forwarding Integration | High | Integration, API | High |
| REQ-05 | Email Notification Triggers | Medium | Functional, Integration | Medium |
| REQ-06 | Monthly Report Generation | Medium | Functional, Performance | Low |
| REQ-07 | Role-Based Access Control (RBAC) | Critical | Security, Functional | Critical |

---

## 3.3 Risk Register

| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|------------|
| Requirements not finalised before testing | High | High | Raise blocker; test only confirmed requirements |
| Test environment instability | Medium | High | Dedicated QA env; daily health checks |
| Payment gateway integration delays | Medium | High | Use mock/stub for early testing; real integration in UAT |
| Insufficient test data (POs, vendors) | High | Medium | Prepare test data scripts upfront |
| Timeline compression reducing coverage | Medium | High | Risk-based prioritisation; defer low-risk scenarios |
| Security vulnerabilities in file upload | Medium | Critical | Dedicated security test cycle with OWASP ZAP |

---

## 3.4 Resource Allocation

| Role | Responsibilities | Allocation |
|------|----------------|------------|
| QA Lead | Strategy, planning, risk management, sign-off | Full-time |
| QA Engineer (Functional) | Test design, manual execution, defect reporting | 2 x Full-time |
| QA Engineer (Automation) | API and regression automation in Postman/Cypress | 1 x Full-time |
| Performance Tester | JMeter/k6 load scripts; performance reporting | Part-time (Phase 6) |
| Security Analyst | OWASP testing, vulnerability assessment | Part-time (Phase 6) |

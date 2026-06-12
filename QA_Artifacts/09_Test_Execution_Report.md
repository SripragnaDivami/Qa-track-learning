# 9. Test Execution Report

**Project:** Vendor Invoice Management Portal  
**Version:** 1.0 | **Date:** June 2026

---

## 9.1 Execution Summary

| Metric | Count | Percentage |
|--------|-------|-----------|
| Total Test Cases Planned | 35 | 100% |
| Test Cases Executed | 20 | 57% |
| Passed | 14 | 70% (of executed) |
| Failed | 6 | 30% (of executed) |
| Blocked | 2 | 10% (of executed) |
| Not Executed | 15 | 43% (of planned) |
| Total Defects Raised | 8 | — |
| Critical Defects Open | 2 | — |
| High Defects Open | 3 | — |

---

## 9.2 Defect Summary by Severity

| Severity | Total | Open | Fixed | Verified |
|----------|-------|------|-------|---------|
| Critical | 2 | 2 | 0 | 0 |
| High | 4 | 3 | 1 | 0 |
| Medium | 1 | 0 | 1 | 0 |
| Low | 1 | 0 | 1 | 0 |

---

## 9.3 Observations and Recommendations

- **RBAC Critical Gap:** RBAC module has a critical gap — vendor role can access AP URLs directly. This must be fixed before UAT.
- **Invoice Validation Incomplete:** Invoice submission validation is incomplete — file attachment is not enforced server-side. Fix required.
- **Notification Testing Blocked:** Notification triggers for REQ-05 have not been tested. Test environment email service is not yet configured.
- **Payment Integration Blocked:** Payment integration (REQ-04) testing is blocked pending availability of the payment gateway sandbox.
- **Automation Recommendation:** Recommend adding automated regression tests for all login and RBAC scenarios before next sprint.

---

## 9.4 Sign-Off Status

| Role | Name | Signature | Date |
|------|------|-----------|------|
| QA Lead | | | |
| Project Manager | | | |
| Business Owner | | | |

# 8. Requirements Traceability Matrix (RTM)

**Project:** Vendor Invoice Management Portal

---

The RTM links every requirement to its test scenarios and test cases, ensuring full coverage. Every requirement must have at least one test scenario and at least one test case. Gaps indicate missing coverage and must be addressed before testing closes.

| Req ID | Requirement | Test Scenarios | Test Case IDs | Exec Status | Result |
|--------|------------|----------------|---------------|-------------|--------|
| REQ-01 | Vendor registration and login | TS-001, TS-002, TS-003, TS-004, TS-005, TS-006, TS-007 | TC-001, TC-002, TC-003 | Executed | Pass |
| REQ-02 | Invoice submission against POs | TS-008 to TS-014 | TC-010, TC-011, TC-012 | Executed | Fail |
| REQ-03 | AP team approval / rejection | TS-015 to TS-019 | TC-020, TC-021 | In Progress | — |
| REQ-04 | Payment forwarding for approved invoices | TS-020, TS-021 | TC-030 to TC-035 | Not Started | — |
| REQ-05 | Email notifications on status changes | TS-022 to TS-025 | TC-040 to TC-048 | Not Started | — |
| REQ-06 | Monthly invoice activity reports | TS-026, TS-027, TS-028 | TC-050 to TC-055 | Not Started | — |
| REQ-07 | Role-based access control | TS-029 to TS-035 | TC-029, TC-030 | Executed | Fail |

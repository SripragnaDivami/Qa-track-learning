# 4. Test Scenarios

**Project:** Vendor Invoice Management Portal

---

Test scenarios represent high-level 'what to test' items — one per user situation or feature area — derived from the 7 requirements. Each scenario maps to one or more detailed test cases.

| Scenario ID | Feature Area | Scenario Description |
|-------------|-------------|----------------------|
| TS-001 | Vendor Registration | Vendor can successfully register with all required details |
| TS-002 | Vendor Registration | Registration fails with missing or invalid mandatory fields |
| TS-003 | Vendor Registration | Duplicate vendor registration is prevented |
| TS-004 | Vendor Login | Registered vendor can log in with valid credentials |
| TS-005 | Vendor Login | Login fails with incorrect password and shows appropriate error |
| TS-006 | Vendor Login | Account is locked after N consecutive failed login attempts |
| TS-007 | Vendor Login | Session expires after configured idle timeout |
| TS-008 | Invoice Submission | Vendor submits a valid invoice linked to an existing PO |
| TS-009 | Invoice Submission | Submission fails when a required invoice field is missing |
| TS-010 | Invoice Submission | File upload rejects unsupported format (e.g., .exe, .zip) |
| TS-011 | Invoice Submission | File upload rejects files exceeding the maximum size limit |
| TS-012 | Invoice Submission | System prevents duplicate invoice number submission |
| TS-013 | Invoice Submission | Vendor can view list of their submitted invoices and status |
| TS-014 | Invoice Submission | Vendor cannot submit invoice against a non-existent or closed PO |
| TS-015 | AP Approval Workflow | AP user can view all pending invoices in their queue |
| TS-016 | AP Approval Workflow | AP user approves a valid invoice and it moves to payment queue |
| TS-017 | AP Approval Workflow | AP user rejects an invoice with a mandatory reason |
| TS-018 | AP Approval Workflow | Rejected invoice can be resubmitted by the vendor with corrections |
| TS-019 | AP Approval Workflow | Multi-level approval escalates correctly to next approver |
| TS-020 | Payment Processing | Approved invoice is forwarded to the payment system with correct data |
| TS-021 | Payment Processing | Payment confirmation is stored and visible on the invoice record |
| TS-022 | Notifications | Vendor receives email when invoice is submitted successfully |
| TS-023 | Notifications | Vendor receives email when invoice is approved |
| TS-024 | Notifications | Vendor receives email when invoice is rejected (with reason) |
| TS-025 | Notifications | AP team receives email when a new invoice is pending their review |
| TS-026 | Reporting | AP manager can generate a monthly invoice activity report |
| TS-027 | Reporting | Report can be exported in Excel and PDF formats |
| TS-028 | Reporting | Report can be filtered by vendor, date range, and status |
| TS-029 | Access Control | Vendor cannot access AP team approval screens |
| TS-030 | Access Control | AP Clerk cannot access payment processing module |
| TS-031 | Access Control | Unauthenticated user is redirected to login page on all protected routes |
| TS-032 | Access Control | Admin can create, modify, and deactivate user accounts |
| TS-033 | Security | File upload does not execute malicious scripts or payloads |
| TS-034 | Security | Invoice API endpoints reject requests without valid auth tokens |
| TS-035 | Performance | Invoice list page loads within 3 seconds with 500 invoices |

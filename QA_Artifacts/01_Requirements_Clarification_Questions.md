# 1. Requirements Clarification Questions

**Project:** Vendor Invoice Management Portal  
**Document Type:** QA Artifacts Package  
**Version:** 1.0 | **Prepared By:** QA Team | **Date:** June 2026

---

Before any test design begins, the QA engineer must challenge ambiguous requirements. The following questions were identified against each of the 7 functional requirements.

| Ref | Clarification Question | Client Response / Resolution |
|-----|------------------------|------------------------------|
| **REQ-01** | **Vendors can register and log in to the portal** | |
| Q1 | What information is required during vendor registration (company name, GST/tax ID, bank details, contact person)? | Pending |
| Q2 | Is there an approval/verification step before a vendor account is activated? | Pending |
| Q3 | What authentication method is required — username/password, OTP, SSO, or multi-factor? | Pending |
| Q4 | What is the password policy (length, complexity, expiry)? | Pending |
| Q5 | Can a single vendor company have multiple user accounts with different roles? | Pending |
| Q6 | How does account recovery work — email link, admin reset, or security questions? | Pending |
| Q7 | Should there be account lockout after N failed login attempts? | Pending |
| Q8 | Is there a session timeout requirement for logged-in users? | Pending |
| **REQ-02** | **Vendors can submit invoices against purchase orders** | |
| Q9 | What file formats are accepted for invoice upload (PDF, Excel, image, ZIP)? | Pending |
| Q10 | What is the maximum allowed file size per invoice? | Pending |
| Q11 | Can a vendor submit multiple invoice files in a single submission? | Pending |
| Q12 | Must every invoice be linked to an existing Purchase Order? What happens if the PO does not exist? | Pending |
| Q13 | What mandatory fields must be present on the invoice (invoice number, date, PO number, line items, tax, total)? | Pending |
| Q14 | Can the same invoice number be submitted more than once by the same vendor? | Pending |
| Q15 | Can a vendor edit or withdraw a submitted invoice before it is reviewed? | Pending |
| Q16 | Is there a deadline or cut-off date by which invoices for a period must be submitted? | Pending |
| Q17 | Should the system perform any automated validation on the invoice amounts vs. PO values? | Pending |
| **REQ-03** | **The AP team can view, approve, or reject invoices** | |
| Q18 | Is approval a single-step or multi-level workflow (e.g., team lead → finance manager)? | Pending |
| Q19 | Is rejection mandatory to include a reason/comment? Is this visible to the vendor? | Pending |
| Q20 | Can a rejected invoice be resubmitted by the vendor? How many times? | Pending |
| Q21 | Can an AP user reassign an invoice to another approver? | Pending |
| Q22 | Is there a Service Level Agreement (SLA) or deadline for approval decisions? | Pending |
| Q23 | Can an AP user partially approve an invoice (approve some line items, reject others)? | Pending |
| Q24 | What search, filter, and sort options should the AP team's invoice list provide? | Pending |
| Q25 | Can the AP team add internal notes that are not visible to vendors? | Pending |
| **REQ-04** | **Approved invoices are forwarded for payment processing** | |
| Q26 | What does 'forwarded for payment' mean technically — integration with ERP/SAP, email to finance, or a queue? | Pending |
| Q27 | What is the target payment turnaround time after invoice approval? | Pending |
| Q28 | Who in the system can view the payment status of an invoice? | Pending |
| Q29 | What payment methods are supported (bank transfer, cheque, digital wallet)? | Pending |
| Q30 | Should the system store payment confirmation/reference numbers? | Pending |
| Q31 | What happens if payment fails — does the invoice return to a pending state? | Pending |
| Q32 | Are there any compliance or audit trail requirements for payment records? | Pending |
| **REQ-05** | **Both parties receive email notifications on status changes** | |
| Q33 | What are all the events that should trigger an email notification? | Pending |
| Q34 | Who exactly receives each notification — vendor only, AP team only, or both? | Pending |
| Q35 | Should notifications also be sent as in-app alerts in addition to email? | Pending |
| Q36 | Can users configure their own notification preferences (opt-out of certain alerts)? | Pending |
| Q37 | What should happen if email delivery fails — is there a retry mechanism? | Pending |
| Q38 | Are there template requirements for notification email content and branding? | Pending |
| **REQ-06** | **The system generates monthly invoice activity reports** | |
| Q39 | What data fields must appear in the monthly report (vendor name, invoice count, total value, approval rate, etc.)? | Pending |
| Q40 | In what format should the report be available — PDF, Excel, dashboard view, or all? | Pending |
| Q41 | Who has access to generate and download reports — all AP users, only managers, or all users? | Pending |
| Q42 | Can reports be filtered by vendor, date range, status, or department? | Pending |
| Q43 | Should reports be auto-generated and emailed at month-end, or generated on demand? | Pending |
| Q44 | Is there a requirement to retain historical reports for a specific period (e.g., 7 years for compliance)? | Pending |
| **REQ-07** | **Only authorized users may access the system** | |
| Q45 | What are the distinct user roles in the system (Vendor, AP Clerk, AP Manager, Finance, Admin, Auditor)? | Pending |
| Q46 | What specific permissions does each role have for each module (view/create/edit/approve/delete/export)? | Pending |
| Q47 | Can an Admin user grant or revoke individual permissions on a per-user basis? | Pending |
| Q48 | Is IP whitelisting or VPN access required for AP team members? | Pending |
| Q49 | Is there a requirement to log all user access and actions for audit purposes? | Pending |
| Q50 | How is access revoked when a vendor relationship ends or an employee leaves? | Pending |

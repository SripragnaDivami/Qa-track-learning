# 5. Test Cases

**Project:** Vendor Invoice Management Portal

---

The following section contains detailed test cases covering all test scenarios. Each test case includes preconditions, step-by-step instructions, and expected results.

---

## TC-001 — Successful Vendor Registration

| Field | Details |
|-------|---------|
| **Test Case ID** | TC-001 |
| **Scenario ID** | TS-001 |
| **Requirement** | REQ-01 |
| **Priority** | High |
| **Type** | Positive |
| **Title** | Successful Vendor Registration |
| **Preconditions** | Registration page is accessible. No existing account with the test email. |
| **Test Steps** | 1. Navigate to the Vendor Portal registration page<br>2. Enter Company Name: 'ABC Supplies Pvt Ltd'<br>3. Enter Tax/GST ID: 'GSTIN123456'<br>4. Enter Email: 'vendor@abcsupplies.com'<br>5. Enter Password: 'Test@1234' and confirm password<br>6. Enter Contact Person: 'John Doe', Phone: '9876543210'<br>7. Click the 'Register' button |
| **Expected Result** | Registration is successful. Confirmation email is sent. Vendor is redirected to a 'Pending Activation' or dashboard screen. |
| **Actual Result** | |
| **Pass / Fail** | |

---

## TC-002 — Registration Fails with Missing Mandatory Fields

| Field | Details |
|-------|---------|
| **Test Case ID** | TC-002 |
| **Scenario ID** | TS-002 |
| **Requirement** | REQ-01 |
| **Priority** | High |
| **Type** | Negative |
| **Title** | Registration Fails with Missing Mandatory Fields |
| **Preconditions** | Registration page is accessible. |
| **Test Steps** | 1. Navigate to the Vendor Portal registration page<br>2. Leave the 'Company Name' field empty<br>3. Fill all other mandatory fields with valid data<br>4. Click the 'Register' button |
| **Expected Result** | Registration is rejected. An inline validation error 'Company Name is required' is displayed next to the field. No account is created. |
| **Actual Result** | |
| **Pass / Fail** | |

---

## TC-003 — Account Lockout After 5 Failed Login Attempts

| Field | Details |
|-------|---------|
| **Test Case ID** | TC-003 |
| **Scenario ID** | TS-006 |
| **Requirement** | REQ-01 |
| **Priority** | High |
| **Type** | Negative |
| **Title** | Account Lockout After 5 Failed Login Attempts |
| **Preconditions** | A registered and activated vendor account exists for 'vendor@abcsupplies.com'. |
| **Test Steps** | 1. Navigate to the login page<br>2. Enter username: 'vendor@abcsupplies.com' and incorrect password: 'Wrong@123'<br>3. Click Login — note the error message<br>4. Repeat step 2–3 four more times (5 attempts total)<br>5. Observe the system response on the 5th failed attempt |
| **Expected Result** | After the 5th failed attempt, account is locked. Message: 'Your account has been temporarily locked. Please contact support or try again after 30 minutes.' Further attempts are blocked. |
| **Actual Result** | |
| **Pass / Fail** | |

---

## TC-010 — Successful Invoice Submission with Valid PO

| Field | Details |
|-------|---------|
| **Test Case ID** | TC-010 |
| **Scenario ID** | TS-008 |
| **Requirement** | REQ-02 |
| **Priority** | Critical |
| **Type** | Positive |
| **Title** | Successful Invoice Submission with Valid PO |
| **Preconditions** | Vendor is logged in. PO-1001 exists in the system with status 'Open'. A valid PDF invoice file (size: 2MB) is prepared. |
| **Test Steps** | 1. Click 'Submit Invoice' from the vendor dashboard<br>2. Enter Invoice Number: 'INV-2026-0055'<br>3. Select PO Number: 'PO-1001' from the dropdown<br>4. Enter Invoice Date: '01-Jun-2026'<br>5. Enter Invoice Amount: '50,000'<br>6. Upload file: 'invoice_june.pdf' (2MB PDF)<br>7. Click 'Submit' |
| **Expected Result** | Invoice is accepted. Status shows 'Pending Review'. Invoice appears in AP team's queue. Confirmation email is sent to the vendor. |
| **Actual Result** | |
| **Pass / Fail** | |

---

## TC-011 — File Upload Rejects Unsupported Format

| Field | Details |
|-------|---------|
| **Test Case ID** | TC-011 |
| **Scenario ID** | TS-010 |
| **Requirement** | REQ-02 |
| **Priority** | High |
| **Type** | Negative |
| **Title** | File Upload Rejects Unsupported Format |
| **Preconditions** | Vendor is logged in. A file 'malware.exe' is available. |
| **Test Steps** | 1. Click 'Submit Invoice'<br>2. Fill all mandatory fields with valid data<br>3. Attempt to upload 'malware.exe'<br>4. Click 'Submit' |
| **Expected Result** | Upload is rejected before submission. Error message: 'File format not supported. Please upload PDF, JPEG, or PNG files only.' Invoice is not created in the system. |
| **Actual Result** | |
| **Pass / Fail** | |

---

## TC-012 — File Upload Rejects Files Exceeding Size Limit

| Field | Details |
|-------|---------|
| **Test Case ID** | TC-012 |
| **Scenario ID** | TS-011 |
| **Requirement** | REQ-02 |
| **Priority** | High |
| **Type** | Negative |
| **Title** | File Upload Rejects Files Exceeding Size Limit |
| **Preconditions** | Vendor is logged in. A 12MB PDF file is prepared (assumed limit: 10MB). |
| **Test Steps** | 1. Click 'Submit Invoice'<br>2. Fill all mandatory fields with valid data<br>3. Upload '12mb_invoice.pdf'<br>4. Click 'Submit' |
| **Expected Result** | Upload is rejected. Error message: 'File size exceeds the 10MB limit. Please upload a smaller file.' Invoice is not created. |
| **Actual Result** | |
| **Pass / Fail** | |

---

## TC-020 — AP User Approves a Valid Invoice

| Field | Details |
|-------|---------|
| **Test Case ID** | TC-020 |
| **Scenario ID** | TS-016 |
| **Requirement** | REQ-03 |
| **Priority** | Critical |
| **Type** | Positive |
| **Title** | AP User Approves a Valid Invoice |
| **Preconditions** | AP user is logged in. Invoice INV-2026-0055 exists in 'Pending Review' status. |
| **Test Steps** | 1. Navigate to the 'Invoice Queue' as the AP user<br>2. Locate invoice INV-2026-0055<br>3. Click 'View Details' on the invoice<br>4. Review invoice details, PO match, and uploaded document<br>5. Click 'Approve'<br>6. Confirm the approval in the dialog |
| **Expected Result** | Invoice status changes to 'Approved'. Invoice moves to the payment forwarding queue. Vendor and AP team receive email notifications. Approval timestamp and approver name are logged. |
| **Actual Result** | |
| **Pass / Fail** | |

---

## TC-021 — AP User Rejects Invoice with Reason

| Field | Details |
|-------|---------|
| **Test Case ID** | TC-021 |
| **Scenario ID** | TS-017 |
| **Requirement** | REQ-03 |
| **Priority** | High |
| **Type** | Positive |
| **Title** | AP User Rejects Invoice with Reason |
| **Preconditions** | AP user is logged in. Invoice INV-2026-0055 exists in 'Pending Review'. |
| **Test Steps** | 1. Navigate to Invoice Queue<br>2. Click 'View Details' on INV-2026-0055<br>3. Click 'Reject'<br>4. Leave the rejection reason field empty and click 'Confirm'<br>5. Observe validation error<br>6. Enter reason: 'Invoice amount does not match PO-1001 agreed value'<br>7. Click 'Confirm Rejection' |
| **Expected Result** | Step 4: Validation error shown — 'Rejection reason is required.' Step 7: Invoice status changes to 'Rejected'. Vendor receives email with the rejection reason. Invoice is returned to vendor for resubmission. |
| **Actual Result** | |
| **Pass / Fail** | |

---

## TC-029 — Vendor Cannot Access AP Approval Module

| Field | Details |
|-------|---------|
| **Test Case ID** | TC-029 |
| **Scenario ID** | TS-029 |
| **Requirement** | REQ-07 |
| **Priority** | Critical |
| **Type** | Security |
| **Title** | Vendor Cannot Access AP Approval Module |
| **Preconditions** | Vendor user is logged in with role = 'Vendor'. |
| **Test Steps** | 1. Log in as a vendor user<br>2. Attempt to navigate directly to the AP approval URL: '/ap/invoice-queue'<br>3. Observe the system response |
| **Expected Result** | Access is denied. User is redirected to their vendor dashboard or shown a '403 Forbidden' error. No AP invoice data is exposed. |
| **Actual Result** | |
| **Pass / Fail** | |

---

## TC-030 — File Upload Security — Malicious Script Injection

| Field | Details |
|-------|---------|
| **Test Case ID** | TC-030 |
| **Scenario ID** | TS-033 |
| **Requirement** | REQ-07 |
| **Priority** | Critical |
| **Type** | Security |
| **Title** | File Upload Security — Malicious Script Injection |
| **Preconditions** | Vendor user is logged in. A file containing an embedded script is prepared. |
| **Test Steps** | 1. Click 'Submit Invoice'<br>2. Fill valid invoice fields<br>3. Upload a file named 'invoice.pdf' that contains an embedded JavaScript payload<br>4. Submit the invoice<br>5. If accepted, attempt to view/download the uploaded file |
| **Expected Result** | Either the file is rejected at upload (preferred), or the file is stored but the script is never executed when retrieved. No XSS or remote code execution occurs. |
| **Actual Result** | |
| **Pass / Fail** | |

# 6. Test Data Specification

**Project:** Vendor Invoice Management Portal

---

Test data must be prepared and loaded into the QA environment before test execution begins. The table below specifies the exact datasets required for each module.

---

## 6.1 Vendor Accounts

| User ID | Email | Company | Role | Status |
|---------|-------|---------|------|--------|
| V001 | vendor1@test.com | Alpha Supplies | Vendor | Active |
| V002 | vendor2@test.com | Beta Traders | Vendor | Active |
| V003 | vendor3@test.com | Gamma Corp | Vendor | Inactive |
| AP001 | apclerk@company.com | Internal | AP Clerk | Active |
| AP002 | apmanager@company.com | Internal | AP Manager | Active |
| ADM01 | admin@company.com | Internal | Admin | Active |

---

## 6.2 Purchase Orders

| PO Number | Vendor | PO Value | Status | Notes |
|-----------|--------|----------|--------|-------|
| PO-1001 | Alpha Supplies (V001) | ₹1,00,000 | Open | Use for positive flows |
| PO-1002 | Beta Traders (V002) | ₹50,000 | Open | Partial invoicing tests |
| PO-1003 | Alpha Supplies (V001) | ₹25,000 | Closed | Test submission against closed PO |
| PO-9999 | N/A | N/A | Does not exist | Test invalid PO entry |

---

## 6.3 Test Invoice Files

| File Name | Format | Size | Purpose |
|-----------|--------|------|---------|
| valid_invoice.pdf | PDF | 2 MB | Standard successful submission test |
| large_invoice.pdf | PDF | 12 MB | Exceeds file size limit — negative test |
| invoice.exe | EXE | 1 MB | Unsupported format — negative test |
| invoice_script.pdf | PDF | 3 MB | PDF with embedded script — security test |
| invoice_image.jpg | JPEG | 1.5 MB | Image format support test |
| boundary_5mb.pdf | PDF | 5.0 MB | Boundary value at exact limit |
| boundary_5_1mb.pdf | PDF | 5.1 MB | Boundary value just over limit |

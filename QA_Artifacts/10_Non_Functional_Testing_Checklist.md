# 10. Non-Functional Testing Checklist

**Project:** Vendor Invoice Management Portal

---

The following checklist covers performance, security, accessibility, compatibility, usability, and documentation testing for the Vendor Invoice Management Portal.

| Category | Test Check | Status / Result |
|----------|-----------|-----------------|
| **Performance** | Invoice list page loads in < 3 seconds with 500+ records | [ ] Pass &nbsp; [ ] Fail &nbsp; [ ] N/A |
| **Performance** | Invoice submission API responds in < 2 seconds under normal load | [ ] Pass &nbsp; [ ] Fail &nbsp; [ ] N/A |
| **Performance** | System handles 500 concurrent users without degradation (JMeter) | [ ] Pass &nbsp; [ ] Fail &nbsp; [ ] N/A |
| **Performance** | Report generation completes in < 10 seconds for 1 month of data | [ ] Pass &nbsp; [ ] Fail &nbsp; [ ] N/A |
| **Security** | SQL injection attempt on login form returns error, not data | [ ] Pass &nbsp; [ ] Fail &nbsp; [ ] N/A |
| **Security** | XSS payload in invoice notes field is sanitised and not rendered | [ ] Pass &nbsp; [ ] Fail &nbsp; [ ] N/A |
| **Security** | All API endpoints return 401 Unauthorized without valid auth token | [ ] Pass &nbsp; [ ] Fail &nbsp; [ ] N/A |
| **Security** | File upload does not accept disguised executable files | [ ] Pass &nbsp; [ ] Fail &nbsp; [ ] N/A |
| **Security** | Session tokens expire after logout or idle timeout | [ ] Pass &nbsp; [ ] Fail &nbsp; [ ] N/A |
| **Security** | Sensitive data (passwords, bank details) are not logged in server logs | [ ] Pass &nbsp; [ ] Fail &nbsp; [ ] N/A |
| **Accessibility** | All form inputs have associated accessible labels (WCAG 2.1 AA) | [ ] Pass &nbsp; [ ] Fail &nbsp; [ ] N/A |
| **Accessibility** | Invoice portal is fully navigable by keyboard without mouse | [ ] Pass &nbsp; [ ] Fail &nbsp; [ ] N/A |
| **Accessibility** | Error messages meet minimum colour contrast ratio (4.5:1) | [ ] Pass &nbsp; [ ] Fail &nbsp; [ ] N/A |
| **Compatibility** | Portal renders correctly on Chrome, Firefox, Edge, Safari | [ ] Pass &nbsp; [ ] Fail &nbsp; [ ] N/A |
| **Compatibility** | Portal is responsive and usable on mobile and tablet viewports | [ ] Pass &nbsp; [ ] Fail &nbsp; [ ] N/A |
| **Usability** | Error messages are descriptive and guide the user to correct the issue | [ ] Pass &nbsp; [ ] Fail &nbsp; [ ] N/A |
| **Usability** | Vendor can complete invoice submission in under 5 minutes without guidance | [ ] Pass &nbsp; [ ] Fail &nbsp; [ ] N/A |
| **Documentation** | All displayed error messages match documented error catalogue | [ ] Pass &nbsp; [ ] Fail &nbsp; [ ] N/A |
| **Documentation** | User guide instructions match actual UI for all vendor flows | [ ] Pass &nbsp; [ ] Fail &nbsp; [ ] N/A |

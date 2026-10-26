# Test Plan — Jawwal eStore
**Version:** 2.0  
**Date:** 30 June 2026  
**Prepared by:** Mohammed Hazem Abu Raida  
**Role:** QA Engineer

---

## 1. Introduction

This Test Plan outlines the comprehensive testing strategy for **Jawwal eStore**, a Palestinian/Jordanian e-commerce platform selling mobile phones and accessories. It describes **what we will test**, **how we will test it**, and **when we are done**. The plan covers functional and non-functional testing approaches for manual testing.

---

## 2. Project Overview

| Field | Details |
|-------|---------|
| **Application** | Jawwal eStore |
| **URL** | https://estore.jawwal.ps/ |
| **Type** | E-commerce website (mobile phones & accessories) |
| **Testing Type** | Manual Testing |
| **Tester** | Mohammed Hazem Abu Raida |
| **Duration** | 3 Months |

---

## 3. Scope

### In Scope:
- User Authentication (Registration, Login, Logout, Password Recovery)
- Product Search and Browsing
- Product Filtering and Sorting
- Product Details Page
- Shopping Cart Management
- Checkout Process
- Order Management
- User Account Management
- Product Comparison Feature
- Wishlist/Favorites
- UI & Usability
- Browser Compatibility

### Out of Scope:

| Feature | Reason |
|---------|--------|
| Real payment processing | Third-party system (not our responsibility) |
| Performance / Load / Stress Testing | Requires special tools (e.g., LoadRunner) |
| Backend database | No access |
| Admin Dashboard / Panel | Out of tester's access |
| Automation Testing | Manual testing phase only |

---

## 4. Testing Objectives

- Verify all core functionalities work as designed
- Identify defects in user workflows
- Ensure data consistency and accuracy
- Validate UI/UX usability
- Ensure mobile and desktop compatibility
- Identify security vulnerabilities in user-facing features
- Create comprehensive test documentation for QA process improvement

---

## 5. Test Strategy

### Testing Types:

**5.1 Functional Testing (80%)**
- Positive Testing- happy case senarioe: Verify correct behavior with valid inputs
- Negative Testing - invalid testing : Verify error handling with invalid inputs
- Boundary Testing: Test edge cases and limits

**5.2 Non-Functional Testing (20%)**
- Usability Testing: UI clarity, navigation ease
- Compatibility Testing: Browser and device compatibility
- Security Testing: Password protection, data masking
- Performance Testing: Manual observation of speed

---

## 6. Test Coverage by Features

### Feature 1: User Authentication (15 Test Cases)
- User Registration
- Email Verification
- Login with Valid/Invalid Credentials
- Password Recovery
- Session Management
- Logout Functionality

### Feature 2: Product Search & Browsing (20 Test Cases)
- Search by Keyword
- Search with Special Characters
- Search with Numbers
- Empty Search Results
- Case Sensitivity
- Pagination

### Feature 3: Product Filtering & Sorting (15 Test Cases)
- Filter by Brand (Apple, Samsung, OPPO, Xiaomi)
- Filter by Price Range
- Filter by Rating
- Multiple Filters Combined
- Clear All Filters
- Filter Result Accuracy

### Feature 4: Shopping Cart (20 Test Cases)
- Add Product to Cart
- Remove Product from Cart
- Update Product Quantity
- Empty Cart
- Cart Persistence (after logout/login)
- Cart Total Calculation
- Stock Availability Check

### Feature 5: Checkout Process (15 Test Cases)
- Proceed to Checkout
- Shipping Information
- Billing Information
- Payment Method Selection
- Order Summary Review
- Order Confirmation
- Order Cancellation

### Feature 6: Product Details (15 Test Cases)
- Display Product Information
- Display Product Images
- Display Product Price
- Display Product Description
- Display Product Reviews/Ratings
- Stock Status Display
- Add to Cart from Details Page
- Add to Wishlist from Details Page

### Feature 7: User Account Management (10 Test Cases)
- View Profile
- Edit Profile Information
- Change Password
- View Order History
- Track Order Status
- Account Settings
- Notification Preferences

### Feature 8: Wishlist / Favorites (5 Test Cases)
- Add Product to Wishlist
- Remove Product from Wishlist
- View Wishlist Items
- Move Item from Wishlist to Cart

### Feature 9: Non-Functional Testing (10 Test Cases)
- Page Load Time (Homepage < 3 seconds)
- Search Response Time (< 2 seconds)
- Mobile Responsiveness
- Button Accessibility
- Color Contrast for Readability
- Cross-browser Compatibility (Chrome, Firefox, Safari, Edge)

**Total Test Cases: 180 (100 core + 80 extended/edge + API)**

---

## 7. Test Priority

| Priority | Features |
|----------|----------|
| **Critical** | Login, Cart, Checkout |
| **High** | Search, Filter, Product Details |
| **Medium** | Account Management, Wishlist, Orders |
| **Low** | UI, Compatibility, Performance |

---

## 8. Test Environment **resou and envi needs

### Hardware:
- Laptop/Desktop Computer
- Mobile Device (iOS and Android)
- Tablet

### Software:
- Browsers: Chrome, Firefox, Safari, Edge (Latest versions)
- Operating Systems: Windows, macOS, iOS, Android
- Test Data: Live Jawwal eStore website (https://estore.jawwal.ps/)

### Test Tools:

| Tool | Purpose |
|------|---------|
| **Jira** | Log and manage bugs |
| **Excel** | Write and track Test Cases |
| **Postman** | API testing (extended phase) |
| **Chrome / Firefox / Safari / Edge** | Test the website |
| **Screenshots / Screen recording** | Evidence for bugs |
| **jmeter for performemecr testing**|


---

## 9. Testing Approach & Phases

### Phase 1 — Month 1: Test Case Preparation
- Understand the application by exploring all features
- Write and document 100 test cases in Excel
- Cover positive, negative, and edge cases
- Create test case templates
- Define test data requirements
- Prepare test environment

### Phase 2 — Month 2: Execution & Defect Reporting
- Execute all 100 functional & non-functional test cases on the live website
- Document results (Pass / Fail)
- Capture evidence (screenshots/videos)
- Write Defect Reports for every bug found
- Log, prioritize, and track all defects in Jira

### Phase 3 — Month 3: Expand & Finalize
- Write 80 additional test cases (edge cases + Postman API)
- Finalize all Jira tickets
- Generate metrics and statistics
- Create Test Summary Report
- Final portfolio documentation

---

## 10. Test Data Requirements

### User Accounts:
- Valid email addresses (for registration)
- Passwords (minimum 8 characters, 1 uppercase, 1 number)
- Invalid emails (for negative testing)
- SQL injection attempts (for security testing)

### Product Data:
- Various price ranges (100–5000 ILS)
- Different brands (Apple, Samsung, OPPO, Xiaomi)
- Products with and without stock
- Products with and without reviews

### Test Cards:
- Valid credit card numbers (for checkout testing)
- Expired card numbers (for negative testing)
- Invalid CVV (for negative testing)

---

## 11. Test Deliverables

| Deliverable | When |
|-------------|------|
| 100 Test Cases (Excel) | End of Month 1 |
| 30+ Defect Reports (Jira) | End of Month 2 |
| 180 Total Test Cases | End of Month 3 |
| Test Summary Report & Metrics | End of Month 3 |

---

## 12. Entry Criteria (Before We Start)

- [ ] Website is accessible and running
- [ ] Test account created on the website
- [ ] Excel test case template is ready
- [ ] Jira project is set up

---

## 13. Exit Criteria (When We Are Done)

Testing will be considered complete when:
- ✅ 150+ test cases have been executed
- ✅ Minimum 90% of test cases passed
- ✅ All critical/high severity defects are logged in Jira
- ✅ Test documentation is complete
- ✅ Test Summary Report and metrics are generated
- ✅ Portfolio is ready for presentation

---

## 14. Risks & Mitigation

| Risk | Impact | Mitigation |
|------|--------|-----------|
| Website downtime during testing | High | Test at different times; use backup environment or offline screenshots |
| Lack of test data / no account access | High | Create test accounts and use existing products before starting |
| Browser compatibility issues | Medium | Test on all major browsers from the start |
| Feature changes mid-testing | Medium | Re-test affected features |
| Time constraints | Medium | Prioritize critical features first |
| Data loss during testing | High | Use test accounts; don't affect real user data |

---

## 15. roles & Responsibilities

| Role | Responsibility |
|------|-----------------|
| QA Engineer (Mohammed abu raida) | Test execution, defect logging, documentation |
| Test Lead | Review test results, approve final report |
| Development | Fix reported defects |

|project  manger |
|business analyst|
---

## 16. Appendix

### Appendix A: Test Case Template Structure
```
Test Case ID: TC_XXX
Title: [Clear description]
Feature: [Feature name]
Priority: [Critical/High/Medium/Low]
Pre-conditions: [Required setup]
Steps:
  1. [Step 1]
  2. [Step 2]
  3. [Step 3]
Expected Result: [What should happen]
Actual Result: [What actually happened]
Status: [PASS/FAIL]
Remarks: [Additional notes]
```

### Appendix B: Defect Report Template Structure
```
Bug ID: BUG_XXX
Title: [Clear bug description]
Severity: [Critical/High/Medium/Low]
Priority: [P1/P2/P3/P4]
Steps to Reproduce: [Exact steps]
Expected Behavior: [What should happen]
Actual Behavior: [What actually happens]
Attachments: [Screenshots/videos]
Reporter: [Your name]
Date: [Date found]
```

---

**End of Test Plan Document**

---

*For questions or clarifications, contact: Mohammed Hazem Abu Raida*

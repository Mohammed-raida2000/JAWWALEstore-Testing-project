# DEFECT REPORT TEMPLATE
## Jawwal eStore - QA Testing

---

## DEFECT REPORT EXAMPLE #1

### **Header Information**
| Field | Value |
|-------|-------|
| **Bug ID** | BUG_001 |
| **Title** | Search Button Not Responding on Mobile |
| **Date Reported** | 30 June 2026 |
| **Reported by** | Mohammed Hazem Abu Raida |
| **Environment** | iOS Safari, iPhone 12 |

---

### **Severity & Priority**

| Level | Definition |
|-------|-----------|
| **Severity** | **High** - Feature completely broken |
| **Priority** | **P1** - Fix immediately, blocking testing |

---

### **Description**

**Summary:**
When searching for products on mobile device (iOS), the search button fails to respond to user clicks, preventing any search functionality.

**Detailed Description:**
User attempts to search for "iPhone" on the Jawwal eStore mobile app. After typing the keyword in the search bar and clicking the search button, no action is triggered. The page remains on the same view without displaying results or any error message.

---

### **Steps to Reproduce**

1. Open Jawwal eStore on iOS mobile device (iPhone)
2. Click on the search bar at the top of the page
3. Type keyword: "iPhone"
4. Click the search/magnifying glass button
5. Observe the result

---

### **Expected Behavior**

- Search button should respond to the click
- Page should display search results for "iPhone"
- Result count should be shown
- Filter options should appear

---

### **Actual Behavior**

- Search button does not respond to clicks
- Page remains unchanged on the search bar page
- No results displayed
- No error message shown
- No loading indicator appears

---

### **Environment Details**

| Item | Details |
|------|---------|
| **Device** | iPhone 12 |
| **OS Version** | iOS 16.5 |
| **Browser** | Safari 16.5 |
| **Network** | WiFi (4G connection tested too) |
| **App Version** | Latest (v2.1.0) |
| **Screen Resolution** | 390 x 844 pixels |

---

### **Attachments**

**Screenshots:**
- [Screenshot_1.png] - Search bar with keyword typed
- [Screenshot_2.png] - Button not responding after click
- [Screenshot_3.png] - No error message shown

**Video:**
- [Video_BUG_001.mp4] - Screen recording of the issue (30 seconds)

---

### **Additional Information**

**Related Test Case:** TC_001 (Search for Product by Brand)

**Root Cause Analysis (if known):**
Possible JavaScript event listener not attached to the search button on mobile devices.

**Workaround (if available):**
- Try using the browser's back button and search again
- Close Safari and reopen the app
- Use desktop version as alternative (not a real fix)

---

### **Reproduction Frequency**

- **100% Reproducible** - Happens every time on iOS Safari
- **Not Reproducible on Desktop** - Works fine on Chrome/Firefox desktop browsers

---

### **Impact Assessment**

| Area | Impact |
|------|--------|
| **Business** | High - Core feature blocked, users cannot search |
| **Users** | Mobile users cannot search for products |
| **Development** | Requires immediate investigation |

---

### **Resolution Notes** (To be filled by Developer)

| Field | Value |
|-------|-------|
| **Status** | Open → In Progress → Fixed |
| **Assigned to** | [Developer Name] |
| **Fixed Date** | [Date] |
| **Resolution Summary** | [How it was fixed] |

---

---

## DEFECT REPORT EXAMPLE #2

### **Header Information**
| Field | Value |
|-------|-------|
| **Bug ID** | BUG_002 |
| **Title** | Cart Total Calculation Error |
| **Date Reported** | 30 June 2026 |
| **Reported by** | Mohammed Hazem Abu Raida |
| **Environment** | Chrome Desktop, Windows 10 |

---

### **Severity & Priority**

| Level | Definition |
|-------|-----------|
| **Severity** | **Critical** - Data integrity issue, financial impact |
| **Priority** | **P1** - Block all testing, fix immediately |

---

### **Description**

**Summary:**
When adding multiple products to the cart, the cart total is calculated incorrectly, showing wrong final amount.

**Detailed Description:**
Added two products to cart:
- Product A: iPhone 13 - Price: 500 ILS
- Product B: Phone Case - Price: 50 ILS

Expected Total: 550 ILS
Actual Total: 550 ILS ✓ (but quantity multiplier error)

When updating quantity of Product A to 2 units:
- Expected Total: (500 × 2) + 50 = 1050 ILS
- Actual Total: 500 + 50 = 550 ILS ❌

---

### **Steps to Reproduce**

1. Go to Jawwal eStore homepage
2. Add "iPhone 13" (500 ILS) to cart
3. Add "Phone Case" (50 ILS) to cart
4. Open cart and verify total = 550 ILS ✓
5. Change iPhone quantity from 1 to 2
6. Observe the cart total

**Expected:** 1050 ILS
**Actual:** 550 ILS

---

### **Expected Behavior**

Cart total should dynamically update when:
- Product quantity changes
- New products are added
- Products are removed
- Discount codes are applied

Formula: Total = Σ(Product Price × Quantity) + Tax - Discounts

---

### **Actual Behavior**

Cart total does NOT update when changing product quantities. It only updates when adding/removing products completely. The quantity multiplier is not being applied to the calculation.

---

### **Environment Details**

| Item | Details |
|------|---------|
| **Browser** | Google Chrome 121.0.6167.160 |
| **OS** | Windows 10 (Build 19045) |
| **Screen Resolution** | 1920 x 1080 |
| **Device** | Desktop Computer |
| **Network** | Stable WiFi connection |
| **Cache** | Cleared before testing |

---

### **Attachments**

**Screenshots:**
- [BUG_002_Screenshot_1.png] - Cart with 2 items, total = 550
- [BUG_002_Screenshot_2.png] - After updating quantity to 2, total still = 550
- [BUG_002_Screenshot_3.png] - Expected total calculation formula

**Video:**
- [BUG_002_Screen_Recording.mp4] - Full reproduction video (1 minute)

---

### **Additional Information**

**Related Test Cases:**
- TC_010 (Update Product Quantity)
- TC_012 (Cart Total Calculation)

**Root Cause Analysis (if known):**
JavaScript total calculation function may not be triggered on quantity change event. Likely missing event listener on quantity input field.

**Workaround:**
- Refresh the page after changing quantity (not practical)
- Add product again instead of changing quantity

**Severity Justification:**
This is CRITICAL because:
1. **Financial Impact** - Customers may be overcharged or undercharged
2. **Legal Issue** - Incorrect billing can cause disputes
3. **User Trust** - Security concern for payment
4. **Business Loss** - Can lead to revenue loss or chargebacks

---

### **Resolution Notes** (To be filled by Developer)

| Field | Value |
|-------|-------|
| **Status** | Open |
| **Assigned to** | [Lead Developer] |
| **Fixed Date** | [Pending] |
| **Resolution Summary** | [To be filled] |
| **QA Sign-off** | [Pending] |

---

---

## DEFECT REPORT TEMPLATE (BLANK) - USE THIS FORMAT

### **Header Information**
| Field | Value |
|-------|-------|
| **Bug ID** | BUG_XXX |
| **Title** | [Clear, concise title] |
| **Date Reported** | [Date] |
| **Reported by** | Mohammed Hazem Abu Raida |
| **Environment** | [Browser, Device, OS] |

---

### **Severity & Priority**

| Level | Definition |
|-------|-----------|
| **Severity** | **Critical/High/Medium/Low** |
| **Priority** | **P1/P2/P3/P4** |

---

### **Description**

**Summary:**
[One-line summary of the bug]

**Detailed Description:**
[Detailed explanation of what is happening]

---

### **Steps to Reproduce**

1. [Step 1]
2. [Step 2]
3. [Step 3]
4. [Step 4]

---

### **Expected Behavior**

[What should happen according to requirements]

---

### **Actual Behavior**

[What actually happens - the bug]

---

### **Environment Details**

| Item | Details |
|-------|---------|
| **Browser** | [Name and version] |
| **OS** | [Operating System and version] |
| **Device** | [Device type] |
| **Network** | [Connection type] |
| **App Version** | [Version number] |

---

### **Attachments**

**Screenshots:**
- [Screenshot names]

**Videos:**
- [Video names]

**Other:**
- [Any other relevant files]

---

### **Additional Information**

**Related Test Case:** [TC ID]

**Root Cause Analysis (if known):**
[Your analysis]

**Workaround (if available):**
[Any temporary workaround]

---

### **Reproduction Frequency**

- [ ] Always reproducible
- [ ] Sometimes reproducible
- [ ] Rarely reproducible

---

### **Impact Assessment**

| Area | Impact |
|------|--------|
| **Business** | [Impact] |
| **Users** | [Impact] |
| **Development** | [Impact] |

---

### **Resolution Notes** (To be filled by Developer)

| Field | Value |
|-------|-------|
| **Status** | [Status] |
| **Assigned to** | [Developer Name] |
| **Fixed Date** | [Date] |
| **Resolution Summary** | [How it was fixed] |

---

---

## SEVERITY LEVELS GUIDE

| Severity | Definition | Example |
|----------|-----------|---------|
| **Critical** | System completely broken, data loss, security issue | Payment calculation wrong, user cannot checkout |
| **High** | Major feature not working, significant impact | Search button not responding, login fails |
| **Medium** | Feature partially working, workaround exists | Sorting not working, but filtering does |
| **Low** | Minor issue, cosmetic, no workaround needed | Button color slightly off, typo in text |

---

## PRIORITY LEVELS GUIDE

| Priority | Definition | Timeline |
|----------|-----------|----------|
| **P1** | Fix immediately, blocking multiple features | Within 24 hours |
| **P2** | Fix ASAP, impacting core functionality | Within 3-5 days |
| **P3** | Fix in next release, nice to have improvement | Within 2-3 weeks |
| **P4** | Fix when time permits, very low impact | Next major release |

---

## HOW TO WRITE GOOD DEFECT REPORTS

### ✅ DO:
1. **Be Specific** - Clear title and description
2. **Include Steps** - Exact reproduction steps
3. **Add Evidence** - Screenshots and videos
4. **Be Concise** - No unnecessary information
5. **Use Clear Language** - Professional Arabic/English
6. **Separate Issues** - One bug per report
7. **Add Environment** - Browser, OS, device info

### ❌ DON'T:
1. "It's broken" - Too vague
2. "Probably something wrong with code" - Not your job
3. Multiple issues in one report - Create separate bugs
4. No screenshots or evidence - Proof is essential
5. Emotional language - Stay professional
6. Assume root cause - Just report what you see
7. Forget environment details - Critical for reproduction

---

**End of Defect Report Template Document**

**Created by:** Mohammed Hazem Abu Raida  
**Date:** 30 June 2026  
**For:** Jawwal eStore QA Testing Project

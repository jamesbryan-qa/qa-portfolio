# SauceDemo QA Project – Test Execution Summary

**Project Version:** September 2025, v1.0  
**Role:** Manual QA Tester  
**Tools Used:** Zephyr (Test Case Management), Jira (Bug Tracking), Google Sheets/Docs

---

## 📌 Overview
This document summarizes the execution of all test cases for the **SauceDemo QA Project**.  
Test execution was done in **Zephyr**, and related defects were tracked in **Jira**.

---

## ✅ User Authentication
| Test Case ID | Description                               | Status |
|--------------|-------------------------------------------|--------|
| TC-LOGIN-001 | Validate login with valid credentials     | ✅ Passed |
| TC-LOGIN-002 | Validate login with case-sensitive username | ✅ Passed |
| TC-LOGIN-003 | Validate login with invalid username      | ✅ Passed |
| TC-LOGIN-004 | Validate login with empty username        | ✅ Passed |
| TC-LOGIN-005 | Validate login with empty password        | ✅ Passed |
| TC-LOGIN-006 | Validate login with invalid password      | ✅ Passed |
| TC-LOGIN-007 | Validate login with locked out user       | ✅ Passed |

---

## ✅ Product Catalog
| Test Case ID | Description                               | Status |
|--------------|-------------------------------------------|--------|
| TC-PC-001    | Validate product list is displayed correctly | ✅ Passed |
| TC-PC-002    | Validate browser back/forward navigation after login | ✅ Passed |
| TC-PC-003    | Validate sorting by Name (A to Z)        | ✅ Passed |
| TC-PC-004    | Validate sorting by Name (Z to A)        | ✅ Passed |
| TC-PC-005    | Validate sorting by Price (Low to High)  | ✅ Passed |
| TC-PC-006    | Validate sorting by Price (High to Low)  | ✅ Passed |
| TC-PC-007    | Validate product details page navigation | ✅ Passed |

---

## ✅ Hamburger Menu
| Test Case ID | Description                               | Status |
|--------------|-------------------------------------------|--------|
| TC-MENU-001  | Validate “All Items” Menu Option          | ✅ Passed |
| TC-MENU-002  | Validate "About" Menu Option              | ✅ Passed |
| TC-MENU-003  | Validate "Logout" Menu Option             | ✅ Passed |
| TC-MENU-004  | Validate "Reset App State" Menu Option    | ✅ Passed |
| TC-MENU-005  | Validate Back Navigation After Logout     | ✅ Passed |

---

## 🛒 Shopping Cart
| Test Case ID | Description                               | Status | Notes |
|--------------|-------------------------------------------|--------|-------|
| TC-CT-001    | Validate Add to Cart is working           | ✅ Passed | - |
| TC-CT-002    | Validate user cannot add more than one of the same product | ✅ Passed | - |
| TC-CT-003    | Validate cart badge count updates correctly | ✅ Passed | - |
| TC-CT-004    | Validate removing product from cart       | ✅ Passed | - |
| TC-CT-006    | Validate cart persistence after logout and login | ✅ Passed | - |
| TC-CT-005    | Validate behavior when cart is empty      | ❌ Failed | Checkout button active, allows proceeding with empty cart. [PDF](../bug-reports/SDP-35%20Checkout%20is%20allowed%20when%20the%20cart%20is%20empty.pdf) / [Screenshot/Video](../bug-reports/attachments/Checkout_bug.mp4) |

---

## 🛒 Checkout
| Test Case ID | Description                               | Status | Notes |
|--------------|-------------------------------------------|--------|-------|
| TC-CHECKOUT-001 | Checkout with Valid Information          | ✅ Passed | - |
| TC-CHECKOUT-002 | Checkout with Missing First Name        | ✅ Passed | - |
| TC-CHECKOUT-003 | Checkout with Missing Last Name         | ✅ Passed | - |
| TC-CHECKOUT-004 | Checkout with Missing Postal Code       | ✅ Passed | - |
| TC-CHECKOUT-005 | View Checkout Overview and Complete Order | ✅ Passed | - |
| TC-CHECKOUT-006 | Cancel Checkout Before Completion       | ✅ Passed | - |
| TC-CHECKOUT-007 | Validate Order Confirmation Page UI     | ❌ Failed | Back Home button missing. [PDF](../bug-reports/SDP-38%20No%20Back%20Button%20Available%20After%20Completing%20Checkout%20Order.pdf) / [Screenshot/Video](../bug-reports/attachments/Confirmation_BackButton.png) |

---

## 📊 Overall Execution Status
- **Total Test Cases:** 32  
- **Passed:** 30  
- **Failed:** 2  
- **Blocked / Not Executed:** 0  
- **Execution Rate:** 100% (with 2 defects logged)  

---

## 🐛 Defects Logged from Failed Test Cases
*Click the links to view the detailed bug reports or supporting evidence.*  

1. **SDP-35 – Checkout is allowed when the cart is empty** → Linked to TC-CT-005  
   → [PDF](../bug-reports/SDP-35%20Checkout%20is%20allowed%20when%20the%20cart%20is%20empty.pdf)  
   → [Screenshot/Video](../bug-reports/attachments/Checkout_bug.mp4)  

2. **SDP-38 – No Back Button Available After Completing Checkout Order** → Linked to TC-CHECKOUT-007  
   → [PDF](../bug-reports/SDP-38%20No%20Back%20Button%20Available%20After%20Completing%20Checkout%20Order.pdf)  
   → [Screenshot/Video](../bug-reports/attachments/Confirmation_BackButton.png)  

---

## 🐞 Additional Defects Observed During Passed Test Cases
These defects were identified while executing passing test cases. Test steps executed as expected, but issues were noted and logged in Jira.

| Bug ID | Description | Observed During | Evidence |
|--------|------------|----------------|----------|
| SDP-37 | Cart items persist across different user accounts | TC-CT-006 – Validate cart persistence after logout and login | [PDF](../bug-reports/SDP-37%20Cart%20items%20persist%20across%20different%20user%20accounts.pdf) / [Screenshot/Video](../bug-reports/attachments/Cross_acc_bug.mp4) |
| SDP-34 | Social media links in the footer are not working | TC-PC-001 – Validate product list is displayed correctly | [PDF](../bug-reports/SDP-34%20Social%20media%20links%20in%20the%20footer%20are%20not%20working.pdf) / [Screenshot/Video](../bug-reports/attachments/UI_SOCIALS.png) |
| SDP-32 | Back button text formatting inconsistent | TC-PC-007 – Validate product details page navigation | [PDF](../bug-reports/SDP-32%20Back%20button%20text%20formatting%20inconsistent.pdf) / [Screenshot/Video](../bug-reports/attachments/UI_BACK.png) |
| SDP-31 | Footer section is too large | TC-PC-001 – Validate product list is displayed correctly | [PDF](../bug-reports/SDP-31%20Footer%20section%20is%20too%20large.pdf) / [Screenshot/Video](../bug-reports/attachments/UI_FOOTER.png) |
| SDP-30 | Product description contains placeholder text | TC-PC-007 – Validate product details page navigation | [PDF](../bug-reports/SDP-30%20Product%20description%20contains%20placeholder%20text.pdf) / [Screenshot/Video](../bug-reports/attachments/UI_TXT.png) |


---

# Manual Test Cases

Manual functional, UI and mobile test cases for SauceDemo, DemoQA and the Sauce Labs My Demo App RN (SQA Batch 18, executed 12/06/2026).

## Summary

| Metric | Count |
|---|---|
| Total test cases | 18 |
| Passed | 13 |
| Failed | 5 |

| Section | Application | Link | Test cases |
|---|---|---|---|
| A | SauceDemo | https://www.saucedemo.com/ | TC_A_SD_001 to 004 |
| B | DemoQA | https://demoqa.com/ | TC_B_DA_005 to 011 |
| C | Sauce Labs My Demo App RN | https://github.com/saucelabs/my-demo-app-rn/releases | TC_C_MAT_012 to 018 |

## Test case index

| ID | Title | Status |
|---|---|---|
| [TC_A_SD_001](#tc_a_sd_001) | Verify login error message for locked_out_user | ✅ Pass |
| [TC_A_SD_002](#tc_a_sd_002) | Verify items added to cart | ✅ Pass |
| [TC_A_SD_003](#tc_a_sd_003) | Verify validation for empty checkout fields | ✅ Pass |
| [TC_A_SD_004](#tc_a_sd_004) | Verify product listing page | ❌ Fail |
| [TC_B_DA_005](#tc_b_da_005) | Verify form validation on empty submission | ❌ Fail |
| [TC_B_DA_006](#tc_b_da_006) | Validate mobile field character restrictions | ✅ Pass |
| [TC_B_DA_PT_007](#tc_b_da_pt_007) | Verify successful dismissal of standard JS Alert | ✅ Pass |
| [TC_B_DA_NT_008](#tc_b_da_nt_008) | Verify application handling when a browser alert is forcefully blocked or unhandled | ✅ Pass |
| [TC_B_DA_009](#tc_b_da_009) | Verify dynamic CRUD updates in Web Tables | ✅ Pass |
| [TC_B_DA_010](#tc_b_da_010) | Verify the maximum character limits for all text fields in the "Add Record" form using Boundary Value Analysis | ✅ Pass |
| [TC_B_DA_011](#tc_b_da_011) | Verify 'Add Record' input validation against special characters and Numbers | ❌ Fail |
| [TC_C_MAT_012](#tc_c_mat_012) | Verify successful application launch and primary navigation accessibility | ✅ Pass |
| [TC_C_MAT_013](#tc_c_mat_013) | Verify login with valid credentials | ✅ Pass |
| [TC_C_MAT_014](#tc_c_mat_014) | Verify UI rendering of product attributes | ✅ Pass |
| [TC_C_MAT_015](#tc_c_mat_015) | Verify items added to cart | ✅ Pass |
| [TC_C_MAT_016](#tc_c_mat_016) | Verify UI responsiveness during orientation change | ❌ Fail |
| [TC_C_MAT_017](#tc_c_mat_017) | Verify state preservation after minimizing the app | ✅ Pass |
| [TC_C_MAT_018](#tc_c_mat_018) | Verify application behavior when internet is disabled | ❌ Fail |

## Section A: SauceDemo

### TC_A_SD_001

| Field | Details |
|---|---|
| Title | Verify login error message for locked_out_user |
| Application | SauceDemo |
| Link | https://www.saucedemo.com/ |
| Prerequisites | 1. SauceDemo site should be on live 2. login page should be available |
| Status | **Pass** |

**Steps**

1. open the chrome browser
2. browse the link - https://www.saucedemo.com/
3. enter valid username to the username field : locked_out_user
4. enter valid password to the password field : secret_sauce
5. click login button

**Expected result:** System should display a clear, user-friendly error message indicating the account is locked.

**Actual result:** The system displays: "Epic sadface: Sorry, this user has been locked out."

---

### TC_A_SD_002

| Field | Details |
|---|---|
| Title | Verify items added to cart |
| Application | SauceDemo |
| Link | https://www.saucedemo.com/ |
| Prerequisites | 1. SauceDemo site should be on live 2. login page should be available |
| Status | **Pass** |

**Steps**

1. open the chrome browser
2. browse the link - https://www.saucedemo.com/
3. enter valid username to the username field : standard_user
4. enter valid password to the password field : secret_sauce
5. click login button
6. Add 'Sauce Labs Backpack' and 'Sauce Labs Fleece Jacket' to cart.
7. Click cart icon.

**Expected result:** Items should be listed with correct names and prices.

**Actual result:** Both items are listed with correct names and prices ($29.99 and $49.99).

---

### TC_A_SD_003

| Field | Details |
|---|---|
| Title | Verify validation for empty checkout fields |
| Application | SauceDemo |
| Link | https://www.saucedemo.com/ |
| Prerequisites | 1. SauceDemo site should be on live 2. login page should be available |
| Status | **Pass** |

**Steps**

1. open the chrome browser
2. browse the link - https://www.saucedemo.com/
3. enter valid username to the username field : standard_user
4. enter valid password to the password field : secret_sauce
5. click login button
6. Add 'Sauce Labs Backpack' and 'Sauce Labs Fleece Jacket' to cart.
7. Click cart icon.
8. Click 'Continue' with empty fields

**Expected result:** All errors displayed simultaneously

**Actual result:** Errors displayed sequentially (one by one)

---

### TC_A_SD_004

| Field | Details |
|---|---|
| Title | Verify product listing page |
| Application | SauceDemo |
| Link | https://www.saucedemo.com/ |
| Prerequisites | 1. SauceDemo site should be on live 2. login page should be available |
| Status | **Fail** |

**Steps**

1. open the chrome browser
2. browse the link - https://www.saucedemo.com/
3. enter valid username to the username field : problem_user
4. enter valid password to the password field : secret_sauce
5. click login button
6. Browse inventory page.
7. Attempt to filter or remove items.

**Expected result:** Page loads images correctly; buttons responsive.

**Actual result:** Images are broken (repeated dog image); page lags/freezes.

---


## Section B: DemoQA

### TC_B_DA_005

| Field | Details |
|---|---|
| Title | Verify form validation on empty submission |
| Application | DemoQA |
| Link | https://demoqa.com/automation-practice-form |
| Prerequisites | User is on the Practice Form page |
| Status | **Fail** |

**Steps**

1. open the chrome browser
2. browse the link - https://demoqa.com/automation-practice-form
3. Navigate to DemoQA → Forms → Practice Form.
4. Click 'Submit' button without filling any fields.

**Expected result:** All mandatory fields (Name, Gender, Mobile, State/City) should display validation errors.

**Actual result:** Name, Gender, and Mobile show errors; State and City dropdowns do not.

---

### TC_B_DA_006

| Field | Details |
|---|---|
| Title | Validate mobile field character restrictions |
| Application | DemoQA |
| Link | https://demoqa.com/automation-practice-form |
| Prerequisites | User is on the Practice Form page |
| Status | **Pass** |

**Steps**

1. open the chrome browser
2. browse the link - https://demoqa.com/automation-practice-form
3. Navigate to DemoQA → Forms → Practice Form.
4. Type abc!@# into the Mobile Number field.

**Expected result:** Field should strictly reject non-numeric keystrokes and remain empty.

**Actual result:** Field should strictly reject non-numeric keystrokes and remain empty.

---

### TC_B_DA_PT_007

| Field | Details |
|---|---|
| Title | Verify successful dismissal of standard JS Alert |
| Application | DemoQA |
| Link | https://demoqa.com/alerts |
| Prerequisites | User is on the Practice Form page |
| Status | **Pass** |

**Steps**

1. open the chrome browser
2. browse the link - https://demoqa.com/alerts
3. Navigate to demoqa.com → Alerts, Frame & Windows → Alerts
4. Click the first "Click me" button next to "Click Button to see alert".
5. Verify the browser alert appears.
6. Click "OK".

**Expected result:** The alert dialog closes cleanly, and the user can freely click other elements on the main page again.

**Actual result:** The alert dialog closes cleanly, and the user can freely click other elements on the main page again.

---

### TC_B_DA_NT_008

| Field | Details |
|---|---|
| Title | Verify application handling when a browser alert is forcefully blocked or unhandled |
| Application | DemoQA |
| Link | https://demoqa.com/alerts |
| Prerequisites | User is on the Practice Form page |
| Status | **Pass** |

**Steps**

1. open the chrome browser
2. browse the link - https://demoqa.com/alerts
3. Navigate to demoqa.com → Alerts, Frame & Windows → Alerts
4. Configure browser settings/extensions to block automatic pop-ups or trigger an abrupt tab closure while the modal is open.
5. Click the first "Click me" button next to "Click Button to see alert".
6. Verify the browser alert appears.
7. Click "OK".
8. Observe application behavior if the alert is suppressed.

**Expected result:** The underlying web application should gracefully handle the exception without crashing, throwing a console script error, or permanently locking up the UI thread.

**Actual result:** The underlying web application should gracefully handle the exception without crashing, throwing a console script error, or permanently locking up the UI thread.

---

### TC_B_DA_009

| Field | Details |
|---|---|
| Title | Verify dynamic CRUD updates in Web Tables |
| Application | DemoQA |
| Link | https://demoqa.com/webtables |
| Prerequisites | User is on the Web Tables page |
| Status | **Pass** |

**Steps**

1. open the chrome browser
2. browse the link - https://demoqa.com/webtables
3. Navigate to demoqa.com → Elements → Web Tables
4. Add record
5. Modify record data fields.
6. Delete record

**Expected result:** Table grid records should render updates synchronously on screen immediately.

**Actual result:** Table dynamically updates DOM presentation values without manual refresh hooks.

---

### TC_B_DA_010

| Field | Details |
|---|---|
| Title | Verify the maximum character limits for all text fields in the "Add Record" form using Boundary Value Analysis |
| Application | DemoQA |
| Link | https://demoqa.com/webtables |
| Prerequisites | User is on the Web Tables page and has clicked the 'Add' button. |
| Status | **Pass** |

**Steps**

1. open the chrome browser
2. browse the link - https://demoqa.com/webtables
3. Navigate to demoqa.com → Elements → Web Tables
4. Input a string of 50+ characters into the First Name field & Last Name field.
5. Input 9999999999 into the Salary field.
6. Fill other fields validly and click 'Submit'.

**Expected result:** 1. The UI should handle long strings gracefully without breaking the row layout. 2. The application should not crash or throw database overflow errors.

**Actual result:** 1. The UI should handle long strings gracefully without breaking the row layout. 2. The application should not crash or throw database overflow errors.

---

### TC_B_DA_011

| Field | Details |
|---|---|
| Title | Verify 'Add Record' input validation against special characters and Numbers |
| Application | DemoQA |
| Link | https://demoqa.com/webtables |
| Prerequisites | User is on the Web Tables page and has clicked the 'Add' button. |
| Status | **Fail** |

**Steps**

1. open the chrome browser
2. browse the link - https://demoqa.com/webtables
3. Navigate to demoqa.com → Elements → Web Tables
4. Input FuadHasan@123hasan in the First Name field.
5. Input `Hasan@123#$\%` in the Last Name field.
6. Fill other fields validly and click 'Submit'.

**Expected result:** The system should either prevent non-alphabetic characters from being entered in the name fields through client-side validation or store and display them as plain text without causing parsing errors.

**Actual result:** The modal accepts the input, submits without warning, and saves the symbols/numbers directly into the main table grid.

---


## Section C: Sauce Labs My Demo App RN

### TC_C_MAT_012

| Field | Details |
|---|---|
| Title | Verify successful application launch and primary navigation accessibility |
| Application | Sauce Labs My Demo App RN |
| Link | https://github.com/saucelabs/my-demo-app-rn/releases |
| Prerequisites | User has installed and launched "My Demo App RN" on an Android device. |
| Status | **Pass** |

**Steps**

1. Launch the installed "My Demo App".
2. Navigate through the Hamburger menu and Cart icon.
3. Apply a sort/filter on the product catalog.

**Expected result:** The app launches without crashing; all navigation menus and filters respond as expected.

**Actual result:** The app launches without crashing; all navigation menus and filters respond as expected.

---

### TC_C_MAT_013

| Field | Details |
|---|---|
| Title | Verify login with valid credentials |
| Application | Sauce Labs My Demo App RN |
| Link | https://github.com/saucelabs/my-demo-app-rn/releases |
| Prerequisites | User is on the login screen with valid test credentials. |
| Status | **Pass** |

**Steps**

1. Launch the installed "My Demo App".
2. Enter valid username : bob@example.com
3. Enter valid password : 10203040
4. Tap "Login".

**Expected result:** User is successfully authenticated and redirected to the product catalog page.

**Actual result:** User is successfully authenticated and redirected to the product catalog page.

---

### TC_C_MAT_014

| Field | Details |
|---|---|
| Title | Verify UI rendering of product attributes |
| Application | Sauce Labs My Demo App RN |
| Link | https://github.com/saucelabs/my-demo-app-rn/releases |
| Prerequisites | User is logged in and is viewing the product catalog. |
| Status | **Pass** |

**Steps**

1. Launch the installed "My Demo App".
2. Enter valid username : bob@example.com
3. Enter valid password : 10203040
4. Tap "Login".
5. Navigate to the catalog.
6. Inspect displayed products.

**Expected result:** Product names, images, and prices are rendered correctly and are legible.

**Actual result:** Product names, images, and prices are rendered correctly and are legible.

---

### TC_C_MAT_015

| Field | Details |
|---|---|
| Title | Verify items added to cart |
| Application | Sauce Labs My Demo App RN |
| Link | https://github.com/saucelabs/my-demo-app-rn/releases |
| Prerequisites | User is on a product detail page. |
| Status | **Pass** |

**Steps**

1. Launch the installed "My Demo App".
2. enter valid username to the username field : bob@example.com
3. enter valid password to the password field : 10203040
4. click login button
5. Add 'Sauce Labs Backpack' and 'Sauce Labs Bike Light' to cart.
6. Click cart icon.

**Expected result:** Items should be listed with correct names and prices $ Sub total prices

**Actual result:** Both items are listed with correct names and prices ($29.99 and $9.99) & Sub total price is ($39.98).

---

### TC_C_MAT_016

| Field | Details |
|---|---|
| Title | Verify UI responsiveness during orientation change |
| Application | Sauce Labs My Demo App RN |
| Link | https://github.com/saucelabs/my-demo-app-rn/releases |
| Prerequisites | App is installed and running on an Android device. |
| Status | **Fail** |

**Steps**

1. Launch the installed "My Demo App".
2. enter valid username to the username field : bob@example.com
3. enter valid password to the password field : 10203040
4. click login button
5. Open the app in Portrait mode.
6. Rotate the device to Landscape mode.

**Expected result:** The UI layout should dynamically adjust to the new orientation without clipping elements.

**Actual result:** Layout fails to adapt; UI remains in Portrait mode.

---

### TC_C_MAT_017

| Field | Details |
|---|---|
| Title | Verify state preservation after minimizing the app |
| Application | Sauce Labs My Demo App RN |
| Link | https://github.com/saucelabs/my-demo-app-rn/releases |
| Prerequisites | App is in an active state. |
| Status | **Pass** |

**Steps**

1. Launch the installed "My Demo App".
2. enter valid username to the username field : bob@example.com
3. enter valid password to the password field : 10203040
4. click login button
5. Minimize the app.
6. Reopen the app immediately.

**Expected result:** The app should resume smoothly, retaining the previous state/screen.

**Actual result:** App resumes smoothly without issues.

---

### TC_C_MAT_018

| Field | Details |
|---|---|
| Title | Verify application behavior when internet is disabled |
| Application | Sauce Labs My Demo App RN |
| Link | https://github.com/saucelabs/my-demo-app-rn/releases |
| Prerequisites | App is connected to the network. |
| Status | **Fail** |

**Steps**

1. Launch the installed "My Demo App".
2. enter valid username to the username field : bob@example.com
3. enter valid password to the password field : 10203040
4. click login button
5. Load the product catalog.
6. Disable internet connectivity on the device.

**Expected result:** The app should display a meaningful "No Internet" or "Offline" message.

**Actual result:** App retains the last viewed state; no active notification of network status change.

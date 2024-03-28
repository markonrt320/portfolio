# Bug report #
Bug reports are documents that detail the occurrence and characteristics of software defects or anomalies. They typically include information such as the steps to reproduce the bug, expected versus actual behavior, screenshots or recordings, and any relevant system configurations.<br><br>
Academy Bugs helps you to understand the different types of bugs and aids you to differentiate between them by showcasing what/where might be a bug.


## 1. BUG REPORT ##
<br><br>
**Summary:** Browse Candy | ‘Wham Bars’ product picture does not appear <br>
**Environment:** Windows 10 | OperaGX <br>
**BugID:** BrowseCandy#001 <br>
**Description:** When browsing through the products pictures of certain product does not appear. <br>

**Steps:** 
  1. Visit page https://sweetshop.netlify.app<br>
  2. Click to Sweets from navigation menu.<br>
  3. Scroll down to ‘Wham Bars’ product.<br>

**Expected result:** Every product in Sweets page should have picture.<br>
**Actual result:** When scrolling through page Wham Bars image is broken.<br>
**Repro rate:** 100%<br>
**Type of bug:** Visual<br>
**Severity:** Low<br>
**Priority:** Low<br>
**Attachment:** <br>
![png](https://github.com/markonrt320/QA-portfolio/assets/164415938/9e624d9a-6407-441a-9b27-91e359903da8)

<br>
<hr>
<br>

## 2. BUG REPORT ##
<br><br>
**Summary:** Items Page | Page freezes and is unresponsive after selecting currency in dropdown that is not USD.<br>
**Environment:** Windows 10 | OperaGX<br>
**BugID:** AcademyBugs#001<br>
**Description:** <br>
**Steps to reproduce:** <br> 
  1. Visit url https://academybugs.com/find-bugs/<br>
  2. Select any product.<br>
  3. Select any other currency in currency dropdown menu that is not equal to USD. <br>

**Expected:** Price of every product should have new selected currency and it should be displayed in dropdown menu.<br>
**Actual:** After changing currency in dropdown menu of any product from USD to any other currency page freezes completely. Also currency is not changed when going through products.<br>
**Repro rate:** 100%<br>
**Type of bug:** Visual<br>
**Severity:** High<br>
**Priority:** High<br>
**Attachment:** <br> <br>
![bugreport](https://github.com/markonrt320/QA-portfolio/assets/164415938/2cd3ba91-789d-4b35-9a8e-c74c762ced24)
<br>
<hr>
<br>

## 3. BUG REPORT ##
<br><br>
**Summary:** Contact Form | Data isn’t passed to server after filling form with valid data <br>

**BugID:** AcademyBugs#002<br>

**Type of bug:** Functional<br>

**Description:** <br>

**Steps to reproduce:** <br> 
  1. Visit page https://academybugs.com/contact-us-form/ <br>
  2. Fill input fields with valid data. <br>
  3. Click ‘Send’ button. <br>

**Expected:** When user fills contact form with valid data and clicks ‘Send’ button that data should be passed to server and message should be displayed that the process was successful.<br>
**Actual:** When the text field was filled by a user and the ‘Send’ button was clicked, only error message was displayed but data isn’t send to server.<br>

**Environment:** Desktop OperaGX(Version 107.0.5045.37), Desktop Chrome(122.0.6261.111/112) <br>

**Severity:** Medium<br>
**Priority:** Medium<br>
**Repro rate:** 100%<br>
**Attachment:** <br><br>
![Slika1](https://github.com/markonrt320/QA-portfolio/assets/164415938/3207795b-de56-4ff5-8f9a-bef4ae6cb785)
![Slika2](https://github.com/markonrt320/QA-portfolio/assets/164415938/d6e92cab-fee3-4624-bbca-7de0ec73e743)


<br>
<hr>
<br>

## 4. BUG REPORT ##
<br><br>
**Summary:** Cart | Grand Total of the cart isn’t equal to the price of the products that are placed in the cart. <br>

**BugID:** AcademyBugs#003<br>

**Type of bug:** Functional<br>

**Description:** <br>

**Steps to reproduce:** <br> 
  1. Visit page https://academybugs.com/contact-us-form/ <br>
  2. Click on ‘Add to cart’ for several products. <br>
  3. Press on the appeared green button ‘Checkout now’.<br>

**Expected:** Grand Total should be equal to summed prices of products that were added to cart.<br>
**Actual:** Grand Total of the added products isn’t equal to the sum of the products.<br>

**Environment:** Chrome on Xiaomi Mi 12 Lite (Chrome version 122.0.6261.105) <br>

**Severity:** Medium<br>
**Priority:** High<br>
**Repro rate:** 100%<br>
**Attachment:** <br><br>

![Slika3](https://github.com/markonrt320/QA-portfolio/assets/164415938/c4c509fb-e0ad-4174-bd2e-0674b78e608a)

<br>
<hr>
<br>

## 5. BUG REPORT ##
<br><br>
**Summary:** Cart | Grand Total of the cart isn’t equal to the price of the products that are placed in the cart. <br>

**BugID:** AcademyBugs#004<br>

**Type of bug:** Visual<br>

**Description:** <br>

**Steps to reproduce:** <br> 
  1. Visit page https://academybugs.com/contact-us-form/ <br>
  2. Click on ‘Add to cart’ for several products. <br>
  3. Press on the appeared green button ‘Checkout now’.<br>
  4. After being redirected to the cart, remove items from cart by clicking ‘X’ button on the left side of the product.<br>

**Expected:** After removing all the products from the cart blue button should appear with the text ‘RETURN TO STORE’<br>
**Actual:** When user emptied cart, button is displayed with the text that has spelling mistake ‘RETURN TO STOR	E’.<br>

**Environment:** Any browser <br>

**Severity:** Low<br>
**Priority:** Low<br>
**Repro rate:** 100%<br>
**Attachment:** <br><br>

https://github.com/markonrt320/QA-portfolio/assets/164415938/a005e0df-14f7-4c06-bd20-e089436d4e11

<br>
![Slika4](https://github.com/markonrt320/QA-portfolio/assets/164415938/48d0cbe0-6b08-4749-a24f-bb101756c162)


<br>
<hr>
<br>

## 6. BUG REPORT ##
<br><br>
**Summary:** Account page | Text isn’t written in English. <br>

**BugID:** AcademyBugs#005<br>

**Type of bug:** Content<br>

**Description:** <br>

**Steps to reproduce:** <br> 
  1. Visit page https://academybugs.com/contact-us-form/ <br>
  2. Navigate to the ‘New user’ section. <br>

**Expected:** All text should be written in English since it is the main language of the website.<br>
**Actual:** Text in ‘New user’ section isn’t displayed in English language.<br>

**Environment:** Any browser <br>

**Severity:** Low<br>
**Priority:** Low<br>
**Repro rate:** 100%<br>
**Attachment:** <br><br>

![Slika5](https://github.com/markonrt320/QA-portfolio/assets/164415938/2bff81fa-ff6c-4603-ad78-36d4a05f49b0)
<br>
<hr>
<br>

## 7. BUG REPORT ##
<br><br>
**Summary:** Anchor Bracelet page | Page is loading infinitely after opening the page. <br>

**BugID:** AcademyBugs#006<br>

**Type of bug:** Performance<br>

**Description:** <br>

**Steps to reproduce:** <br> 
  1. Open any product on the page.<br>
  2. Open the product on the ‘Hot item’ section named ‘Anchor Bracelet’.<br>

**Expected:** After opening the product page it should load immediately.<br>
**Actual:** Spinner is spinning infinitely.<br>

**Environment:** Any browser <br>

**Severity:** Medium<br>
**Priority:** Medium<br>
**Repro rate:** 100%<br>
**Attachment:** <br> <br>

https://github.com/markonrt320/QA-portfolio/assets/164415938/e6e566cd-d651-4da6-88f6-894cb7e4c52b


<br>
<hr>
<br>

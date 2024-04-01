# Calculation Test cases #

**TestCrafters** is a pioneering platform dedicated to constructing engaging exercises through intricate applications. Our platform empowers users to design tests, run code against those tests, and receive comprehensive feedback on their test design skills.<br>
<br>
**Exercise resume:** This exercise presents a comprehensive scenario involving price calculation for goods purchased online, incorporating various rules and conditions. Participants are tasked with designing a system to calculate the final price to be paid by the customer, considering factors such as price reductions, delivery costs, payment methods, and order specifications.<br>
<br>
![123](https://github.com/markonrt320/QA-portfolio/assets/164415938/124ed4de-c8bc-45a5-9141-a7fe04a341a8)

**Link towards exercise:** https://exercises.test-design.org/price-calculation/

**Link towards done exercise:** [https://exercises.test-design.org/price-calculation/](https://docs.google.com/spreadsheets/d/1hwt04WsVG31fMBzntjA8nLbWcb6BRelyOqFmTMKn4JM/edit?usp=sharing)

### <hr>Test case with Decision table technique</hr>
<br>

### Test case 1 ###
<br>

**TC#ID:** TC#5 <br>
**Test case title:** Verify 10% Price Reduction <br><br>
**Description:** Verify that the customer receives a 10% price reduction when the price of the goods exceeds 200 euros. <br><br>
**Precondition:** "User has browser opened and is located on page https://exercises.test-design.org/price-calculation/" <br><br>
**Steps:**

|No.|Test Steps|Test Data|Expected Results|
| :-: | :- | :-: | :- |
|1|Enter valid price.|245|Price input field should be filled.|
|2|Enter valid weight.|4|Weight input field should be filled.|
|3|Click button 'Next step'||Calculator should accept provided values. Discount should be included and total price should be reduced by 10%|

<br>

### Test case 2 ###
<br>

**TC#ID:** TC#2 <br>
**Test case title:** Verify 15% Price Reduction for Credit Card Payment, Price at Threshold, and Weight Under Limit <br><br>
**Description:** Ensure that the system applies a 15% price reduction when the price reaches 200 euros, the customer pays with a credit card, and the weight is under 5 kg. <br><br>
**Precondition:** User has browser opened and is located on page https://exercises.test-design.org/price-calculation/ <br><br>
**Steps:**

|No.|Test Steps|Test Data|Expected Results|
| :-: | :- | :-: | :- |
|1|Enter valid price for discount.|202|Price input field should be filled.|
|2|Enter valid weight for discount.|4.3|Weight input field should be filled.|
|3|Check 'Pay with credit card' checkbox.||Checkbox should be checked.|
|4|Click button 'Next step'||Calculator should accept provided values. Discount should be included and total price should be reduced by 15%.|

<br>

### <hr>Test cases with Boundary value analysis</hr>
<br>

### Test case 3 ###
<br>

**TC#ID:** TC#6 <br>
**Test case title:** Verifying 10% Price Reduction Just Below Threshold <br>
**Description:** Ensure that the system does not apply the price reduction when the price of the goods is just below the threshold of 200 euros. <br>
**Precondition:** "User has browser opened and is located on page https://exercises.test-design.org/price-calculation/" <br>
**Steps:**

|No.|Test Steps|Test Data|Expected Results|
| :-: | :- | :-: | :- |
|1|Enter invalid price for discount.|199.9|Price input field should be filled.|
|2|Enter valid weight.|15|Weight input field should be filled.|
|3|Click button 'Next step'||Calculator should accept provided values. Discount should not be included and total price should not be reduced by 10%.|

<br>

### Test case 4 ###
<br>

**TC#ID:** TC#7 <br>
**Test case title:** Verify 10% Price Reduction at Threshold <br>
**Description:** Ensure that the system correctly applies the price reduction when the price of the goods reaches exactly the threshold of 200 euros. <br>
**Precondition:** User has browser opened and is located on page https://exercises.test-design.org/price-calculation/ <br>
**Steps:**

|No.|Test Steps|Test Data|Expected Results|
| :-: | :- | :-: | :- |
|1|Enter invalid price for discount.|200|Price input field should be filled.|
|2|Enter valid weight.|15|Weight input field should be filled.|
|3|Click button 'Next step'||Calculator should accept provided values. Discount should not be included and total price should not be reduced by 10%.|

<br>

### Test case 5 ###
<br>

**TC#ID:** TC#8 <br>
**Test case title:** Verify 10% Price Reduction Just Above Threshold <br>
**Description:** Ensure that the system correctly applies the price reduction when the price of the goods exceeds the threshold of 200 euros. <br>
**Precondition:** User has browser opened and is located on page https://exercises.test-design.org/price-calculation/ <br>
**Steps:**

|No.|Test Steps|Test Data|Expected Results|
| :-: | :- | :-: | :- |
|1|Enter valid price for discount.|200|Price input field should be filled.|
|2|Enter valid weight.|15|Weight input field should be filled.|
|3|Click button 'Next step'||Calculator should accept data from input fields. Discount should be included and total price should be reduced by 10%.|

# Test cases - API testing #

Root end point is `https://simple-books-api.glitch.me`, also this end point is placed in collection variable {{baseUrl}}.

## TC#ID: 1 ##
**Test case title:** Verify endpoint status response<br>
**Description:** Ensure that the status endpoint returns the expected response with a status code of 200 and the status message is "OK". <br>
**Precondition:** User has "POSTMAN" app opened and collection variable baseUrl is set.<br><br>
**Steps:**
|No.|Test Steps|Test Data|Expected Results|
| :-: | :- | :- | :- |
|1|Send a GET request to the status endpoint /status||The response status code should be 200.|
|2|Verify that the response time is less than 500ms.||The response time should be less than 500ms.|
|3|Parse the response body as JSON.||The status property in the response body should be "OK".|


## TC#ID: 2 ##
**Test case title:** Verify Books Endpoint Response<br>
**Description:** Ensure that the books endpoint returns the expected response with a status code of 200, a response time of less than 500ms and the correct content type header. <br>
**Precondition:** User has "POSTMAN" app opened and collection variable baseUrl is set.<br><br>
**Steps:**
|No.|Test Steps|Test Data|Expected Results|
| :-: | :- | :- | :- |
|1|Send a GET request to the books endpoint /books.||The response status code should be 200.|
|2|Verify that the response time is less than 500ms.||The response time should be less than 500ms.|
|3|Verify that the Content-Type header is present in the response.||The Content-Type header should be present.|
|4|Verify that the Content-Type header is set to "application/json; charset=utf-8".||The Content-Type header should be set to "application/json; charset=utf-8".|


## TC#ID: 3 ##
**Test case title:** Verify Books Endpoint Response with Limited Length.<br>
**Description:** Ensure that the books endpoint returns the expected response when limited to a specified length. Verify that the response time is within acceptable limits, the status code is 200, the response is an array, and the length of the array matches the specified limit.<br>
**Precondition:** User has "POSTMAN" app opened and collection variable baseUrl is set.<br><br>
**Steps:**
|No.|Test Steps|Test Data|Expected Results|
| :-: | :- | :- | :- |
|1|Send a GET request to the books endpoint /books?limit={{limitLength}} .|limitLength=3|The response status code should be 200.|
|2|Verify that the response time is less than 500ms.||The response time should be less than 500ms.|
|3|Parse the response body as JSON and verify that the response is an array.||The response should be an array.|
|4|Check that the length of the array matches the specified limit (limitLength).||The length of the array should match the specified limit (3 in this case).|


## TC#ID: 4 ##
**Test case title:** Verify Books Endpoint Response for Non-Fiction Books.<br>
**Description:** Ensure that the books endpoint returns the expected response when filtered by non-fiction books. Verify that the response time is within acceptable limits, the status code is 200, the response is an array, and every book in the response is of type non-fiction.<br>
**Precondition:** User has "POSTMAN" app opened and collection variable baseUrl is set.<br><br>
**Steps:**
|No.|Test Steps|Test Data|Expected Results|
| :-: | :- | :- | :- |
|1|Send a GET request to the books endpoint /books?type=non-fiction.||The response status code should be 200.|
|2|Verify that the response time is less than 500ms.||The response time should be less than 500ms.|
|3|Parse the response body as JSON and verify that the response is an array.||The response should be an array.|
|4|Check that every book in the response has a type property equal to "non-fiction".||Every book in the response should be of type "non-fiction".|



## TC#ID: 5 ##
**Test case title:** Verify Books Endpoint Response for Fiction Books.<br>
**Description:** Ensure that the books endpoint returns the expected response when filtered by fiction books. Verify that the response time is within acceptable limits, the status code is 200, the response is an array, and every book in the response is of type fiction.<br>
**Precondition:** User has "POSTMAN" app opened and collection variable baseUrl is set.<br><br>
**Steps:**
|No.|Test Steps|Test Data|Expected Results|
| :-: | :- | :- | :- |
|1|Send a GET request to the books endpoint /books?type=fiction.||The response status code should be 200.|
|2|Verify that the response time is less than 500ms.||The response time should be less than 500ms.|
|3|Parse the response body as JSON and verify that the response is an array.||The response should be an array.|
|4|Check that every book in the response has a type property equal to "fiction".||Every book in the response should be of type "fiction".|


## TC#ID: 6 ##
**Test case title:** Verify Detailed Information for a Specific Book<br>
**Description:** Ensure that the endpoint for retrieving detailed information about a specific book returns the expected response with a status code of 200 and a response time of less than 500ms.<br>
**Precondition:** User has "POSTMAN" app opened and collection variable baseUrl is set.<br><br>
**Steps:**
|No.|Test Steps|Test Data|Expected Results|
| :-: | :- | :- | :- |
|1|Send a GET request to the endpoint for retrieving detailed information about a specific book /books/:{{bookId}})|bookId=2|The response status code should be 200.|
|2|Verify that the response time is less than 500ms.||The response time should be less than 500ms.|



## TC#ID: 7 ##
**Test case title:**  Register API Client and Retrieve Access Token<br>
**Description:** Ensure that the endpoint for registering an API client returns the expected response with an access token, and the access token is correctly stored in collection variables for further use.<br>
**Precondition:** User has "POSTMAN" app opened and collection variable baseUrl is set.<br><br>
**Steps:**
|No.|Test Steps|Test Data|Expected Results|
| :-: | :- | :- | :- |
|1|Set a random client name and email in the pre-request script.||Name and email collection variables should be set.|
|2|Set the request body with the client name and email.|{"clientName": "{{name}}","clientEmail": "{{email}}"}|Request body should be set.|
|3|Set a random client name and email in the pre-request script.||Name and email collection variables should be set.|
|4|Send a POST request to the endpoint for registering an API client /api-clients/||The response status code should be 200.|
|5|Verify that the response is an object.||The response should be an object where auth token should be placed.|
|6|Retrieve the access token from the response and store it in collection variables.||An access token should be retrieved from the response and stored in collection variables for further use.|


## TC#ID: 8 ##
**Test case title:**  Attempt to Submit Order for Unavailable Book<br>
**Description:** Ensure that attempting to submit an order for an unavailable book returns the expected response with a status code of 404.<br>
**Precondition:** In the Authorization tab set the type as 'Bearer Token' and in Token tab place {{authToken}} variable that was previously made.<br><br>
**Steps:**
|No.|Test Steps|Test Data|Expected Results|
| :-: | :- | :- | :- |
|1|Set the request body with the ID of an unavailable book({{unavailableBookId}}) and a random customer name.|{"bookId": "{{unavailableBookId}}","customerName": "{{name}}"}|Request body should be set.|
|2|Send a POST request to the endpoint for submitting an order /orders and verify that the response status code is 404.||The response status code should be 404 because book isn't on stock.|








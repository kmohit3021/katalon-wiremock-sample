Katalon WireMock Integration
Katalon Studio integrates with WireMock, a leading provider of mocking services that delivers both an open source version as well as a cloud version.    
With WireMock Cloud, Katalon users will be able to easily mimic a production API’s behavior for end to end testing even if the production API is not yet developed or available. These virtualized services (aka service virtualization) can then be shared and used across teams without additional effort or maintenance.

Why is service virtualization so important for Katalon users?
Virtualizing a service enables Katalon users:

to build test assets even when the APIs you need aren’t ready or released.
to guard against unstable 3rd party API’s when developing tests to reduce test flakiness
to simulate edge cases and faults easily, to help with unhappy path testing.
Real World Example

Consider there is a Banking application that contains thousands of APIs that take inputs from a web page (Customer details, Fund details, Interest calculations, etc.). This application communicates to external services (endpoints -> SOAP/REST) and it is not the tester’s responsibility to worry about getting the test data for testing & having to wait for these environments. However, APIs designed need to be tested against a set of data (Customer details, fund details, etc.). There is a need to remove this external Network Call (dependency) and create something at the run time and simulate the network calls.

A network call can return different status codes 404, 500, 200, 303, etc with a JSON response. The application has to work for all such scenarios along with a different set of data for 200 responses. Having a database server running to test the API is inefficient and not a right way to go about API testing.

That is where Mocking services come into picture.

How to Integrate Katalon with WireMock Cloud 
To integrate Katalon Studio with WireMock Cloud, you need to follow these steps:    
1. WireMock Cloud offers a free forever edition as well as paid plans for enterprises. You will need to create a WireMock Cloud account to leverage WireMock with Katalon.    
2. Verify the response of the WireMock API: In your Katalon test script, you need to verify the response of the WireMocked API to ensure that it meets your expectations.     
3. You can do this by using the API testing and Verification Validation mechanisms to check the status code, headers, and response body of the HTTP response.    
4. Call the WireMocked API in your test: In your Katalon test script, you need to call the WireMocked API to verify the behavior of your system under test. You can do this by making HTTP requests using the WebUI.callRestApi method in Katalon.

Step 1: Below step shows a mock service on wiremock cloud in the settings tab: 

Wiremock Step 1   
 

Step 2: The below screenshot shows a sample API from the internet.

 Wiremock Step 2

 

Step 3: There are various ways to create a mock service in WireMock Cloud  

Manually via the web UI  
Swagger or OpenAPI specification import  
Record traffic to and from another API  
Import an existing project from WireMock  
Automate via the REST API or WireMock  
The below screenshot shows how to use recording in order to create a sample stub within the mock service created in wiremock. You can also watch a 90 seconds video hereWiremock Step 3

 

Step 4: Once the real API service is recorded you can observe that multiple stubs are created with all the responses captured during the recording. Wiremock Step 4 
 

Step 5: Once recorded, we head over to Katalon studio and create a new web service request and hit the mock API service which was recorded using Wiremock Cloud:

Wiremock Step 5 
 

Step 6: We now run the sample request and observe that the responses are from the MockAPI vs the real API service.

Wiremock Step 6

Step 7: We can now create an API test within Katalon and compare using verification and validation mechanism

Salesforce Katalon Screenshot 7

Wiremock Step 7.2   
This is just an example to demonstrate how to integrate Katalon Studio with WireMock Cloud. You can modify and expand the code as needed to meet your specific testing requirements. 

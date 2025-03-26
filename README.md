# PostmanAPI

This project showcases my skills in API automation testing using Postman and the Restful booker website. It covers various testing techniques, including pre-request scripts, authentication handling, performance testing, data-driven testing, and mock servers

**Prerequisites:**
Before running this project, ensure you have the following installed:
Postman
Node.js & npm
Optional to run the tests from command line: Newman (npm install -g newman)

**Project Structure:**
api-automation-postman/
│── collections/              # Stores Postman collections
│   ├── RestfulBooker.json     # API test collection
│── environments/             # Stores environment variables
│   ├── dev_environment.json
│   ├── prod_environment.json
│── reports/                  # Stores test execution reports
│── postman-runner.sh         # Shell script to run tests with Newman
│── README.md                 # Project documentation

**How to Run the Restful Booker API Locally:**
Download the Restful Booker code from (https://restful-booker.herokuapp.com/) by clicking on Code > Download ZIP.
Save the code in a directory of your choice.
Open a terminal in that directory and run:
npm install
npm start
Configure your local environment variables accordingly.
Skip this step by running the collection in the Production environment instead.

**Features Implemented** 
General API Testing:
Pre-request scripts at collection level for dynamic data handling.
Auth token inheritance for authentication across requests.
Assertions to validate status codes (e.g., 200, 201, 400, etc.).
Tests to validate JSON responses against expected values.
Performance testing – Checking response times.

**Advanced API Automation Features**
Pre-request scripts at request level for conditional execution.
Chaining requests – Using responses from one request in another.
External dataset integration – Running requests with dynamic data.
Using Lodash – Generating random numbers dynamically.
Using Moment.js – Formatting dates for API requests.
Mock Server Setup – Simulating authentication responses.

**Running Tests with Newman (CLI)**
To execute API tests via the command line: 
newman run collections/RestfulBooker.json -e environments/dev_environment.json
For HTML Reports, run:
newman run collections/RestfulBooker.json -e environments/dev_environment.json -r html --reporter-html-export reports/test-report.html

**CI/CD Integration**
This project can be integrated into GitHub Actions or Jenkins for automated test execution. You can set up scheduled or trigger-based API testing pipelines.

**Future Enhancements**
Set up a Postman Monitor for scheduled API testing.
Integrate with Jenkins/GitHub Actions for CI/CD automation.
Add visual regression testing with API snapshots.

The Collection contains:
1. A pre-request script on collection level
2. An auth token used on all calls by setting them to "inherit from parent
3. Tests to check status codes
4. Tests to check json values that match
5. Test that checks response time - performance testing
6. Pre-request scripts on individual request level
7. Sending requests inside another request as part of pre-request script
8. External Data set to be used for running one of the calls with the external data set.
9. Using lodash module to get random numbers
10. Using moment module to format dates
11. Creating an object on collection level that is used in other requests
12. Mock server and response setup for the auth request
13. No monitor setup. Add this manually.





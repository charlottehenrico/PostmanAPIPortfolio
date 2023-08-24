# PostmanAPI

A project to showcase hat I have learned on API automation testing. Making use of Postman and Restful Booker website. 

To run the Restful Booker website locally, go to Restul Booker website, https://restful-booker.herokuapp.com/ and click on code to download
Save the code in directory on your drive
Then use npm start to run it from the saved directory
Ensure you set up the local environment then as per your own environment. 

To skip this step, run the collection in Production environment

The Collection contains:
1. A pre-request script on collection level
2. An auth token used on all calls by setting them to "inherit from parent
3. Tests to check status codes
4. Tests to check json values that match
5. Tests that check response times
6. Pre-request scripts on individual request level
7. Sending requests inside another request as part of pre-request script
8. External Data set to be used for running one of the calls with the external data set.
9. Using lodash module to get random numbers
10. Using moment module to format dates
11. Creating an object on collection level that is used in other requests
12. Mock server and response setup for the auth request
13. Monitor is setup. Remember to set your own user email to receive the monitor results. Postman allows for 1000 monitor results per month.





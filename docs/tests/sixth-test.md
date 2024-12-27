# SIXTH TEST

Let's test a REST API endpoint.

* For the REST API test, let's add a new Thread Group to simulate only 1 single user running the test.

* Then add a new HTTP Request
    * I'll use this REST API endpoint `https://restcountries.com/v3.1/lang/spanish?fields=name,capital,currencies` to test.

    ![Alt text](/images/rest-api/REST-api-1.png "HTTP Request configuration")

* Add a new `HTTP Header Manager` config element to add a content-type: 

    * `Add > Config Element > HTTP Header Manager`

    ![Alt text](/images/rest-api/REST-api-2.png "HTTP Header Manager configuration")

* Add a new `Response Assertion` element to check for a specific value from the body response.

    ![Alt text](/images/rest-api/REST-api-3.png "Response Assertion configuration")

* Run the test and check it passes.

    ![Alt text](/images/rest-api/REST-api-4.png "Check test pass")


## Dry Run
Open this [jmx file](/REST%20API%20-%20Test%20Plan.jmx) in JMeter and run the test.

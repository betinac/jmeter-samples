# SEVENTH TEST

Let's test a SOAP API endpoint.

* For the SOAP API test, let's add a new Thread Group to simulate only 1 single user running the test.

* Then add a new HTTP Request.
    * I'll use this SOAP API endpoint `http://webservices.oorsprong.org/websamples.countryinfo/CountryInfoService.wso` to test.

* I'll define a `host` variable by adding the `User Defined Variables` config element.

    ![Alt text](/images/soap-api/SOAP-api-1.png "User Defined Variables")

* Then I'll add the `HTTP Request Defaults` config element to specify the host as a variable: `${host}`. The below request will "inherit" this configuration.

    ![Alt text](/images/soap-api/SOAP-api-2.png "HTTP Request Defaults")

* Add an `HTTP Request` and specify `POST` as the HTTP Request method and `/websamples.countryinfo/CountryInfoService.wso` as the path.

    ![Alt text](/images/soap-api/SOAP-api-3.png "HTTP Request configuration")

* Add a new `HTTP Header Manager` config element to add a content-type: 

    ![Alt text](/images/soap-api/SOAP-api-4.png "HTTP Header Manager configuration")

* Add a new `Response Assertion` element to check for a specific value from the body response, i.e `</m:CountryFlagResult>`.

    ![Alt text](/images/soap-api/SOAP-api-5.png "Response Assertion")

* Run the test and check it passes.

    ![Alt text](/images/soap-api/SOAP-api-6.png "Check test pass")

## Dry Run
Open this [jmx file](/REST%20API%20-%20Test%20Plan.jmx) in JMeter and run the test.

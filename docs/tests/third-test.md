# THIRD TEST

Let's check the content on the Response. For that we use Assertions that we add like this:

`Add > Assertions > Response Assertion`

## Response Assertion

### All tests pass
- We will apply the assertion to the `Main sample only` Thread Group and we will select the `Response Code` value under `Field to Test`.
- Finally, we want to check if the response is equal to `200`.

    ![Alt text](/images/assertions/Assertions_UsersRequest_1.png "Add an Assertion")

- Check all the requests passed.

    ![Alt text](/images/assertions/Assertions_UsersRequest_2.png "Check all tests passed")
 

### All tests fail

If we instead enter `201` as the expected code, we will see that the same tests fail.

![Alt text](/images/assertions/Assertions_UsersRequest_3.png "Update the expected Response Code")

![Alt text](/images/assertions/Assertions_UsersRequest_4.png "Check all tests failed")

Let's add another report to better check assertions, as every time a request fails, it will log it in this report:

`Add > Listeners > Assertion Results`

![Alt text](/images/assertions/Assertions_UsersRequest_5.png "Check the Assertion Results report")

## Duration Assertion

Another Assertion we can use is the `Duration Assertion` to check for the duration of the response:

`Add > Assertions > Duration Assertion`

- On the `Duration in miliseconds` field we add i.e. `1900`. This means any response that takes more than 1900 miliseconds (or 1.9 seconds), will be considered a failure.

    ![Alt text](/images/assertions/Assertions_UsersRequest_8.png "Add an expected duration on the Duration report")

- All those tests that had a Duration time greater than the value specified above, fail.

    ![Alt text](/images/assertions/Assertions_UsersRequest_7.png "Check the results")

## Size Assertion
We can use the `Size Assertion` to check for the size in bytes of the response:

`Add > Assertions > Size Assertion`

- On the `Size to Assert > Size in bytes` field we add i.e. `539750` and in the `Type of Comparison` we select the `<` (less than) option. This means any response size that weights more than 539750 bytes, will be considered a failure.

    ![Alt text](/images/assertions/Assertions_UsersRequest_9.png "Add an expected size on the Size Assertion report")

- All those tests that had a Size greater than the value specified above, fail.

    ![Alt text](/images/assertions/Assertions_UsersRequest_10.png "Check the results")

    ![Alt text](/images/assertions/Assertions_UsersRequest_11.png "Check the Assertion Results report")

## HTML Assertion

To check the format of the response and if it's valid or not, let's add the `HTML Assertion` assertion:

`Add > Assertions > HTML Assertion`

- We can add some thresholds for errors and warnings. 

    ![Alt text](/images/assertions/Assertions_UsersRequest_12.png "Add an expected threshold on the HTML Assertion report")

- All those tests that went outside the thresholds specified above, fail.

    ![Alt text](/images/assertions/Assertions_UsersRequest_14.png "Check the results")

    ![Alt text](/images/assertions/Assertions_UsersRequest_13.png "Check the Assertion Results report")

Now, to know where are those errors that are making the HTML format invalid, we will write those results to a file.

- Let's add a path to a `txt` file where we will save the test results.

    ![Alt text](/images/assertions/Assertions_UsersRequest_16.png "Add a path to the file that will contain the results")

- Check the [saved txt report](/saved-reports/HTML-invalid-format-report.txt)

    ![Alt text](/images/assertions/Assertions_UsersRequest_17.png "Check the content of the saved file")


## Dry Run
Open this [jmx file](/Feature%20-%20Test%20Plan.jmx) in JMeter and run the third test.

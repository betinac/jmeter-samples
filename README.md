# jmeter-samples

Introduction on how to run performance tests with JMETER.

![Alt text](/images/Jmeter-logo.png "JMETER Logo")

## Pre-requisites
* Check you have JAVA installed: `java -version`

![Alt text](/images/java-version.png "Check your java version")

* Make sure the `JAVA_HOME` environment variable is set.

* Download JMeter: https://jmeter.apache.org/download_jmeter.cgi

* Install JMeter:

    - Unzip the zip/tar file into the directory where you want JMeter to be installed.
    - Another option is to use Homebrew: `brew install jmeter`

* Start JMeter:
    - Go to the `/bin` folder and run the `jmeter.bat` (for Windows) or `./jmeter` (or `sh jmeter.sh`) (for Unix) file.
    - More details in the Apache website: https://jmeter.apache.org/usermanual/get-started.html#running

## Some Definitions 
### Test Plan
Contains a series of steps that JMeter will execute when run: Thread Groups, Logic controllers, listeners, timers, assertions, configuration elements, etc.

### WorkBench
Place to keep elements temporarily, but they will not be saved.

### Thread Group
We will simulate virtual users in a performance test.

### Sampler
Here we add the requests we can send to the server being tested (i.e HTTP FTP, etc)

### Listeners
We use them to gather info, save, view and analyze the performance test results in tabular or graphical form.

* **View Results in Table**
    * It saves results in a table format.
    * This visualizer creates a row for every sample result (or user request).
    * It uses a lot of memory and CPU, so it's not suggested to be used for Load tests.
    * Displays the sampler response header and response body.

| Column       | Centered        |
| :----------- | :-------------- |
| Sample Time (ms) | the response time of the reques in miliseconds  |
| Status | *by default*: green means the test passed, red means it failed (if we have assertions the status will depend on them) |
| Bytes | quantity of data in the sample response returned from the server (the size of the response). |
| Sent Bytes/sec | bytes virtual user(s) sent per second (request throughput) |
| Latency | the time to the first byte is returned, so the time it takes for a request to be sent and a response to be received (to acquire a connection) |
| Connect Time (ms) | time to establish connection |
 

---
## TESTS

* Create a new Test Plan
    ![Alt text](/images/Test_Plan.png "Add a new Test Plan")
* [First basic test](/docs/tests/first-test.md "Add your first basic test")
* [Second test - Simulate multiple users](/docs/tests/second-test.md "Run a test with multiple users")
* [Third test - Assert the content](/docs/tests/third-test.md "Assert the content of the results")
* [Fourth test - Check report types](/docs/tests/fourth-test.md "Check the different report types")
* [Fifth test - Run the tests from the CLI](/docs/tests/fifth-test.md "Run the tests from the CLI")
* [Sixth test - REST API test](/docs/tests/sixth-test.md "REST API tests")
* [Seventh test - SOAP API test](/docs/tests/seventh-test.md "SOAP API tests")

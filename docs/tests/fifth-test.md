# FIFTH TEST

This time I want to run the performance tests from the command line (CLI), as running them from the UI consumes more resources (like memory and CPU), which is not recommended for heavy load testing. Additionally, we can integrate the test execution with other CI/CD systems.

`jmeter -n -t <path to the test script> -l <path to the file where you store the results>`

| Column       | Centered        |
| :----------- | :-------------- |
|`-n` | we are using the non-ui mode |
|`-t` | followed by the location of the test plan file we're going to execute |
|`-l` | followed by the location of the file that will contain the test results |

![Alt text](/images/jmeter-from-cli/Run-jmeter-from-CLI_1.png "Run the performance tests from the CLI")

Let's check the content of the generated report:

![Alt text](/images/jmeter-from-cli/Run-jmeter-from-CLI_2.png "Content of the saved results (part 1)")

![Alt text](/images/jmeter-from-cli/Run-jmeter-from-CLI_3.png "Content of the saved results (part 2)")

## Dry Run
Open this [jmx file](/CommandLine%20-%20Test%20Plan.jmx) in JMeter and run the first test.

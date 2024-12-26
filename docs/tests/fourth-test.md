# FOURTH TEST

Time to check more reports (Listeners). 

## Aggregate Report

The `Aggregate Report` summarizes the results in a single line, as it accumulates all the metrics in one line.

What the results mean:

| Column       | Centered        |
| :----------- | :-------------- |
| `Average` | average time the requests took in miliseconds |
| `Median` | half of the results took more than the value shown, and half of the requests took less than that |
| `90% Line` | it means 90% of the requests took less than the value shown |
| `95% Line` | it means 95% of the requests took less than the value shown |
| `99% Line` | it means 99% of the requests took less than the value shown |
| `Min` | the minimum time the requests took to completion |
| `Max` | the maximum time the requests took to completion |
| `Error %` | percentage of errors found |
| `Throughput` | number of requests per second |
| `KB/sec` | the size of the requests per second |


Let's add more threads and iterations and run the tests:
![Alt text](/images/listeners/Listeners_UsersRequest_1.png "Add a Thread Group")

Check the summarized results:
![Alt text](/images/listeners/Listeners_UsersRequest_2.png "Check the Aggregate Report")

## Graph Results

The `Graph Results` report will show the data points, the average, median, deviation and throughput values on a chart.

![Alt text](/images/listeners/Listeners_UsersRequest_3.png "Check the Graph Results")

## Summary Report

The `Summary Report` is similar to the `Aggregate Report` with small differences, as it shows the Standard deviation and average of bytes sent.

![Alt text](/images/listeners/Listeners_UsersRequest_4.png "Check the Summary Report")

## Simple Data Writer Report

We can also add the `Simple Data Writer` report where we can download all the results instead of loading them up in the UI. For that, we just need to specify the file (with an `.xml`, `.jtl` or `.csv` extension) where we will store such results.

![Alt text](/images/listeners/Listeners_UsersRequest_5.png "Check the Simple Data Writer Report")

Select which fields we want to save in the file.

![Alt text](/images/listeners/Listeners_UsersRequest_6.png "Select field to save")

Check the content of the saved report.

![Alt text](/images/listeners/Listeners_UsersRequest_8.png "Check the content of the saved report")

Here's the [saved txt report](/saved-reports/Simple-Data-Writer-report.csv)

## Dry Run
Open this [jmx file](/Feature%20-%20Test%20Plan.jmx) in JMeter and run the fourth test.

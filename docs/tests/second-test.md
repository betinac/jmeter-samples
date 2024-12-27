# SECOND TEST

Now we will simulate multiple users hitting the same page.

* The first step is to add a new Thread Group
* Check the `MultipleUsersVisitHomePage` Thread Group, and update the following values:
    * `Number of Threads (users)`: 10
    * `Ramp-Up period (seconds)`: 20
    * `Loop Count`: 10 
* So we will simulate that 10 users are hitting the same request, and they will not do that concurrently, but in a period of 20 seconds (i.e. 1 user will hit the request, then 2 seconds later the 2nd user, then 2 secons later the 3rd user, and so on). As the `Loop Count` is=10, this scenario will run for 10 iterations (so 10 users times 10 iterations, you should see 100 records in the results).
    
    ![Alt text](/images/multiple-users/MultipleUsersRequest_1.png "Add a new Thread Group")

* Add a new HTTP request, and a report to see the results in a table and in a tree.

    ![Alt text](/images/multiple-users/MultipleUsersRequest_2.png "Add a new HTTP Request")

* Report to view test results in a Table:

    ![Alt text](/images/multiple-users/MultipleUsersRequest_3.png "Report - View Results in Table")

* Report to view test results in a Tree:

    ![Alt text](/images/multiple-users/MultipleUsersRequest_4.png "Report - View Results Tree")

## Dry Run
Open this [jmx file](/Feature%20-%20Test%20Plan.jmx) in JMeter and run the second test.

# Jmeter

1- KIND OF PERFORMANCE TESTS:

Performance testing is a form of software testing that focuses on how a system performs under a particular load. It is not about finding software bugs or defects, but rather about measuring the quality, speed, reliability, and scalability of the system. Performance testing can help developers identify and eliminate bottlenecks, optimize resource usage, and ensure that the system meets the expected performance standards.

• Load Tests: These are tests that simulate an expected amount of users or simultaneous transactions on a system, to verify if it meets the requirements of response time, resource consumption and quality of service. Load tests can be used to validate the system’s ability to support normal or expected demand, or to identify bottlenecks and improvement points. 

• Stress Tests: These are tests that subject the system to extreme or abnormal conditions, such as very high loads, component failures, malicious attacks or network variations. The objective of stress tests is to verify the system’s limits, its robustness, its fault tolerance and its recovery after a critical situation. 

• Spike Tests: These are tests that simulate sudden or unexpected spikes of load on the system, to verify if it can handle these situations without compromising performance or availability. Spike tests can be used to evaluate the system’s behavior in the face of seasonal, promotional or extraordinary events, that generate a significant increase in demand. 

• Stability Tests: These are tests that keep the system under a constant or variable load for a long period of time, to verify if it presents any problem of performance, resource consumption, memory leak or data inconsistency. Stability tests can be used to evaluate the reliability and durability of the system in real or simulated scenarios.

2- HOW IS THE OBJECTIVE TO VALIDATE IN PERFORMANCE TESTS?

The objective of validation is to evaluate whether the system meets the project requirements (user), that is, whether it works as expected and satisfies the customer’s needs. Some important metrics to be considered in the performance test results are:

	• Average response time: it is the average time that the system takes to respond to a user request. The lower this time, the better the system performance.
	• Median: it is the value that divides the distribution of response times into two equal parts, that is, 50% of the requests have response time less than or equal to the median and 50% have response time greater than or equal to the median. This metric is less sensitive to extreme values than the average and can better represent the typical behavior of the system.
	• Standard deviation: it is a measure of dispersion of response times around the average. The higher the standard deviation, the greater the variability of response times and the more inconsistent the system performance.
	• Throughput: it is the amount of requests that the system can process per unit of time, usually expressed in requests per second. The higher the throughput, the greater the system’s ability to meet user demand.
	• Error rate: it is the percentage of requests that failed or were not met by the system. The lower the error rate, the higher the reliability and availability of the system.

The listeners configured in Jmeter are tools that allow you to visualize the performance test results in different formats, such as tables, graphs or files. I usually use:

	• Summary Report: shows a statistical summary of test results, including metrics of average response time, median, standard deviation, throughput and error rate for each request and for the total set of requests.
	• Aggregate Report: shows an aggregated report of test results, similar to Summary Report, but with some additional information, such as minimum and maximum response time and 90th percentile, which indicates the response time below which 90% of requests are.
	• Graph Results: shows a dynamic graph of test results, with the following markings: 
		○ Data: indicates the elapsed time since the start of testing in seconds on the horizontal axis and number of active requests on left vertical axis.
		○ Average: indicates green line that represents average response time in milliseconds on right vertical axis.
		○ Median: indicates blue line that represents median response time in milliseconds on right vertical axis.
		○ Deviation: indicates red line that represents standard deviation of response times in milliseconds on right vertical axis.
		○ Throughput: indicates black line that represents throughput in requests per minute on right vertical axis.

3- HOW TO START A JMETER PROJECT?

To start a Project in Jmeter, you firstly need to :
1 - Download the entire  Jmeter .zp bin in a virtual machine and extract it;
2 - Setup the environment variable;
3 - To open Jmeter you need to executa 'Jmeter.bat' in a bin folder;
4 - Create a Test Plan, giving a name for the test plan;
5  - add Thread Group (that simulates the users) and setup:
     - Nº of threads (users);
     - Ramp-up period (Second);
    - Loop count (second);
   - Important analyse if the performance will be executed using the same user or not. If yes, mark 'Same user on each iteraction' check;
6 - add HTTP request Sampler
	- Setup name, protocol, server name or IP, Port Number, http request, path, parameters (if necessary)
7 - Add listeners to analyse the test result, for example (summary report, aggregate report, graph results);
8 - Click on 'Start' button to start performance test; You could start to execute using prompt command to guarantee more speed; 
	A) jmeter -n -t [file jmx] -l [results files] -e -o [the folder's path where the web report was] 
9 - To erase all performance test results, click on 'Clear all' button (broom icon);
![image](https://github.com/2904201922082022/Jmeter/assets/126620601/1581e2cf-cb07-4467-a6a8-9c28f0eefecf)

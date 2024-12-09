# sustainservLoadTesting
Want to know how many users can be handel by website
1.Test Overview
•	Test Name: Website Stress Test
•	Test Date: 6-12-2024
•	Test Duration: [12/6/24 10:58 PM – 12/6/24 11:05 PM ]
•	Test Type: Stress Test
•	Test Conducted By: Hina Sarmad
•	Website URL : sda.sustainserv.com
________________________________________
2. Test Objective
•	Objective: To determine how many concurrent users the website sda.sustainserv.com can handle before performance degrades or errors occur.
•	Scope: Testing of the Home Page, Login functionality, and Logout pages.
________________________________________
3. Test Configuration
•	Testing Tool: JMeter
•	Number of Users Simulated: 1000
•	Request Type: GET, POST
•	Ramp-up Period: 600ms (The users were ramped up in intervals of 600ms)
•	Loop Count: Infinite loop
•	Request Types: Home Page, Login, Logout, Test, Lunch Application, etc.
________________________________________
4. Test Results
4.1 Summary of Results
•	Total Requests Sent: 3711 requests
•	Successful Requests: 2805 requests (75.59% success rate)
•	Failed Requests: 906 requests (24.41% failure rate)
•	Error Rate: 75.59% of the requests resulted in errors
•	Throughput: 8.89 transactions/second
•	Response Time (Average): 13645.52 ms (over all requests)
 
4.2 Detailed Response Time
•	Minimum Response Time: 125 ms
•	Maximum Response Time: 179134 ms
•	90th Percentile: 90373.00 ms
•	95th Percentile: 90495.40 ms
________________________________________
5. Errors and Issues
•	Error Types:
o	429 Too Many Requests: 1273 errors (45.38%)
o	403 Forbidden: 1100 errors (39.22%)
o	504 Gateway Timeout: 432 errors (15.40%)
•	Error Analysis:
o	The errors are primarily due to rate-limiting (429 errors), which indicates the server is not able to handle a large number of concurrent requests.
o	403 Forbidden errors suggest permission issues or server restrictions.
o	504 Gateway Timeout errors indicate the server could not respond in time due to overload or resource exhaustion.
________________________________________
6. Performance Analysis
•	Observations:
o	Throughput: The system can handle 8.89 transactions per second.
o	Response Time: The response time is very high, with an average of 13645.52 ms, indicating poor performance under load.
o	Server Bottleneck: Based on the errors (429, 403, 504), there appear to be bottlenecks in server capacity or misconfiguration in handling high traffic loads.
•	Max Number of Users Handled: Based on the high error rate and the observed throughput, the website can handle up to around 300-500 concurrent users effectively without excessive performance degradation. Beyond that, errors like 429 (Too Many Requests) and 504 (Gateway Timeout) start to appear, indicating server overload.
________________________________________
 
7. Recommendations
•	System Optimization: Optimize server handling capacity by increasing the server’s resources or load balancing across multiple servers.
•	Rate Limiting Adjustments: Review the current rate limits to ensure they are set appropriately for the expected number of concurrent users.
•	Increase Timeout Thresholds: The 504 errors suggest that the server is unable to process requests within the time limits, so increasing timeout thresholds may help.
•	Optimize Backend: Investigate backend processes that could be slowing down response times, such as database queries or third-party integrations.
________________________________________
8. Conclusion
•	Based on the stress test, the website was able to handle up to 300-500 concurrent users with reasonable performance. After this point, error rates increased significantly, indicating server overload and performance bottlenecks.
•	Next Steps: It is recommended to optimize server performance, increase server capacity, and adjust rate-limiting and timeout settings to accommodate more users.




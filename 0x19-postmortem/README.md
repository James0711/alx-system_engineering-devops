# Post-mortem Summary

## Duration

• Start Time: October 15, 2023, 14:00 WAT
• End Time: October 15, 2023, 17:00 WAT

## Impact

• The service affected was our company e-commerce website.
• Users experienced intermittent outages and slow response times
during the incident.
• Approximately 25% of our users were affected, causing a notable decline in sales and user satisfaction.

## Timeline

• 14:00 (GMT+1): Issue Detected
The issue was detected when the monitoring system triggered
high latency alerts for our website's API.

• 14:10 (GMT+1): Initial Investigation
The operations team initiated an investigation, suspecting a
potential database bottleneck due to increased traffic.

• 14:45 (GMT+1): Misleading Path
Initial findings suggested that the database stress. Database queries were optimized and resources were scaled up
resources.

• 15:15 (GMT+1): Escalation
Despite optimizations, the issue persisted. Incident escalated to the development team, suspecting a code-level problem.

• 15:30 (GMT+1): Code Review
Developers identified a recent code deployment with a
performance regression. A new product recommendation
Algorithm contained a bug causing excessive database queries.

• 15:45 (GMT+1): Temporary Workaround
To mitigate the issue, the recent code deployment was rolled back,
temporarily improving performance.

• 16:00 (GMT+1): Full Resolution
Developers quickly patched the code issue by optimizing the
recommendation algorithm. The fix was deployed resulting in a
significant improvement in response times.

• 17:00 (GMT+1): Issue Resolved
Monitoring confirmed full service recovery, and
response times returned to normal levels.

## Root Cause and Resolution

• Root Cause:
A faulty product recommendation algorithm introduced a performance regression, leading to excessive and inefficient database queries

• Resolution:
Developers optimized the recommendation algorithm, reducing database queries.
Problematic code deployment was rolled back for temporary stability.
The optimized code underwent thorough testing and was deployed to the production environment


## Corrective and Preventative Measures:

To address the issue: The following reviews were done to curtail the challenge
1. Code Review Process Enhancement:
Implement stricter code review processes to identify performance regressions before deployment

2. Monitoring Improvements:
Enhance monitoring systems for more granular insights into system performance, enabling quicker issue detection.

3. Automated Testing:
Develop comprehensive automated tests, including performance testing, to identify potential bottlenecks.

4. Load Testing:
Conduct regular load testing to simulate high traffic scenarios and ensure the system can handle increased loads without degrading performance.

Preventative Measures

1. Performance Regression Checks:
Implement automated tools analyzing code changes for potential performance regressions before merging into the main branch..



2. Continuous Monitoring:
Invest in continuous monitoring and alerting systems for proactive identification of performance issues

3. Redundancy and Scalability:
Develop plans for scaling infrastructure horizontally and vertically to handle unexpected traffic spikes


4. Documentation and Training:
Ensure all team members are well-trained in performance optimization techniques and maintain up-to-date documentation on best practices.
on best practices.

## Conclusion
By implementing these measures, our goal is to prevent similar incidents in the future, ensuring the reliability and performance of the company’s e-commerce platform.



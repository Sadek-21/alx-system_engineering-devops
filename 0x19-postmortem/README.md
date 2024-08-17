# 0x19. Postmortem

**By Sadek Mohamed**

## Introduction
In this project, I will write a postmortem report for a hypothetical outage that occurred in our system. A postmortem is a critical tool used in the tech industry to analyze the cause of an outage, understand the impact, and ensure it doesn't happen again.

## Issue Summary
**Duration**: 3 hours, from 2:00 PM to 5:00 PM (UTC)  
**Impact**: The main website was unavailable for 70% of users during the outage. As a result, users could not access key services, leading to significant frustration and potential loss of revenue.  
**Root Cause**: A configuration error in the load balancer caused traffic to be routed incorrectly, overwhelming certain servers while leaving others underutilized.

## Timeline
- **2:00 PM**: Monitoring system alerted a sharp drop in server response times.
- **2:05 PM**: The issue was confirmed by engineers, suspecting a sudden spike in traffic.
- **2:10 PM**: The network team was notified, and initial investigations focused on potential DDoS attacks.
- **2:30 PM**: Misleading debugging paths involved increasing security measures, which did not resolve the issue.
- **3:00 PM**: The issue was escalated to the infrastructure team, who identified the load balancer configuration error.
- **4:00 PM**: The load balancer settings were corrected, and services began to recover.
- **5:00 PM**: Full functionality was restored, and monitoring confirmed stability.

## Root Cause and Resolution
The root cause was an incorrect configuration in the load balancer, which led to uneven distribution of traffic. Some servers received too much traffic while others were idle. To fix the issue, we adjusted the load balancer settings to evenly distribute the load across all servers, restoring normal functionality.

## Corrective and Preventative Measures
To prevent this issue from recurring:
- **Improve Load Balancer Configuration**: Review and update the configuration process to ensure settings are verified before deployment.
- **Enhanced Monitoring**: Implement more granular monitoring to detect traffic imbalances sooner.
- **Load Testing**: Conduct regular load tests to identify potential weaknesses in traffic distribution.
- **Training**: Provide additional training for the team on load balancer configurations and traffic management.

## Making It Engaging
To make this postmortem more engaging, consider adding a humorous analogy:
*"It was as if our load balancer was playing favorites, sending all the guests to one room while the others remained empty!"*
Also, consider adding a simple diagram that shows how traffic was being misrouted before and after the fix.

## Additional Resources
- **Postmortem Document**: [Google Docs Link](https://docs.google.com/document/d/1cc0O4o23eA4JnANrhi_cxkJIuysUhEKhO4Bc9Oaoua8/edit?usp=sharing)


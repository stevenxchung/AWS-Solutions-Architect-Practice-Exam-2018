# Practice Exam 5

Topics to review:

1. Distributed session data management -> ElasticCache.

2. Consumers (such as a custom application running on Amazon EC2, or an Amazon Kinesis Data Firehose delivery stream) can store their results using an AWS service such as Amazon DynamoDB, Amazon Redshift, or Amazon S3.

3. A golden image means it is a customized AMI.

4. Spot instances charges:
  * Terminated or stopped by AWS within the first hour -> No charge
  * Terminated or stopped by AWS within the subsequent hour -> Charged to the nearest second
  * Terminate yourself -> Charged to the nearest second
  * Note: you do not pay what you bid on spot prices, if your bid price is higher or lower than the spot price you will still pay the **spot price**

5. A service that collect, process, and analyze data in real-time -> Amazon Kinesis.

6. AWS Trusted Advisor analyzes your AWS environment and provides best practice recommendations in these five categories: Cost Optimization, Performance, Fault Tolerance, Security, and Service Limits.

7. Amazon plans:
  * Basic - 24x7 access to resources
  * Developer - 24x7 access to resources
  * Business - 24x7 access to resources + full set of Trusted Advisor checks (cheaper)
  * Enterprise - 24x7 access to resources + full set of Trusted Advisor checks (expensive)

8. Amazon RDS and DynamoDB are examples of managed services in AWS.

9. Tags enable you to categorize your AWS resources in different ways, for example, by purpose, owner, or environment. This is useful when you have many resources of the same type — you can quickly identify a specific resource based on the tags you've assigned to it.

10. A network access control list (ACL) is an optional layer of security for your VPC that acts as a firewall for controlling traffic in and out of one or more subnets. This means that if you block an IP address in the Network ACL, it would not be able to access your VPC anymore.

11. If an instance is showing out of service the health check configuration may not be properly defined.

12. You can use Run Command from the console to configure instances without having to login to each instance.

13. If an EC2 retrieves a message from SQS and crashes, the message will become available for processing by other EC2 instances after the VTO (visability timeout) expires.

14. Types of load balancers:
  * Application Load Balancer -> HTTP and HTTPS
  * Network Load Balancers -> TCP

15. To access an EC2 from the internet:
  * IGW (Internet Gateway) attached to the VPC
  * Route entry to the IGW in the route table of the VPC
  * A public IP attached to the EC2 instance

16. If the Hardward Security Module has be zeroed in CloudHSM, the keys are lost permanently if you did not have a copy.

17. In CloudFormation you can check the Outputs section for DNS hostname of the ELB

18. IAM roles are global service that are available to all regions. All you have to do is assign the existing IAM role to the instance in the new region.

19. By using Cached volumes, you store your data in Amazon Simple Storage Service (Amazon S3) and retain a copy of frequently accessed data subsets locally in your on-premise network. Cached volumes offer substantial cost savings on primary storage and minimize the need to scale your storage on-premises. You also retain low-latency access to your frequently accessed data.

20. AWS Elastic Beanstalk makes it easier for developers to quickly deploy and manage applications in the AWS Cloud. Developers simply upload their application and Elastic Beanstalk automatically handles the deployment details of capacity provisioning, load balancing, auto-scaling, and application health monitoring.

21. Cloud infrastructure which allows you to leverage existing security controls in AWS while having the ability to communicate with on-premise network -> AWS Directory Services, VPN connection, and Amazon Workspaces.

22. You manage your DB engine configuration through the use of parameters in a DB parameter group. DB parameter groups act as a container for engine configuration values that are applied to one or more DB instances.

23. A VPC endpoint enables you to privately connect your VPC to supported AWS services and VPC endpoint services powered by PrivateLink without requiring an internet gateway, NAT device, VPN connection, or AWS Direct Connect connection. Instances in your VPC do not require public IP addresses to communicate with resources in the service. Traffic between your VPC and the other service does not leave the Amazon network

24. Amazon SQS automatically deletes messages that have been in a queue for more than the maximum message retention period. The default message retention period is 4 days. Since the queue is configured to the default settings and the batch job application only processes the messages once a week, the messages that are in the queue for more than 4 days are deleted.

25. AWS CloudHSM provides hardware security modules in the AWS Cloud. A hardware security module (HSM) is a computing device that processes cryptographic operations and provides secure storage for cryptographic keys.

26. Elastic Load Balancing provides access logs that capture detailed information about requests sent to your load balancer. Each log contains information such as the time the request was received, the client's IP address, latencies, request paths, and server responses. You can use these access logs to analyze traffic patterns and troubleshoot issues.

27. Databases which do not support read replicas:
  * Oracle
  * Microsoft SQL Server
  * MongoDB

28. The CloudWatch Logs agent provides an automated way to send log data to CloudWatch Logs from Amazon EC2 instances. The agent is comprised of the following components:
  * A plug-in to the AWS CLI that pushes log data to CloudWatch Logs.
  * A script (daemon) that initiates the process to push data to CloudWatch Logs.
  * A cron job that ensures that the daemon is always running.

29. Just maintain a single snapshot of the EBS volume since the latest snapshot is both incremental and complete.

You can back up the data on your Amazon EBS volumes to Amazon S3 by taking point-in-time snapshots. Snapshots are incremental backups, which means that only the blocks on the device that have changed after your most recent snapshot are saved. This minimizes the time required to create the snapshot and saves on storage costs by not duplicating data.

When you delete a snapshot, only the data unique to that snapshot is removed. Each snapshot contains all of the information needed to restore your data (from the moment the snapshot was taken) to a new EBS volume.

30. In event of an AWS Aurora failover:
  * The Aurora Replica will flip the CNAME of the primary instance to point at the healthy replica which in turn will be promoted to the new pirmary
  * If there are no Aurora Replicas, AWS Aurora will attempt to create a new DB instance in the same AZ as the original and if that fails it will try to create a new DB instance in another AZ

31. CloudTrail encrypts all log files by default.

32. Amazon Route 53 can help configure the DNS zone apex record to point to the load balance by creating an A record aliased to the load balancer DNS name.

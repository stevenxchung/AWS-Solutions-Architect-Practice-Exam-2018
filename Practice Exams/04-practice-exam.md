# Practice Exam 4

Topics to review:

1. Require storage service that provides the scale and performance that their big data applications require such as high throughput to compute nodes coupled with read-after-write consistency and low-latency **file** operations -> EFS.

2. Detailed logging and auditing in S3 -> Enable server access logging for all required S3 buckets.

3. In AWS VPC, an instance retains it's private IP addresses when the instance is stopped.

4. Shell scripts to duplicate resources in another region -> AWS CloudFormation.

5. Running an EC2 instance or having EBS volumes attached to stopped EC2 instances will incur a cost.

6. If an instance is in the public subnet (also has same AMI and security group configuration as others) but cannot be accessed from the internet, try assigning an Elastic IP address to the instance.

7. Acts as a firewall that controls the traffic allowed to reach one or more instances -> Security group.

8. Automated way to perform configuration tasks and run start scripts after the instance starts -> User data

9. If something is being processed twice where required once try using AWS SWF.

10. Basic monitoring metrics from AWS CloudWatch for RDS:
  * Amount of available random access memory
  * Average number of disk I/O operations per second during the polling period
  * Percentage of CPU utilization

11. When you create or update a distribution in Cloudfront, you can add an origin access identity (OAI) and automatically update the bucket policy to give the origin access identity permission to access your bucket. Alternatively, you can choose to manually change the bucket policy or change ACLs, which control permissions on individual objects in your bucket.

12. This allows you to use Amazon CloudFront to protect your web application, even if you are not serving static content. Amazon CloudFront only accepts well-formed connections to prevent many common DDoS attacks like SYN floods and UDP reflection attacks from reaching your origin. DDoS attacks are geographically isolated close to the source, which prevents the traffic from affecting other locations. These capabilities can greatly improve your ability to continue serving traffic to end users during larger DDoS attacks. You can use Amazon CloudFront to protect an origin on AWS or elsewhere on the Internet.

13. S3 bucket URL format: < bucket-name >.s3-website-< AWS-region >.amazonaws.com

14. Amazon Athena is an interactive query service that makes it easy to analyze data directly in Amazon Simple Storage Service (Amazon S3) using standard SQL. With a few actions in the AWS Management Console, you can point Athena at your data stored in Amazon S3 and begin using standard SQL to run ad-hoc queries and get results in seconds.

Athena is serverless, so there is no infrastructure to set up or manage, and you pay only for the queries you run. Athena scales automatically—executing queries in parallel—so results are fast, even with large datasets and complex queries.

Athena helps you analyze unstructured, semi-structured, and structured data stored in Amazon S3. Examples include CSV, JSON, or columnar data formats such as Apache Parquet and Apache ORC. You can use Athena to run ad-hoc queries using ANSI SQL, without the need to aggregate or load the data into Athena.

15. Spot instances are terminated by default when interrupted.

16. Minimum size of an object that can be uploaded in a bucket -> 0 byte.

17. EBS statuses:
  * **ok** -> All checks pass
  * **impaired** -> A check fails
  * **insufficient-data** -> Checks in progress

18. Integrating AWS IAM with an on-premise LDAP directory service -> Develop an on-premise custom identity broker app and use STS to issue short-lived AWS credentials.

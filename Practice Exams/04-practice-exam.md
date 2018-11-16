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

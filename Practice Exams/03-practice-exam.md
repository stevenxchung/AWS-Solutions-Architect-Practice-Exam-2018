# Practice Exam 3

Topics to review:

1. The retention period for a one-minute datapoint in AWS CloudWatch is 15 days.

2. If you are not able to connect to the web server using your browser:
  * Check the security group rules
  * Check the route table

3. An AWS SWF decision task tells the decider the state of the workflow execution.

4. Need EC2 to run continuously for years -> Reserved instances.

5. S3 encryption at rest can be achieved by:
  * Using S3 server-side S3-managed keys (SSE-S3)
  * Using S3 server-side encryption with AWS KMS (SSE-KMS)
  * Using S3 server-side encryption with customer-provided keys (SSE-C)
  * Using client-side encryption with AWS KMS (CMK)
  * Using client-side encryption with their master key

6. To limit a third party app to a specific S3 bucket:
  * Create an IAM user for the third party app
  * Set up a custom user policy which only allows access to the specific S3 bucket

7. When an EC2-VPC instance with an Elastic IP is stopped and started:
  * The underlying host for the instance is possibly charged
  * All data on the attached instance-store devices will be lost

8. CloudFront supports the following as origin servers:
  * S3 buckets
  * HTTP or web servers hosted in EC2 or in private web servers

9. Standard queues in SQS do **not** preserve the order of messages.

10. The following are invalid VPC peering configurations:
  * Overlapping CIDR blocks
  * Transitive peering
  * Edge to edge routing via a gateway

11. To create a new AMI and launch a fleet of EC2 instances create a new launch configuration.

12. In S3 the following statements are true:
  * The total volume of the data and number of objects your can store are unlimited
  * S3 is a simple key-based object store
  * The largest object that can be uploaded in a single PUT is 5 GB

13. You are limited to running a total of 20 On-Demand instances across the instnace family. Additionally, if the maximum size of your Auto Scaling group has been reached, it would not create any new EC2 instance.

14. When an EC2 instance is terminated:
  * The root device volume is deleted by default
  * The root volume is deleted by default - EBS-backed instances
  * All the data is deleted on all volumes - Instance store-backed AMI

15. Benefits of using read replicas:
  * It provides elasticity to the AWS RDS database
  * It improves performance of the primary database by taking workload from it

16. For VPC subnets:
  * Each subnet maps to a single AZ
  * Every subnet that you create is automatically associated with the main route table for the VPC
  * If a subnet's traffic is routed to an IGW, the subnet is known as a public subnet

17. ELBs are designed to run in one region and not across multiple regions.

18. To setup a bastion host in the cheapest yet most secure way:
  * Setup a small EC2 instance and a security group which only allows access on port 22 via your IP address

19. You are only billed when an EC2 is running.

20. To setup a Linux bastion host which will allow access to the EC2 instances via clients connecting from the corporate external public IP; set up a security group inbound rule with TCP protocol on port range 22, source xxx.xx.xxx.xxx/32

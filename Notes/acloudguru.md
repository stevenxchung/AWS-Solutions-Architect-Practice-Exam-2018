# EC2

1. Do EBS volumes persist independently from the life of an EC2 instance?

# Mega Quiz 1 Review

1. S3 is an object based storage.

2. A policy is a document that provides a formal statement of one or more permissions.

3. To allow EC2 to access other resources such as S3, use IAM roles.

4. EBS -> Elastic Block Storage.

5. Vulnerability scans require notifying AWS first.

6. You cannot access the OS for RDS instances.

7. Opening port 22 to 0.0.0.0/0 CIDR is a massive security risk.

8. Manage your EC2 instances with tags.

9. AZs are distinct zones within a region which are isolated from failures.

10. RDS Aurora stores 6 copies of data by default.

11. Maximum RDS retention period -> 35 days.

12. Automated backups are enabled by default for a new DB instance.

13. RDS does not support increasing storage on a SQL Server DB instance.

14. You can now scale the storage of RDS for SQL Server as of 2017.

15. Provisioned IOPS RDS -> OLTP.

16. To run a DB on an EC2 use EBS.

17. You cannot move a Reserved EC2 instance from one region to another.

18. When creating a new security group all inbound traffic is denied while all outbound traffic is allowed by default.

19. AWS RDS Engine Types:
  * Aurora
  * PostgreSQL
  * MySQL
  * MariaDB
  * Oracle
  * SQL Server

# Final Exam

1. If there is a separate environment for DEV, QA, STAGE, and PROD, they will need to be isolated from each other. Use separate VPCs in this case.

2. By default, all subnets are able to communicate with each other using the main route table.

3. Redshift uses a block size of 1 MB or 1024 KB for columnar storage.

4. Auto Scaling termination policy:
  * Determine which AZs have the most instances
  * Determine which instance has the oldest launch configuration

5. Maximum visibility timeout -> 12 hours.

6. Network access logging -> Make use of an OS level logging tool such as IP tables and log events to CloudWatch or S3.

7. The public IP is not managed on the instance, it is an alias applied as a NAT (network address translation) or the private IP address.

8. Spread instances our to maximize fault tolerance.

9. DynamoDB automatically spreads the data and traffic for your tables over a sufficient number of servers to handle your throughput and storage requirements, while maintaining consistent and fast performance. All of your data is stored on solid state disks (SSDs) and automatically replicated across multiple Availability Zones in an AWS region, providing built-in high availability and data durability.

10. The attribute name and value cannot exceed 400 KB in DynamoDB.

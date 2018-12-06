# Practice Exam 6

Topics to review:

1. On start:
  * EC2-Classic -> Private IPv4 address
  * EC2-VPC -> Static IPv4 address (does not change)

2. Distribute requests to EC2s in multiple AZs -> Cross-zone load balancing

3. The recommended storage engine for MySQL is InnoDB and **not** MyISAM which is more heavy duty

4. Workloads that require high, sequential read and write access to very large data sets on local storage -> Storage Optimized Instances

5. Lambda max execution duration per request -> 15 minutes

6. An Elastic IP address doesn’t incur charges as long as the following conditions are true:
  * The Elastic IP address is associated with an Amazon EC2 instance.
  * The instance associated with the Elastic IP address is running.
  * The instance has only one Elastic IP address attached to it.

7. You can manage the following in IAM:
  * API Keys
  * MFA
  * Roles
  * Users
  * Groups
  * Policies

8. Different types of DNS record support in Route 53:
  * A (address record)
  * AAAA (IPv6 address record)
  * CNAME (canonical name record)
  * CAA (certification authority authorization)
  * MX (mail exchange record)
  * NAPTR (name authority pointer record)
  * NS (name server record)
  * PTR (pointer record)
  * SOA (start of authority record)
  * SPF (sender policy framework)
  * SRV (service locator)
  * TXT (text record)

9. Mobile app using OpenID Connect compatible identity provider -> AWS STS with Web Identity Federation

10. Problems connecting to EC2 with RDP (already has public IP, IGW, and routes) -> Adjust security group to allow traffic from port 3389

11. Benefits of adding multi-AZ deployments in AWS RDS:
  * Increased database availability in the case of system upgrades like OS patching or DB instance scaling
  * It makes the data fault-tolerant to an AZ failure

12. You can send log data to CloudWatch Logs from EC2 by using the CloudWatch Logs agent. The CloudWatch Logs agent is comprised of the following components:
  * A plug-in to the AWS CLI that pushes log data to CloudWatch Logs
  * A script (daemon) that initiates the process to push data to CloudWatch Logs
  * A cron job that ensures that the daemon is always running

13. Business division autonomy + cost oversight from IT:
  * Enable IAM cross-account access for all IT admins
  * Use AWS Consolidated Billing by creating AWS organizations to link the divisions' accounts to a parent corporate account

14. How can you improve the availability of your Aurora database to prevent any unnecessary downtime of the online portal -> Amazon Aurora Replicas

15. Different types of IAM identities:
  * Users
  * Roles
  * Groups

16. Elastic web tier services:
  * ELB
  * EC2
  * Auto Scaling

17. What does a new IAM User need to be able to make API calls? A set of access keys

18. VPC feature that allows the IPv6 EC2 instance to communicate to the internet but prevents inbound traffic -> Egress-only IGW (egress-only Internet gateway is a horizontally scaled, redundant, and highly available VPC component that allows outbound communication over IPv6 from instances in your VPC to the Internet, and prevents the Internet from initiating an IPv6 connection with your instances, for IPv4 user NAT gateway instead)

19. IAM user access URL: https://<Account Id>.signin.aws.amazon.com/console/

20. Services which can be used for session management:
  * ElastiCache
  * AWS RDS
  * DynamoDB


# Practice Exam 6

Topics to review:

1. On start:
  * EC2-Classic -> Private IPv4 address
  * EC2-VPC -> Static IPv4 address (does not change)

2. Distribute requests to EC2s in multiple AZs -> Cross-zone load balancing

3. The recommended sotrage engine for MySQL is InnoDB and **not** MyISAM which is more heavy duty

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

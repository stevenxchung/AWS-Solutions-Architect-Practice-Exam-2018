# Practice Exam 2

Topics to review:

1. To login to an EC2 instance use key pairs. To see API calls use access keys.

2. AMIs are a regional resource, if needed in another region, they must be copied over.

3. These are the key reasons to use S3 Standard - IA:
  * It is designed for data that is accessed less frequently
  * It is designed for data that requires rapid access when needed
  * It is ideal for long-term storage, backups, and as a data store for disaster recovery

4. To secure AWS credentials like access keys and secret access keys:
  * Enable MFA
  * Assign an IAM role to the EC2 instance

5. AWS Storage Gateway and Glacier encrypts data at rest by default.

6. Perfect Forward Secrecy is used to offer SSL/TLS cipher suites for CloudFront and ELB. It provies additional safeguards against the eavesdropping of encrypted data, through the use of a unique random session key. This prevents the decoding of captured data, even if the secret long-term key is compromised.

7. You can back up the data on EBS volumes to S3 by creating snapshots of EBS volumes.

8. Key reasons to use EBS:
  * When you create an EBS volume in an Availability Zone, it is automatically replicated within that zone to prevent data loss due to failure of any single hardware component
  * An EBS volume is off-instance storage that can persist independently from the life of an instance
  * EBS volumes support live configuration changes while in production which means that you can modify the volume type, volume size, and IOPS capacity without service interruptions
  * Amazon EBS encryption uses 256-bit Advanced Encryption Standard algorithms (AES-256)

9. Prerequisites for routing traffic to a website hosted in an S3 bucket:
  * The bucket must have the same name as your domain or subdomain
  * A registered domain name
  * Route 53 as the DNS service for the domain

10. Possible event notifications for S3 buckets:
  * SNS
  * SQS
  * Lambda Function

11. You can use Route 53 with failover option to a static S3 website bucket or CloudFront distribution in an event of a load failure.

12. To establish a successful site-to-site VPN an internet-routable IP address (static) of the customer gateway's external interface for the on-premise network will need to be configured. Figure 2-1 depicts how a site-to-site VPN is established.
<div align="center">
  <img src="2-1-site-to-site-vpn.jpg">
  <h3>Figure 2-1. Site-to-site VPN connection from the customer to the AWS VPC</h3>
</div>

13. A bastion host is a special purpose computer on a network specifically designed and configured to withstand attacks. If you have a bastion host in AWS, it is basically just an EC2 instance. It should be in a public subnet with either a public or Elastic IP address with sufficient RDP or SSH access defined in the security group. Users log on to the bastion host via SSH or RDP and then use that session to manage other hosts in the private subnets.

14. Amazon Glacier is used for storing infrequently accessed data and storing data archives.

15. When failing over, Amazon RDS simply flips the canonical name record (CNAME) for your DB instance to point at the standby, which is in turn promoted to become the new primary.

16. Security Groups usually control the list of ports that are allowed to be used by your EC2 instances and the NACLs control which network or list of IP addresses can connect to your whole VPC.

17. To route domain traffic to an ELB load balancer, use Amazon Route 53 to create an alias record that points to your load balancer. An alias record is a Route 53 extension to DNS. It's similar to a CNAME record, but you can create an alias record both for the root domain, such as tutorialsdojo.com, and for subdomains, such as portal.tutorialsdojo.com. Use alias with type "AAAA" or "A" record set.

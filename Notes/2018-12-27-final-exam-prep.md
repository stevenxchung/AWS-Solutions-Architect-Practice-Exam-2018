# Test 1 Final Review

1. Lambda automatically encrypts environment variables with KMS. By default, a KMS key is created when creating a Lambda function. However, if you want to use encryption helpers you will need to create a new KMS key (default key will give you errors) which will allow you to manage them easily.

2. Kinesis Data Firehose loads streaming data into four main services:
  * S3
  * Redshift
  * ElasticSearch Service
  * Splunk

3. If write throughput to the database needs to be increased try using a RAID (RAID is joining a bunch of EBS volumes together) configuration or increasing the size of the EC2 instance. RAID 0 stripes multiple volumes together whereas RAID 1 mirrors 2 volumes together.

4. EBS can encrypt data at rest, data moving between the volume and instance, snapshots, and volumes created from encrypted snapshots. Knowing this, there are ways you can protect your unencrypted EBS volume:
  * Apply encryption to the volume while copying the unencrypted volume as a snapshot, then from that encrypted snapshot restore to an encrypted EBS volume
  * Create a new encrypted EBS volume, move data to the new volume, and delete the old unencrypted volume

5. There are no default EC2 CloudWatch metrics for:
  * Memory utilization
  * Disk swap utilization
  * Disk space utilization
  * Page file utilization
  * Log collection

# Test 2 Final Review

1. EBS volumes are only available in the same AZ as the EC2 instance.

2. If internet problems in the VPC can be isolated to a single instance try adding a public IP or EIP. If there is more than one instance involved the problem could be associated with route tables, IGW, NACL, or security groups.

3. Snowball can move 50-80 TB whereas Snowball Edge can transfer up to 100 TB.

4. The EC2 auto scaling cooldown period:
  * Ensures that the ASG (auto scaling group) does not launch or terminate additional EC2 instances before the previous scaling activity takes effect
  * Has a default value of 300 seconds or 5 minutes
  * Is a configurable setting for your ASG

5. A customer gateway is a physical device or software on your side of the VPN connection. To create a VPN connection you must create a customer gateway and setup an internet-routable IP address (static).

# Test 3 Final Review

1. To store sensitive data on EBS or S3:
  * Use EBS encryption
  * S3 client-side via KMS keys or customer supplied master keys
  * S3 server side via SSE-S3, SSE-KMS, SSE-C

Additionally, it is recommended to:
  * Configure CloudFront to deliver content over HTTPS using custom domain names with an SSL certificate
  * Configure origin access identity to prevent S3 objects from being directly accessed publicly via S3 URL
  * Configure access permissions with a bucket policy

2. Glacier retrieval times are as follows:
  * Expedited: 1-5 minutes (requires purchasing Provisioned Capacity)
  * Standard: 3-5 hours
  * Bulk: 5-12 hours (lowest cost retrieval option)

3. Read replicas provide elasticity to your RDS database and improves performace of the primary database by taking workload from it (read replicas do not improve the actual read throughput on the primary instance however, watch out for wording).

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

# Test 4 Final Review

1. Below are several of services which are not well known/recently added by AWS:
  * S3 Select - Provides ability to retrieve a subset of data from an object in S3 using simple SQL expressions
  * Athena - **Serverless** interactive query service that makes it easy to analyze data in S3 using standard SQL
  * Redshift Spectrum - Allows you to directly run **complex** SQL queries against exabytes of unstructured data in S3
  * Neptune - A fully-managed graph database that makes it easy to build and run applications that work with highly connected datasets
  * X-Ray - Provides an end-to-end view of requests as they travel through your application, and shows a map of your application's underlying components
  * Glue - A fully-managed ETL (extract, transform, and load) service that makes it easy for customers to prepare and load their data for analytics

2. In Cognito, you can add multi-factor authentication (MFA) to a user pool to protect the identity of your users. MFA adds a second authentication method that doesn't rely solely on user name and password. You can choose to use SMS text messages, or time-based one-time (TOTP) passwords as second factors in signing in your users. You can also use adaptive authentication with its risk-based model to predict when you might need another authentication factor. It's part of the user pool advanced security features, which also include protections against compromised credentials.

# Test 5 Final Review

1. API Gateway is a fully-managed service which can create APIs that act as a front-door for applications to access data, business logic, or functionality from back-end services. All APIs created with API Gateway expose **HTTPS** endpoints only. API Gateway does not support unencrypted (HTTP) endpoints.

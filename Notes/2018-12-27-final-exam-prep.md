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


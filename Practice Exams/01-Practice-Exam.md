# Practice Exam 1

Topics to review:

1. The EC2-Classic platform does not retain its associated Elastic IP addresses when the EBS-backed EC2 instance is stopped.

2. Pre-built AMIs are not accessible to another region so you have to copy them to another region to properly establish disaster recovery.

3. AWS DynamoDB Accelerator DAX that can reduce Amazon DynamoDB response times from milliseconds to microseconds, even at millions of requests per second.

4. Transferring data from an EC2 instance to an S3 instance to an S3 bucket in the same region has no cost at all.

5. If a company is using a corporate Active Directory, it is best to use AWS Directory Service AD Connector for easier integration. In addition, since the roles are already assigned using groups in the corporate Active Directory, it would be better to also use IAM Roles.

6. AWS Elastic Map Reduce and EC2 are not managed services meaning that you can have access to the underlying operating system for the resource.

7. In an enterprise identity federation, you can authenticate users in your organization's network, and then provide those users access to AWS without creating new AWS identities for them and requiring them to sign in with a separate user name and password. This is known as the single sign-on (SSO) approach to temporary access. AWS STS supports open standards like Security Assertion Markup Language (SAML) 2.0, with which you can use Microsoft AD FS to leverage your Microsoft Active Directory. You can also use SAML 2.0 to manage your own solution for federating user identities.

8. Amazon Elastic File System (Amazon EFS) provides simple, scalable3, elastic file storage for use with AWS Cloud services and on-premises resources. When mounted on Amazon EC2 instances, an Amazon EFS file system provides a standard file system interface and file system access semantics, allowing you to seamlessly integrate Amazon EFS with your existing applications and tools. Multiple Amazon EC2 instances can access an Amazon EFS file system at the same time, allowing Amazon EFS to provide a common data source for workloads and applications running on more than one Amazon EC2 instance.

9. If your Spot instance is terminated or stopped by Amazon EC2 in the first instance hour, you will not be charged for that usage. However, if you terminate the instance yourself, you will be charged to the nearest second. If the Spot instance is terminated or stopped by Amazon EC2 in any subsequent hour, you will be charged for your usage to the nearest second. If you are running on Windows and you terminate the instance yourself, you will be charged for an entire hour.

10. To apply high availability and fault tolerance without an ELB, you can write a script that checks the health of the EC2 instance (if instance does not respond then the script will switch the elastic IP address to a standby EC2 instance) and assigns an elastic IP address to the instance.

11. Snapshots occur asynchronously which means that the point-in-time snapshot is created immediately, but the status of the snapshot is pending until the snapshot is complete (when all of the modified blocks have been transferred to Amazon S3), which can take several hours for large initial snapshots or subsequent snapshots where many blocks have changed. While it is completing, an in-progress snapshot is not affected by ongoing reads and writes to the volume hence, you can still use the volume.

12. If you need a highly available DB and full control over the OS, try using AWS EC2 instances with data replication between two different AZs.

13. If traffic spikes are expected and the backend needs to be protected we can use throttling limits in API gateway. Amazon API Gateway provides throttling at multiple levels including global and by a service call. Throttling limits can be set for standard rates and bursts. For example, API owners can set a rate limit of 1,000 requests per second for a specific method in their REST APIs, and also configure Amazon API Gateway to handle a burst of 2,000 requests per second for a few seconds.

14. You can configure your application to use the KMS API to encrypt all data before saving it to disk.

15. For DynamoDB tables, the optimal usage of a table's provisioned throughput depends not only on the workload patterns of individual items, but also on the partition-key design. This doesn't mean that you must access all partition key values to achieve an efficient throughput level, or even that the percentage of accessed partition key values must be high. It does mean that the more distinct partition key values that your workload accesses, the more those requests will be spread across the partitioned space. In general, you will use your provisioned throughput more efficiently as the ratio of partition key values accessed to the total number of partition key values increases.

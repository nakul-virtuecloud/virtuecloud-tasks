# tasks solutions

*Q.How to do Static website hosting on S3.(React, HTML)*
- Create bucket
- Enable versioning 
- Allow all access to bucket from permissions 
- Generate bucket policies from permissions 
- Static website hosting from properties

**Q.How S3 synchronization of bucket from one region to another.(replication)**
- You can replicate data between AZ and region as well (disaster recovery) and versioning must be enabled
*types of replication*
 - S3 Same-Region Replication (SRR)
 - S3 Cross-Region Replication (CRR) 
 - S3 Replication Time Control (S3 RTC) 

If you need a guarantee that your files will be copied to another location within a specific time (usually 15 minutes), you use S3 RTC.
It's like paying for a faster, more reliable delivery service for your data.

To replicate existing objects, you can use S3 Batch Replication 

**What you will accomplish In this task, you will:
Create an S3 bucket** 

- Create an S3 Replication rule on your S3 bucket
- Choose destination S3 bucket
- Choose or create IAM roles for replication
- Specify encryption type (optional)
- Choose destination S3 storage class
- Enable additional replication options (optional)

**Q.S3 bucket actions using aws SNS.(notification send when something happen in s3)**

Whenever you want to send any notification use this service
- Publisher - who send notifications
- Subscriber - who gets notifications
first Create topic then create subscriber.

so While creating topic you can add policy to that topic as well like no, of retries,maxiumum delay etc.

- triggering notifications through Amazon SNS (Simple Notification Service) when some actions/events happen in an S3 bucket — like file uploads, deletions, or changes.
- You configure your S3 bucket to send notifications to an SNS topic when specific events happen. Then subscribers to that SNS topic (email, SMS, Lambda, SQS, etc.) will be notified.

# SecurityGroup_watch
Observe security groups for any updates on inbound rules.


Steps to observe modification in SG.

> Create the S3 bucket and configure the bucket policy to push logs from Cloud Trail.

> Navigate to Cloud Trail, create the trail, with existing S3 bucket. It will start pushing the logs to S3 bucket.

> Once Trail has been configured, navigate to SNS dashboard and create the topic. Configure the Subscriptions for the topic. 

> Navigate to Cloudwatch > Events > Rules then create rule with proper Event pattern and Targets.

Once above configuration is done, we will receive the notification email once changes occured in Security groups.
Cloud Trail is global service. It will start captchuring the API across regions. 

https://docs.aws.amazon.com/awscloudtrail/latest/userguide/how-cloudtrail-works.html 

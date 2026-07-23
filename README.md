# Cloud_Cost_Optimization
Identifying Stale EBS Snapshots
In this example, we'll create a Lambda function that identifies EBS snapshots that are no longer associated with any active EC2 instance and deletes them to save on storage costs.

Description:
The Lambda function fetches all EBS snapshots owned by the same account ('self') and also retrieves a list of active EC2 instances (running and stopped). For each snapshot, it checks if the associated volume (if exists) is not associated with any active instance. If it finds a stale snapshot, it deletes it, effectively optimizing storage costs.
This Project can be extended to perform this functions:
1. EC2 Rightsizing Engine

Uses CloudWatch metrics to recommend smaller instance types for consistently underutilized instances.

2. Unattached EBS Volume Cleanup

Finds orphaned EBS volumes and notifies or deletes them after approval.

3. Elastic IP Optimizer

Identifies Elastic IPs not associated with running instances and releases them.

4. S3 Intelligent Lifecycle Analyzer

Detects buckets without lifecycle policies and recommends transitions to cheaper storage classes.

5. CloudWatch Log Optimizer

Finds log groups with long retention periods and recommends or enforces lower retention.

6. ECR Image Cleanup

Deletes untagged images or images older than a configurable age while keeping recent versions.

7. RDS Scheduler

Automatically starts and stops development or test databases according to business hours.

8. Idle Load Balancer Detector

Finds Application and Network Load Balancers with little or no traffic over a defined period.

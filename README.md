Project: Scalable Log Processing & Monitoring Pipeline (Free-Tier Friendly)

AWS Services: EC2, S3, IAM, CloudWatch, Lambda, SNS, CloudTrail, DynamoDB, VPC, AWS CLI, Python, Bash, Linux, SQL-like queries via DynamoDB Partitions


STAGE 1 — VPC & Networking (implementation + verification + interview notes)

Goal: Create a minimal production-like network for the log pipeline:

VPC 10.0.0.0/16

Public subnet 10.0.1.0/24

Private subnet 10.0.2.0/24

Internet Gateway (IGW) attached to permit outbound internet from public subnet

Route table and association

Security groups for EC2 and Lambda (secure, minimal)

Everything in eu-west-1 (Ireland) to match your timezone/region preference and free-tier behaviour

Free-tier note: VPC, subnets, IGW, route tables, and security groups are free. Keep resources small (t2.micro) to stay inside free tier.

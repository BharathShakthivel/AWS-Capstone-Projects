# AWS Cloud Capstone Project: Scalable Log Processing & Monitoring Pipeline

## Project Overview
This project demonstrates a **fully automated, cloud-native log monitoring and alerting system** on AWS. Logs generated on EC2 are automatically ingested into S3, monitored by CloudWatch, parsed by Lambda, stored in DynamoDB, and analyzed using Python for actionable insights. Alerts are sent via SNS for anomalies.

## AWS Services Used
- **EC2**: Log generation
- **S3**: Log backup
- **IAM**: Secure access management
- **CloudWatch**: Monitoring and metric filters
- **Lambda**: Serverless log parsing
- **DynamoDB**: Structured log storage
- **SNS**: Email alerts
- **Python, Bash, Linux**: Automation and analytics

## Architecture Diagram


## Features
- Automated log ingestion and backup
- Real-time monitoring with CloudWatch
- Serverless log parsing with Lambda
- Structured storage in DynamoDB
- Error trends and frequent log messages analytics
- SNS email notifications for anomalies

## Key Troubleshooting & Debugging
- Fixed **SSH PEM key issues** for EC2 access
- Installed missing Python/pip packages on EC2
- Corrected Lambda gzip decompression errors using AWS templates
- Added IAM permissions for EC2 and Lambda to access DynamoDB
- Handled mixed timestamp formats in Python Pandas
- Resolved region errors in Boto3 by specifying `region_name`

## Impact Metrics
- **95% reduction** in manual log monitoring
- Fully automated pipeline from log generation → analytics
- Cost-efficient, **Free Tier compliant**
- Serverless architecture demonstrating cloud best practices

## Analytics Scripts
- `query_logs.py` — queries DynamoDB and generates error trends chart (`error_trends.png`)
- Top 5 frequent log messages displayed in terminal output

## How to Run
1. Clone this repository to EC2.
2. Install dependencies: `pip3 install boto3 pandas matplotlib`
3. Run the analytics script: `python3 query_logs.py`
4. Check generated chart at `/home/ec2-user/error_trends.png`

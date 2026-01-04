# AWS Free Tier - Complete Reference

The most comprehensive, up-to-date guide to AWS Free Tier. Covers the July 2025 changes, all services, and common billing traps.

[![Last Updated](https://img.shields.io/badge/Updated-December%202025-green.svg)](https://costgoat.com)

---

## Contents

- [What Changed on July 15, 2025](#what-changed-on-july-15-2025)
- [Always Free (Never Expires)](#always-free-never-expires)
- [12-Month Free Tier (Legacy Accounts Only)](#12-month-free-tier-legacy-accounts-only)
- [Short-Term Trials](#short-term-trials-paid-plan--legacy-only)
- [Free Tier in AWS Organizations](#free-tier-in-aws-organizations)
- [Common Gotchas](#common-gotchas-things-that-cost-money)
- [Track Your Free Tier Usage](#track-your-free-tier-usage)
- [Quick Reference](#quick-reference)

---

## What Changed on July 15, 2025

AWS completely restructured Free Tier for new accounts. This is the biggest change since Free Tier launched.

| | **Free Plan** | **Paid Plan** | **Legacy** (pre-July 15) |
|--|---------------|---------------|--------------------------|
| **Who** | New accounts choosing Free | New accounts choosing Paid | Existing accounts |
| **Duration** | 6 months max | Indefinite | 12 months + always-free |
| **Initial credits** | $100 | $100 | None |
| **Bonus credits** | Up to $100 more | Up to $100 more | None |
| **Always Free services** | Yes (30+) | Yes (30+) | Yes (30+) |
| **Short-term trials** | No | Yes | Yes |
| **12-month free tier** | No | No | Yes |
| **When credits run out** | Account closes | Pay-as-you-go | N/A |
| **At 6 months** | Account closes | Nothing | N/A |
| **After account closes** | 90 days to recover data | N/A | N/A |

### How to Earn $200 in Credits (New Accounts)

| Mission | Credit | Task |
|---------|--------|------|
| Sign up | $100 | Automatic |
| Launch EC2 | $20 | Start a virtual server |
| Create RDS | $20 | Provision a managed database |
| Build Lambda | $20 | Create a serverless function |
| Try Bedrock | $20 | Use the AI playground |
| Set Budget | $20 | Configure AWS Budgets |

### Services Blocked on Free Plan

- Reserved Instances
- Savings Plans
- AWS Marketplace purchases
- Hardware (Outposts, Snow devices)

---

## Always Free (Never Expires)

These limits reset monthly and never expire. Available to all account types.

| Service | Free Limit | Notes |
|---------|------------|-------|
| **Amazon Q Developer** | 50 agentic requests/mo + 1K lines code transform | In IDE and CLI |
| **AppSync** | 250K queries + 250K real-time updates/mo | GraphQL APIs |
| **Aurora DSQL** | 100K Distributed Processing Units + 1 GB storage/mo | Serverless PostgreSQL |
| **Budgets** | 2 action-enabled budgets free | Cost management alerts |
| **CloudFormation** | 1,000 handler operations/mo | IaC; pay for resources created |
| **CloudFront** | 1 TB data out + 10M requests/mo | CDN; also separate Free Plan (3 dists, 1M req/mo, hard cap) |
| **CloudTrail** | 1 trail + 90-day event history | Management events only |
| **CloudWatch** | 10 metrics + 10 alarms + 5 GB logs + 1M API requests | Plus 3 dashboards |
| **CodeBuild** | 100 build min/mo (general1.small) | Plus 6K Lambda build seconds |
| **CodeCatalyst** | 2K build min + 60 dev env hrs + 10 GB storage/mo | Dev collaboration |
| **CodePipeline** | 1 active V1 pipeline + 100 V2 action min/mo | Per month |
| **Cognito** | 10K MAUs (direct/social) or 50 MAUs (SAML/OIDC) | User authentication |
| **DataZone** | 20 MB metadata + 4K API requests + 0.2 compute units/mo | Data governance |
| **DynamoDB** | 25 GB storage + 25 RCU/WCU | On-demand: 200M requests/mo |
| **ECR Public** | 50 GB storage + 500 GB transfer (anonymous) or 5 TB (authenticated)/mo | Public container repos |
| **EventBridge** | 14M Scheduler invocations/mo | Plus 5M Schema Discovery events |
| **Glue Data Catalog** | 1M objects stored + 1M requests/mo | Metadata only |
| **IAM** | Unlimited | Identity management |
| **KMS** | 20K requests/mo | Excludes asymmetric key operations |
| **Lambda** | 1M requests + 400K GB-sec/mo | Includes 100 GiB HTTP response streaming |
| **Managed Prometheus** | 40M samples ingested + 10 GB storage/mo | Plus 200B query samples |
| **Pinpoint** | 5K targeted endpoints + 100M events + 1M push notifications/mo | Marketing campaigns |
| **Route 53** | 50 health checks for AWS endpoints | Plus free alias queries to AWS services |
| **S3 Glacier** | 10 GB retrieval/mo | Standard retrievals via Glacier API |
| **Shield Standard** | Unlimited | DDoS protection for all AWS resources |
| **SimpleDB** | 25 machine hrs + 1 GB storage/mo | Legacy NoSQL |
| **SNS** | 1M publishes/mo | Plus 100K HTTP, 1K email deliveries |
| **SQS** | 1M requests/mo | Standard and FIFO queues |
| **Step Functions** | 4,000 state transitions/mo | Standard Workflows only |
| **SWF** | 10K tasks + 30K workflow-days + 1K executions/mo | Workflow orchestration |
| **Systems Manager** | Most features free | Parameter Store, Session Manager, etc. |
| **WAF Bot Control** | 10M Common Bot requests/mo | Plus 1M Targeted Bot requests |
| **X-Ray** | 100K traces recorded + 1M traces scanned/mo | Tracing and debugging |

---

## 12-Month Free Tier (Legacy Accounts Only)

Only available to accounts created **before** July 15, 2025. Expires 12 months after signup.

| Service | Free Limit | Notes |
|---------|------------|-------|
| **Amplify** | 1K build min + 5 GB storage + 15 GB transfer + 500K SSR requests/mo | Frontend hosting |
| **API Gateway** | 1M REST + 1M HTTP + 1M messages + 750K connection min/mo | REST and WebSocket |
| **Comprehend** | 50K units (5M chars) per API/mo | NLP; 5 topic modeling jobs |
| **Data Transfer** | 100 GB/mo OUT | Aggregated across services; 15 GB for new accounts |
| **EBS** | 30 GB + 2M I/Os + 1 GB snapshots | SSD or Magnetic |
| **EC2** | 750 hrs/mo (t2.micro or t3.micro) | Linux or Windows |
| **ECR Private** | 500 MB storage/mo | Private container repos |
| **EFS** | 5 GB standard storage | Regional file systems only |
| **ElastiCache** | 750 hrs/mo (cache.t3.micro) | Redis or Memcached |
| **Elastic Load Balancing** | 750 hrs + 15 GB data processing/mo | Classic and Application LBs |
| **IoT Core** | 250K messages/mo | Pub/sub messaging |
| **IoT Device Management** | 50 remote actions/mo | Device management |
| **IoT Events** | 2,500 message evaluations/mo | Event detection |
| **IoT Greengrass** | 3 devices | Edge computing |
| **OpenSearch** | 750 hrs/mo t2/t3.small.search + 10 GB EBS | Single-AZ |
| **Polly** | 5M chars standard + 1M neural + 500K long-form + 100K generative/mo | Text-to-speech |
| **RDS** | 750 hrs/mo (db.t2/t3/t4g.micro) | MySQL, PostgreSQL, MariaDB, SQL Server Express; 20 GB storage + 20 GB backup |
| **Rekognition** | 1K images + 60 min video/mo | Image and video analysis |
| **S3** | 5 GB standard + 20K GET + 2K PUT/mo | Standard storage class only |
| **SES** | 3,000 messages/mo | For 12 months from first use |
| **Transcribe** | 60 min/mo | Speech-to-text |
| **Translate** | 2M chars/mo | Neural translation |

---

## Short-Term Trials (Paid Plan & Legacy Only)

NOT available to Free Plan accounts. Duration starts when you first activate the service.

| Service | Duration | What You Get |
|---------|----------|--------------|
| **App Studio** | 60 days | 250 user hours (Available on both plans) |
| **CloudTrail Lake** | 30 days | 5 GB data ingestion + 5 GB scanning |
| **Detective** | 30 days | Security investigation and analysis |
| **DocumentDB** | 30 days | 750 hrs db.t3.medium + 5 GB storage + 30M I/Os |
| **Forecast** | 2 months | 100K data points + 10 GB storage + 10 training hrs/mo (not accepting new customers) |
| **GuardDuty** | 30 days | Full threat detection (CloudTrail, VPC Flow, DNS) |
| **Inspector** | 15 days | Unlimited vulnerability scanning (EC2, Lambda, ECR, repos) |
| **IoT Device Defender** | 30 days | 1 fleet audit + 1M metric datapoints (Available on both plans) |
| **Kendra** | 30 days | 750 hrs intelligent search (GenAI Enterprise) |
| **Keyspaces** | 3 months | 30M write + 30M read units + 1 GB storage/mo |
| **Lightsail** | 3 months | 750 hrs/mo on select bundles ($5-22 plans) |
| **Macie** | 30 days | Automated data discovery + 150 GB inspection |
| **Managed Grafana** | 90 days | Up to 5 users per account |
| **MemoryDB** | 2 months | 750 hrs t4g.small + 10 TB writes (Valkey) or 20 GB (Redis)/mo |
| **Neptune** | 30 days | 750 hrs db.t3/t4g.medium + 1 GB storage + 10M I/Os |
| **Personalize** | 2 months | 20 GB data + 100 training hrs (or 5M interactions) + 180K recommendations/mo |
| **QuickSight** | 30 days | 10 GB SPICE capacity for 4 users |
| **Redshift** | 2 months | 750 DC2.Large node hrs/mo |
| **Redshift Serverless** | 90 days | $300 credit toward compute and storage |
| **SageMaker** | 2 months | 250 hrs/mo ml.t3.medium notebooks |
| **Storage Gateway** | Until used | First 100 GB free |
| **Textract** | 3 months | 1K Detect pages + 100 Analyze pages/mo |
| **Translate (Custom)** | 2 months | 500K chars/mo Active Custom Translation |
| **Wickr** | 3 months | Up to 30 users, unlimited controls (Available on both plans) |

---

## Free Tier in AWS Organizations

If your account is part of an AWS Organization, free tier behavior changes significantly.

| Free Tier Type | Organization Behavior |
|----------------|----------------------|
| **Always Free** | Shared/aggregated across all accounts in the org |
| **12-Month Free Tier** | Shared/aggregated across all accounts in the org |
| **Free Plan credits** | Expire immediately when joining an org |
| **Short-Term Trials** | Per-account AND per-region |

### Always Free & 12-Month Tiers Are Shared

Usage is aggregated across all accounts. Example:
- Account A uses 400 EC2 hours
- Account B uses 400 EC2 hours
- Total: 800 hours against the 750-hour limit = 50 hours billed

The 12-month eligibility starts from when the **management account** was created, not each member account.

### Free Plan Credits Expire on Joining

If you have a Free Plan account (post-July 2025) and join an Organization:
- Your credits expire immediately
- Account converts to Paid Plan
- You cannot earn more Free Plan credits

### Short-Term Trials Are Independent

Services like GuardDuty give each account its own 30-day trial, in each region:
- Enable GuardDuty in us-east-1 → 30 days free
- Enable it later in eu-west-1 → another 30 days free there
- Each account in the org gets its own trials

---

## Common Gotchas (Things That Cost Money)

### 1. Hidden Charges Within Free Tier

| Trap | Cost | Why It Happens |
|------|------|----------------|
| **Elastic IP** (unattached) | $0.005/hr (~$3.60/mo) | Charged when NOT attached to running instance |
| **NAT Gateway** | $0.045/hr (~$32/mo) | No free tier, always charged |
| **EBS Snapshots** | $0.05/GB-mo | Beyond 1 GB not covered |
| **Cross-region transfer** | $0.02/GB | Never covered by free tier |
| **IPv4 addresses** | $0.005/hr | Public IPv4 charged (as of Feb 2024) |
| **Secrets Manager** | $0.40/secret/mo | No always-free tier; only credits |

### 2. The 750-Hour Trap

- 750 hours = 31.25 days for ONE instance 24/7
- **2 instances** = exhausted in ~15 days
- **3 instances** = exhausted in ~10 days

### 3. Request Limits Are Separate From Storage

S3 example:
- Storage: 5 GB free
- GET requests: 20,000 free
- PUT requests: 2,000 free
- **Can exhaust requests while storage is under limit**

### 4. Free Plan Auto-Closes

Your Free Plan account **automatically closes** when:
- 6 months pass (even with credits remaining)
- Credits run out

After closure:
- 90-day grace period to upgrade
- Then all data permanently deleted

### 5. Services Without Free Tier

These popular services have **no free tier** at all:
- AWS Fargate
- Amazon EKS
- AWS Secrets Manager (credits only)
- Amazon Athena
- AWS Glue ETL jobs
- Amazon Kinesis

---

## Track Your Free Tier Usage

| Method | Pros | Cons |
|--------|------|------|
| **AWS Console** | Official, accurate | Delayed updates, manual checking |
| **CloudWatch Alarms** | Automated alerts | Total cost only, not per-service |
| **AWS Budgets** | Granular, 2 free budgets | Setup complexity |
| **CostGoat** | Real-time, per-service and total cost alerts | Requires install |

---

## Quick Reference

### Which Plan Do I Have?

| Created Account... | Your Plan |
|--------------------|-----------|
| Before July 15, 2025 | Legacy (12-month free tier) |
| After July 15, 2025 + chose Free | Free Plan (6 months, auto-closes) |
| After July 15, 2025 + chose Paid | Paid Plan (indefinite) |

### What Do I Get?

| Benefit | Legacy | Free Plan | Paid Plan |
|---------|--------|-----------|-----------|
| Always Free (30+ services) | Yes | Yes | Yes |
| $200 credits | No | Yes | Yes |
| 12-month free tier | Yes | No | No |
| Short-term trials | Yes | No | Yes |
| Account auto-closes | No | Yes (6 mo) | No |

---

## Data Sources

All data verified from official AWS pricing pages (December 2025):
- [AWS Free Tier](https://aws.amazon.com/free/)
- [AWS Free Tier FAQs](https://aws.amazon.com/free/free-tier-faqs/)
- Individual service pricing pages

---

## Contributing

Found outdated info? [Open an issue](https://github.com/costgoat/aws-free-tier/issues) with:
- Service name
- Current vs expected limit
- Source (AWS docs URL)

---

## Links

- [AWS Official Free Tier Page](https://aws.amazon.com/free/)
- [AWS Free Tier FAQs](https://aws.amazon.com/free/free-tier-faqs/)
- [CostGoat - Track Free Tier Usage](https://costgoat.com)

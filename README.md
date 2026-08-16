# AWS Free Tier - Complete Reference

The most comprehensive, up-to-date guide to AWS Free Tier. Covers the July 2025 changes, every service AWS lists, and the common billing traps.

[![Last Updated](https://img.shields.io/badge/Updated-August%202026-green.svg)](https://costgoat.com)

---

## Contents

- [What Changed on July 15, 2025](#what-changed-on-july-15-2025)
- [Always Free (Never Expires)](#always-free-never-expires)
- [12-Month Free Tier (Legacy Accounts Only)](#12-month-free-tier-legacy-accounts-only)
- [Short-Term Trials](#short-term-trials-paid-plan--legacy-only)
- [Credit-Model Only (No Per-Service Allowance)](#credit-model-only-no-per-service-allowance)
- [Free Tier in AWS Organizations](#free-tier-in-aws-organizations)
- [Common Gotchas](#common-gotchas-things-that-cost-money)
- [Track Your Free Tier Usage](#track-your-free-tier-usage)
- [Quick Reference](#quick-reference)

---

## What Changed on July 15, 2025

AWS completely restructured Free Tier for new accounts. This is the biggest change since Free Tier launched.

For a new account today, "free tier" means two things: the Always Free services below (permanent monthly limits, no time limit), plus up to $200 in shared credits. The classic per-service 12-month allowances and many short-term trials now apply to legacy accounts only, and AWS has removed some of them from its pricing pages entirely.

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

These limits reset monthly and never expire. Available to all account types (Free, Paid, Legacy) unless a row is tagged [Free plan: no]. Services use their official AWS names.

| Service | Free Limit | Notes |
|---------|------------|-------|
| **Amazon Q Developer** | 50 agentic requests/mo + 1K lines code transform | In IDE and CLI |
| **Amazon Aurora DSQL** | 100K Distributed Processing Units + 1 GB storage/mo | Serverless PostgreSQL |
| **AWS Budgets** | 2 action-enabled budgets free | Cost management alerts |
| **AWS CloudFormation** | 1,000 handler operations/mo | IaC; pay for resources created |
| **Amazon CloudFront** | 1M requests + 100 GB transfer + 5 GB S3 credits/mo per distribution | New flat-rate Free plan, no overage charges; bundles WAF, DDoS protection, Route 53 DNS, TLS cert |
| **AWS CloudTrail** | 1 trail + 90-day event history | Management events only. CloudTrail Lake: 30-day trial (5 GB ingestion + 5 GB scanning) |
| **Amazon CloudWatch** | 10 metrics + 10 alarms + 5 GB logs + 1M API requests | Plus 3 dashboards + 1,800 min Live Tail + 100 Synthetics canary runs |
| **AWS CodeArtifact** | 2 GB-month storage + 100K requests/mo | [Free plan: no] Allowance resets monthly, measured across all repositories |
| **AWS CodeBuild** | 100 build min/mo (general1.small) | Plus 6K Lambda build seconds |
| **AWS CodeCommit** | 5 active users/mo | Closed to new customers; existing customers only |
| **AWS CodePipeline** | 1 active V1 pipeline + 100 V2 action min/mo | Per month |
| **Amazon Cognito** | 10K MAUs (direct/social) or 50 MAUs (SAML/OIDC) | User authentication |
| **AWS Control Tower** | No charge for the control plane | [Free plan: no] Pay standard rates for services it provisions (Config, CloudTrail, S3, etc.) |
| **Amazon DataZone** | 20 MB metadata + 4K API requests + 0.2 compute units/mo | Data governance; powers SageMaker Unified Studio |
| **Amazon DynamoDB** | 25 GB storage + 25 RCU/WCU | On-demand: ~200M requests/mo |
| **Amazon Elastic Container Registry** | Public repos: 50 GB storage + 500 GB/5 TB transfer/mo (always free) | Private repos: 500 MB/mo for 12 months (legacy) |
| **Amazon EventBridge** | 14M Scheduler invocations/mo | Plus 5M Schema Discovery events |
| **AWS Glue** | Data Catalog: 1M objects stored + 1M requests/mo | Metadata only. ETL jobs, crawlers, DataBrew are NOT free |
| **AWS Identity and Access Management (IAM)** | Unlimited | Free by design (not a metered directory tier) |
| **AWS Key Management Service (KMS)** | 20K requests/mo | Excludes asymmetric key operations |
| **AWS Lambda** | 1M requests + 400K GB-sec/mo | Includes 100 GiB HTTP response streaming |
| **AWS License Manager** | No charge | Pay only for the underlying AWS resources |
| **Amazon Managed Service for Prometheus** | 40M samples ingested + 10 GB storage/mo | Plus 200B query samples |
| **Amazon Pinpoint** | 5K targeted endpoints + 100M events + 1M push notifications/mo | Resets monthly. AWS ends Pinpoint support Oct 30, 2026 (moves to AWS End User Messaging) |
| **AWS Migration Hub** | No charge | Pay for the migration tools used; now consolidated under AWS Transform |
| **Migration Evaluator** | Complimentary (no metering) | Request-based migration assessment |
| **AWS Organizations** | No charge | Pay standard rates for resources in member accounts |
| **AWS Resource Access Manager** | No charge (share resources at no cost) | Pay for the underlying shared resources |
| **AWS Resource Explorer** | No charge | Some console features depend on other billable services |
| **Amazon Route 53** | 50 health checks for AWS endpoints | Plus free alias queries to AWS services |
| **Amazon SageMaker** | Catalog (via DataZone): 20 MB metadata + 4K API + 0.2 compute/mo | Studio notebooks have a separate 2-month, 250 hrs/mo trial |
| **AWS Security Hub** | 10,000 finding-ingestion events/mo | [Free plan: no] Essentials plan has a separate 30-day trial |
| **AWS Service Catalog** | 1,000 API calls / account / Region / mo | AppRegistry create/associate/tag actions always free |
| **AWS Shield Standard** | Unlimited | DDoS protection for all AWS resources; free by design |
| **Amazon SimpleDB** | 25 machine hrs + 1 GB storage/mo | Legacy NoSQL |
| **Amazon Simple Notification Service (SNS)** | 1M publishes/mo | Plus 100K HTTP, 1K email deliveries |
| **Amazon Simple Queue Service (SQS)** | 1M requests/mo | Standard and FIFO queues |
| **AWS Step Functions** | 4,000 state transitions/mo | Standard Workflows only |
| **Amazon Simple Workflow Service (SWF)** | 10K tasks + 30K workflow-days + 1K executions/mo | Workflow orchestration |
| **AWS Storage Gateway** | First 100 GB written to AWS free | [Free plan: no] Per account, no time limit |
| **AWS Systems Manager** | Most features free | Parameter Store, Session Manager, etc. |
| **Amazon AppStream 2.0** | 10 free hrs/mo of session time (per Region) | [Free plan: no] Rebranded "WorkSpaces applications"; recurring monthly, resets, no rollover |
| **AWS WAF Bot Control** | 10M Common Bot requests/mo | Plus 1M Targeted Bot requests |
| **AWS Well-Architected Tool** | No charge | Pay only for the underlying AWS resources |
| **Amazon X-Ray** | 100K traces recorded + 1M traces scanned/mo | Tracing and debugging |
| **AWS Application Discovery Service** | No charge (unlimited discovery) | Pay for S3/Athena/Firehose used to store and query data; now under AWS Transform |
| **AWS Application Migration Service (MGN)** | 2,160 hrs (90 days) free per source server | Pay for the underlying EC2/EBS/staging resources |
| **AWS re:Post** | Free community Q&A | re:Post Private is a separate paid product |

---

## 12-Month Free Tier (Legacy Accounts Only)

Only available to accounts created **before** July 15, 2025. Expires 12 months after signup. New accounts get the $200 credit model instead.

| Service | Free Limit | Notes |
|---------|------------|-------|
| **AWS Amplify** | 1K build min + 5 GB storage + 15 GB transfer + 500K SSR requests/mo | Frontend hosting |
| **Amazon API Gateway** | 1M REST + 1M HTTP + 1M messages + 750K connection min/mo | REST and WebSocket |
| **Amazon AppSync** | 250K queries + 250K real-time updates + 600K connection-minutes/mo | GraphQL APIs; expires 12 months after signup |
| **Amazon Augmented AI (A2I)** | 500 human reviews total (~42/mo) for the first year | Excludes AWS Marketplace / Mechanical Turk workforce costs |
| **Amazon Cloud Directory** | 1 GB + 100K eventually-consistent reads + 10K strong reads/writes /mo | Closed to new customers (Nov 7, 2025) |
| **Amazon Comprehend** | 50K units (5M chars) per API/mo | NLP; 5 topic modeling jobs |
| **Data Transfer** | 100 GB/mo OUT | Aggregated across all services and Regions (excludes China, GovCloud) |
| **Amazon Elastic Block Store (EBS)** | 30 GB + 2M I/Os + 1 GB snapshots | SSD or Magnetic |
| **Amazon Elastic File System (EFS)** | 5 GB standard storage | Regional file systems only |
| **Amazon ElastiCache** | 750 hrs/mo (cache.t3.micro) | Redis or Memcached |
| **Elastic Load Balancing** | 750 hrs + 15 GB data processing/mo | Classic and Application LBs |
| **AWS HealthImaging** | 20 GB storage/mo + 20,000 API requests/mo | New customers; calculated across Regions, no rollover |
| **Amazon Interactive Video Service** | 5 hr live input + 100 hr SD output + 20 participant-hrs + messages /mo | Live video streaming |
| **AWS IoT Core** | 500K messages/mo + 2.25M connection-minutes | Plus 250K rules triggered + 250K actions applied |
| **AWS IoT Device Management** | 50 remote actions/mo | Device management |
| **AWS IoT Greengrass** | 3 devices | Edge computing |
| **Amazon Polly** | 5M chars standard + 1M neural + 500K long-form + 100K generative/mo | Text-to-speech |
| **Amazon RDS** | 750 hrs/mo (db.t2/t3/t4g.micro) | MySQL, PostgreSQL, MariaDB, SQL Server Express; 20 GB storage + 20 GB backup |
| **Amazon Rekognition** | 1K images + 60 min video/mo | Image and video analysis |
| **Amazon Transcribe** | 60 min/mo | Speech-to-text |
| **Amazon Translate** | 2M chars/mo | Neural translation. Active Custom Translation: 500K chars/mo (2 months) |

---

## Short-Term Trials (Paid Plan & Legacy Only)

Not available to Free Plan accounts unless a row is tagged [Free plan: yes]. Duration starts when you first activate the service.

| Service | Duration | What You Get |
|---------|----------|--------------|
| **App Studio** | 60 days | [Free plan: yes] 250 user hours |
| **AWS AppFabric** | 30 days | First 2 connected apps free |
| **AWS Audit Manager** | 2 months | 35,000 resource assessments/mo (first-time customers) |
| **Amazon Braket** | 12 months | 1 hr on-demand simulation/mo (local simulator is always free) |
| **Amazon Comprehend Medical** | First month | 85,000 units (8.5M chars) |
| **Amazon Detective** | 30 days | Security investigation and analysis |
| **Amazon DevOps Guru** | 3 months | 7,200 resource-hrs per price group + 10K API calls/mo |
| **AWS Device Farm** | One-time | 1,000 device minutes |
| **AWS Directory Service** | 30 days | 1,500 domain-controller hours (Managed Microsoft AD) |
| **Amazon DocumentDB** | 30 days | 750 hrs db.t3.medium + 5 GB storage + 30M I/Os |
| **Amazon ECS Anywhere** | 6 months | [Free plan: yes] 2,200 external instance-hrs/mo |
| **Amazon Forecast** | 2 months | 100K data points + 10 GB storage + 10 training hrs/mo |
| **Amazon GuardDuty** | 30 days | Full threat detection (CloudTrail, VPC Flow, DNS) |
| **AWS HealthOmics** | 2 months | [Free plan: yes] 275 instance-hrs + 49K GB-hrs storage + sequence/variant stores /mo |
| **AWS HealthScribe** | 2 months | 300 audio minutes/mo |
| **Amazon Inspector** | 15 days | Unlimited vulnerability scanning (EC2, Lambda, ECR) |
| **AWS IoT Device Defender** | First month | [Free plan: yes] Audit all fleet devices + 1M metric datapoints |
| **Amazon Kendra** | 30 days | 750 hrs intelligent search (GenAI Enterprise) |
| **Amazon Keyspaces** | 3 months | 30M write + 30M read units + 1 GB storage/mo |
| **Amazon Location Service** | 3 months | [Free plan: yes] 500K map tiles + 30K place requests + geofence and tracking allowances/mo |
| **Amazon Lookout for Equipment** | First month | 50 GB ingestion + 250 training hrs + 168 inference hrs |
| **Amazon Macie** | 30 days | Bucket monitoring (up to 10,000 buckets) + automated sensitive-data discovery |
| **Amazon Managed Grafana** | 90 days | Up to 5 users per account |
| **Amazon Neptune** | 30 days | 750 hrs db.t3/t4g.medium + 1 GB storage + 10M I/Os |
| **Amazon Personalize** | 2 months | 20 GB data + 100 training hrs + 180K recommendations/mo |
| **AWS Private Certificate Authority** | 30 days | 1 private CA, no CA-operation charge (certificates still billed) |
| **Amazon Redshift** | 2 months | 750 DC2.Large node hrs/mo. Redshift Serverless: $300 credit for 90 days |
| **AWS Resilience Hub** | 6 months | First 3 applications free |
| **Amazon Security Lake** | 15 days | Full-feature trial |
| **Amazon Textract** | 3 months | 1K Detect pages + 100 Analyze pages/mo |
| **AWS Wickr** | 3 months | [Free plan: yes] Up to 30 users, unlimited controls |

---

## Credit-Model Only (No Per-Service Allowance)

AWS has removed these services' classic per-service free-tier limits (in or since the July 2025 migration). Their pricing pages now show only the shared $200-credit / 6-month-free-plan model. New accounts draw from the credit pool; legacy accounts may retain the old allowance, but AWS no longer publishes it. The removed limits are recorded below for reference.

| Service | What Was Removed |
|---------|------------------|
| **AWS Secrets Manager** | Classic 30-day free trial |
| **Amazon Lex** | Classic 12-month allowance (10K text + 5K speech requests/mo) |
| **Amazon MQ** | Classic 12-month broker allowance (only a 5 GB-months storage remnant survives) |
| **AWS Database Migration Service** | Legacy: 750 hrs dms.t3.micro + 50 GB for 12 months; new accounts: credits |
| **Amazon CloudSearch** | No service-specific free tier published |
| **Amazon Connect** | No per-service allotment; quote-based pricing page |
| **Amazon GameLift** | No dedicated free-tier allotment |
| **AWS Billing Conductor** | AWS-managed pricing plans are free; customer-managed plans cost $50 per AWS Organization/month, with a 2-month free trial for new customers |
| **Amazon EC2** | Classic 12-month: 750 hrs/mo t2.micro or t3.micro |
| **Amazon S3** | Classic 12-month: 5 GB Standard + 20K GET + 2K PUT/mo (plus S3 Glacier 10 GB retrieval) |
| **Amazon Simple Email Service (SES)** | Classic 12-month: 3,000 messages/mo (62K when sent from EC2) |
| **Amazon OpenSearch Service** | Classic 12-month: 750 hrs/mo t2/t3.small.search + 10 GB EBS |
| **Amazon Lightsail** | Classic 3-month trial: 750 hrs/mo on select bundles |
| **Amazon MemoryDB** | Classic 2-month trial: 750 hrs t4g.small + write allowance |
| **Amazon Quick Sight** (formerly QuickSight) | Classic 30-day trial: 4 authors + 10 GB SPICE; service rebranded |

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
- Account A uses 400 RDS hours
- Account B uses 400 RDS hours
- Total: 800 hours against the 750-hour limit = 50 hours billed

The 12-month eligibility starts from when the **management account** was created, not each member account.

### Free Plan Credits Expire on Joining

If you have a Free Plan account (post-July 2025) and join an Organization:
- Your credits expire immediately
- Account converts to Paid Plan
- You cannot earn more Free Plan credits

### Short-Term Trials Are Independent

Services like GuardDuty give each account its own 30-day trial, in each region:
- Enable GuardDuty in us-east-1 -> 30 days free
- Enable it later in eu-west-1 -> another 30 days free there
- Each account in the org gets its own trials

---

## Common Gotchas (Things That Cost Money)

### 1. Hidden Charges Within Free Tier

| Trap | Cost | Why It Happens |
|------|------|----------------|
| **Elastic IP** (unattached) | $0.005/hr (~$3.60/mo) | Charged when NOT attached to a running instance |
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

S3 example (legacy 12-month allowance):
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
- Amazon Athena
- Amazon Kinesis
- AWS Glue ETL jobs
- AWS HealthLake (Data Store runs 24/7 at $0.27/hr; the 10 GB storage and 3,500 queries/hr are included in that charge, not free)
- AWS Elemental MediaConnect (only the Gateway software is free; flows and data transfer are billed)
- AWS Data Exchange (AWS lists it as free, but that means free data products, not a service tier; receivers pay provider fees)

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

All data verified from official AWS pricing pages and the AWS Free Tier service listing (August 2026):
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

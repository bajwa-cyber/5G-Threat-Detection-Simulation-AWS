# Setup & Reproduction Guide

This file condenses the Appendix of the thesis reproduction instructions. See full thesis at `docs/Ammad-Masters-Thesis.pdf`. :contentReference[oaicite:5]{index=5}

## Overview
We create:
- VPC: `10.0.0.0/16`
- Core Subnet: `10.0.1.0/24`
- RAN Subnet: `10.0.2.0/24`
- Two EC2 instances: Core (Open5GS) and RAN (srsRAN)
- GuardDuty enabled to monitor findings

> **Warning:** follow AWS best practices: do not expose private keys, use IAM roles, and avoid using root credentials.

---

## AWS Prerequisites
- AWS CLI installed & configured
- IAM user with permissions:
  - AmazonEC2FullAccess
  - AmazonVPCFullAccess
  - AmazonGuardDutyFullAccess
  - CloudWatchLogsFullAccess
(These policy names match the thesis recommendations.) :contentReference[oaicite:6]{index=6}

---

## EC2 / VPC Quick Steps (CLI overview)
1. Create VPC, subnets, IGW, route tables:
```bash
aws ec2 create-vpc --cidr-block 10.0.0.0/16
# create subnets 10.0.1.0/24 and 10.0.2.0/24

2. Launch EC2 instance for Core (Ubuntu 20.04 recommended) and for RAN.

3. Configure security groups:

- allow SSH (22)

- Core: allow SCTP (38412), UDP (2152, 8805) from RAN subnet

- RAN: custom traffic to Core private IPs
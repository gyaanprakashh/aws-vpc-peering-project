# AWS VPC Peering Implementation & Verification

## 📌 Project Overview
This repository contains the implementation details and verification report for an AWS Virtual Private Cloud (VPC) Peering project. The objective was to establish secure, non-transitive private connectivity between two isolated VPCs using AWS VPC Peering, while maintaining strict routing and security controls.

## 🏗️ Architecture Details
- **Region:** ap-southeast-2 (Sydney)
- **VPC A (Requester):** `10.10.0.0/16` (Contains Public Subnet with Bastion Host & Private Subnet with App-A)
- **VPC B (Accepter):** `10.20.0.0/16` (Contains Private Subnet with App-B)
- **Connection:** Active VPC Peering Connection enabling direct private IPv4 routing.

## 🧪 Validation & Testing Performed
1. **Baseline Failure:** Verified isolation before peering (100% packet loss).
2. **Forward & Reverse Path:** Successful two-way ICMP ping tests across the peered VPCs using private IPs.
3. **Private SSH Access:** Secure SSH access to the private App-B instance using SSH ProxyJump via the Bastion Host.
4. **Controlled Failure:** Demonstrated that Peering alone does not bypass Security Groups by temporarily removing inbound ICMP rules.

## 📄 Documentation
The complete step-by-step documentation, including architecture diagrams, route table configurations, security group rules, and terminal execution evidence, is available in the attached PDF report.

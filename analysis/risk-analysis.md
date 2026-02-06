# Security Risk Analysis

## Overview
This section analyzes the cloud infrastructure configurations to identify
potential security risks and misconfigurations.

## Identified Security Risks

### 1. Public SSH Access
The EC2 instance allows SSH access (port 22) from all IP addresses (0.0.0.0/0),
which exposes the system to brute-force and unauthorized access attacks.

### 2. Over-Permissive Security Groups
Security group rules are too broad and do not follow the principle of least privilege.

### 3. Unencrypted Storage
Storage volumes are not encrypted, increasing the risk of data exposure in case of compromise.

### 4. Public IP Exposure
Assigning public IP addresses directly to instances increases the attack surface.

## Impact
These risks may lead to data breaches, unauthorized access, compliance violations,
and potential service downtime.

## Recommendation Summary
- Restrict SSH access using specific IP ranges
- Apply least-privilege security group rules
- Enable encryption for data at rest
- Minimize public-facing resources

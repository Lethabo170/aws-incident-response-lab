# AWS Incident Response & Forensics Lab

A hands-on AWS Incident Response lab involving a compromised EC2 instance. This project demonstrates threat hunting via CloudTrail, log analysis, threat containment, and system hardening.

## Overview

This project simulates a real-world security incident where an EC2 instance (Cafe Web Server) was compromised due to an overly permissive Security Group. The attacker created a backdoor user and defaced the website. The lab covers the entire incident response lifecycle: Detection, Analysis, Containment, Eradication, and Recovery.

## Architecture

```text
[Attacker IP: 44.252.71.199]
          |
          | (SSH via 0.0.0.0/0)
          v
[EC2 Web Server: 44.252.71.199]
          |
          | (Logs)
          v
[CloudTrail] -> [S3 Bucket: monitoring1880] -> [Athena Queries]

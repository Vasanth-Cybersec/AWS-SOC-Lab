# AWS-SOC-Lab

This project documents the creation of a cloud-based Security Operations Center (SOC) lab environment built in AWS.

The purpose of this lab is to simulate attacker activity and practice detecting suspicious behavior using system logs and SIEM monitoring tools.

The environment includes Windows and Linux systems that generate logs which are forwarded to a centralized monitoring platform for investigation and analysis.

### Lab Architecture

**The SOC lab environment consists of the following components:**

• Windows Server – Target machine generating security events and system logs

• Ubuntu Server – Attacker / testing system used to simulate malicious activity

• SIEM Platform – Centralized log monitoring and analysis

• AWS EC2 – Cloud infrastructure hosting the lab environment

Current Progress
Completed

• AWS EC2 instances deployed

• Security group firewall rules configured

• Windows Server auditing policies enabled

• Sysmon installed for enhanced system monitoring

• SIEM dashboard configured for log visibility

In Progress

• Attack simulation experiments

• Detection rule development

• SOC investigation workflows

Tools Used

• AWS EC2

• Windows Server

• Ubuntu Linux

• Sysmon

• Windows Event Viewer

• SIEM Platform

Repository Structure

architecture → SOC lab architecture diagrams

infrastructure → AWS environment configuration

host-configuration → Windows logging and monitoring setup

siem → SIEM installation and configuration

attack-simulations → simulated attacker activity

screenshots → lab screenshots

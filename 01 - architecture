# SOC Lab Architecture

This document describes the architecture of the cloud-based Security Operations Center (SOC) lab environment.

The lab is designed to simulate attacker activity and analyze system logs using centralized monitoring tools. The environment consists of multiple virtual machines hosted in AWS that generate and collect security telemetry.

![SOC Lab Architecture Diagram](soc-lab-diagram.png)

---

# Architecture Overview

The SOC lab consists of three primary systems deployed in the same AWS environment:

• Ubuntu attacker machine  
• Windows Server monitored host  
• SIEM monitoring platform  

These systems communicate within the same AWS Virtual Private Cloud (VPC). The goal of the architecture is to simulate attacker behavior against a monitored system and analyze the resulting security logs through a centralized monitoring platform.

---

# Components

## Ubuntu Attacker Machine

The Ubuntu server acts as the attacker system within the lab environment.

This machine is used to simulate suspicious or malicious activity against the monitored Windows host. The goal is to generate realistic security events that can later be detected and analyzed by the monitoring platform.

Examples of activities that may be simulated from this system include:

- authentication attempts
- network scanning
- remote access attempts
- command execution

These activities generate logs on the target system which are later ingested by the SIEM platform.

---

## Windows Server (Monitored Host)

The Windows Server functions as the primary monitored system in the lab environment.

It generates a variety of security telemetry including:

- Windows Event Logs
- authentication activity
- account creation and deletion events
- process execution logs

To increase visibility into system behavior, Sysmon is installed on the Windows server. Sysmon generates detailed telemetry such as:

- process creation events
- network connections
- file activity
- registry modifications

These logs provide the data required for security monitoring and detection.

---

## SIEM Platform

The SIEM platform acts as the centralized log collection and analysis system.

Logs from the Windows server are forwarded to the SIEM where they can be searched, visualized, and analyzed through dashboards.

The SIEM dashboard provides visibility into security activity including:

- successful and failed login attempts
- account creation events
- authentication activity
- suspicious system behavior

This allows the lab environment to simulate the workflow of a real Security Operations Center.

---

## AWS Infrastructure

The SOC lab is hosted in AWS using EC2 virtual machines.

All systems are deployed inside the same Virtual Private Cloud (VPC), allowing them to communicate with one another while remaining isolated from external networks.

Security groups are used to restrict inbound access to administrative ports such as:

- SSH (22)
- RDP (3389)

Additional ports are opened for SIEM functionality including:

- 8000 (SIEM web interface)
- 9997 (log ingestion)

---

# Log Flow

The flow of security telemetry in the SOC lab is as follows:

1. Activity occurs on the Windows server
2. Windows Event Logs and Sysmon logs are generated
3. Logs are forwarded to the SIEM platform
4. The SIEM dashboard aggregates and visualizes security events

This workflow allows simulated attacks to be detected and investigated within the monitoring environment.

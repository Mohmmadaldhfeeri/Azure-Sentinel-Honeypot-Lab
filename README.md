# Azure Sentinel Honeypot Lab

## Overview

This project demonstrates the design and implementation of a cloud-based honeypot using Microsoft Azure and Microsoft Sentinel to monitor and analyze real-world cyber attacks.

A Windows virtual machine is intentionally exposed to the internet to attract malicious activity, particularly brute-force login attempts. Security events are collected through Log Analytics and analyzed using Kusto Query Language (KQL) within Microsoft Sentinel.

The project simulates a basic Security Operations Center (SOC) environment, showcasing how security analysts detect, investigate, and visualize threats using modern SIEM tools.


## Project Objectives

The objective of this project is to simulate a real-world cyber attack environment by deploying a vulnerable Windows virtual machine in Microsoft Azure. The system is intentionally exposed to the internet to attract malicious login attempts. These attacks are then captured, analyzed, and visualized using Microsoft Sentinel and KQL, allowing for better understanding of attacker behavior and demonstrating a basic SOC (Security Operations Center) workflow.


## 🛠️ Technologies Used

* ☁️ Microsoft Azure
* 🛡️ Microsoft Sentinel (SIEM)
* 📊 Log Analytics Workspace
* 💻 Windows Virtual Machine
* 🔍 Kusto Query Language (KQL)
* 🌐 Remote Desktop Protocol (RDP)


## Lab Architecture

![Azure Resources](Resource Group (RG-SOC-LAB).jpeg)

## Honeypot Configuration

![Firewall Disabled](Firewall.jpeg)

## Network Security Group (NSG)

![NSG Rules](NSG.jpeg)

## Attack Visualization

![Attack Map](Attack%20Map.jpeg)


## Sample KQL Query

```kql id="x1kql9"
SecurityEvent
| where EventID == 4625
| summarize FailedAttempts = count() by IpAddress
| order by FailedAttempts desc
```

## Key Results

* Successfully captured multiple failed login attempts from different countries
* Identified attacker IP addresses and patterns
* Visualized attack data using Microsoft Sentinel
* Demonstrated basic threat detection and analysis

## Skills Gained

* SIEM configuration (Microsoft Sentinel)
* Log analysis and investigation
* KQL querying
* Cyber threat detection
* Cloud security fundamentals
* SOC analyst workflow

## 📌 Conclusion

This lab demonstrates how a simple exposed system can attract real-world cyber attacks and how security tools like Microsoft Sentinel can be used to detect, analyze, and respond to threats effectively.


## Status

✅ Completed

## Author

Mohmmad Aldhfeeri

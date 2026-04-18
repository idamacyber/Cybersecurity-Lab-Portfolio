📌 Cloud-Based SIEM Implementation Using Microsoft Sentinel

🔎 Project Overview

This project demonstrates the deployment and configuration of a cloud-based Security Information and Event Management (SIEM) solution using Microsoft Sentinel in Microsoft Azure.

The objective was to:

Deploy Azure resources

Enable log ingestion

Create detection rules

Simulate suspicious activity

Generate and investigate security incidents

🏗️ Environment Setup

Microsoft Azure subscription

Resource Group (SOC-LAB-RG)

Log Analytics Workspace

Microsoft Sentinel enabled

Azure Activity logs connected

📊 Log Ingestion Verification

Used KQL query to confirm log collection:

AzureActivity
| take 5

Verified that Azure Activity logs were successfully ingested into the Log Analytics Workspace.

🚨 Detection Engineering

Created a scheduled analytics rule:

Rule Name: Suspicious Azure Resource Creation Activity

Data Source: AzureActivity

Detection Logic: OperationName contains "write"

Severity: Medium

MITRE ATT&CK mapping applied

🧪 Simulated Suspicious Activity

Created a new Azure Resource Group to simulate administrative activity and trigger detection.

🔔 Incident Generation

The analytics rule successfully generated an incident in Microsoft Sentinel.

🔍 Incident Investigation

Reviewed:

Alert timeline

Detection details

Associated entities

Incident status

Demonstrated end-to-end detection and investigation workflow.

🛠️ Tools & Technologies

Microsoft Azure

Microsoft Sentinel

Kusto Query Language (KQL)

🎯 Key Skills Demonstrated

Cloud SIEM deployment

Log ingestion configuration

Detection rule creation

Incident investigation

Threat monitoring in cloud environments

### 📊 Evidence & Documentation

All screenshots and explanations for this project are documented here:

🔗 [Google Slides ](https://docs.google.com/presentation/d/1Tu700oaqtEwhLhNY-c4kyfmKmd3Na4aknultw_nIO7A/edit?usp=sharing)

## Summary 
This project demonstrates the deployment and configuration of a cloud-base SIEM solution using Microsoft Sentinel in Microsoft Azure.


# CodeAlpha NIDS — Evidence Index

This directory contains screenshots documenting the implementation, configuration, testing, detection results, and GitHub publication of the CodeAlpha Network Intrusion Detection System (NIDS) project using Suricata on Kali Linux.

## 1. Custom Detection Rule and Alerts

| Evidence filename | Description |
|---|---|
| `Custom ICMP Detection.png` | Custom ICMP detection alerts recorded by Suricata. |
| `Custom ICMP Rule.png` | Custom ICMP signature used to detect traffic to the Kioptrix target. |
| `Custom Rule Validation.png` | Validation of the custom detection rule. |
| `Eve Json Alerts.png` | Matching alert records in the EVE JSON log. |
| `Project Rule and Alert Count.png` | Verification of the custom rule and recorded alert counts. |

## 2. Virtual Lab and Network Connectivity

| Evidence filename | Description |
|---|---|
| `Interface Neighbors.png` | Network neighbor discovery on the lab network. |
| `Kioptrix Connectivity.png` | Connectivity test between Kali Linux and the Kioptrix target. |
| `Kioptrix Network Configuration.png` | Kioptrix target network configuration. |
| `Kioptrix Running.png` | Evidence that the Kioptrix virtual machine was running. |
| `Network Interface Discovery.png` | Identification of network interfaces for monitoring. |
| `Virtual Lab VM Status.png` | Status of the virtual machines used in the lab. |

## 3. Suricata Installation and Configuration

| Evidence filename | Description |
|---|---|
| `Suricata Captured Health.png` | Capture and detection health checks. |
| `Suricata Configuration Validation.png` | Suricata configuration validation. |
| `Suricata Configuration and Backup.png` | Configuration and backup evidence. |
| `Suricata Default Capture Interface.png` | Initial capture-interface configuration. |
| `Suricata Engine Started.png` | Suricata engine startup on the monitoring interface. |
| `Suricata Installation and Processed Ruleset.png` | Installation and community ruleset processing. |
| `Suricata Rule Inventory.png` | Available Suricata detection rules. |
| `Suricata Statistics.png` | Suricata statistics recorded during testing. |
| `Suricata eth1 Config Validation.png` | Validation of the monitoring interface configuration. |

## 4. Logs and Project Documentation

| Evidence filename | Description |
|---|---|
| `Logs Preserved After Suricata Shutdown.png` | Verification that detection logs remained available after Suricata stopped. |
| `NIDS ReadMe.png` | Project README displayed on GitHub. |
| `Project Report and Gitignore.png` | Project report and Git ignore configuration. |

## 5. Git and GitHub Publication

| Evidence filename | Description |
|---|---|
| `GitHub Remote Staged Files.png` | GitHub remote configuration and staged project files. |
| `git Initialization and Log Exclusions.png` | Git initialization and exclusion of raw logs. |
| `gitignore and Project Structure.png` | Project directory structure and `.gitignore` configuration. |

## Evidence Summary

The screenshots document the lab setup, Suricata installation and configuration, custom ICMP rule validation, controlled traffic generation, detection alerts, log preservation, project documentation, and repository preparation.

The controlled test produced three matching custom ICMP alerts in `fast.log` and three corresponding records in `eve.json`.

**Scope limitation:** These results validate the configured ICMP detection scenario only. They do not demonstrate comprehensive intrusion detection coverage or automatic traffic blocking.

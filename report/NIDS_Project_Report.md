# Network Intrusion Detection System (NIDS) Project Report

**Program:** CodeAlpha Cybersecurity Internship  
**Project:** Network Intrusion Detection System using Suricata  
**Platform:** Kali Linux on VirtualBox

## 1. Objective
To configure Suricata as a network intrusion detection system, implement a custom ICMP detection rule, generate controlled test traffic, and verify that matching events are recorded.

## 2. Lab Environment
- Monitoring machine: Kali Linux — `192.168.56.101`
- Target machine: Kioptrix — `192.168.56.102`
- Monitoring interface: `eth1`
- IDS software: Suricata 8.0.7

## 3. Implementation
Suricata was installed and its configuration validated successfully. Community rules were updated, and a custom rule was added to `/etc/suricata/rules/codealpha.rules`. The rule was also copied into the project directory for documentation and version control.

The custom signature was configured to alert on ICMP echo requests originating from the Kali monitoring address and destined for the Kioptrix lab target.

## 4. Testing Method
A controlled ping test was run from Kali Linux to the Kioptrix machine. The target returned three replies, with zero packet loss reported by the ping command.

## 5. Results
- Three matching custom alerts were recorded in `fast.log`.
- Three matching alert records were verified in `eve.json`.
- The records used signature ID `1000001`.
- After Suricata was stopped, both logs remained available and the three matching records were still present.

## 6. Security Significance
Network intrusion detection can help administrators identify suspicious or policy-relevant traffic. Custom signatures allow detection logic to be tailored to a particular environment. Centralized alert logs can support incident investigation and evidence-based analysis.

## 7. Limitations
The test validates only the configured ICMP echo-request scenario. It does not demonstrate detection of every attack type, comprehensive network coverage, or prevention/blocking of traffic. The test was performed in a controlled virtual lab.

## 8. Recommendations
1. Add and test further rules for relevant threats in an authorized lab.
2. Monitor alert logs and investigate unexpected events.
3. Keep Suricata and its rule sets updated.
4. Validate the monitoring interface and traffic visibility before each test.
5. Protect raw logs and sanitize evidence before public publication.
6. Repeat tests and document both successful detections and missed detections.

## 9. Conclusion
The project successfully demonstrated Suricata configuration, a custom ICMP signature, controlled traffic generation, alert verification, and preservation of logs after shutdown. The results establish a working baseline for further NIDS testing.

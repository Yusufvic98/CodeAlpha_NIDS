# CodeAlpha Internship — Network Intrusion Detection System (NIDS)

## Project Overview
This project demonstrates a basic Network Intrusion Detection System (NIDS) using Suricata on Kali Linux. A custom detection rule was created to identify ICMP echo requests sent from the Kali monitoring machine to a controlled Kioptrix lab target.

## Objectives
- Install and configure Suricata.
- Load community detection rules and a custom local rule.
- Monitor traffic on the lab network interface.
- Generate controlled ICMP traffic and verify detection.
- Review alerts in fast.log and eve.json.
- Document the results and limitations.

## Tools and Environment
- Kali Linux
- Suricata 8.0.7
- VirtualBox lab environment
- Kali monitoring machine: `192.168.56.101`
- Kioptrix lab target: `192.168.56.102`
- Monitoring interface: `eth1`

## Custom Detection Rule
```text
alert icmp 192.168.56.101 any -> 192.168.56.102 any (msg:"CODEALPHA NIDS - ICMP Echo Request to Kioptrix"; itype:8; sid:1000001; rev:1;)
```

The rule generates an alert when an ICMP echo request from the specified Kali IP is sent to the specified Kioptrix IP.

## Testing and Results
A controlled ping test was performed from Kali Linux to the Kioptrix lab target. The ping completed successfully, with three replies received and no packet loss.

The custom rule produced three matching alerts in `fast.log`. Three matching alert records were also verified in `eve.json` using signature ID `1000001`.

## Evidence
Screenshots documenting the rule configuration, successful traffic test, generated alerts, Suricata statistics, and log preservation after shutdown should be stored in the `evidence/` directory.

## Limitations
This test validates one specific detection scenario: ICMP echo requests from the configured source IP to the configured target IP. It does not establish detection coverage for all intrusion techniques, nor does it demonstrate automatic traffic blocking. Suricata was used in IDS alerting mode for this test.

## Conclusion
The project demonstrates how Suricata can inspect lab network traffic, apply a custom detection signature, and record matching events for investigation. It provides a foundation for further testing with additional controlled detection rules and traffic scenarios.

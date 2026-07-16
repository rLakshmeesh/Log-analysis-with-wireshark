# 14-Day PCAP Analysis Challenge

## Overview

This repository documents a 14-day self-directed training challenge focused on network traffic analysis and malware traffic identification. Each day, I analyze one PCAP file and publish a full incident-style report covering indicators of compromise (IOCs), attack chain reconstruction, and detection recommendations.

The goal is to build hands-on, demonstrable experience in packet analysis, traffic-based threat detection, and SOC-style reporting — skills directly applicable to SOC Analyst, Detection Engineer, and VAPT roles.

## Source Material

All PCAP files used in this challenge are sourced from **[Malware-Traffic-Analysis.net](https://www.malware-traffic-analysis.net/training-exercises.html)**, a well-known public resource maintained for training network defenders. The site provides real (defanged/sanitized) malicious traffic captures paired with scenario write-ups, making it a standard reference used across the security community for practicing traffic analysis.

Each exercise typically includes:
- A `.pcap` file containing the captured network traffic
- A short scenario description (e.g., "an employee's workstation got infected")
- Associated alerts or hints in some cases

I do not redistribute the PCAP files themselves in this repository — only my analysis reports. Anyone wanting to reproduce the exercises should download the PCAP directly from the source site.

## Methodology

For each PCAP, I follow a consistent analysis workflow:

1. **Initial triage** – Load the PCAP in Wireshark/tshark, review protocol hierarchy and conversations.
2. **DNS & HTTP review** – Identify suspicious domains, user-agents, and file downloads.
3. **Stream reconstruction** – Follow TCP/HTTP streams to extract payloads, executables, or exfiltrated data.
4. **IOC extraction** – Pull IPs, domains, hashes (via extracted files), and URIs.
5. **Threat correlation** – Cross-reference IOCs against VirusTotal, urlscan.io, and other OSINT sources.
6. **MITRE ATT&CK mapping** – Map observed behavior to relevant tactics/techniques.
7. **Report writeup** – Document findings, timeline, and detection/prevention recommendations.

## Tools Used

- Wireshark / tshark
- NetworkMiner
- VirusTotal / urlscan.io / Any.Run (for IOC enrichment)
- Suricata / Zeek (for signature and log-based validation, where applicable)
- MITRE ATT&CK Navigator (for technique mapping)

## Repository Structure

```
├── README.md
├── reports/
│   ├── day01-<exercise-name>.pdf
│   ├── day02-<exercise-name>.pdf
│   ├── ...
│   └── day14-<exercise-name>.pdf
└── progress-log.md   (optional running log of exercises attempted)
```

Each report follows a consistent structure: **Scenario Summary → Timeline of Events → IOCs → ATT&CK Mapping → Detection/Response Recommendations**.

## Progress Tracker

| Day | Exercise / PCAP | Date | Report |
|-----|------------------|------|--------|
| 1   |                  |      |        |
| 2   |                  |      |        |
| 3   |                  |      |        |
| 4   |                  |      |        |
| 5   |                  |      |        |
| 6   |                  |      |        |
| 7   |                  |      |        |
| 8   |                  |      |        |
| 9   |                  |      |        |
| 10  |                  |      |        |
| 11  |                  |      |        |
| 12  |                  |      |        |
| 13  |                  |      |        |
| 14  |                  |      |        |

## Disclaimer

All PCAP files analyzed are publicly available training material provided by malware-traffic-analysis.net for educational purposes. No live/active malware is executed as part of this exercise — analysis is strictly limited to static packet inspection. This repository is intended solely for skill-building and portfolio purposes.

## About

This challenge is part of my ongoing preparation for entry-level cybersecurity roles (SOC Analyst / Detection Engineer / VAPT), aimed at building a portfolio of practical, demonstrable network forensics work.

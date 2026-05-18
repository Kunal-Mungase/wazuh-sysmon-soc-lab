# wazuh-sysmon-soc-lab
Wazuh-Sysmon SOC Lab — A hands-on security monitoring project using Wazuh, Sysmon, and Windows Event Logs to simulate threat detection, log analysis, and incident response in a home lab.

wazuh-sysmon-soc-lab/

├── README.md

└── Report & Screenshots/

----------------------------------------------------------------------------------------------------------------------

# SOC Home Lab with Wazuh and Sysmon

## Project Overview
This project demonstrates a 4-week SOC home lab built using Wazuh, Windows telemetry, Sysmon, and File Integrity Monitoring to simulate and detect basic security incidents in a virtual environment.

## Objectives
- Deploy and configure a SIEM solution in a virtual lab
- Monitor Windows security logs and Sysmon events
- Simulate brute-force and malware-related activity
- Validate detections through Wazuh alerts
- Build dashboards and document findings

## Tools Used
- Wazuh Manager and Agent
- Sysmon
- Windows Event Logs
- File Integrity Monitoring (FIM)
- Oracle VirtualBox

## Lab Setup
- Wazuh Manager deployed in a virtual environment
- Windows endpoint configured with Wazuh Agent
- Sysmon installed for process creation monitoring
- FIM enabled for selected directories

## Implemented Use Cases
- Malware detection using EICAR test file
- Brute-force login detection
- Monitoring of `net user` execution through Sysmon Event ID 1
- Authentication log review using Event IDs 4624, 4625, and 4688

## Dashboard and Results
- Alert trend visualization
- Top triggered rules
- Agent status overview
- Incident evidence captured with screenshots

## Key Outcomes
- Built a working SOC lab from scratch
- Improved log analysis and event correlation skills
- Validated real-time detections for simulated incidents
- Gained practical exposure to SOC workflows and reporting

## Report & Screenshots-
Detailed project report is available in the `Report & Screenshots/` folder.

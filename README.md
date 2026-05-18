# wazuh-sysmon-soc-lab
Wazuh-Sysmon SOC Lab — A hands-on security monitoring project using Wazuh, Sysmon, and Windows Event Logs to simulate threat detection, log analysis, and incident response in a home lab.

wazuh-sysmon-soc-lab/

└── README.md
  |--Report & Screenshots/

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

-------------------------------------------------------
-------------------------------------------------------
## Report & Screenshots-
--------------------------------------------------------
--------------------------------------------------------


------------------------------------

CFSS GLOBAL INTERNSHIP 2026

-------------------------------------

SOC ANALYST 

-------------------------------------

Name: Kunal Mungase

Project Title: SOC Operations & Threat Detection Mastery

Domain: SOC Analyst & Blue Teaming

TOOL: WAZUH ( SERVER + Agent - Window )

Duration: 4 Weeks (21st April-21st May 2026)

Objective: Built and operated a security monitoring lab.

-------------------------------------


APPENDIX

Environment Specifications:
- Host OS: Windows 11
- Wazuh Manager Version: 4.14.5
- Wazuh Agent Version: 4.14.5-1
- Sysmon Version: v15.15
- Virtualization: Oracle VirtualBox v7.2.4 r170995 (Qt6.8.0 on windows)

GitHub Repository:
https://github.com/Kunal-Mungase/wazuh-sysmon-soc-lab

LinkedIn Posts:
https://www.linkedin.com/posts/kunalmungase_cfssintern2026-socanalyst-cybersecurity-ugcPost-7462166609332256768-V39q?utm_source=share&utm_medium=member_desktop&rcm=ACoAACZGGgYBo_Jj3X43Uv1JkHmiSmu9Wg9VIao

Contact: Kunal Mungase
Location: Pune, Maharashtra
mungasekunal18@gmail.com
www.linkedin.com/in/kunalmungase 


DECLARATION

I hereby declare that this project report is based on my own work and understanding. All screenshots are captured from my personal lab environment. No content has been plagiarized 
from external sources.

Signature: Kunal Mungase
Date: May 18, 2026

-------------------------------------

TABLE OF CONTENTS

1. Executive Summary

2. Week 1: Lab Architecture & Deployment

3. Week 2: Log Analysis & Event Monitoring

4. Week 3: Attack Simulation & Detection

5. Week 4: Dashboarding & Final Reporting

6. Key Learnings & Technical Insights

7. Conclusion


-------------------------------------

EXECUTIVE SUMMARY

Objective:
–Build and operate a functional Security Operations Center (SOC) 
–environment to monitor security events, detect threats, and 
–create professional security reports.

Environment Setup:
- Wazuh SIEM Manager/Server (v4.14.5) deployed on virtual machine.
- Wazuh Agent (v4.14.5-1) installed on Windows host system
- Sysmon integrated for advanced process monitoring.
- File Integrity Monitoring (FIM) enabled

Key Achievements:
- Deployed Wazuh SIEM with 1 active agent
- Monitored 1000+ security events
- Successfully detected brute-force attacks and malware
- Created professional security dashboards

Technical Skills Demonstrated:
- SIEM deployment and configuration
- Log analysis and event correlation
- Threat detection and incident response
- Security visualization and reporting
- Windows security auditing

-------------------------------------

Week 1: Lab Setup -  LAB ARCHITECTURE & DEPLOYMENT

Week 1 at CFSS: Successfully built my own SIEM lab! #CFSS #SOCAnalyst #Learning #CFSSIntern2026 

I installed VirtualBox and deployed Wazuh Manager using OVA file. Successfully connected Windows agent.
Wazuh Dashboard with active agent.

Objective: Build personal SOC environment

Tasks Completed:
1. Installed Oracle VirtualBox
2. Deployed Wazuh Manager using OVA file
3. Configured network connectivity
4. Installed Wazuh Agent on Windows host
5. Verified agent-manager connectivity

Technical Configuration:
- Wazuh Manager IP: 192.168.56.102
- Agent Name: Windows-Host: wazuh-agent-4.14.5-1
- Connection Protocol: TCP/1514
- Agent Status: Active ✓

–Challenges Encountered: 

1)Understanding Virtual Environment Setup-
–Problem:
Starting from zero knowledge - didn't know what VirtualBox or OVA files were, or how virtual machines work 

–Resolution:
Learned that VirtualBox creates "computers within computers" and OVA files are pre-packaged virtual machines. Successfully imported Wazuh OVA and understood the concept of isolated testing environments. 
2)Wazuh Agent Connection-
–Problem:
After installing agent on Windows host, it needed to communicate with Wazuh Manager VM but wasn't sure how to configure the connection properly.

–Resolution:
Identified Wazuh Manager IP address from the VM console, configured agent's ossec.conf file with correct server address, and verified connectivity by checking "1 Agent Active" status in dashboard.

--Evidence-

<img width="2880" height="1704" alt="Screenshot 2026-05-18 141235" src="https://github.com/user-attachments/assets/b3d55e94-5728-4b67-b59b-0d10ba814a85" />

Screenshot shows Wazuh dashboard displaying "1 Agent Active" 
with green status indicator, confirming successful deployment.

-------------------------------------
-------------------------------------
-------------------------------------

Week 2: Log Analysis -  Log Analysis & Event Monitoring

Week 2 at CFSS: Diving deep into log analysis and identifying system event patterns. #BlueTeaming #LogAnalysis #CFSSIntern2026 

Event Viewer screenshots (Event ID 4624, 4625) & Top 10 security events table
I Analyzed Windows Security logs and identified normal vs suspicious login patterns.


Objective: Understand Normal vs Malicious Patterns


Tasks Completed:
1. Analyzed Windows Security Event Logs
2. Identified Event ID 4624 (Successful Logons)
3. Identified Event ID 4625 (Failed Logon Attempts)
4. Created custom agent groups in Wazuh
5. Extracted top 10 security events


Analysis:
–All events fall within normal operational parameters. 
–No suspicious patterns detected during the monitoring period.


–Challenges Encountered:

1) Understanding Event IDs-
–Problem: 
Windows Event Viewer showed thousands of cryptic Event IDs (4624, 4625, 4688) without clear meaning - overwhelming and confusing.

–Resolution: 
Learned that Event IDs are standardized: 4624 = successful login, 4625 = failed login, 4688 = process creation. Used Event Viewer filtering to focus on specific IDs and understand security patterns.

2) Filtering Relevant Logs in Wazuh-

–Problem:
Wazuh dashboard displayed too many events - couldn’t find specific logs among thousands of entries.

–Resolution: 
Applied search filters using Wazuh query syntax (e.g.,  rule.id:4624 ) and time range selection to narrow down results. Created custom views to focus on security-relevant events only.

--Evidence

<img width="2880" height="1704" alt="Screenshot 2026-05-15 160012" src="https://github.com/user-attachments/assets/27e86ca1-f930-4ab3-916a-b14a63f46c84" />

-------------------------------------
-------------------------------------
-------------------------------------

Week 3: Attack Simulation -  Attack Simulation & Detection

Week 3 at CFSS: Simulated a brute-force attack to test my SOC alerts. Detection is key! #CyberSecurity #SOC 

Brute force alert, EICAR detection & Command monitoring logs.
Simulated real-world attacks to validate detection capabilities. All attacks were successfully detected.

Objective: Validate Detection capabilities through controlled testing.

–Challenges Encountered: 

1) EICAR File Not Detected by Wazuh-
–Problem: 
Downloaded EICAR test file but Wazuh didn’t generate any alerts - Windows Defender quarantined it before Wazuh could see it.

Resolution: 
Enabled File Integrity Monitoring (FIM) in Wazuh’s ossec.conf for Desktop and Downloads folders with real-time monitoring. Temporarily disabled Windows Defender, placed EICAR in monitored directory, and successfully triggered Wazuh alerts with custom detection rule.

2) Command Monitoring Not Working-
–Problem: 
Ran commands like  whoami ,  ipconfig , and  systeminfo  in CMD but they weren’t visible in Wazuh - only  net user  appeared.

–Resolution: 
Discovered Windows doesn’t log CMD commands by default. Installed Sysmon (System Monitor) for advanced process tracking and modified Sysmon configuration from default filtering mode to verbose logging mode. This captured all command executions with Event ID 1 (Process Creation).

3) Sysmon Filtering Out Common Commands-
–Problem: 
Even after installing Sysmon, only security-relevant commands like  net user  were logged - common commands filtered out to reduce noise.

–Resolution: 
Modified sysmonconfig-export.xml to remove exclusion filters for common system commands. Updated Sysmon configuration using  Sysmon64.exe -c sysmon-verbose.xml  and restarted service. This enabled comprehensive logging of all process creation events for learning purposes.

--------------------------------------------------------------------------
--------------------------------------------------------------------------


3.1 BRUTE FORCE ATTACK SIMULATION

–Test Procedure:
- Created test user account
- Attempted failed login attempts
- Monitored Wazuh for high-severity alerts

–Results:
–Wazuh triggered Level 5+ alert after few failed attempts
– Alert description: "Multiple authentication failures"
– Detection time: < 2 minutes
– Rule ID: 

--Evidence

<img width="2880" height="1704" alt="Screenshot 2026-05-14 160624" src="https://github.com/user-attachments/assets/1ad65953-4aff-4a85-a2eb-0f77e3155fb9" />

--------------------------------------------------------------------------
--------------------------------------------------------------------------

3.2 MALWARE DETECTION TEST (EICAR)

–Test Procedure:
- Downloaded EICAR standard test file
- Placed in monitored directory (Desktop)
- Observed detection by File Integrity Monitoring

–Results:
–EICAR detected by Wazuh FIM
–Alert level: 12 (High severity)
–MD5 Hash verified: 44d88612fea8a8f36de82e1278abb02f
–Response time: Real-time detection

–Configuration Applied:
- Enabled FIM on Desktop, Downloads, Temp folders
- Real-time monitoring active

--Evidence

<img width="2880" height="1704" alt="Screenshot 2026-05-15 134950" src="https://github.com/user-attachments/assets/8f5b843b-c34a-42df-b76c-13bdb7d45163" />

--------------------------------------------------------------------------
--------------------------------------------------------------------------

3.3 COMMAND MONITORING


Test Procedure:
- Installed Sysmon for process monitoring
- Executed reconnaissance commands (whoami, net user, ipconfig)
- Tracked command execution in Wazuh


Results:
– Sysmon Event ID 1 (Process Creation) logged
– Command-line arguments captured
– Parent process identified
– User context recorded


Commands Detected:
- net user → Detected ✓
- whoami → Detected ✓ (after config optimization)
- ipconfig → Detected ✓ (after config optimization)
- systeminfo → Detected ✓ (after config optimization)


Key Learning:
–Default Sysmon configurations filter common commands to reduce noise. 
–Modified configuration to verbose mode for comprehensive logging during the learning phase.

--Evidence

<img width="2880" height="1704" alt="Screenshot 2026-05-15 160012" src="https://github.com/user-attachments/assets/7c90feda-ecb4-4b85-862b-6296fe683c71" />

---------------------------------
---------------------------------
---------------------------------

Week 4: Dashboard & Analysis - Dashboarding & Final Reporting

Week 4 at CFSS: Project Completed! Successfully finished my 1-month SOC Analyst project with CFSS. Built a SIEM lab, analyzed threats, and created a security dashboard. Ready for the next challenge! #CareerGrowth #CFSSInternship #CFSSIntern2026 

Full dashboard - 
             ■ Total Alerts per Day. ■ Top 5 Security Rules Triggered. ■ Agent Status 

Most common alert-
User Login (Level 3), Detected 1 simulated malware, System health: 100% uptime.

Objective- Build a multi-visual dashboard for security events & Present findings professionally.


Dashboard Components Created:

1. Daily Alerts Trend (Line Chart)
   - Visualizes alert volume over 7-day period
   - Identifies peak activity periods
   - Trend: [Stable/Increasing/Decreasing]

2. Top 5 Security Rules Triggered
   - Displays most frequently triggered alerts
   - Enables prioritization of security focus
   - Top rule: Registry Value Entry Added to the System with 4K triggers

3. Agent Status Monitoring
   - Real-time agent health indicator
   - Current status: 1 Active, 0 Disconnected
   - Uptime: 100% during monitoring period


Dashboard Capabilities:
- Real-time security event monitoring
- Historical trend analysis
- Quick incident identification
- Executive-level reporting view

Business Value:
This dashboard enables security teams to:
- Monitor overall security posture at a glance
- Identify anomalous patterns quickly
- Prioritize incident response efforts
- Report metrics to management


–Challenges Encountered: 

1)Creating Visualizations with No Data
Problem: 
–Attempted to create dashboard visualizations but got “No results found” errors - couldn’t build charts.

Resolution:
–Identified the issue was using wrong index pattern. Changed from  wazuh-alerts-*  to  wazuh-monitoring-*  for agent status data. Adjusted time range from “Last 15 minutes” to “Last 7 days” to capture sufficient data for meaningful visualizations.


2) Finding Correct Field Names for Visualizations
Problem: 
–Couldn’t locate  rule.description.keyword  field when building horizontal bar chart - field selector showed hundreds of options.

Resolution: Learned the difference between  .keyword  (exact match) and regular fields (analyzed text). Used Wazuh Discover to browse available fields first, then applied correct field names in visualizations. Used search function in field selector to quickly find needed fields.

3) Agent Status Not Displaying Properly
Problem: Wanted to show Active vs Disconnected agents with color coding but visualization appeared empty or showed only one status.
Resolution: Realized monitoring index needs to be queried instead of alerts index. Created pie chart using  wazuh-monitoring-*  index with  agent.status.keyword  field for proper status breakdown. Understood that seeing only “active” is normal when all agents are connected.


--Evidence

<img width="2880" height="1704" alt="Screenshot 2026-05-14 141222" src="https://github.com/user-attachments/assets/3fb6f190-1797-4696-aa64-857440d1be74" /><img width="2880" height="1704" alt="Screenshot 2026-05-15 134950" src="https://github.com/user-attachments/assets/ca8981ff-695c-4b1d-a131-4c7168d294ee" />


---------------------------------
---------------------------------
---------------------------------

KEY LEARNINGS & TECHNICAL INSIGHTS


Technical Skills Acquired:

1. SIEM Deployment & Configuration
   - Virtual environment setup
   - Agent-manager architecture
   - Network connectivity troubleshooting

2. Log Analysis
   - Windows Event Log interpretation
   - Event ID significance (4624, 4625, 4688)
   - Correlation of multiple log sources

3. Threat Detection
   - File Integrity Monitoring implementation
   - Behavior-based detection (brute force)
   - Signature-based detection (EICAR)

4. Tool Proficiency
   - Wazuh SIEM platform
   - Sysmon advanced monitoring
   - Windows security auditing
   - VirtualBox virtualization

5. Professional Reporting
   - Data visualization best practices
   - Executive summary creation
   - Evidence-based documentation

---------------------------------
---------------------------------
---------------------------------

Challenges & Solutions:

Challenge : Firstly this SOC Project was so hard to understand, deploy and apply.

Solution:  Then I read multiple resources to complete this project during this Tenure and uses multiple tools like AI, Google, Youtube, Publish Research & Documentations, etc.


Real-World Applications:

This project simulates actual SOC analyst responsibilities:
- Continuous monitoring of security infrastructure
- Threat hunting using SIEM queries
- Incident detection and validation
- Documentation for compliance/reporting

---------------------------------
---------------------------------
---------------------------------

--Conclusion

Successfully completed 4-week intensive SOC operations project, demonstrating practical skills in:
—Security monitoring infrastructure deployment ( SIEM Deployment & Configuration )
—Log analysis and threat detection
—Attack simulation and validation ( Security Incident Simulation )
—Professional security reporting

This hands-on experience provides foundational knowledge for 
pursuing roles in:
- SOC Analyst (Tier 1/2)
- Security Monitoring
- Incident Response
- Cyber Defense

Next Steps:
- Expand lab with additional vulnerable systems
- Practice advanced threat hunting techniques & Incident Response Plan
- Pursue industry certifications (Security+, CEH, OSCP)
- Continue building security portfolio.

---------------------------------
---------------------------------
---------------------------------

REFERENCES-

install wazuh-
https://wazuh.com/install/

wazuh manager-
https://documentation.wazuh.com/current/deployment-options/virtual-machine/virtual-machine.html

wazuh agent- 
https://documentation.wazuh.com/current/installation-guide/wazuh-agent/index.html
https://documentation.wazuh.com/current/upgrade-guide/wazuh-agent/windows.html
https://documentation.wazuh.com/current/user-manual/agent/agent-enrollment/index.html
https://documentation.wazuh.com/current/user-manual/agent/agent-enrollment/requirements.html
https://documentation.wazuh.com/current/user-manual/agent/agent-enrollment/enrollment-methods/via-manager-API/index.html

https://github.com/sherifrahim/Wazuh-SIEM-Defneder-Integrated

https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon

https://github.com/SwiftOnSecurity/sysmon-config

ip-
192.16X.XX.XXX


Authentication key-

MDAxIEJPT0stU1IzVlVCS0XXXXXXXXXXXXXXXXXXXX


---------------------------------
---------------------------------
---------------------------------

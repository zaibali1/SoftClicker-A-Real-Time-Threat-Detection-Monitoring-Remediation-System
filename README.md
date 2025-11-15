SoftClicker: Threat Detection, Monitoring, and Remediation System
================================================================

Overview
--------
SoftClicker is a defensive cybersecurity system designed for real-time threat detection, monitoring, and remediation on personal or organizational computers. It monitors files and processes, calculates risk scores, and takes remediation actions such as quarantining high-risk files and terminating malicious processes.

The system emphasizes educational, defensive, and ethical cybersecurity practices.

Features
--------
- Real-time File Monitoring: Detects file creation, modification, deletion, and movement.
- Process Monitoring: Continuously evaluates running processes for suspicious behavior.
- Risk Scoring: Uses heuristics and Shannon Entropy to identify high-risk files and processes.
- Automated Remediation: Quarantines or deletes high-risk files and terminates critical processes.
- Temporary File Cleanup: Removes unnecessary temp files and checks common persistence locations.
- GUI Interface: Tkinter-based interface provides logs, alerts, and user control.

Architecture
------------
- Watchdog: Monitors filesystem events.
- Psutil: Inspects system processes and metadata.
- Tkinter: Provides the GUI interface for logging and alerts.

Logic Flow:
[File Event] --> [File Analyzer] --> [Risk Score] --> [Quarantine/Log]
[Process Iteration] --> [_analyze_process] --> [Risk Score] --> [Terminate/Log]
[GUI Interface] <--> [Logs / Alerts / User Actions]

Installation
------------
1. Clone the repository:
   git clone https://github.com/zaibali1softclicker.git
   cd softclicker
2. Install dependencies:
   pip install psutil watchdog
3. Run the application:
   python main.py

Usage
-----
- Select directories to monitor from the GUI.
- Enable alerts and remediation in the settings.
- The system will log events and automatically take action on high-risk items.
- Check logs for detailed risk scores and remediation actions.

Risk Scoring
------------
- Suspicious Keywords: keygen, crack, patch → Risk: 75
- High Entropy Files: ≥7.5 → Risk: 70
- Temp Directory Execution: Risk: 85
- Persistence Attempt (Registry / Scheduled Tasks): Risk: 98
- Risk ≥95% → Immediate process termination
- Risk ≥75% → High-risk alert
- Risk >0 → Warning alert

Security & Compliance
--------------------
- Defensive Tool Only: Operates only on local files and processes.
- Non-invasive: Does not exploit third-party systems.
- Educational Purpose: Demonstrates risk scoring, entropy analysis, and remediation.
- Ethical: Safe to use in personal or lab environments.

Future Enhancements
-------------------
- Cloud-based threat intelligence integration.
- Machine-learning models for dynamic risk scoring.
- Sandbox-style execution for unknown files.
- Enhanced cross-platform GUI dashboards.

Contributing
------------
Contributions are welcome! Please fork the repository and create pull requests with improvements.

License
-------
This project is licensed under the MIT License.

Contact
-------
For questions or support, contact [Zaib Un Nissa Qureshi] at [zaib.sharafqureshi@gmail.com].

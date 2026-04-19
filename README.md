# Python Log Monitoring Tool

A simple Python-based log monitoring tool that analyzes authentication log data, detects repeated failed login attempts, and flags suspicious IP addresses using threshold-based logic.

## Features
- Parses log entries from `auth.log`
- Detects:
  - Failed password attempts
  - Invalid user login attempts
- Counts failed attempts by IP address
- Flags suspicious IPs based on a configurable threshold
- Writes alerts to `alerts.txt`

## Technologies Used
- Python 3
- Regular Expressions (`re`)

## Project Files
- `log_monitor.py` - main Python script
- `auth.log` - sample authentication log file
- `alerts.txt` - generated alert output
- `README.md` - project documentation

## How It Works
The script scans each line in the log file and looks for suspicious authentication activity.  
If an IP address exceeds the defined threshold, it is flagged as suspicious and written to `alerts.txt`.

## Example Log Entries
```text
Apr 19 10:12:01 server sshd[123]: Failed password for root from 192.168.1.10 port 22
Apr 19 10:12:05 server sshd[124]: Failed password for admin from 192.168.1.10 port 22
Apr 19 10:13:00 server sshd[126]: Failed password for root from 192.168.1.10 port 22
Apr 19 10:14:00 server sshd[127]: Invalid user hacker from 192.168.1.20 port 22

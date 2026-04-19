# Python Log Monitoring Tool

A Python-based log monitoring tool designed to analyze authentication logs and detect suspicious login activity, including brute-force attempts and unauthorized access.

## Overview

This project simulates a lightweight intrusion detection system by parsing authentication logs and identifying patterns of malicious behavior using regex-based analysis and threshold-based alerting.

## Features

* Detects failed password attempts
* Identifies invalid user login attempts
* Tracks login activity per IP address
* Flags suspicious IPs based on configurable thresholds
* Generates alert reports (`alerts.txt`)

## Technologies Used

* Python 3
* Regular Expressions (`re`)

## Project Structure

log-project/

* auth.log        # Sample authentication logs
* log_monitor.py  # Main script
* alerts.txt      # Generated alerts
* README.md       # Documentation

## How It Works

The script scans each log entry and extracts IP addresses associated with failed or invalid login attempts.
It aggregates the number of attempts per IP and flags those exceeding a predefined threshold as suspicious.

## Example Output

Suspicious IPs:
192.168.1.10 → 3 failed attempts

All Failed Attempts:
192.168.1.10 → 3 attempts
192.168.1.20 → 1 attempt

## How to Run

```bash
python3 log_monitor.py
```

## Future Improvements

* Real-time log monitoring (tail-based)
* Support for system logs (`/var/log/auth.log`)
* Email or alert notifications
* Visualization/dashboard integration
* Integration with network scanning tools



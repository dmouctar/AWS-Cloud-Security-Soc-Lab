# AWS Cloud Security-SOC Lab

**Project Status:** In Progress 🚧  
**Documentation:** Coming Soon

## Overview

This project focuses on building a cloud-based Security Operations Center (SOC) environment using Amazon Web Services (AWS).

The goal is to develop a hands-on security monitoring and threat detection environment that collects cloud infrastructure logs, identifies suspicious activity, analyzes potential threats, and generates security alerts.

The project combines AWS CloudWatch, Python-based detection scripts, and an AI-assisted security analysis component to demonstrate how security monitoring and incident investigation can be implemented in a cloud environment.

## Project Objectives

- Build a cloud-based security monitoring environment using AWS.
- Collect and centralize Linux and Apache web server logs.
- Monitor suspicious HTTP requests and potential reconnaissance activity.
- Develop Python scripts to retrieve and analyze CloudWatch events.
- Generate automated security alerts based on suspicious activity.
- Implement an AI-assisted security analyst component.
- Develop a web-based SOC dashboard for viewing security findings.

## Technology Stack

| Technology | Purpose |
|---|---|
| AWS EC2 | Cloud-hosted Linux environment |
| Amazon CloudWatch | Centralized log collection and monitoring |
| Amazon Linux 2023 | Server operating system |
| Apache HTTP Server | Web server and HTTP activity logging |
| Python | Security detection and analysis |
| Boto3 | AWS SDK integration |
| Flask | SOC dashboard development |
| AWS IAM | Identity and access management |
| Git & GitHub | Version control and project documentation |

## Key Features

- **Cloud Log Collection:** Configured the Amazon CloudWatch Agent to collect Apache access logs, Apache error logs, and Linux system messages.
- **Log Analysis:** Used CloudWatch Logs Insights to investigate HTTP requests and identify suspicious endpoint activity.
- **Python Detection Engine:** Developed a detection script to identify suspicious requests targeting administrative and potentially sensitive endpoints.
- **AWS Integration:** Connected Python detection scripts to Amazon CloudWatch using Boto3.
- **Automated Alert Generation:** Generated structured JSON security reports containing source IP addresses, suspicious requests, targeted paths, and severity classifications.
- **AI-Assisted Analysis:** Developed an initial security analyst component that produces findings, assessments, and recommended investigation actions.
- **SOC Dashboard:** Started developing a Flask-based web dashboard to display security alerts and AI-generated findings.

## Detection Examples

The detection engine currently identifies requests targeting endpoints such as:

- `/admin`
- `/wp-admin`
- `/.env`
- `/phpmyadmin`
- `/api/login`

These requests are analyzed as potential reconnaissance activity. A 404 response indicates that the requested resource was not found; it does not establish that an attack succeeded.

## Project Structure

```text
soc-lab/
└── detection/
    ├── detector.py
    ├── ai_analyst.py
    ├── app.py
    ├── soc_alerts.json
    ├── ai_analysis.json
    └── templates/
        └── dashboard.html
```

## Documentation

**Full project documentation is currently in development.**

Upcoming documentation will cover:

- AWS architecture and environment setup
- IAM permissions and security configuration
- CloudWatch Agent installation and configuration
- Log collection and analysis
- Python detection engine implementation
- AI-assisted security analysis
- SOC dashboard deployment
- Security testing and investigation results

Step-by-step instructions, configuration examples, screenshots, and technical explanations will be added as development progresses.

## Project Goals

The long-term goal is to expand this environment into a more comprehensive cloud security monitoring platform that demonstrates practical SOC operations, cloud security visibility, threat detection, and incident investigation.

## Disclaimer

This project is intended for educational purposes, cybersecurity training, and authorized security testing in a controlled lab environment.

It is not intended to replace a production SIEM or enterprise security monitoring platform.

---

**Project Status:** Active Development

*More documentation and implementation details coming soon.*

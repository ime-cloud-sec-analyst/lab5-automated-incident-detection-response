# lab5-automated-incident-detection-response
This lab demonstrates an end-to-end setup for automated incident detection and response on AWS using CloudWatch, GuardDuty, Lambda, SNS, and EC2 stress simulation. It is part of a real-world DevSecOps portfolio aligned with cloud security job roles.
Lab 5: Automated Incident Detection and Response Using AWS
Repository Name
lab5-automated-incident-detection-response
Overview
This lab simulates and implements a real-world automated incident detection and response system on AWS. It leverages Amazon CloudWatch, EC2, SNS, Lambda, and GuardDuty to create a full pipeline from monitoring to automated response. It’s a critical component of any modern DevSecOps or Cloud Security Engineer portfolio.
Tools & Services Used
- Amazon EC2 (Linux Instance)
- Amazon CloudWatch (Monitoring + Alarms)
- Amazon SNS (Notification)
- AWS Lambda (Incident Response Automation)
- Amazon GuardDuty (Threat Detection)
- IAM (Roles & Policies)
- GitHub (Documentation Repository)
Objectives
- Simulate a CPU spike on an EC2 instance.
- Create a CloudWatch alarm that triggers when CPU > 80% for 5 minutes.
- Integrate the alarm with SNS to send notifications.
- Automate response actions using Lambda.
- Prepare this lab as part of a professional DevOps/Cloud Security portfolio.
Implementation Steps
- Launch EC2 instance with Amazon Linux 2.
- Install `stress` tool using: sudo yum install stress
- Simulate CPU load with: stress --cpu 2 --timeout 300
- Create CloudWatch alarm with CPUUtilization > 80% for 5 minutes.
- Attach SNS topic to alarm for notification.
- Create Lambda function to auto-log or remediate the incident.
- Grant Lambda proper IAM permissions.
- Test and observe alarm trigger, SNS notification, and Lambda execution.
- Upload lab screenshots and code to GitHub.
Results
- Alarm successfully triggered by stress command.
- SNS notification sent to email.
- Lambda function executed upon alarm state change.
- Logs confirmed successful end-to-end automation.
Limitations
- CloudWatch metric delay (~5 mins)
- GuardDuty not triggered by CPU load (reserved for other detections)
- Lambda must be tested with correct IAM role and error-handling logic
Repository Files
- lambda_function.py: Lambda script triggered by CloudWatch
- alarm-setup-guide.md: Instructions for setting up the alarm
- screenshots/: All 52 screenshots taken during lab execution
- README.md: Full lab report and documentation
Author
Ime Ben
AWS Cloud Security Engineer & DevOps Portfolio Builder
📍 Based in Glasgow, UK
🔗 GitHub: https://github.com/ime-cloud-sec-analyst
📫 Email: imegcu55@gmail.com
🌐 Blog: https://www.iemsquad.com
Contributions to DevSecOps
This project demonstrates how cloud-native tools can automate incident detection and response. It reflects best practices in:
- Monitoring
- Automated remediation
- Security automation
- Real-world stress testing
- Continuous improvement of cloud posture
License
MIT License – Feel free to use, contribute, and modify with credit.

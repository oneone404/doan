# PROJECT REQUIREMENTS ENGINEERING

## Project Proposal

**Version:** 1.0  
**Date:** 

---

## PROJECT TITLE

**Developing an Endpoint Detection and Response (EDR) System with Behavioral Analysis and Cloud-based Monitoring**

---

## Created by GROUP _LỚP

*(Cập nhật theo nhóm thực tế)*

---

## Approval of Mentor

| Name | Signature | Date |
|------|-----------|------|
|      |           |      |

---

# PROJECT INFORMATION

**Project Acronym:** ObserOne  
**Project Title:** ObserOne – Behavioral-based Endpoint Detection and Response System  
**Start Date:**  
**End Date:**  

**Lead Institution:**  
**Project Mentor:**  
**Product Owner:**  

**Project Leader & Contact Details:**  
Name:  
Email:  
Tel:  
Student ID:  

**Partner Organization:**  
**Project Web URL:**  

---

## Team Members

| Student ID | Name | Email | Tel |
|-----------|------|-------|-----|
|           |      |       |     |

---

## REVISION HISTORY

| Version | Date | Comments | Author | Approval |
|--------|------|----------|--------|----------|
| 1.0 | | Initial Release | All members | |

---

## 1. Project Title

Developing an Endpoint Detection and Response (EDR) System with Behavioral Analysis and Cloud-based Monitoring.

---

## 2. Team Members

| Name | Student ID | Role | Contact Email |
|------|-----------|------|---------------|
| | | Project Leader | |
| | | Backend Developer | |
| | | Agent Developer | |
| | | Frontend Developer | |

---

## 3. Supervisor(s)

| Name | Contact Email | Faculty |
|------|---------------|---------|
| | | |

---

## 4. Problem Statement

With the rapid growth of information technology, computers and endpoints are increasingly exposed to cyber threats such as malware, ransomware, and zero-day attacks. Traditional antivirus solutions mainly rely on signature-based detection, which is ineffective against new and unknown threats. 

Organizations and individuals lack a centralized system that can monitor endpoint behavior in real time, detect abnormal activities, respond automatically to attacks, and provide centralized visibility through a web interface. Therefore, there is a strong need for an intelligent security system capable of proactive detection and response.

---

## 5. Survey / Existing Solutions

Current solutions such as traditional antivirus software provide basic protection but have limitations in detecting unknown or behavior-based attacks. Advanced commercial EDR products (e.g., CrowdStrike, SentinelOne) offer powerful features but are expensive and closed-source, making them unsuitable for learning, research, and small organizations.

This project aims to develop a simplified yet effective EDR system that applies behavioral analysis and cloud-based monitoring while remaining flexible and extensible.

---

## 6. Objectives and Scope

### Objectives
- Develop an endpoint agent capable of monitoring system behavior in real time
- Detect abnormal and malicious behaviors using rule-based and behavioral analysis
- Automatically respond to detected threats to minimize damage
- Provide a cloud-based backend and web dashboard for centralized monitoring

### Scope
- Endpoint monitoring on personal computers
- Behavioral detection and alerting
- Centralized cloud data collection
- Web-based monitoring and management interface

---

## 7. Key Features & Requirements

### 7.1 Key Features
- Real-time monitoring of processes, files, and network activities
- Behavioral anomaly detection
- Automatic response (process termination, isolation)
- Cloud-based data aggregation
- Web dashboard with real-time alerts

### 7.2 Functional Requirements
- User authentication (login / logout)
- Endpoint agent collects and sends security events
- System detects abnormal behaviors and generates alerts
- Administrators can view alerts and system status via web
- System supports remote response actions

### 7.3 Non-Functional Requirements
- High performance with minimal system overhead
- Secure communication between agent and cloud (TLS)
- Scalability to support multiple endpoints
- Reliability and fault tolerance

---

## 8. Availability

The system will be designed to operate continuously (24/7). Endpoint agents must continue basic protection even when cloud connectivity is temporarily unavailable.

---

## 9. Target Users

- **System Owner / Investor:** oversees system performance and security effectiveness
- **System Operator / Administrator:** monitors endpoints and handles security incidents
- **End Users:** use protected computers without direct interaction with the system

---

## 10. System Architecture Overview

### System Context Diagram (Description)

- Endpoint Agent monitors system behavior and performs local response
- Cloud Backend receives logs and alerts from agents
- Web Dashboard displays real-time information and supports management actions
- Users authenticate to the web system to monitor and control endpoints

The system follows a three-layer architecture: Endpoint Agent – Cloud Backend – Web Interface, ensuring real-time protection and centralized visibility.

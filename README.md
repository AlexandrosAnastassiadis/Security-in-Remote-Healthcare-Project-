Security in the Healthcare Industry

Project: Cybersecurity Implementation & Simulation

This project demonstrates how to build and test a secure remote healthcare environment by implementing multiple cybersecurity layers. It includes both theoretical analysis and practical simulations performed in an isolated VMware lab.

# Project Overview #

The goal of this project is to create a secure infrastructure that protects sensitive patient data and enables safe communication between healthcare staff and systems. The work includes:

Active Directory (IAM & RBAC)

Secure remote access using VPN (Tailscale)

Multi-Factor Authentication (Duo MFA)

Network segmentation using firewall rules

Phishing simulation (Gophish)

Vulnerability scanning (Nmap)

Logging and monitoring using built-in Windows tools

# Lab Environment #

All components were deployed in an isolated VMware network:

Server1 – Windows Server 2022 (Domain Controller, DNS)

Server2 – Windows Server 2022 (VPN, MFA, Firewall, Monitoring)

Client – Windows 10 (doctor workstation)

Attacker – Kali Linux (phishing simulation, vulnerability scanning)

# Implemented Security Layers #
1. Identity & Access Management

Active Directory was configured with organizational units, users, groups, and role-based access control using the principle of least privilege.

2. Secure Remote Access (VPN)

Tailscale VPN was used to provide encrypted communication between the client and server, protecting remote access such as RDP from public exposure.

3. Multi-Factor Authentication

Duo MFA was integrated into the RDP login process on Server2, ensuring that even compromised credentials cannot grant unauthorized access.

4. Network Segmentation

Firewall rules on Server2 block specific IP addresses to simulate segmentation and restrict movement within the network.

5. Phishing Simulation

A phishing attack was simulated using Gophish. A fake email was sent to the user dr.alex, and the system captured link clicks and entered credentials to demonstrate risk.

6. Vulnerability Scanning

Nmap was used from Kali Linux to identify open ports and services on Server2, illustrating common attack surfaces.

7. Monitoring & Threat Detection

Event Viewer, Windows Firewall logs, and Resource Monitor were used to identify and analyze unusual activity, including Nmap scan attempts.

# Summary & Conclusion #

This project successfully demonstrates how layered security such as RBAC, VPN tunneling, MFA, segmentation, phishing awareness, and system monitoring can significantly strengthen the cybersecurity posture of remote healthcare environments. Even with limited tools, the practical simulations show how essential these defenses are in protecting healthcare infrastructures from modern cyber threats.

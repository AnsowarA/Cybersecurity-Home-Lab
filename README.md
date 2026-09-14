# Cybersecurity & Infrastructure Home Lab

## Overview

This project documents the design, deployment, and administration of my personal cybersecurity home lab.

The environment was built to provide hands-on experience with virtualization, networking, storage, Windows and Linux administration, DNS filtering, service monitoring, reverse proxy configuration, cybersecurity tooling, and infrastructure resilience.

The lab combines physical and virtual infrastructure including:

- Proxmox VE virtualization host
- Windows and Linux virtual machines
- Synology NAS
- Raspberry Pi systems
- Primary and secondary network routers
- Ethernet switch
- Pi-hole
- Nginx reverse proxy
- Uptime Kuma
- T-Pot honeypot
- Wazuh SIEM
- UPS battery backup

This repository documents the infrastructure, configuration, and services that make up the environment.

---

## Lab Objectives

The primary goals of this home lab are to:

- Build hands-on experience with virtualization
- Deploy and manage Windows and Linux systems
- Configure local network infrastructure
- Manage network-attached storage
- Operate Raspberry Pi infrastructure services
- Monitor service availability
- Implement DNS filtering
- Configure reverse proxy services
- Deploy security monitoring tools
- Practice network and system troubleshooting
- Improve infrastructure reliability
- Maintain technical documentation

---

## Technologies Used

### Virtualization

- Proxmox VE
- Windows 11
- Ubuntu Linux
- Virtual networking
- Virtual storage

### Networking

- Primary router
- Secondary router
- Ethernet switch
- Wired Ethernet
- TCP/IP
- DNS
- Linux bridges

### Storage

- Synology NAS
- NFS
- Local storage
- Network-attached storage

### Raspberry Pi Services

- Raspberry Pi
- Pi-hole
- Nginx reverse proxy
- Uptime Kuma

### Cybersecurity

- T-Pot Honeypot
- Wazuh SIEM
- Endpoint monitoring
- Threat hunting
- Vulnerability detection
- MITRE ATT&CK

### Infrastructure

- UPS battery backup
- Windows endpoints
- Linux systems
- Self-hosted services

---

## Lab Architecture

The environment contains a mixture of physical and virtual infrastructure.

Current high-level design:

```text
                         Internet
                            |
                       Main Router
                            |
                     Secondary Router
                            |
                         Switch
            ┌───────────────┼────────────────┐
            │               │                │
        Proxmox Host    Synology NAS    Raspberry Pi
            │               │                │
       ┌────┼────┐          │          ┌─────┼──────┐
       │    │    │          │          │     │      │
    Windows Linux T-Pot    NFS      Pi-hole Nginx Uptime
      VM     VM  Honeypot                    Proxy   Kuma

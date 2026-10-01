# Homelab

A personal Linux homelab built using an old laptop as a hands-on environment for learning **Linux administration, networking, remote access, self-hosting, and cybersecurity fundamentals**.

Rather than learning these topics only through tutorials, this project gives me a system I can configure, troubleshoot, and experiment with.

## Overview

The homelab runs **Debian Linux** on an old Dell laptop and is connected to my home LAN.

Current areas of exploration include:

- Linux system administration
- Local networking and DHCP
- SSH and remote administration
- Docker and self-hosted services
- Tailscale for remote access
- Network traffic analysis with Wireshark
- File sharing with Samba
- Troubleshooting Linux services and permissions

## Hardware & Network

| Component | Details |
|---|---|
| Server | Old Dell laptop |
| Operating System | Debian Linux |
| Network | Home LAN |
| Server IP | Reserved local address |
| Remote Administration | SSH |
| Remote Access | Tailscale |

The server uses a DHCP reservation so its local address remains consistent across reboots.

## Technologies & Tools

- **OS:** Debian Linux
- **Containers:** Docker
- **Remote Access:** SSH, Tailscale
- **Networking:** TCP/IP, LAN, DHCP, DNS
- **Network Analysis:** Wireshark
- **File Sharing:** Samba
- **Version Control:** Git, GitHub

## Repository Structure

```text
homelab/
├── Docs/
│   ├── network.md
│   ├── samba.md
│   ├── ssh.md
│   ├── troubleshoot.md
│   └── wireshark.md
├── .gitattributes
└── README.md
```

The `Docs/` directory contains notes and documentation from experiments carried out while building and managing the homelab.

## What I've Practiced

### Linux Administration

- Installing and configuring Debian
- Managing packages, services, permissions, and users
- Working with system services through `systemctl`
- Managing a server remotely without relying on a desktop environment

### SSH

SSH is used for remote administration of the server.

The documentation covers:

- Remote terminal access
- File transfers with SCP
- SSH service management
- Password and public-key authentication
- Basic SSH security considerations

See [SSH Notes](Docs/ssh.md).

### Networking

The homelab is connected to a local network with a DHCP reservation for consistent addressing.

I've used the environment to understand:

- DHCP
- DNS
- Local IP addressing
- TCP/IP
- Network connectivity and troubleshooting

See [Network Setup](Docs/network.md).

### Network Analysis

I've used Wireshark to inspect network traffic and identify protocols such as:

- TCP
- DNS
- TLS 1.3

See [Wireshark Notes](Docs/wireshark.md).

### File Sharing

Samba has been used as part of the homelab to experiment with network file sharing.

The repository also documents troubleshooting a Samba share caused by incorrect directory permissions.

See [Troubleshooting](Docs/troubleshoot.md).

## Architecture

```text
                    Internet
                       │
                       │
                  Home Router
                       │
                ┌──────┴──────┐
                │             │
          Personal Devices   Homelab
                              │
                         Debian Linux
                              │
              ┌───────────────┼───────────────┐
              │               │               │
             SSH            Docker         Samba
              │               │               │
       Remote Administration  Services    File Sharing
                              │
                         Tailscale
                              │
                       Remote Access
```

## Troubleshooting

A major part of this project is learning by fixing problems rather than only following setup instructions.

For example, a Samba share was initially inaccessible because of incorrect directory permissions. The issue was resolved by correcting the permissions and restarting Samba.

See [Troubleshooting Notes](Docs/troubleshoot.md).

## Goals

This is an ongoing learning project.

Future work will focus on:

- Documenting more services and configurations
- Learning more about Docker networking
- Improving server security
- Exploring monitoring and logging
- Experimenting with reverse proxies
- Building services for the homelab
- Connecting the homelab with other personal projects

## Why I Built This

I wanted a practical environment where I could **break things, troubleshoot them, and understand how Linux and networking work in practice**.

The homelab is a sandbox for my interests in **Linux, networking, cybersecurity, and systems engineering**.

---

**Status:** Active / Continuously evolving

**Author:** Kanishk Dongre  
**GitHub:** https://github.com/Nilltheory

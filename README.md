# Homelab

A personal Linux homelab built using an old laptop to experiment with **Linux administration, networking, self-hosting, virtualization, Docker, and remote access**.

The goal of this project is to turn otherwise unused hardware into a practical environment where I can learn by deploying, configuring, and troubleshooting real services.

## Overview

The homelab currently runs **Debian Linux** and is used as a personal server and experimentation environment.

I use it to explore:

* Linux system administration
* Networking and remote access
* Docker and containerized applications
* SSH
* Tailscale
* Self-hosted services
* Server configuration and troubleshooting

## Hardware

* **Device:** Old Dell laptop
* **Operating System:** Debian Linux
* **Network:** Home LAN
* **Remote Access:** Tailscale + SSH

## Technologies & Tools

| Category              | Technologies     |
| --------------------- | ---------------- |
| Operating System      | Debian Linux     |
| Containers            | Docker           |
| Remote Access         | SSH, Tailscale   |
| Networking            | TCP/IP, LAN, DNS |
| Security / Networking | Nmap, WireGuard  |
| Version Control       | Git, GitHub      |

## Services

Some of the services and experiments deployed on the homelab include:

* **Docker containers** for running self-hosted applications
* **File Browser** for accessing files through a web interface
* **Homepage** for organizing and accessing services
* **SSH** for remote administration
* **Tailscale** for secure remote access to the homelab

The exact services may change as the homelab evolves.

## What I've Learned

This project has helped me move beyond simply using Linux and start understanding how systems actually work.

Through the homelab, I've practiced:

* Installing and configuring Debian from scratch
* Managing users, permissions, packages, and services
* Connecting to machines using SSH
* Deploying applications using Docker
* Understanding containers and ports
* Accessing services over a local network
* Setting up remote access using Tailscale
* Troubleshooting networking and service configuration issues
* Managing a server without a traditional desktop environment

## Architecture

```text
                    Internet
                       │
                       │
                  Home Network
                       │
              ┌────────┴────────┐
              │                 │
        Personal Devices    Homelab Server
                                │
                         Debian Linux
                                │
                ┌───────────────┴───────────────┐
                │                               │
              SSH                            Docker
                                                │
                              ┌─────────────────┼─────────────────┐
                              │                 │                 │
                        File Browser        Homepage          Other Services
                              │
                              │
                         File Storage

                         Tailscale
                             │
                    Remote Access Layer
```

## Project Goals

The homelab is an ongoing learning project rather than a finished product.

Future experiments may include:

* Deploying additional self-hosted services
* Improving monitoring and logging
* Learning more about Docker networking
* Experimenting with reverse proxies
* Improving server security
* Building services specifically for the homelab
* Integrating the homelab with other personal projects

## Why I Built This

Instead of learning Linux and networking only through tutorials, I wanted an environment where I could **break things, troubleshoot them, and understand how the pieces fit together**.

The homelab serves as a practical sandbox for my interests in **Linux, networking, cybersecurity, and systems engineering**.

---

**Status:** Active / Continuously evolving

**Author:** Kanishk Dongre
**GitHub:** https://github.com/Nilltheory



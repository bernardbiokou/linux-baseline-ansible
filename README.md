# Linux Baseline - Ansible
Production Ansible role implementing a secure Linux server baseline for Debian/Ubuntu LTS.

## Features
Secure users & sudo access (baseline admin accounts with passwordless sudo if desired).
Hardened SSH (key‑based authentication only, no root login, no password auth).
UFW firewall with restrictive defaults and port 22 allowed for SSH access.
The full kit is designed to be readable and easy to extend, with each concern split into its own task file so you always know what is happening on your servers.

## Requirements
Control machine with Ansible installed (for example, your laptop or an admin VM).
Target hosts running a supported Debian/Ubuntu LTS release, reachable over SSH.
SSH user with sudo privileges on each target host.

## Quick Test
Dry‑run the baseline against the hosts defined in inventory.ini:
ansible-playbook -i inventory.ini site.yml --check
Apply the changes for real:
ansible-playbook -i inventory.ini site.yml

## Structure
├── linux-baseline-ansible
│   ├── inventory.ini
│   ├── roles
│   │   └── linux_baseline
│   │       ├── defaults
│   │       │   └── main.yml
│   │       ├── handlers
│   │       │   └── main.yml
│   │       ├── tasks
│   │       │   ├── basics.yml
│   │       │   ├── logs.yml
│   │       │   ├── main.yml
│   │       │   ├── post_check.yml
│   │       │   ├── ssh.yml
│   │       │   ├── timesync.yml
│   │       │   ├── ufw.yml
│   │       │   ├── unattended_upgrades.yml
│   │       │   └── users.yml
│   │       └── templates
│   │           └── sshd_config.j2
│   └── site.yml
└── README.md

If you want a step-by-step, production-ready implementation, including:

- full walkthrough
- safety checklists
- real-world usage guidance

A complete Pack is available here:

https://aloba.gumroad.com/l/linux-baseline-ansible-kit

## Final note
This repository is meant to be a reference implementation. Adapt it to your organization’s security policies and operational requirements.

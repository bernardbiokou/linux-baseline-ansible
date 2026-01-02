# Linux Baseline - Ansible
Automate and secure your **Debian / Ubuntu servers** with a clean, reusable Linux baseline — even if you **don’t have a DevOps team**.

This repository provides the **technical implementation** of a Linux baseline using Ansible.  
For a **production-ready, step-by-step deployment guide**, real-world use cases, and operational checklists, see the **Production Pack** below.

## Why this project exists?

In many small teams and SMEs:
- Servers are configured manually
- Security settings drift over time
- Access management becomes risky
- One person holds all the infra knowledge

This project helps you **standardize and automate** a Linux baseline so your infrastructure stays **boring, predictable, and secure**.

## What you get here (Free)

This repository includes:

- ✔️ Ansible role for a Linux baseline
- ✔️ SSH hardening
- ✔️ Firewall configuration (UFW)
- ✔️ User and sudo management
- ✔️ Example inventory and playbook

This is a **solid technical foundation** you can test, study, or extend.

> ⚠️ This repository focuses on *implementation*, not full production operations.

## Production Pack (Paid)

If you want to deploy this **in production without guessing**, the Production Pack is designed for you.

It includes:

- ✅ Step-by-step deployment guide (from empty server to baseline)
- ✅ Real production use cases    
- ✅ Security & production checklists
- ✅ Rollback and validation strategies
- ✅ Operational tips (maintenance, reviews, updates)
- ✅ Troubleshooting & common pitfalls

👉 Get the Production Pack here:  
https://aloba.gumroad.com/l/linux-baseline-ansible-kit

**You keep the code. You pay for clarity, safety, and time saved.**

## Typical use cases

- Solo sysadmin managing several servers
- IT managers without a dedicated DevOps team
- SMEs looking for a repeatable Linux baseline
- Consultants who need a clean starting point

## Quick Test
git clone https://github.com/bernardbiokou/linux-baseline-ansible.git
cd linux-baseline-ansible
ansible-playbook -i inventory playbook.yml

## Structure
```bash
inventory.ini        # Example inventory
site.yml             # Main playbook
roles/
└── linux_baseline/  # Linux baseline role (security, users, firewall, SSH)

For p
```roduction deployment recommendations and validation steps, see the Production Pack.

## FAQ 
Is this production-ready out of the box?
The code is solid, but production requires decisions, validation, and operational discipline.
That’s exactly what the Production Pack provides.

Why is the detailed documentation not included here?
This repository is meant to stay simple and accessible.
Advanced production scenarios, checklists, and runbooks are packaged separately.

Can I adapt this to my infrastructure?
Yes. The structure is modular and designed to be extended.

## License
MIT License - commercial use is allowed.

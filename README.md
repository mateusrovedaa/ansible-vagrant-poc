# Ansible + Vagrant POC

This is a simple Proof of Concept using Vagrant and Ansible to provision an Ubuntu VM using Ansible roles.

## Requirements

- [Vagrant](https://www.vagrantup.com/downloads)
- [VirtualBox](https://www.virtualbox.org/wiki/Downloads) (or another provider)

## Getting Started

### 1. Clone the repo

```bash
git clone https://github.com/mateusrovedaa/ansible-vagrant-poc.git
cd ansible-vagrant-poc
```

### 2. Start the VM with Vagrant and Ansible tasks

```bash
vagrant up
```

> This will download the box start the VM and run Ansible to setting up.

## To Clean Up

```bash
vagrant destroy -f
```

## Tips
```bash
vagrant ssh
```
> To connect to the VM using SSH

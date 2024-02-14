# Ansible Practice Lab with Vagrant and VMware Workstation

This repository contains a simple Ansible practice lab environment set up using Vagrant with VMware Workstation as the provider.

## Overview

In this lab environment, we have set up two virtual machines:
- **master**: This server acts as the Ansible control node.
- **node**: This server is the target machine where Ansible will perform configurations.

## Requirements

Before you begin, ensure you have the following software installed on your machine:
- [Vagrant](https://www.vagrantup.com/downloads)
- [VMware Workstation](https://www.vmware.com/products/workstation-pro.html)

## Setup

1. Clone this repository to your local machine:

    ```bash
    git clone <repository-url>
    ```

2. Navigate to the project directory:

    ```bash
    cd ansible-practice-lab
    ```

3. Start the lab environment:

    ```bash
    vagrant up --provider=vmware_workstation
    ```

4. Once the VMs are up, you can SSH into each VM to verify the configurations:

    ```bash
    vagrant ssh master
    vagrant ssh node
    ```

## Ansible Playbooks

- **`provision/master/playbook.yml`**: Ansible playbook for the master server.
- **`provision/node/playbook.yml`**: Ansible playbook for the node server.

## Clean Up

To stop and destroy the VMs, run:

```bash
vagrant destroy -f


## Author

Boni Yeamin - boniyeamin.cse@gmail.com

## License

Replace `[repository-url]`, `[Your Name]`, and `[Your Contact Information]` with appropriate values.

This README provides an overview of the project, setup instructions, details about Ansible playbooks, and instructions for cleaning up the environment. Feel free to customize it further according to your needs.

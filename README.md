# Final_Project
Windows and Linux Automation with Ansible

This repository contains a collection of Ansible roles and playbooks designed for automated configuration and management of Windows and Linux environments. The automation tasks include software installations, security configurations, disk encryption, system monitoring, web server setup, and much more.

## Project Structure

The project is organized into roles, each tailored for specific tasks on either Windows or Linux platforms. Here's an overview of the directory structure and the roles included:

FINAL_PROJECT
│
├── roles
│ ├── linux_email_server_setup
│ │ ├── handlers
│ │ │ └── main.yml
│ │ ├── tasks
│ │ │ └── main.yml
│ ├── linux_firewall_configuration
│ │ └── ...
│ ├── linux_freeradius_setup
│ │ └── ...
│ ├── linux_web_server_setup
│ │ ├── handlers
│ │ │ └── main.yml
│ │ ├── tasks
│ │ │ └── main.yml
│ │ ├── templates
│ │ │ └── nginx.conf.j2
│ │ └── vars
│ │ └── main.yml
│ └── ...
│
├── windows_disk_encryption
│ └── ...
├── windows_security_configuration
│ └── ...
├── windows_software_installation
│ └── ...
├── windows_system_monitoring
│ └── ...
├── windows_updates_reboot
│ └── ...
├── inventory
└── main.yml


## Usage

To execute any of the playbooks, you need to have Ansible installed on your control machine, and the target hosts must be prepared for Ansible automation.

### Executing a Playbook

To run a playbook, use the following command:

```sh
ansible-playbook -i inventory roles/<role_name>/tasks/main.yml
Replace <role_name> with the name of the role you wish to execute. For example, to install and configure Nginx on Linux machines, run:
ansible-playbook -i inventory roles/linux_web_server_setup/tasks/main.yml
Windows Automation
Here are the available roles for Windows:

Software Installation: Install common software packages.
Security Configuration: Configure firewall and antivirus settings.
Disk Encryption: Enable BitLocker for disk encryption.
System Monitoring: Collect system performance metrics.
Updates and Reboot: Manage Windows updates and reboots.
Linux Automation
Here are the available roles for Linux:

Web Server Setup: Install and configure the Nginx web server.
Firewall Configuration: Configure firewall settings for web traffic.
Email Server Setup: Install and configure an open-source email server.
FreeRADIUS Server Setup: Install and configure a FreeRADIUS server.
Customization
You can customize the behavior of each role by modifying the variables in the vars/main.yml file within the role directory.

Contributing
Contributions are welcome! Feel free to fork this repository, make your changes, and submit a pull request.

License
This project is licensed under the MIT License.

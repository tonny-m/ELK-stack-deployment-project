## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

![Diagrams/Diagram.png](Diagrams/Diagram_v2.2.png)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the YAML file may be used to install only certain pieces of it, such as Filebeat.

[ELK_stack_playbook](Ansible/ELK_playbook.yml)

This document contains the following details:
- Description of the Topology
- Access Policies
- ELK Configuration
- Beats in Use
- Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the Damn Vulnerable Web Application.

Load balancing ensures that the application will be highly available, in addition to restricting unauthorized access to the network.
Load balancers provide sustain availability by even distribution of the trafic between servers. 
A jump box helps to narrow an attack surface of the environment by a lot. 

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the logs and system metrics.
Filebeat helps to forward and centralize lod data.
Metricbeat records metrics and statistics.

The configuration details of each machine may be found below.
_Note: Use the [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove values from the table_.

| Name             | Function                | IP Address | Operating System |
|------------------|-------------------------|------------|------------------|
| Jump-Box         | Gateway                 | 10.0.0.4   | Linux            |
| Web-1            | Web server              | 10.0.0.5   | Linux            |
| Web-2            | Web server              | 10.0.0.6   | Linux            |
| Web-3            | Web server              | 10.0.0.7   | Linux            |
| Elk-Stack-Server | Log management platform | 10.2.0.4   | Linux            |

### Access Policies
 
The Jump-Box machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
"admin_public_IP" ## "admin_public_IP" has to be set by the system administrator.

All machines within the network can only be accessed by Jump-Box (10.0.0.4)

A summary of the access policies in place can be found in the table below.

| Name             | Publicly Accessible | Allowed IP Addresses        |
|------------------|---------------------|-----------------------------|
| Jump-Box         | Yes                 | "admin_public_IP"           |
| Web-1            | No                  | 10.0.0.4                    |
| Web-1            | No                  | 10.0.0.4                    |
| Web-3            | No                  | 10.0.0.4                    |
| Elk-Stack-Server | Yes                 | 10.0.0.4; "admin_public_IP" |
| Load Balancer    | Yes                 | "admin_public_IP"           |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- _TODO: What is the main advantage of automating configuration with Ansible?_

The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- ...
- ...

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

![TODO: Update the path with the name of your screenshot of docker ps output](Images/docker_ps_output.png)

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- _TODO: List the IP addresses of the machines you are monitoring_

We have installed the following Beats on these machines:
- _TODO: Specify which Beats you successfully installed_

These Beats allow us to collect the following information from each machine:
- _TODO: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., `Winlogbeat` collects Windows logs, which we use to track user logon events, etc._

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the _____ file to _____.
- Update the _____ file to include...
- Run the playbook, and navigate to ____ to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook? Where do you copy it?_
- _Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on?_
- _Which URL do you navigate to in order to check that the ELK server is running?

_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._

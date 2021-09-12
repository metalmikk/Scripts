# Scripts
Linux and Ansible Scripts from my CyberSecurity Bootcamp 2021

## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

![Week 12 Homework Submission](https://user-images.githubusercontent.com/84828582/132951284-0174e5e1-cd24-48a8-92e6-cce3df52eed2.png)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the CONFIGURATION fileS may be used to install only certain pieces of it, such as Filebeat.

  - _TODO: Enter the playbook file._

This document contains the following details:
- Description of the Topologu
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly SECURE, in addition to restricting ACCESS to the network.

- Load balancers add resiliency by rerouting live traffic from one server to another if a server falls prey to a DDoS attack or otherwise becomes unavailable.

- Jump-box are highly secured computers that are never used for non-admin tasks. -Throughout the years, jump-box has improved into an even more comprehensive/lock-down secure admin workstation to decrease the chances of hackers/malware infection.

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the NETWORK and system LOGS.

What does Filebeat watch for? 
- It monitors the log files/locations that you specify and forwards them to Elasticsearch/Logstash for indexing.
 
What does Metricbeat record?
- It records metrics/statistics data and transports them to the output that you specifics thru Elasticsearch/Logstash.

The configuration details of each machine may be found below.
_Note: Use the [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove values from the table_.

| Name      | Function | IP Address | Operating System |
|-----------|----------|------------|------------------|
| Jump Box  | Gateway  | 10.1.0.4   | Linux            |
| Web-1     | VM       | 10.1.0.7   | Linux            |
| Web-2     | VM       | 10.1.0.6   | Linux            |
| ELK-Server| VM       | 10.3.0.4   | Linux            |

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the JUMPBOX PROVISIONER machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- 20.36.32.197

Machines within the network can only be accessed by JUMPBOX PROVISIONER.

Which machine did you allow to access your ELK VM?
- JUMPBOX PROVISIONER

What was its IP address?
- 10.1.0.4 (PRIVATE)
- 20.36.32.197 (PUBLIC)

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box | Yes                 | 20.36.32.197    |
| Web-1         | No                     | 10.1.0.4                     |
| Web-2         | No                    | 10.1.0.4                      |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- IT ALLOWS FOR SETUP IN MINUTES USING SSH WITHOUT INSTALLING ANYTHING ON SERVERS
- IT AUTOMATES MULTIPLE IT APPLICATIONS

The playbook implements the following tasks:
- INSTALL DOCKER.IO
- INSTALL PYTHON-PIP
- DOWNLOAD AND LAUNCH ELK DOCKER CONTAINER

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

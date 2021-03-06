# Cybersecurity
## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

(Images/Project1EricL.png)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the .yml file may be used to install only certain pieces of it, such as Filebeat.

  Install-ELK.yml

This document contains the following details:
- Description of the Topologu
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly reliable and efficient, in addition to restricting traffic to the network.
-What aspect of security do load balancers protect? What is the advantage of a jump box?
	Load Balancers protect application servers. The advantage of a load balancer is that can add additional layers of security to your website without any changes to your application.

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the logs and system traffic.

-What does Filebeat watch for? Collects data about the file system.
-What does Metricbeat record? Collects machine metrics, such as uptime and memory.

The configuration details of each machine may be found below.
_Note: Use the [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove values from the table_.

| Name     | Function | IP Address | Operating System |
|----------|----------|------------|------------------|
| Jump Box | Gateway  | 10.0.0.4   | Linux            |
| DVWA1    |Web Server| 10.0.0.5   | Linux            |
| DVWA2    |Web Server| 10.0.0.6   | Linux            |
| ELK      |Web Server| 10.0.0.7   | Linux            |

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the Jump Box machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
		- 67.160.140.185
Machines within the network can only be accessed by __ssh___.
- : Which machine did you allow to access your ELK VM? What was its IP address?
- JumpBox @ 10.0.0.4

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box | Yes                 |  67.160.140.185      |
| ELK      | No                  |    10.0.0.4          |
| DVWA 1   | No                  |    10.0.0.4          |
| DVWA 2   | No                  |    10.0.0.4          |
### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- What is the main advantage of automating configuration with Ansible?
-  The main advantage of using Ansible is that it helps IT Admin save time with difficult manual tasks that become repeatable and less vulnerable to error.

The playbook implements the following tasks:
- In 3-5 bullets, explain the steps of the ELK installation play.
. config Web VM with Docker 
. docker.io
. Instal pip3
. Install Python Docker Module
. Use more memory
. Install Docker container

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.
 

![TODO: Update the path with the name of your screenshot of docker ps output](Images/Elkinstall.png)

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
Web1 (10.0.0.5) Web2 (10.0.0.6) Web3 (10.0.0.7)

We have installed the following Beats on these machines:
- Filebeat and Metricbeat

These Beats allow us to collect the following information from each machine:
- `Winlogbeat` collects Windows logs, which we use to track user logon events, Filebeat collects specified log data and forwards it to Elasticsearch or Logstash. Metricbeat collects metrics from the OS and from services running on the server

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

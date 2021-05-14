## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

![](https://github.com/jamesdewhirst/Automated-ELK-Stack-Deployment/blob/main/Diagrams/20210319_00012.png)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the playbook file may be used to install only certain pieces of it, such as Filebeat.

  - ![](https://github.com/jamesdewhirst/Automated-ELK-Stack-Deployment/blob/main/Images/20210319_00005.png)

This document contains the following details:
- Description of the Topologu
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly reliable, in addition to restricting access to the network.

- Load balancers 
    - Help protect and restrict availability of content
    - Aid in prevention of a DoS attack
- Jump Box
    - Restriction of access to one administrator

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the log files and system system metrics.
- Filebeat
    - Aids us in the generation and organization of log files which are used in Logstash and Elasticsearch.
    - These logs and important information that needs to be protected such as system files
- Metricbeat
    - A data collector you can schedule to collect system metrics to be analyzed in Logstsh and Elasticsearch. 

The configuration details of each machine may be found below.
_Note: Use the [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove values from the table_.

```git
| Name                 | Function         | IP Address | Operating System |
|----------------------|------------------|------------|------------------|
| Jump-Box-Provisioner | Gateway          | 10.0.0.4   | Linux            |
| Web-1                | DVWA Containers  | 10.0.0.5   | Linux            |
| Web-2                | DVWA Containers  | 10.0.0.6   | Linux            |
| ELK                  | Configuration VM | 10.2.0.4   | Linux            |
```

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the Jump Box machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- 24.9.228.255 - My personal machine

Machines within the network can only be accessed by using the DVWA container in the Jump Box Virtual Machine.
- Access to the ELK server is from 24.9.228.255 (my personal machine)
- Access to the Jump Box VM is at 10.0.0.4

A summary of the access policies in place can be found in the table below.

```git
| Name                 | Publicly Accessible | Allowed IP Address      |
|----------------------|---------------------|-------------------------|
| Jump-Box-Provisioner | Yes                 | 10.0.0.4, 52.250.13.233 |
| Web-1                | No                  | 10.0.0.5                |
| Web-2                | No                  | 10.0.0.7                |
| ELK                  | No                  | 10.2.0.4, 41.121.108.9  |
```

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

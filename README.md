# ***Ansible Playbook & Jenkins CasC & Docker-Compose***

![This is an image](https://i.ibb.co/swNGYRZ/ansible.png#gh-light-mode-only) ![This is an image](https://i.ibb.co/j34FMrK/pngwing-com-1.png#gh-light-mode-only) ![This is an image](https://i.ibb.co/C8BqmLr/jenkins.png#gh-light-mode-only)

#### **What is Jenkins?**
Jenkins is an open source automation server.  
It helps automate the parts of software development related to building, testing, and deploying, facilitating continuous integration and continuous delivery. 

#### **What is Jenkins Configuration as Code plugin?**
The Jenkins Configuration as Code (JCasC) feature defines Jenkins configuration parameters in a human-readable YAML file that can be stored as source code.  
This essentially captures the configuration parameters and values that are used when configuring Jenkins from the web UI.

#### **What is Docker?**
Docker is a software platform that allows you to build, test, and deploy applications quickly.  
Docker packages software into standardized units called containers that have everything the software needs to run including libraries, system tools, code, and runtime.

#### **What is Docker-Compose?**
Docker Compose is a tool that was developed to help define and share multi-container applications. 
With Compose, we can create a YAML file to define the services and with a single command, can spin everything up or tear it all down.

#### **What is Ansible?**
Ansible is defined as an open-source, cross-platform tool for resource provisioning automation that DevOps professionals popularly use for continuous delivery of software code by taking advantage of an “infrastructure as code” approach.

#### **What is Playbook? (ansible-playbook)**
Ansible Playbooks are lists of tasks that automatically execute against hosts.  
Groups of hosts form your Ansible inventory. 
Each module within an Ansible Playbook performs a specific task.  
Each module contains metadata that determines when and where a task is executed, as well as which user executes it. 

--------------------------------------------------------------------------------------------

![This is an image](https://i.ibb.co/9ZZGqNJ/wp4399607-removebg.png)

I wrote an automation file (Playbook) using "Ansible". 
The purpose of the file is to perform a sequence of operations, from a main computer (server) to remote computers (hosts) by running the automation file.  

Sequence:
1. Install "Docker", "Docker-Compose", "Docker.io" and "Docker-Registry".
2. Clone a repository form my "GitHub" to the remote computers (hosts) in order to get a "docker-compose.yml" file.
3. Running the "docker-compose.yml" file.

What this Docker-Compose file do?

+ Build Jenkins Image (2.332.2) with "Dockerfile".
+ Setting up a "Jenkins" server with the "Configuration as a Code" plugin  with "plugins_extra.txt".
+ Create users with a predefined password with "jenkins.yaml".

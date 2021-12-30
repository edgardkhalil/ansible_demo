# ansible_demo

This is my demo ansible repository for learning and testing. 

What I have learned and built so far:

1. Installed ansible on a local control node: https://docs.ansible.com/ansible/latest/installation_guide/index.html

2. Created some EC2 instances, with Ubuntu and RedHat. Made sure to allow SSH to the hosts in the Security Group so that ansible could connect to it. Downloaded the ssh key and copied it to my control node. 

3. Created a local inventory file and ansible.cfg file. Added the EC2 instances to the inventory, and made sure to specify "ansible_user" for the hosts since the EC2 logins are different. Defined path to the local inventory file in ansible.cfg. Also specified the path to the private SSH key.


4. Ran some adhoc commands to make sure that connectivity to the EC2 instances is working: 
- ansible all -m gather_facts
- ansible all -m ping

5. Created first playbook, which is configured perform apt-get update, install apache server, and php. 


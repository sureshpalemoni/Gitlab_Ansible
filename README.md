# Gitlab_Ansible
Ansible role for installing gitlab on centos 7

1. Configure the Main playbook where you include this role.

Example: My Main playbook looks like below:

- name: Configure the Gitlab sever  
  hosts: gitlabserver  
  remote_user: root  
  become: yes  
  become_user: root  
  become_method: sudo
  
  roles:    
   - gitlab
   
 2. Configure the hosts file
 
 add the below lines to the file - /etc/ansible/hosts
 
 [gitlabserver]
 192.168.X.X

3. Create a file with name gitlabserver in folder /etc/ansible/group_vars

In the file add:

\---

ansible_ssh_user: centos

**centos is my username - add yours, how ansible should ssh to the destination server

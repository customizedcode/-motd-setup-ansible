motd-setup-ansible
=========

Setup simple message of the day for both CentOS 8 and Ubuntu 18,20  

It does a few things:  
1 - Disables the "MOTD commercials" from Ubuntu and the Cockpit notification from RedHat.  
2 - It adds your own custom MOTD to the system.  
3 - You can change these messages as often as you want using this role and Ansible playbook.  
  
There are three line variables: motd_var1, motd_var2, motd_var3  

If these are not changed, the default values of the role will be used.  

<pre>
motd_var1: 'Customized.local'  
motd_var2 = 'Authorized Users Only'  
motd_var3 = '*********************'  
</pre>

Example Playbook
----------------

<pre>
-
   hosts: all  
   become: yes  
   roles:  
     - role: motd-setup-ansible  
       vars:  
         motd_var1: 'Customized Enterprise (customized.local)'  
         motd_var2: '*******Authorized Users Only************'  
         motd_var3: '****************************************'  
</pre>

License
-------

BSD

Author Information
------------------
Roy Kim  
https://github.com/customizedcode  
customizedcode.us  
  
This is part of a tutorial for creating portable roles from playbooks.  
Please see the playbook this came from if your interested.  
  

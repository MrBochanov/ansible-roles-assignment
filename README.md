# ansible-roles-assignment

The task is to create ansible roles for implementing nginx servers with simple php app, and ha-proxy in front of to load-balance traffic between web-servers.

# solution

3 roles were created for this task:
    nginx - for installing nginx server and site configuring depending on template and domain variable
    app - simple php app with template depending oh hostname variable
    ha - ha proxy installation with auto-generated config based on hosts in web-server group

hosts with 3 nginx servers and one ha-proxy
playbook, which installs nginx and app roles on nginx servers and ha on lb-servers   

Ansible host must have access to all servers

```
ansible-playbook play.yml -kK
```

New nginx host can be added, roles will be applyed and haconfig will be regenrated after.
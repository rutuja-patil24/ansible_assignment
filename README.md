# ansible_assignment:

## Files description:
inventory.ini file has the webservers information.
webserver_apache.yml has playbook with tags to deploy and undeploy to VMs.

## Commands to run:
ansible -i inventory.ini webservers -m ping
ansible-playbook -v -i inventory.ini webserver_apache.yml --tags "deploy" 
ansible-playbook -v -i inventory.ini webserver_apache.yml --tags "undeploy" 

## Console outputs:
ssh_ping.txt ---> SSH connection to VMs
deploy_console_output.txt ---> Shows the plays for deploy tags
undeploy_console_output.txt ---> Shows the plays for undeploy tags

vm1_console.log --->  From GCP for VM1 serial port 1 console log
vm2_console.log --->  From GCP for VM2 serial port 1 console log

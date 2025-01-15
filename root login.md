### Following security audits, the xFusionCorp Industries security team has rolled out new protocols, including the restriction of direct root SSH login.
Your task is to disable direct SSH root login on all app servers within the Stratos Datacenter.
#### open Three Terminal and ssh on all App server
- give execute permission to sshd_config file
```
sudo chmod 777 sshd_config
```
- Run the below command on each app server and Search for #PermitRootLogin yes
```
sudo vi /etc/ssh/sshd_config
```
- Remove the “#” and change “yes” to “no” from PermitRootLogin
- restart sshd service
```
sudo systemctl restart sshd
```

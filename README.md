# docker_deployment_cicd
## when you forget your jenkins login password 
### so go on server 
```
sudo systemctl stop jenkins.service
sudo vim /var/lib/jenkins/config.xml
```
### find this line
<useSecurity>ture</useSecurity>
change to it in 
<useSecurity>false</useSecurity>
### then save file and restart jenkins service
```
sudo systemctl start jenkins.service
```
### then paste http://<your-jenkins-url>/script
### you will see jenkins dont ask you username and password and you see jenkins dashboard 
### then paste this link in new tab
```
https://your_url/script                      ##for example
http://65.2.140.35:8080/script
```
### after that paste this script
```
hudson.model.User.get('mohit').setPassword('12345mg)   ##chaneg in this your username and password
```

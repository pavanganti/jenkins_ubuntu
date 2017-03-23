# jenkins_ubuntu


The cookbook installs Jenkins on the Ubuntu EC2 instance. 

I have created an AWS Chef automate server using the AWS OpsWorks.

The cookbook is uploaded to the Chef automate server using the following command: 
- knife cookbook upload chef_jenkins

I have created an EC2 instance using the AWS Console and bootstrapped the instance to the Chef server using the command:
- knife bootstrap <IP> -N <instance name> --ssh-user ubuntu --sudo --identity-file /Users/anirudh/Documents/chefJenkins/<key pair> --run-list "recipe[jenkins_ubuntu]"

TODO: 
- Use CFT to bootstrap the node to Chef server
- Auto create the user in Jenkins

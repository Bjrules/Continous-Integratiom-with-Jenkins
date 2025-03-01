#### This project is another milestone on my DevOps Journey at darey.io as I succefully impleented t Continous Integration using Jenkings 
#### webhook  is triggered by pushing certain updates made from my local vscode 
#### the AUTOMATION is vscode(commit&push)-> Github(webhook) -> jenkins -> webservers(created earlier in Project7 )

![Alt text](IMG-SCREENSHOTS/Screenshot_20230126_232639.png)
 ubuntu 20.04 was used to create jenkins server 
 
 ![Alt text](IMG-SCREENSHOTS/Screenshot_20230126_232757.png)

![Alt text](IMG-SCREENSHOTS/Screenshot_20230126_232804.png)

![Alt text](IMG-SCREENSHOTS/Screenshot_20230126_232854.png)

installing jdk since jenkins is a java program
![Alt text](IMG-SCREENSHOTS/Screenshot_20230126_232925.png)

Installing jenkins
![Alt text](IMG-SCREENSHOTS/Screenshot_20230126_233251.png)

Jenkins status
![Alt text](IMG-SCREENSHOTS/Screenshot_20230126_233440.png)

![Alt text](IMG-SCREENSHOTS/Screenshot_20230126_233843.png)

remember jenkins runs on port 8080 so I created an inbound rule on my EC2 instance in other to access (view) it on my browser and also copied the default password for jenkins
![Alt text](IMG-SCREENSHOTS/Screenshot_20230126_233953.png)

![Alt text](IMG-SCREENSHOTS/Screenshot_20230126_234008.png)

And so I choose Installed suggested plugin

![Alt text](IMG-SCREENSHOTS/Screenshot_20230126_234114.png)

![Alt text](IMG-SCREENSHOTS/Screenshot_20230126_234136.png)

![Alt text](IMG-SCREENSHOTS/Screenshot_20230126_234142.png)

Registeration with user name and password
![Alt text](IMG-SCREENSHOTS/Screenshot_20230126_234706.png)

![Alt text](IMG-SCREENSHOTS/Screenshot_20230126_235209.png)

Using the parameters(jenkins-server-address/github-webhook/ ) to configure webhooks for github

![Alt text](IMG-SCREENSHOTS/Screenshot_20230202_225535.png)

![Alt text](IMG-SCREENSHOTS/Screenshot_20230203_013049.png)

![Alt text](IMG-SCREENSHOTS/Screenshot_20230203_013057.png)

![Alt text](IMG-SCREENSHOTS/Screenshot_20230126_235221.png)

Started using jenkins
![Alt text](IMG-SCREENSHOTS/Screenshot_20230127_001844.png)

Manual building
![Alt text](IMG-SCREENSHOTS/Screenshot_20230127_093020.png)

![Alt text](IMG-SCREENSHOTS/Screenshot_20230127_112438.png)

![Alt text](IMG-SCREENSHOTS/Screenshot_20230129_115035.png)

![Alt text](IMG-SCREENSHOTS/Screenshot_20230129_115639.png)

Installing the  'PUBLISH OVER SSH' plugin to enable the automation process
![Alt text](IMG-SCREENSHOTS/Screenshot_20230129_115639.png)

![Alt text](IMG-SCREENSHOTS/Screenshot_20230129_115656.png)

Configuration the 'Publish Over SSH' Plugin
![Alt text](IMG-SCREENSHOTS/Screenshot_20230129_120503.png)

you have to scoll to almost the bottom of the page to see the form for configuration
![Alt text](IMG-SCREENSHOTS/Screenshot_20230129_120820.png)

![Alt text](IMG-SCREENSHOTS/Screenshot_20230129_121511.png)

![Alt text](IMG-SCREENSHOTS/Screenshot_20230129_121548.png)

At this point to get the 'success' was not possible until I realise that the plugin 'Publish Over SSH in not compatible with RHEL9 I had to go and recreate  and configure my NFS SERVER with RHEL8 
 
![Alt text](IMG-SCREENSHOTS/Screenshot_20230202_223107.png)

Build artifact over SSH
![Alt text](IMG-SCREENSHOTS/Screenshot_20230202_224820.png)

![Alt text](IMG-SCREENSHOTS/Screenshot_20230202_225517.png)

![Alt text](IMG-SCREENSHOTS/Screenshot_20230203_013123.png)

Wow! it works like magic automatically updated my NFS-SERVER and a chain reaction effect on my webserver.
And so DevOps became even more interesting. this is the techniques for software automated release
Thanks Darey.io




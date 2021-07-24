# miniproject1
TITLE: devOps project.

WHAT AM I DOING : I am trying to work on git; making changes;getting notified...using JENKINS(devOps integration tool) which is deployed on my AWS ec2 instance.

REQUIREMENTS:
- AWS Account
- Amazon ec2 key pair
- GitHub account
- PuTTy Config installed
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------PROCESS :
1) This is a tutorial link to deploy an ec2 instance on your AWS cloud and to deploy and run Jenkins on the ec2 instance using PuTTY Config
https://www.jenkins.io/doc/tutorials/tutorial-for-installing-jenkins-on-AWS/

2) Now install GitHub on your ec2 instance,
- open PuTTY Config
- connect to your ec2 instance
- now first enter into jenkins 
 commands = sudo systemctl start jenkins
 see status using : sudo systemctl status jenkins
- Now download Git by:
 sudo yum install git
 
3) Open your jenkins(after making sure that it's running on your ec2 instance) 
Connect to http://<your_server_public_DNS>:8080 from your favorite browser. You will be able to access Jenkins through its management interface.
Now;
- click on new item >> name it>> create freestyle project
- in general tab>> choose github >> paste your github repository code url (which you would be editing)
- in source management panel >> choose git >> paste the url here also
- in branch specifier >> make it */main (because this is the branch of our github repository)

Now in the Build Trigger panel on jenkins
- check the option of "GitHub hook trigger for GitScam polling"
this option allows me to be notified whenever a developer makes changes in my project.
- click apply and save

4) Finally, return back to your Github Repository that you wanted it to edit and be notified using jenkins.
Now, we need to add a webhook to our Git repository; which would allo external services like jenkins to be notified when certain events happen.To do that :- 
- on your repoitory page >> settings >> webhooks >> add webhook
- on the payload url -> copy the ec2 instance's ipv4 address
- on the option of which events to be notified of -> click the ones you would like to
- click add webhook
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

CONCLUSION:
SO, now if i or some developer makes a change in my repository i will be notified in my Jenkins (on the build panel) tht so and so developer made so and so changes.



THE FOLLOWING IS JUST A TRIAL CHANGES I MADE TO TEST MY PROJECT

the first change that i m doing..!

the second change after adding build step

the third change

fourth change
fifth change

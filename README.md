# CI/CD

## Configuring Jenkins autobuild process with Git repo.

### setting up  jenkins
1. Download jenkins pluging for your machine from https://jenkins.io/.
2. Once downloaded,  install Jenkins in your machine .
3. It will ask to  Unlock Jenkins when localhost opens in your browser(http://localhost:8080). So ,  To ensure Jenkins is    securely set up by the administrator, a password has been written to the log (not sure where to find it?) and this file on the server:

/Users/Shared/Jenkins/Home/secrets/initialAdminPassword

4. Please copy the password from either location and paste it.
5. Next  allow ot to download plugins like:
Folders, OWAS Markup Formatter, Build Timeout ,Credentials Binding ,Timestamper, Workspace Cleanup, Ant ,Gradle, Pipeline ,GitHub, Branch, Source Pipeline: GitHub' Groovy Libraries' Pipeline: Stage View Git Subversion SSH Slaves Matrix Authorization Strategy PAM Authentication LDAP Email Extension Mailer etc.

6. Then, Create First Admin User entering details like:

Username:	
Password:	
Confirm password:	
Full name:	
E-mail address:	

7. Instance Configuration
Jenkins URL:	http://localhost:8080/

8. Now, jenkins is new for new jobs!

### Trigger Jenkins builds by pushing to Github(https://www.fourkitchens.com/blog/article/trigger-jenkins-builds-pushing-github/)

Step 1: Grant your server access to your private Github repository.

You may have Jenkins running on the same machine as your webhost, or they may be on separate machines with Jenkins configured to treat the webhost as a remote node. Either way, you’re going to want to SSH into the webhost and ensure that whichever Linux user Jenkins is building jobs as, can authenticate to Github. We have a robot user called ‘Bender’ exactly for this purpose, so I’ll use that in the examples.

Instead of installing your own private key to the Bender account, create a new set of private/public keys, and then either create a Github user(https://help.github.com/articles/set-up-git/) for Bender or use the Github deploy keys (https://developer.github.com/v3/guides/managing-deploy-keys/)feature. 
Follow the below for setting and ssh to  Github.
 ### How to Install Git on Mac
1. Open a terminal and type

$ brew install git
This will install Git on your system. To confirm the installation, type

$ git --version
This will print the version of Git installed on your machine.

### How to generate SSH key for GitHub authorization
1.Open a terminal
2. Go to your home directory by typing cd ~/
3. Type the following command
$ ssh-keygen -t rsa
4. This will prompt you to enter a filename to store the key
5. Just press enter to accept the default filename (/Users/you/.ssh/id_rsa)
6. Then it will ask you to create a passphrase. This is optional, either create a passphrase or press enter for no passphrase
When you press enter, two files will be created
~/.ssh/id_rsa
~/.ssh/id_rsa.pub
7. Your public key is stored in the file ending with .pub, i.e. ~/.ssh/id_rsa.pub
### How to access and copy public SSH key
In order to authenticate yourself and your device with GitHub, you need to upload your public SSH key which you generated above to your GitHub account.

1.Copy public SSH key

2. Open a terminal and type

3. $ pbcopy < ~/.ssh/id_rsa.pub
This will copy the contents of the id_rsa.pub file to your clipboard.

### How to upload your public SSH key to GitHub
1. Once you have copied your public SSH key, login to your GitHub account and go to
https://github.com/settings/profile
2. On the left-hand side menu, you will see a link “SSH and GPG keys”
3. Click on that link which will take you to a page where you can enter your public SSH key that you copied earlier.
4. Click the button which says ‘New SSH key’
5. Then enter a title name – can be anything, e.g. newMac
6. Paste the public SSH key in the key textbox
7. Click “Add SSH key”
### Test your GitHub authorization:

1. Open a terminal and type

2. $ git clone git@github.com:NautiyalAmit/CI/CD.git
3. It will ask you if you want to continue to connect, type yes
4. If you created a passphrase when you were generating the public key, then it will ask you to enter it.
5. Enter your passphrase and press enter.
6. It will then start to clone the project to your directory.
##### cheers! You are all now set up to use Git and GitHub.


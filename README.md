# CI/CD

## Configuring Jenkins autobuild process with Git repo.

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



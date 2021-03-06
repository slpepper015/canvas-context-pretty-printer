Canvas Pretty Print Utility
============================

This is a handy utility that pretty-prints the Force.com Canvas context in JSON format, with syntax highlighting.  It's useful for debugging information about the current user, org, oauth tokens, etc.  Enjoy!

### How to Build The app locally

    mvn package
    
### First time keystore generation (for local SSL support)

      > keytool -keystore keystore -alias jetty -genkey -keyalg RSA
      Enter keystore password: 123456
      Re-enter new password: 123456
      What is your first and last name?
        [Unknown]:  
      What is the name of your organizational unit?
        [Unknown]:  <Your Org Unit>
      What is the name of your organization?
        [Unknown]:  <Your Org>
      What is the name of your City or Locality?
        [Unknown]:  <Your City>
      What is the name of your State or Province?
        [Unknown]: <Your State> 
      What is the two-letter country code for this unit?
        [Unknown]:  <Your Country>
      Is CN=<Your Name>, OU=<Your OU>, O=<Your O>, L=<Your Locality>, ST=<Your State>, C=<Your Country>?
        [no]:  yes

      Enter key password for <jetty>
	(RETURN if same as keystore password):  
      Re-enter new password: 

### How to Run Canvas locally

    sh target/bin/webapp

### How to invoke app locally

    https:/localhost:8443
    
### Canvas URL

    https://localhost:8443/canvas.jsp
    or on Heroku
    https://<your-heroku-app>.herokuapp.com/canvas.jsp
    
### Canvas Callback URLs
    
    https://localhost:8443/sdk/callback.html
    or on Heroku
    https://<your-heroku-app>.herokuapp.com/sdk/callback.html

### How to push new changes to heroku

      git add -A
      git commit -m "My change comments"
      git push heroku master

### How to get Heroku logs
      
      heroku logs --tail

### Want to clone this application into your org?
   
   If you want to clone this application into your organization as a starting point,
   click on this link: http://spepper-wsl1.internal.salesforce.com:8080/apex/git2canvas?CanvasAppName=Canvas+Pretty+Printer&CanvasDescription=Handy+canvas+application+to+JSON+pretty+print+the+canvas+context&GitRepositoryUrl=git%40github.com%3Aslpepper015%2Fcanvas-context-pretty-printer.git&HerokuAppName=canvas-pretty-print&CanvasUrl=canvas.jsp&LogoUrl=logo.png&IconUrl=icon.png

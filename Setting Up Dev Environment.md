Creating own development environment
=====================================
SSH into the Server
-----
1.	Using Putty or equivalent program, for the address use “firstname@dev1.reelradio.com”. When prompted for the password use “cloud-prime”
2.	Use the command “ssh-keygen” to generate a unique key for your git account to easily access the repositories.
3.	Locate where the “id_rse.pub” file is on the server. Use “cat” to display the generated key file.
4.	Copy the generated key file within your github account.
    + Log into your GitHub account.
  
    + Click your avatar and choose Settings.
  
    + Select SSH and GPG keys.
  
    + Click New SSH key.
  
    + Enter a title in the field.
  
    + Paste your public key into the Key field
  
    + Click Add SSH key.
  
Setting up global variables
------------
1.	Using the command “git config --global user.name 'your name'” set the user.name variable in git for your account.
2.	Using the command “git config --global user.email 'your email'” set the user.email variable in git for your account.
3.	Use the commands “git config user.name” and “git config user.email” to check if the changes have been made.

Setting up development environment
-------------

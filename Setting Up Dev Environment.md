Creating own Development Environment
=====================================
## First Time Set Up
### SSH into the Server
1.	Using Putty or equivalent program, for the address use `firstname@dev1.reelradio.com`. When prompted for the password use `cloud-prime`
2.	Use the command `ssh-keygen`to generate a unique key for your git account to easily access the repositories.
3.  Under `/home/"Name of User"/.ssh` use the command `cat id_rse.pub`
4.	Copy the generated key file within your github account.
    + Log into your GitHub account.
  
    + Click your avatar and choose Settings.
  
    + Select SSH and GPG keys.
  
    + Click New SSH key.
  
    + Enter a title in the field.
  
    + Paste your public key into the Key field
  
    + Click Add SSH key.
  
### Setting up global variables
1.	Using the command `git config --global user.name 'your name'` set the user.name variable in git for your account.
2.	Using the command `git config --global user.email 'your email'` set the user.email variable in git for your account.
3.	Use the commands `git config user.name` and `git config user.email` to check if the changes have been made.

## Setting up a Development Environment
1.	Navigate to `/export/dev`
2.	Clone the dev1 repository by using the command `git clone git@github.com:reelradio/site.git your_name`
3.	Name the repository anything you would like.
4.	When making changes to this development environment use the git command `git branch <branch-name> export/dev/<branch-name>`. After changes are made a pull request will be created under the user who edited the corresponding folder under `/export/dev`
5.	Now you can access `https://"FolderName".dev.reelradio.com/update/sub_server.html` to see how the changes are displayed within the development environment you created.

## Contributing to the Site
1. Instructions for this can be found here: https://github.com/reelradio/site#contributing 

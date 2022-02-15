Creating own Development Environment
=====================================
## First Time Set Up
### SSH into the Server
1.	Using Putty or equivalent program, for the address use `<firstname>@dev1.reelradio.com`
2.	After logging in for the first time, change your password with the command `passwd`
3.	Use the command `ssh-keygen`to generate a unique key for your git account to easily access the repositories.
4.  Under `/home/"Name of User"/.ssh` use the command `cat id_rsa.pub`
5.	Copy the generated key file within your github account.
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
4.	Now you can access `https://"FolderName".dev.reelradio.com` to see how the changes are displayed within the development environment you created.

## Contributing to the Site
1. Instructions for this can be found [here](https://github.com/reelradio/site#contributing) 
2. After making changes, checkout a new branch with `git checkout -b <new-branch-name>`
3. Stage then commit your changes
4. Then type `git push -u origin <new-branch-name>`
5. After your branch is ready, go to GitHub and create a new pull request for your branch

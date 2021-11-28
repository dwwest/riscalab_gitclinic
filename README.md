Welcome to the Risca Lab Github Clinic!

This is a guide to get you started using GitHub to keep track of your code
in the lab.

THE MAIN REASONS TO USE GITHUB ARE:

1) VERSION CONTROL -- This means every time you "push" (or copied savepoint)
your code to GitHub, you will have a record of your code from the 
date and time of that push.  If you break something, you'll be able
to go back and figure out where it is
2) COLLABORATION -- GitHub allows you to work with other users
on larger codebases and resolve issues that may arise from multiple
people working with multiple versions of the code at the same time

HERE IS A LIST OF COMMON GITHUB COMMANDS FOR YOUR REFERENCE:
https://education.github.com/git-cheat-sheet-education.pdf

PART ONE: GETTING STARTED
~~~~~~~~~~~~~~~~~~~~~~~~~

HOW TO MAKE YOUR OWN GITHUB REPOSITORY AND START PUTTING YOUR OWN CODE ON GITHUB

1) Make a Github account here: https://github.com/

2) Configure your ssh keys so your Github account can recongize your computer/
account on the Rockefeller cluster
    a) On the github website, go to "Settings" > "SSH and GPG keys" > "New SSH key"
    b) On your computer or on the cluster, open the command line and run the following command
        cat ~/.ssh/id_rsa.pub
    c) Copy the output and paste into the "Key" window on the GitHub add ssh key page
    and hit "Add SSH Key"

3) On the command line, navigate to the folder you want up on GitHub using the cd command

4) Run the following commands to intialize a git repository
    git init -b main
    git add . $$ git commimt -m "initial commit"

5) 








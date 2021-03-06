Welcome to the Risca Lab Github Clinic!

This is a guide to get you started using GitHub to keep track of your code
in the lab.

THE MAIN REASONS TO USE GITHUB ARE:

1) VERSION CONTROL -- This means every time you "push" (or copy a savepoint)
your code to GitHub, you will have a record of your code from the 
date and time of that push.  If you break something, you'll be able
to go back and figure out where it is
2) COLLABORATION -- GitHub allows you to work with other users
on larger codebases and resolve issues that may arise from multiple
people working with multiple versions of the code at the same time

HERE IS A LIST OF COMMON GITHUB COMMANDS FOR YOUR REFERENCE:
https://education.github.com/git-cheat-sheet-education.pdf

HERE IS AN EXPLANATION OF ALL THE GITHUB TERMS WE'LL BE USING:
https://docs.github.com/en/get-started/quickstart/github-glossary

~~~~~~~~~~~~~~~~~~~~~~~~~

PART ONE: GETTING STARTED
-------------------------

HOW TO MAKE YOUR OWN GITHUB REPOSITORY AND START PUTTING YOUR OWN CODE ON GITHUB

1) Make a Github account here: https://github.com/

2) Configure your ssh keys so your Github account can recongize your computer/
account on the Rockefeller cluster
    a) On the github website, go to "Settings" > "SSH and GPG keys" > "New SSH key"

    b) On your COMPUTER open the command line and run the following command
        cat ~/.ssh/id_rsa.pub

       On the CLUSTER open the command line and run the following commands
        cd ~/.ssh/

       If you have a file called "id_ed25519.pub" run the following command
        cat id_ed25519.pub

       If you don't have a file called "id_ed25519.pub" create it with the following command
        ssh-keygen -t ed25519 -C "<YOUR_GITHUB_EMAIL_HERE>"
        [IT WILL ASK FOR FILENAME DON'T TYPE ANYTHING JUST HIT ENTER]
        cat id_ed25519.pub
        
    c) Copy the output and paste into the "Key" window on the GitHub add ssh key page
        and hit "Add SSH Key"

3) On the command line, navigate to the folder you want up on GitHub using the cd command

4) Run the following commands to intialize a git repository
    git init -b main
    git add . $$ git commimt -m "initial commit"

5) On GitHub, go to your profile page and click the "Repositories" tab and then click "New"

6) Follow the instructions, decide on a name, a description, set the repo to be either public
or private, and for now don't check any of the three boxes at the bottom

7) Copy the line from the Quick setup -- if you've done this kind of thing before

8) Run the following commands from the command line
    git remote add origin <PASTE THE LINE YOU JUST COPIED IN STEP 7 HERE>
    git push --set-upstream origin main

9) That's it!  Go to your profile and your repo should be there!

~~~~~~~~~~~~~~~~~~~~~~~~~
~~~~~~~~~~~~~~~~~~~~~~~~~

PART TWO: MAKING CHANGES
------------------------

HOW TO MAKE CHANGES TO THE REPOSITORY YOU CREATED

1) For the repo you just created, we're going to practice an add, commit, and push.  This
will make changes in your project and share those changes with the remote version
on GitHub.  First, Make some small change to your code, or add a file to this repo

2) On the command line, navigate to the top-most directory of your repo

3) Run the following commands
    git add .
    git commit -m "<WRITE A MESSAGE ABOUT WHAT YOU CHANGED>"
    git push

4) Go to the GitHub website and you'll be able to see the commit has been added.
Click through your commits and see how you can keep track of what lines have been changed.

~~~~~~~~~~~~~~~~~~~~~~~~~
~~~~~~~~~~~~~~~~~~~~~~~~~

PART THREE: COLLABORATING WITH OTHERS
-------------------------------------

HOW TO MAKE CHANGES AND MANAGE CONFLICTS WHEN CODING WITH A GROUP

Now, we're going to learn how to handle merge conflicts!  For this, I'm going
to create an issue so that you learn what to do when you're trying to push to 
a repo that has changes in it that you don't have in your own.

1) First, download VS Code or some other code editor.
https://code.visualstudio.com/

2) cd to directory where you want to put this repository.

3) On GitHub, go to this link: https://github.com/dwwest/riscalab_gitclinic and copy 
the text from the drop down menu that comes up when you hit the Code button.  Make sure
that you are set to ssh key and not https.

4) git clone <copied line>

5) Open VS code and then open names.txt and add your name.

6) Ask me (verbally) to add you as a collaborator on this repo.

7) When it pops up, accept my invitation to the repo.

8) WAIT -- I am going to push something to this repo create a conflict.

9) Follow number 3) of PART 2 to try to push your name.

10) You will get an error that says failed to push some refs.

11) In order to merge your changes with my changes, do git pull

12) Open with code editor and accept both changes.  Then, delete duplicate
    names.  We want everyone in the lab's name on here!

13) Follow PART TWO step 3) again to push

14) You will get another merge conflict if you are doing this clinic
with multiple other people.  If you are the lucky duck whose push got through first,
congrats, you're done!  If not, repeat steps 11-13 until your push is successful. 

~~~~~~~~~~~~~~~~~~~~~~~~~







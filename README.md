Skip to content
Search or jump to…
Pull requests
Issues
Marketplace
Explore
 
@krnv1 
krnv1
/
25July-Batch-DevOps-Notes
Public
forked from Sonal0409/25July-Batch-DevOps-Notes
Code
Pull requests
Actions
Projects
Wiki
Security
Insights
Settings
Update Git-Notes
 main
@Sonal0409
Sonal0409 committed 2 minutes ago 
1 parent b0b1ad4 commit 99bfa9612cb0638f4137efe43c5841fae8f275b1
Showing 1 changed file with 214 additions and 0 deletions.
 214  
Git-Notes
@@ -1 +1,215 @@



to become a super user, which can downloa dand install packages

1.  sudo su -

To install git:

 $ yum install git -y


 mkdir myprojects
 cd myprojects
 touch index1.html
 ls

Intsialise git 
  git init
  ls -al

.git folder will be there

Scenario 1:
***********

Check if git is tracking you files or not in the workspace


git status


git add filename ==> single file

git add file1 file2 ==>  will add 2 files

$ git add . ==> all the files will be stagged

$ git commit -m "message " ==> all the chnages & files will be commited

Scenario 2: git config
*******************

$ git config --global user.name sonal0409
$ git config --global user.email mittal.sonal04@gmail.com

To see the list of configurations:

 git config --list


Scenario 3: log in git
******************

 git log

 git log --oneline

 git show <commitid> ==> show all the details of the changes that have been commited

100644

 644  ==> current user ==> read and write permsision = 6
      ==> group users ==> read permission = 4
      ==> user ==> read permssion

chmod 666 filename

Scenario 4: How modified files with changes can be commited to Local repository
*********************

Take a file that is already committed OR which is already tracked by git

In this case no need to explicitly execute add command, you can directly commit all the changes using the command

   $ git commit -a -m "modified file" 

 - a  : take all the modified files or stagged files and commit them all


vim index1.html

press i

enter data

save the file:

press ESC key on keyboard

then enter the keys :wq! 

press enter key




Scenario 5: Delete a file and commit the changes to Local repo



Step 1: take an exisitng file and delete it 

 git rm newfile1  ==> delete file from LR & Working directory

Step 2: Check status of git, you will deleted file or change is stagged

you need to commit

 git commit -m "deleted file"

See the log

 $ git log --oneline


Scenario 6: revert the changes to its previous state

Select the required commit id

$ git log --oneline

see what happened in  that commit

$ git show 5f62be1   

Lets revert the commitid

whatever was commited, will go back to its previous state

 $ git revert <commitid>

When the above command is executed, 
git will open an editor for you, 
where you have to put a message as to why are your reverting
AND
git will perform revert action and generate a commit id for it

Expected :  file should be back to LR & WD

Scenario 7: Push the changes from LR to Github


Steps to create personal Access token

Personal access tokens function like ordinary OAuth access tokens. They can be used instead of a password for Git over HTTPS, 
or can be used to authenticate to the API over Basic Authentication.

 Go to settings of the github account
 Scroll down and click on developer settings on the left
 on the left side click on personal access token
 Click on generate token
 > in Note give a unique name of token
 > expiration 30 days
 > scope ==> select repo




























































0 comments on commit 99bfa96
@krnv1
 
Leave a comment
No file chosen
Attach files by dragging & dropping, selecting or pasting them.
 You’re not receiving notifications from this thread.
Footer
© 2022 GitHub, Inc.
Footer navigation
Terms
Privacy
Security
Status
Docs
Contact GitHub
Pricing
API
Training
Blog
About

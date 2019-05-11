# Git Details
**What is GIT ?**  
Git is an Open Source Distributed Version Control System. Now that’s a lot of words to define Git.  

Let me break it down and explain the wording:  

**Control System:** This basically means that Git is a content tracker. So Git can be used to store content — it is mostly used to store code due to the other features it provides.  
**Version Control System:** The code which is stored in Git keeps changing as more code is added. Also, many developers can add code in parallel. So Version Control System helps in handling this by maintaining a history of what changes have happened. Also, Git provides features like branches and merges, which I will be covering later.  
**Distributed Version Control System:** Git has a remote repository which is stored in a server and a local repository which is stored in the computer of each developer. This means that the code is not just stored in a central server, but the full copy of the code is present in all the developers’ computers. Git is a Distributed Version Control System since the code is present in every developer’s computer. I will explain the concept of remote and local repositories later in this article.
## Why a Version Control System like Git is needed  
Real life projects generally have multiple developers working in parallel. So a version control system like Git is needed to ensure there are no code conflicts between the developers.  

Additionally, the requirements in such projects change often. So a version control system allows developers to revert and go back to an older version of the code.  

Finally, sometimes several projects which are being run in parallel involve the same codebase. In such a case, the concept of branching in Git is very important.  
  
  

## Let me summerize in my own language  
  
Before GIT, developers used to save the project in their hard disk or in server. WHen they want to share the code, that ussualy done by sharing the whole zip file.  
    
Which is not feasible at all  
In a complex project, lots of developers works in different features. Its very hard to share their own code for the particular project to other developers.   
  
Which is hard to maintain the version and code.  

TO overcome this, GIT came into picture  
  
## Here is the steps how to get start with git  

Download Git for your specific os (Mac,Windows,Linux) from the below link  
https://git-scm.com/downloads  
  
After successfull installation, Open git bash commandline  
TO check version of your git installed in system  

 
To add git to any project , just initialize git inside the project folder  
redirect to The project  

Before move to commands details, lets see the folder structure of git internally  
![alt tag](https://github.com/spdobest/GithubDemo/blob/master/git_structure.png)  

## Some basic Git commands are:## 

**git --version** To print the installed git version  
**git init** It will initialize git and create .git filder in root directory  
### First setup the user in command line for the repository ###  
**git config --global user.name USER_NAME** it will set user name  
**git config --global user.email USER_EMAIL**  
**git config --global --list**  --(To check the user list for the repository in your system )  
Clone the Project now    
**git clone "ENter project repository which ends with .git"**  

**git status** --(It will print the branch name and all the new and edited files which not added)  
**git add filename** --(It will add the particular file)    
**git add .** --(It will add all the newly added and edited files to .git folder)  
**git commit**** --(It will open an edotor to enter commit message with multiline)  
**git commit -m "Your Commit Message"**  --(It will commit directly without opening an;y new window)  
**git push origin branchname** --It will push the code to the repository in web to the branch name  
**ls al** --it will print all the files including . files in console  
**git ls-files** --it will print the files in the git  
  
Now create multilevel folder like this level1/level2/leve3  
**mkdir -p level1/level2/level3**  
create a file in level1  
**git add filename**(This file is added to staging now) 
**Now you want to remove the file**  
**git reset HEAD filename** it will remove that file from from staging  
**Now you have changed something in a file and committed the code, but you want the code from the last commit**  
**git checkout --filename** -- it will put the file committed in the last commit  
  
### Renaming and Moving Folder ###  
**git mv filename1.txt filenameNew.txt** --it will change the file name to filenameNew
**git mv filenameNew.txt filename1.txt** --Now you want to revert back the changes   
### Deleting file ###  
**git rm filename** -- it will delete the file, now git will not track the file  
after deleting when you check the status, it will show **deleting FIle**  
once you commit , it will not track the file 
**git reset HEAD filename** --if you want to put the file back to staging and want to track 
**git add -A** -- if you deleted a file manually and did not commit, you can get the file back by the following command  
**rm -rf folderName** --it will delete the folder  
### Git Alias ###  
when you dont to type a long git command, you can make alias (short name) for the command and store in git config file locally. It can only applicable inside the folder where you put the alias name  
**git log --all --graph decorate --online** --it will show the log with more details  
Now you dont want to type this command everytime  
**git config --global alias.hist "YOur command"** --now instead of long command you can use git hist  
**Example**  
git config --global alias.hist "git log --all --graph decorate --online"
now git hist will do the same task as above  
**YOu can see where the command stored, open ~/.gitconfig, you can see the command**  
### Git Ignore ###  
sometime we need to ignore some file not to track by the git  
Create a file .gitignore in root directory


```
pwd (To print the current directory path in command line) 

git init (This will create a .git folder in root directory of your project)  

```
 
 
 
 
 
 

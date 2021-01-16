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

# Some basic Git commands are:

## git config
- This command sets the author name and email address respectively to be used with your commits.
- Usage: git config –global user.name “[name]”  
- Usage: git config –global user.email “[email address]”  
## git init
- This command is used to start a new repository.
## git clone
- This command is used to obtain a repository from an existing URL.
- git clone [url]  
## git add
- This command adds one or more to the staging area.
- git add [file]
- git add . (to add all the changed files)
## git commit
- Usage: git commit -m “[ Type in the commit message]” 
- Usage: git commit -a  
- This command commits any files you’ve added with the git add command and also commits any files you’ve changed since then.
## git diff
- Usage: git diff  
- This command shows the file differences which are not yet staged.
- Usage: git diff –staged 
- This command shows the differences between the files in the staging area and the latest version present.
- Usage: git diff [first branch] [second branch]  
- This command shows the differences between the two branches mentioned.
## git reset
- Usage: git reset [file]  
- This command unstages the file, but it preserves the file contents.
- Usage: git reset [commit]  
- This command undoes all the commits after the specified commit and preserves the changes locally.
- Usage: git reset –hard [commit]  
- This command discards all history and goes back to the specified commit.
## git status
- Usage: git status  
- This command lists all the files that have to be committed.
## git rm
- Usage: git rm [file]  
- This command deletes the file from your working directory and stages the deletion
## git log
- Usage: git log  
- This command is used to list the version history for the current branch.
- Usage: git log –follow[file]  
- This command lists version history for a file, including the renaming of files also.
## git show
- Usage: git show [commit]  
- This command shows the metadata and content changes of the specified commit.
## git tag
- Usage: git tag [commitID]  
- This command is used to give tags to the specified commit.
## git branch
- Usage: git branch  
- This command lists all the local branches in the current repository.
- Usage: git branch -d [branch name]  
- This command deletes the feature branch.
## git checkout
- Usage: git checkout [branch name]  
- This command is used to switch from one branch to another.
- Usage: git checkout -b [branch name]  
- This command creates a new branch and also switches to it.
## git merge
- Usage: git merge [branch name]  
- This command merges the specified branch’s history into the current branch.
## git remote
- Usage: git remote add [variable name] [Remote Server Link]  
- This command is used to connect your local repository to the remote server.
## git push
- Usage: git push [variable name] master  
- This command sends the committed changes of master branch to your remote repository.
- Usage: git push [variable name] [branch]  
- This command sends the branch commits to your remote repository.
- Usage: git push –all [variable name]  
- This command pushes all branches to your remote repository.
- Usage: git push [variable name] :[branch name]  
- This command deletes a branch on your remote repository.
## git pull
- Usage: git pull [Repository Link]  
- This command fetches and merges changes on the remote server to your working directory.
## git stash
- Usage: git stash save  
- This command temporarily stores all the modified tracked files.  
- Usage: git stash pop  
- This command restores the most recently stashed files.
- Usage: git stash list  
- This command lists all stashed changesets.
- Usage: git stash drop  
- This command discards the most recently stashed changeset.

# Git Merge

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

### MVirtual Merge or Diff toll installation ###
U can use p4Merge visual merge tool and the setup are below  
Download P4merge tool from internet  
https://www.perforce.com/products/helix-core-apps/merge-diff-tool-p4merge

Download and install into your system  
**P4merge Configure to any command prompt(Windows)**  
open git bash  
type p4merge in bitbash -- you will get error  
Lunch p4Merge application in your system  
open p4Merge in the program file  
copy the path and set the ENvironment variable as above path    
set path = the path of p4merge  
P4merge Configure to any command prompt(MAC)  
go to the installation path of p4merge in mac
open  git bash , using config set the diff tool as below  
**git config --global merge.tool p4merge**  

**git config --global mergetool.p4merge.path "installation path/p4merge.exe"  
  
### Comparison  ###  
Sometime we need to compare the changes in a file between the commits and between branches and also local to remote.  
In this we can use **git diff** command   
**git diff HEAD** --Difference between the working directory to the last commit  
**git difftool diff HEAD** -- it will show a graphical window to show diference  
**git diff --staged HEAD** -- Comparison between staging and Repository HEAD  
**dit difftool --staged HEAD**-- Graphical presentation of above command  
Comparison of a current file with its last commit  
**git diff --fileName** -- it will compare a files changes  
**git difftoll --fileName** -- Graphical presentation of above commnad  

### Comparison Between 2 commits ##  
**git log --online**  show history with message  
**git diff COMMITID HEAD** -- It will show all the difference to the last commit with the commit ID  
**git diff HEAD HEAD^** -- Comparison between last commit and its previous commit  
**git diff COMMITID1 COMMITID2** -- difference between 2 commits  
**git difftoll  COMMITID1 COMMITID2** -- Graphical presentation of above command  
  
### Branching and Merging ###  
  
**git branch -a** -- it will list both local and remote branches 
**git branch** -- It will show the current branch  
**git branch NEW_BRANCHNAME -a** -- it will create  a local branch  
**git checkout BRANCHNAME** -- Switch to new branch name  
**git log --online --decorate** -- Details of all commits in al the branches  
**git branch -m Branchname1 branchname2** -- it will 
the branch  
**git branch -d bRANCH_NAME**  --  It will delete the branch  
**git checkout -b branchName** -- It will create a new branch and switch to that branch  
**Merging**  
Before commit , always check the difference between the 2 branches  
**git diff master newBranch**  
**git merge SOURCEBRANCH**  -- Merge the source branch to the current branch  
**git commit -am "Message"** -- One line message  
### Rebase ###  


### STASH ###  


### TAG ###  

  
 ## SOME OTHER USEFUL COMMANDS ##  
 
To setup First time url  
git init  
git remote add origin https://github.com/xxx/yyy.git  
git add .  
git commit -m "first commit"  
git push -u origin master  
To see the existing URL just do:  
git config remote.origin.url  
  
TO see the Existing URL   
git config remote.origin.url  
To change the remote url  
git config remote.origin.url https:github/newgithublink  
Remove Remote Url  
git remote rm  
git remote add    
git remote set-url    
git remote help  
  
git add .   
git commit -m”commit message”  
git push origin master branchName  
git branch  
git checkout new_branch_name  
  
Git config --system --unset credential.helper  
git log  
git diff  
git ignore  
  
refusing to merge unrelated histories  
git pull origin branchName --allow-unrelated-histories  
  
git branch  
git remote  
git branch  
to set up user  
$git config --global user.name [your username]  
$git config --global user.email [your email]   

  
git config remote.origin.url https://github.com/spdobest/CleanArchitecture.git  
  
To setup First time url  
git init  
git remote add origin https://github.com/xxx/yyy.git  
git add .  
git commit -m "first commit"  
git push -u origin master  
To see the existing URL just do:  
git config remote.origin.url  

TO see the Existing URL   
git config remote.origin.url  
To change the remote url  
git config remote.origin.url https:github/newgithublink  
Remove Remote Url  
git remote rm  
git remote add  
git remote set-url  
git remote help  
  
**git squash**  
**git reset**  
**git push --set-upstream origin master**  
**git show-branch** - It will show the diffference between the branches  
**
  
Github writing tricks  
 https://help.github.com/articles/basic-writing-and-formatting-syntax  
   
## DELETE.  
- How to Delete Local Branch
git branch -d test
- How To delete Remote Branch
git branch -a 
git push origin --delete test. 
**2.Delete the old-name remote branch and push the new-name local branch.**    
```
git push origin :old-name new-name
```
**3.Reset the upstream branch for the new-name local branch.**  
Switch to the branch and then:   
```
git push origin -u new-name
```
## RENAME BRANCH
**1. Rename your local branch.**.   
If you are on the branch you want to rename:  
```
  git branch -m new-name
```    
If you are on a different branch:  
```
git branch -m old-name new-name
```  


Merge preserves history whereas rebase rewrites it.  
  
git checkout -b branchName  
  
git add .   
git commit -m”commit message”  
git push origin master branchName  
git branch  
git checkout new_branch_name  
  
How to download specific repositiry which have access to your used ID  
git clone https://<USERNAME>:<PASSWORD>@github.com/path/to/repo.git  
Set the url in github  
git remote set-url origin https://<USERNAME>:<PASSWORD>@github.com/path/to/repo.git  
  
https://www.shellhacks.com/git-config-username-password-store-credentials/  
  
git config --global --edit  
  
Set a Git username:  
$ git config --global user.name "Mona Lisa"  
  
To see the git details (user name details)  
git config --list --global  
  
To see the details of the repository  
git remote show origin  
  
To remove the last commit from git, you can simply run  
git reset --hard HEAD^  
If you are removing multiple commits from the top, you can run   
git reset --hard HEAD~2   
to remove the last two commits  
  
Now if we want to just undo commit without any other changes, we can use  
git reset --soft HEAD^  
  
git reset HEAD@{1}  
  
Git config --system --unset credential.helper  
git log  
git diff  
git ignore  
  
refusing to merge unrelated histories  
git pull origin branchName --allow-unrelated-histories  
  
git branch  
git remote  
git branch  
to set up user  
$git config --global user.name [your username]  
$git config --global user.email [your email]  
  
git config remote.origin.url https://github.com/spdobest/CleanArchitecture.git  
  
To setup First time url  
git init  
git remote add origin https://github.com/xxx/yyy.git  
git add .  
git commit -m "first commit"  
git push -u origin master  
To see the existing URL just do:  
git config remote.origin.url  
  
TO see the Existing URL   
git config remote.origin.url  
To change the remote url  
git config remote.origin.url https:github/newgithublink  
Remove Remote Url  
git remote rm  
git remote add  
git remote set-url  
git remote help  
  
Git sa github_url  
Git pull origin mastegit push origin master  
  
Github writing tricks  
 https://help.github.com/articles/basic-writing-and-formatting-syntax  
  
for example, git c server as all the operation based on server  
Decentralized : All operations are local and there is no centralized server for this  
  
GIT : Distributed versin control system , not require to make it centralized  
  
Key COncept  
Repository contains all files, history, config managed by git  
3 stages of git  
Working Directory - it contains all code in local  
Staging Area - Queueing up the changes for the next commit  
Repository(.git folder) - This file contains all the history  
  
Remote - Master Branch  
  
git version - to know the version installed  

Project set up  
pwd - to print path of current directory u r in  
  
First set up the user in command line for the repository  
git config  --global user.name USER_NAME l  
git config  --global user.email USER_EMAIL  
to check  
git config --global --list    => it will print the list of users  
Clone the project now  
Copy the url  
git clone GitHub_url  
it will create .git directory in the path  
git status => it will show the branch name and the files to commit  
Create a file using command line in mac  
echo "Quick underrating of git" >> start.txt  
cat start.txt => to print the content  
git add name_of_the_file  
git commit -m "Message"  
As of now the file is still in the local directory not in the Remote  
git push origin master => it will push the code to repository  
It will ask for username and password  
   
git version  
git config --global user.name "Abe Lincoln"  
git config --global user.email "mrabe@git.training"  
git config --global --list  
git clone github-https-url # paste in your GitHub HTTPS clone URL ls  
cd github-demo  
ls  
git status  
echo "Test Git Quick Start demo" >> start.txt  
ls  
cat start.txt  
git status  
git add start.txt  
git status  
git commit -m "Adding start text file"  
git status  
git push origin master  
  
Create project from fresh  
Git init project_name  
Cd project_name  
ls  
Ls -al  
Git status  
Git add file_name   ( to add the specific file)   
Git add .  (To add the files)   
Git commit ( it will open another editor to put ur messages)   
Cmd + s  
Cmd + w  
Commit -m  "message"  
  
There few files we can ignore  
For that,  just visit the site and select the. Files u want to ignore   
Www.initializer.com  
  
Download the file  
Unzip path/zipfile.zip  
Mv oldname new name  
  
Set up in an existing project  
Git init   
## CherryPick
- git cherrypick commit_number ( It will pick the changes of the CommitNumber and add to the current branch) 
## Squash (To merge all older Commit messages into one message)
- git rebase -i head~2   (that means you want to include the last 2 commits and combine them to one commit)
- Once done, just replace pick with squash instead of the top commit
- then save and
- git push origin -f



 
 
 
 
 

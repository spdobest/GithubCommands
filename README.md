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

git --version 

To add git to any project , just initialize git inside the project folder  
redirect to The project  
Before move to commands details, lets see the folder structure of git internally 

Some basic Git commands are:
```
git init 
git status
git add   (It will add all the newly added files to .git folder)
git commit (It will open an edotor to enter commit message with multiline)
git commit -m "Your Commit Message"  (It will commit directly without opening an;y new window)

```
 
 
 
 
 
 

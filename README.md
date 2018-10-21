# GitHub Tutorial

_by Irene Chen_

---
## Git vs. GitHub

**_What is GIT?_**  
Git is a software where you can keep track of your changes.  
Git keeps "screenshots" of your code or version control. 

**_What is Github?_**  
Github is a cloud or website that stores your code.  
Github is where you can easily collabrate on the same file.  

**Github requires git while git doesn't require github.**

---
## Initial Setup

**_Don't have a github account?_**  
[Go to the Github sigh up page](https://github.com/) to sign up.

**_What is an SSH key?_**  
SSH stands for **S**ecure **SH**ell.  
SSH Key is use to let the computer know that you are the owner of the account.  

**_Why should we perfer SSH Key over HTTPS?_**  
HTTPS is use the same way as SSH key.  
But the difference is that HTTPS will make you enter your github account information everytime.

---
## Repository Setup

**_How to set up a new repository in github?_**  
1. On you github home page, on the upper right corner, you should see a "+" 
2. After you click the "+", you should see **New Repository**. This will allow you to create a new repository (repo).
3. Fill out the title of the repo. (Remember that when naming the space should be repace by a "-" and no capital letters.)
4. Click **Create Repository**.
5. You'll see a **Quick Setup** section. Make sure the link is in SSH key formate. NOT HTTPS. 

---
**_Setup on Cloud 9 (c9)_**
1. Login to your c9 account. Make sure you're in workspace right now.
2. Make a new folder and name it the same thing you name for the repo in github ```mkdir filename```
3. Move into this the folder ```cd filename``` and make a new file call README.md ```touch filename```
4. type ```git init``` in the new folder. **Never make use ```git init``` in your workspace**
5. type ```git add README.md``` 
6. type ```git commit -m "make README.md"``` 
7. go back to github and click the clipboard to copy. 
8. type ```git remote add origin git@github.com/username/....git``` in your terminal
9. Finally, type ```git push -u origin master```

**IF YOU ARE CONFUSE WHY WE USE THESE COMMANDS, SCOLD DOWN TO FIND WHY**

---
## Workflow & Commands
_Here are the basic understanding of Git_  

**_WORKING DIRECTORY_**-
where you will do all the work: creating, editing, deleting, and organize files

**_STAGING AREA_**- 
where you'll list changes you made to the working directory 

**_A REPOSITORY_**- where Git permanently stores those changes as different versions of the project

---
### ```GIT INIT```
* How to type: ```git init```
* The word init means _initalize_.
* This command will set up all the tools Git needs to begin tracking changes made in the project.

---
### ```GIT STATUS```
*  How to type: ```git status```
*  This command will let you check the status of the changes
* Untracked files means Git sees the file but hasn't start tracking any changes yet.

---
### ```GIT ADD```
* How to type: ```git add <insert filename>```
* In order for Git to start track any file, you need to add it to the stage area
* filename refers to the file you had modify (change)
---
* How to type: ```git add .```
* This command only add all new or modified file.
* It will not add deleted or rename ones  
---
* How to type: ```git add --all```
* This command will add all changes to the staging area, including the renamed and deleted ones

---
### ```GIT COMMIT```
* How to type: ```git commit -m <insert message>```
* A _commit_ permanently stores the changes from the staging area into the repository. 
* The message has to be short, describing what has change since the last commit. 
* -m is an option for _git commit_

---
### ```GIT PUSH```
* How to type: ```git push -u origin master```
* This command is use when you push the first time.
* This command help us sent all our commit into our local in c9 to our remote in github.
* origin is where it will push to. 
* master is where the "main" branch of our project is.
* -u is where it will tell git to remember where it will push to. Without -u you'll have to type ```git push origin master``` everytime you want to push
---
* How to type: ```git push```
* After the first time, we can just type in this command and git will remember to push to origin master.

---
## Rolling Back Changes
_There are many time where we make a mistake. Here are some commits that you can use to undo._

### ```GIT CHECKOUT --<FILENAME>```  
* How to type: ```git checkout --<filename>```
* This command is use to undo edits in the staging area. 
* You can find this command in ```git status``` after you edited it. 
* Outcome: Your changes from the last commit to now will be deleted in the staging area.
---
### ```GIT RESET HEAD <FILENAME>```
* How to type: ```git reset HEAD <filename>```
* This command is use to unstage the files from the staging area.
* You can find this command in ```git status``` where it is green meaning it is added to the stage area
* Outcome: In ```git status``` it will become red meaning the changes hasn't been add
---
### ```GIT RESET --SOFT HEAD~1```
* How to type: ```git reset --soft HEAD~1```
* This command is use to undo commit 
* Outcome: In ```git log``` you can see all your commits. After using this command, you can see that your most recent commit isn't listed.
---
### ```GIT RESET HEAD~1```
* How to type: ```git rest HEAD~1```
* This command undo the most recent commit and unstage the file. 
---
### ```GIT RESET --HARD HEAD~1```
* How to type: ```git reset --hard HEAD~1```
* This command undo the most recent commit, unstage the file, AND undo the edits in the file.
---
### ```GIT REVERT SHA```
* How to type: ```git revert [insert SHA]```
* This command undo the push of the commits.
* SHA is a series of number that can be found in ```git log``` next to the commits.
---  
## Collaboration
**_What is the difference between clone and fork?_**
Cloning a repo is making the same copy of the other person's repo.
Forking a repo is like cloning, but you are making a new remote from the same copy. In order word, remix.

**_How to clone another person's repo?_**
1. In the github page of the other person, click the **clone or download** green button. 
2. Copy the link. (make sure it's in SSH instead of HTTPS)
3. In c9, type ```git clone [SSH url]```

**_How to fork another person's repo?_**
1. In the github page of the other person, click the **Fork** button on the upper right corner.
2. You will see the same exact repo, but with you username instead of the other person.
3. Copy this repo into your c9.
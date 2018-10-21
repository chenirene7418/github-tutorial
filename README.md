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
* The word init means _initalize_.
* This command will set up all the tools Git needs to begin tracking changes made in the project.
* How to type: ```git init```

---
### ```GIT STATUS```
* This command will let you check the status of the changes
* Untracked files means Git sees the file but hasn't start tracking any changes yet.
* How to type: ```git status```

---
### ```GIT ADD [filename]```
* In order for Git to start track any file, you need to add it to the stage area
* filename refers to the file you had modify (change)
* How to type: ```git add <insert filename>```

---
### ```GIT ADD .```
* This command only add all new or modified file.
* It will not add deleted or rename ones
* How to type: ```git add .```

---
### ```GIT ADD --ALL```
* This command will add all changes to the staging area, including the renamed and deleted ones
* How to type: ```git add --all```

---

---
## Rolling Back Changes

---  
## Collaboration
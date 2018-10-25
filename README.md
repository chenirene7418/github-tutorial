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
1. [Go to the Github sigh up page](https://github.com/) to sign up.
2. In step 1, fill out your information and then click **Create an account**
3. In step 2 of choosing our own plans, choose **Unlimited public repositories for free**
4. In step 3, talior your experience
5. Finally, go to your email and verify. 
---
**_What is an SSH key?_**  
SSH stands for **S**ecure **SH**ell.  
SSH Key is use to let the computer know that you are the owner of the account.  

**_Why should we perfer SSH Key over HTTPS?_**  
HTTPS is use the same way as SSH key.  
But the difference is that HTTPS will make you enter your github account information everytime.

**_How to setup a SSH Key?_**
1. In c9, go to the setting's button on the upper right corner 
2. Then click **SSH Keys** 
3. Copy the code that is under **Connect to your private git repository**
4. Go to your github and click your profolio icon
5. Click the setting button 
6. In the sidebar, click **SSH and GPS keys**
7. Then click **New SSH key**
8. Then paste what you copy in c9. (The long code)
9. Click **Add SSH key**
10. Type in your password for github if they tell you to confirm. 

---
## Repository Setup

**_How to set up a new repository in github?_**  
1. On your github home page, on the upper right corner, you should see a "+" 
2. After you click the "+", you should see **New Repository**. This will allow you to create a new repository (repo).
3. Fill out the title of the repo. (Remember that when naming the space should be repace by a "-" and no capital letters.)
4. Click **Create Repository**.
5. You'll see a **Quick Setup** section. Make sure the link is in SSH key formate. NOT HTTPS. 

---
**_Setup on Cloud 9 (c9)_**
1. Login to your [c9 account](https://aws.amazon.com/cloud9/?origin=c9io). Make sure you're in workspace right now.
2. Make a new folder and name it the same thing you name for the repo in github ```mkdir filename```
3. Move into this the folder ```cd filename``` and make a new file call README.md ```touch filename```
4. type ```git init``` in the new folder. **Never make use ```git init``` in your workspace**
5. type ```git add README.md``` 
6. type ```git commit -m "make README.md"``` 
7. go back to github and click the clipboard to copy. 
8. type ```git remote add origin git@github.com/username/....git``` in your terminal
9. Finally, type ```git push -u origin master```

**IF YOU ARE CONFUSED ON WHY WE USE THESE COMMANDS, SCROLL DOWN TO FIND OUT WHY**

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
* filename refers to the file you had to modify (change)

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
* This command help us send all our commit into our local in c9 to our remote in github.
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
In forking, you have permission to _push_, but not in cloning because the remote isn't yours.

**_How to clone another person's repo?_**
1. In the github page of the other person, click the **clone or download** green button. 
2. Copy the link. (make sure it's in SSH instead of HTTPS)
3. In c9, type ```git clone [SSH url]```

**_How to fork another person's repo?_**
1. In the github page of the other person, click the **Fork** button on the upper right corner.
2. You will see the same exact repo, but with you username instead of the other person.
3. Copy this repo into your c9.

**_What is a pull request?_**  
A pull request is when you want to suggest any changes you made in your fork repo to the original repo.

**_How do you pull request?_** 
1. First fork someone else's repo
2. Then you clone your fork repo to c9
3. After making your changes (add and commit), push 
4. In github, click **Pull Request** in the repo header
5. Enter a title and description about what you did
6. Click the **Send pull request** green button 
7. Then wait until your pull request is approved or declined
8. If the original owner of the repo likes your request, they will use ```git pull``` to see your changes in their repo. 

---
## Error Handling  
**_What if you accidently initialize in your workspace?_**  
Solution: ```rm -rf .git```  
This command will undo your git that is running.

**_How do you know if git is running?_**  
There is two ways:
1. ```ls --al``` will show all the hidden files. If you see **git**, then git is running.
2. If you go into your folder (hint: use ```cd <filename>```) and see _(master)_ in your terminal, it means it is running.

**_How do you remove a repository (local and remote)?_**  

**C9 (local)**  
1. In c9, don't go into the file or folder. Stay in the mother-folder (the folder above the repo folder)
2. Type ```rm -rf <filename>``` This will force the folder to be deleted.

**Github (remote)**
1. In your github repo, click **setting** in the repo header
2. Scold down to the **Danger Zone** 
3. Then click **Deleted this repository**
4. Type in your title of this repo and confirm to delete your repo.
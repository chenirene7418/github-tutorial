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

**Don't have a github account?**  
[Go to the Github sigh up page](https://github.com/) to sign up.

**What is an SSH key?**  
SSH Key is use to let the computer know that you are the owner of the account.  

**Why should we perfer SSH Key over HTTPS?**  
HTTPS is use the same way as SSH key.  
But the difference is that HTTPS will make you enter your github account information everytime.

---
## Repository Setup

**How to set up a new repository in github?**  
1. On you github home page, on the upper right corner, you should see a "+" 
2. After you click the "+", you should see **New Repository**. This will allow you to create a new repository (repo).
3. Fill out the title of the repo. (Remember that when naming the space should be repace by a "-" and no capital letters.)
4. Click **Create Repository**.
5. You'll see a **Quick Setup** section. Make sure the link is in SSH key formate. NOT HTTPS. 

**Setup on Cloud 9 (c9)**
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



---
## Rolling Back Changes
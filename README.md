# GitHub Tutorial

_by Cheyenne Nicaisse_

---
## Git vs. GitHub
The difference between git and github is git takes snapshots of code and doesn't need github but **github needs git**.  
Github stores all of the code/snapshots in the cloud. 


---
## Initial Setup
##### To make a github account:  
1. first you go to [github.com](github.com).  
2. Next, you go to the top right of the screen and click "sign up". 
3. Then you fill in the information required. ![image](https://snag.gy/Aykn39.jpg)
4. Github will then ask you for a plan and you click the free plan and move on to the third and final step.
5. The third and final step is optional where github wants to learn more about you and your experience. You can either fill it out or skip this step. 
6. Now when you go to [cloud 9](c9.io), you can easily log in with your github account

##### In cloud 9 to make a new workspace to fit with git projects:
1. First after you log into cloud 9 with github, you press new workspace.
![image](https://snag.gy/LMxCWZ.jpg)
2. Then you type in a name and a description for your workspace (preferably one that relates to git).
3. Next you click public to make your workspace viewable to everyone.
4. Then you choose Blank as your template.
5. After all that is done, you click create workspace. 


---
## Repository Setup



---
## Workflow & Commands
_As you go on with working with your code, you should constantly use these commands to keep track of your code._
#### git status  
Git status is a tool used to see the changes that have been made in your project (the status of your project) which would show up in red and when an edited file has been added to the staging area for a snapshot, it will show up in `git status` as green. So the syntax of `git status` is exactly that. You use git status before you add, after you add, and after you commit. You can also use it any other time to see if anything has been recently motified or what's on the staging area just to keep track as you go along.  
![git status image](https://snag.gy/ayT53B.jpg)
#### git add  
Git add is a tool used to add files to the staging area to be committed. There are many different ways to add. There's `git add 'file'`, `git add .`, and `git add --all`. For `git add 'file'`, this is a simple way to add a single file that you have recently edited to the staging area to be committed. `git add .` adds all of the files that have been edited to the staging area. `git add --all` adds all of the files that have changes including deleted files. 
#### git commit  
Git commit is a tool used for taking snapshots of code that are on the staging area. After you add a file or files and to `git status`, you simply type in `git commit -m`. The -m is for you to type a message **in quotations** of what changes you have made in the file or files. It's imperative that you type in the command as shown because if you don't, it can lead you to somewhere you don't want to go.  
![git commit image](https://snag.gy/5RPNVI.jpg)
#### git push  
Git push is a tool used to add all of your commits to your remote repository. Your remote repository is your repository in github where all of your code is stored. After you commit your code, you push it to the remote repository by using `git push`. You use `git push` after you do `git push -u origin master` which tells git where the code is being pushed to. You only use it once.  
![git push image](https://snag.gy/ZRXhEl.jpg) 

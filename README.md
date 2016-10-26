# GitHub Tutorial

_by Cheyenne Nicaisse_

---
## Git vs. GitHub
The difference between git and github is that git takes snapshots of code and doesn't need github in order to function but **github needs git**.  
Github stores all of your code/snapshots in the cloud or your remote repository


---
## Initial Setup
##### To make a github account:  
1. first you go to [github.com](github.com).  
2. Next, you go to the top right of the screen and click "sign up". 
3. Then you fill in the information required. ![image](https://snag.gy/Aykn39.jpg)
4. Github will then ask you for a plan and you click the free plan and move on to the third step.
5. The third and final step is optional where github wants to learn more about you and your experience. You can either fill it out or skip this step. 
6. Now when you go to [cloud 9](c9.io), you can easily log in with your github account
7. **REMEMBER** to verify your account. an email will be sent from github in order for you to verify you are not a robot, click the link given to verify yourself. if you do not do this, nobody will be able to see any of your remote repositories

##### In cloud 9 to make a new workspace to fit with git projects:
1. First after you log into cloud 9 with github, you press new workspace.
![image](https://snag.gy/LMxCWZ.jpg)
2. Then you type in a name and a description for your workspace (preferably one that relates to git).
3. Next you click public to make your workspace viewable to everyone.
4. Then you choose Blank as your template.
5. After all that is done, you click create workspace. 

##### Making your SSH key (one time set-up meaning it's forever connected to your cloud 9) :
1. First you go to github and make sure you are logged in.
2. Then you go to the top right corner, click your profile icon, and then click settings.
3. On the left sidebar, click SSH and GPG keys.
![image](https://snag.gy/Fxj4Ch.jpg)
4. Then on the top right corner click new SSH key.
5. Then title your key. (An appropriate title would be cloud 9 since it's a key for cloud 9).
6. Then you open a new tap and go to cloud 9 and on the top right click the gear icon.
7. Then on the left sidebar, click SSH keys.
8. In the gray box, copy the whole SSH key. (Starts with ssh-rsa). 
![image](https://snag.gy/cHmTGr.jpg)
9. Add the SSH key to github.
10. Then you open your workspace on cloud 9 and type in `ssh -T git@github.com`. 


---
## Repository Setup
##### When making your local repository in cloud 9:
1. Go to your workspace in cloud 9 and change directories into your workspace by typing `cd ~/workspace`.
2. Next make your directory by typing `mkdir "name"`.
3. Then change directories to your new directory by typing `cd "name"`.
4. Then type `git init`. This initializes git into your local repository. _Always make sure you are in your local repository_. 
5. Next, make a README file by typing `touch README.md`. The md stands for markdown.
6. Type what ever you would like in your readme file.
7. Next, to save this work, you use `git add .` or `git add README.md` to add it to the staging area for it to be commited, or taken a snapshot of for it to be saved. 
8. Then you commit what you added by typing `git commit -m "(message)"`. This takes a snapshot of your changes to your file to be saved in the cloud.

##### To push these changes into the cloud for it to be saved in a remote repository: 
1. First, go to github and click the plus icon to create a new repository.
2. When naming your remote repository in github, make sure it has the **exact** same name as your local repository. 
3. Finally, for your one time set up with the connection between your remote and local repositories, click SSH key at the top right.
4. Then at the bottom, one at a time, copy and paste these lines of code into your cloud 9 (the user and repository will be your own):
![image](https://snag.gy/LYRyMG.jpg)



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


---
## Collaboration 
#### Fork  
Forking is a way to create a replica of someone else's remote repository so that you can take their project, make changes, and push those changes to the forked remote repository without disrupting the original project. When you want to fork a project on github, you simply go to that project and click "fork" on the top right corner. 

#### Clone 
Cloning is when you create a replica of a local repository that has already been made and saved in your own repository. Cloning is good for re-naming your remote repository. When you clone a local repository from a remote, it automatically creates the connection between the remote and local as well as names it and the cloned local repository. To clone, you go to your remote, you click "clone or download", make sure you're cloning with SSH, and copy the link to your clipboard. Then go to your workspace in cloud 9 and type `git clone (url)` and the repository should show up.

#### Pull Requests  
Pull requests are ways that people who have forked your repository and have made changes to it can let you see those changes and possibly add them to the original project. When you submit a pull request, on your forked repository, you click pull request to suggest those changes. ![image](https://snag.gy/6NzseH.jpg)

#### Pull 
After you accept your pull request suggesting changes to your project, you simply type git pull to see those changes in effect on your orininal project. 
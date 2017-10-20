# GitHub Tutorial

_by Xavier Jiang_

---
## Git vs. GitHub
**Git**- a version control that keeps "snapshots" of code/work, it doesn't require Github
---
**Github**- a open source that stores code in the cloud, helps you visually track changes, it requires Git 


---
## Initial Setup
1) First you have to make a [github account](https://github.com/)
2) complete the whole process of signing up 
3) If you don't have a c9 account [press this to sign up](https://c9.io/) follow the steps to get a c9 account
4) Next we have to link c9 with github by going into c9.io > top-right > press gear icon > connected services > find Github and press connect
5) Now that you are connected, you can create your own workspace in c9.io, name it whatever you like and complete the setup
6) The finally step is setting up your SSH key, go to [github](https://github.com/) > top-right where your icon is located > click the down-arrow > go to settings > click on SSH and GPG keys > click new SSH keys > 
lastly input your SSH key which is found in c9.io
(step to find SSH key in c9.io, go to c9.io log in > click gear icon > top-right > click SSH keys > copy the second SSH key, which is below Connect to your private git repository)

---
## Repository Setup
1) Now go ahead and start coding, make your own repository or directory 
2) cd into the repository/repo and then make a file name README.md
3) Stay in your repository, type in git init to initialize your repo
4) go to github, you should see the new repo you made, click to go into the repo > you should see clone or download in the middle-right click it > copy the url and go back to c9.io
 > type in git push -u origin master
5) To make a repository on github, first go to github.com > top-right where the add icon is located > click the down-arrow > click new repository > see the part where it states …or push an existing repository from the command line
> copy the commands below it > paste it in your c9.io workspace, where your command line is located (from now on you just need to git push to push your snapshots into github)



---
## Workflow & Commands
* always use git status to see which files are staged for the commit, this will prevent some errors and helps you keep track of your work
* Get use to doing (**after edits**):
  * git add file- Add the file(s) to the stage to be committed
  * git commit -m "message"- take a ‘snapshot’ of the files on the stage (The message should be present tense and describe what was changed) 
  * git push- we are sending our commit from our local repo to our remote repo.
* Remember that you always have to add, then commit, then push. (Has to be done in this order)

---

## Rolling Back Changes
* undo a edit/add/commit/push
  * Git reset HEAD~ : undo commit and add 
  * Git reset --hard HEAD~ : undo commit, add, and edit 
  * Undoing git push: First do git log to get the commit sha and q to quit git revert <sha code>
  * git reset --soft HEAD~: If you _only_ want to _add_ more changes to the previous commit, or change the commit message1

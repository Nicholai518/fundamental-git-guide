# fundamental-git-guide
A git guide which contains fundamental commands for creating, updating and maintaining git repositories. 
Website:https://github.com/ 


## Creating a repository on Github

**Command: echo "# NAME_OF_YOUR_REPO" >> README.md** 
*Meaning: Copies text into the README.md file*


**Command: git init**
*Meaning: Creates a new git repository. You can begin to start tracking different versions of your project!*


**Command: git add README.md**
*Meaning: Adds a change in the working directory to the staging area. In this case, specifically add the README.md file to the “staging area”.

You can repeat this command with different files such as “git add Main.java” 
You can also add all files to the staging area using: **git add .** *


Command: git commit -m "first commit" 
Meaning: Record a change you’ve made to a file and then store that change in the repository. Commits are referred to as “Snapshots” of your tracked files.. 


**Command: git branch -M main** 
*Meaning: Renames the master branch to main*


**Command: git remote add origin https://github.com/YOUR_REPO_HERE.git**
*Meaning: adds a reference to the remote server in your local project*

**git push -u origin main**
*Meaning: Publish your local code changes to a remote repository, specifically the main branch*

# fundamental-git-guide
A git guide which contains fundamental commands for creating, updating and maintaining git repositories. 
<br/>Website:https://github.com/ 


## Creating a repository on Github

**Command: echo "# NAME_OF_YOUR_REPO" >> README.md** 
<br/>*Meaning: Copies text "NAME_OF_YOUR_REPO" into the README.md file*


**Command: git init**
<br/>*Meaning: Creates a new git repository. You can begin to start tracking different versions of your project!*


**Command: git add README.md** <br/>
*Meaning: Adds a change in the working directory to the staging area. In this case, specifically add the README.md file to the “staging area”.* <br/> 
*You can repeat this command with different files such as “git add Main.java”* <br/> 
*You can also add all files to the staging area using: **git add .***


Command: git commit -m "first commit" 
<br/>Meaning: Record a change you’ve made to a file and then store that change in the repository. Commits are referred to as “Snapshots” of your tracked files.


**Command: git branch -M main** 
<br/>*Meaning: Renames the master branch to main*


**Command: git remote add origin https://github.com/YOUR_REPO_HERE.git**
<br/>*Meaning: adds a reference to the remote server in your local project*

**git push -u origin main**
<br/>*Meaning: Publish your local code changes to a remote repository, specifically the main branch*
<br/>
<br/>

## Creating Repository steps Visualization
![alt text](https://d186loudes4jlv.cloudfront.net/git/images/github_new_repo3.png)

## Local / Remote Repository Visual Representation
![alt text](https://media.dev.to/cdn-cgi/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fvpxeexqyfvf4hw3zxtbn.png)


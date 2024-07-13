# fundamental-git-guide
A git guide which contains fundamental commands for creating, updating and maintaining git repositories. <br/>
Website:https://github.com/ <br/>

## Section 1: Creating a repository on Github

## Picture for reference
![alt text](https://cdn-media-1.freecodecamp.org/images/cxRrZUe-tW2Wkn0WUg-MsN1m1WesvGPlJT7V) 

**Command: echo "# NAME_OF_YOUR_REPO" >> README.md** <br/>
*Meaning: Copies text "NAME_OF_YOUR_REPO" into the README.md file*  <br/>  <br/>

**Command: git init** <br/>
*Meaning: Creates a new git repository. You can begin to start tracking different versions of your project!* <br/>  <br/>

**Command: git add README.md** <br/>
*Meaning: Adds a change in the working directory to the staging area. In this case, specifically add the README.md file to the “staging area”.* <br/> 
*You can repeat this command with different files such as “git add Main.java”* <br/> 
*You can also add all files to the staging area using: **git add .*** <br/>  <br/>

**Command: git commit -m "first commit"** <br/>
*Meaning: Record a change you’ve made to a file and then store that change in the repository. Commits are referred to as “Snapshots” of your tracked files.* <br/>  <br/>

**Command: git branch -M main** <br/>
*Meaning: Renames the master branch to main* <br/>  <br/>

**Command: git remote add origin https://github.com/YOUR_ACCOUNT/YOUR_REPO_HERE.git** <br/> 
*Meaning: adds a reference to the remote server in your local project* <br/>  <br/>

**git push -u origin main** <br/>
*Meaning: Publish your local code changes to a remote repository, specifically the main branch* <br/> <br/>


## Local / Remote Repository Visual Representation
![alt text](https://media.dev.to/cdn-cgi/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fvpxeexqyfvf4hw3zxtbn.png)


## Section 2: How to clone a repository from Github

**Command: git clone https://github.com/YOUR_ACCOUNT/YOUR_REPO_HERE.git**
<br/>*Meaning: Make a clone or copy of that repo at in a new directory, or at another location.*
<br/>*Note: Navigate to the desired directory on your computer before cloning repository*
<br/>*Ex: C:\Dev\Java*

## Picture for reference
![alt text](https://docs.github.com/assets/cb-60499/images/help/repository/https-url-clone-cli.png)

**Steps to clone a repository**
- Go to the Github repository you wish to clone
- Click on "Code"
- Copy and paste the HTTPS Web URL
- Open up Git on your compute
- Navigate to the desired directory
- Use this command to clone the repository: **git clone WEB_URL_GOES_HERE**

## Section 3: How to create a .gitignore file

*Creates an empty .gitignore file*
**Command: echo > .gitignore**
Or
**Command: touch .gitignore**

*Question: What is a .gitignore file?*
**Answer: Specifies intentionally untracked files that Git should ignore.**  

*More information about .gitignore files can be found here*
https://git-scm.com/docs/gitignore 

*.gitignore file templates can be found here*
https://github.com/github/gitignore 

*Question: Should you commit and push your .gitignore file?*
**Answer: Yes, you should commit the . gitignore file to your remote repository. This ensures that all contributors to the project are on the same page regarding which files should not be tracked by Git.**

*Tool to create .gitignore*
*Enter your tech stack, then press create. Copy and paste the contents of the webpage into your .gitignore file*
https://www.toptal.com/developers/gitignore 

## Section 4: Working directory

*Creates a file named fileOne.txt in the current directory with no text (This is not a git command)*
**Command: echo > fileOne.txt**
Or
**Command: touch fileOne.txt**

*Creates a file named fileOne.txt in the current directory with text “Hello World!”*
**Command: echo Hello World! > fileOne.txt**

*Appends “Hello Again!” to the end of a file named fileOne.txt in the current directory OR creates a new file named fileOne.txt if this file does not exist with the text “Hello Again!”*
**Command: echo Hello Again! >> fileOne.txt**

*You can create all different types of files*
**Command: echo Hello World! > fileOne.txt**
**Command: echo Hello World! > app.go**
**Command: echo Hello World! > app.js**
**Command: echo Hello World! > index.html** 

*How to view all files in directory*
**Command: git ls-files**

*How to create a directory (Folder) This is not a git command*
**Command: mkdir folder-name**
**Ex: mkdir all-text-files**

*How to review the changes made to modified files in working directory*
**Command: git diff fileOne.txt **














## Status

### <ins>Show the status of working directory & Staging area</ins>
**Command: git status**

### <ins>Show the status of working directory & Staging area with short description</ins>
**Command: git status -s**
<br/>*Note: -s is the “short status” flag*


## Viewing Changes

### View Staged and Unstaged changes
**Command: git diff FILE_NAME**
<br/>*Note: View changes for a single file*
<br/>*Ex: git diff Main.java* 

**Command: git diff**
<br/>*View all unstaged changes, What is in the working directory VS what is in staging area*
<br/>*Note: Empty response means all files with changes in working directory have been added to staging area*


**Command: git diff --staged**
<br/>*View staged changes to all files that will be included in next commit*



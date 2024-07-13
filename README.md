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

**Command: git clone https://github.com/YOUR_ACCOUNT/YOUR_REPO_HERE.git** <br/> 
*Meaning: Make a clone or copy of that repo at in a new directory, or at another location.* <br/> 
*Note: Navigate to the desired directory on your computer before cloning repository* <br/> 
*Ex: C:\Dev\Java*

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

*Creates an empty .gitignore file* <br/> 
**Command: echo > .gitignore** <br/> 
Or <br/> 
**Command: touch .gitignore** <br/> 

*Question: What is a .gitignore file?* <br/> 
**Answer: Specifies intentionally untracked files that Git should ignore.**  <br/> 

*More information about .gitignore files can be found here* <br/> 
https://git-scm.com/docs/gitignore <br/> 

*.gitignore file templates can be found here* <br/> 
https://github.com/github/gitignore <br/> 

*Question: Should you commit and push your .gitignore file?* <br/> 
**Answer: Yes, you should commit the . gitignore file to your remote repository. This ensures that all contributors to the project are on the same page regarding which files should not be tracked by Git.** <br/> 

*Tool to create .gitignore* <br/> 
*Enter your tech stack, then press create. Copy and paste the contents of the webpage into your .gitignore file* <br/> 
https://www.toptal.com/developers/gitignore  <br/> 

## Section 4: Working directory

*Creates a file named fileOne.txt in the current directory with no text (This is not a git command)* <br/> 
**Command: echo > fileOne.txt** <br/> 
Or <br/> 
**Command: touch fileOne.txt** <br/> 

*Creates a file named fileOne.txt in the current directory with text “Hello World!”* <br/> 
**Command: echo Hello World! > fileOne.txt** <br/> 

*Appends “Hello Again!” to the end of a file named fileOne.txt in the current directory OR creates a new file named fileOne.txt if this file does not exist with the text “Hello Again!”* <br/> 
**Command: echo Hello Again! >> fileOne.txt** <br/> 

*You can create all different types of files* <br/> 
**Command: echo Hello World! > fileOne.txt** <br/> 
**Command: echo Hello World! > app.go** <br/> 
**Command: echo Hello World! > app.js** <br/> 
**Command: echo Hello World! > index.html** <br/> 

*How to view all files in directory* <br/> 
**Command: git ls-files** <br/> 

*How to create a directory (Folder) This is not a git command* <br/> 
**Command: mkdir folder-name** <br/> 
**Ex: mkdir all-text-files** <br/> 

*How to review the changes made to modified files in working directory* <br/> 
**Command: git diff fileOne.txt ** <br/> 

*Removes a file named fileOne.txt in the current directory. This is not a git command* <br/> 
**Command: rm  fileOne.txt**


*Removes a file named fileOne.txt in the current directory AND from the staging area. This is a git command* <br/> 
**Command: git rm -f  fileOne.txt** <br/> 
**Note: Be careful using the -f (force) flag**







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



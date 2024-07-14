# fundamental-git-guide
A git guide which contains fundamental commands for creating, updating and maintaining git repositories. <br/>
Website: https://github.com/ <br/>

## Section 1: Creating a repository on Github

## Picture for reference
![alt text](https://cdn-media-1.freecodecamp.org/images/cxRrZUe-tW2Wkn0WUg-MsN1m1WesvGPlJT7V) 

**Command: echo "# NAME_OF_YOUR_REPO" >> README.md** <br/>
*Explanation:  Copies text "NAME_OF_YOUR_REPO" into the README.md file*  <br/>  <br/>

**Command: git init** <br/>
*Explanation:  Creates a new git repository. You can begin to start tracking different versions of your project!* <br/>  <br/>

**Command: git add README.md** <br/>
*Explanation:  Adds a change in the working directory to the staging area. In this case, specifically add the README.md file to the “staging area”.* <br/> 
*You can repeat this command with different files such as “git add Main.java”* <br/> 
*You can also add all files to the staging area using: **git add .*** <br/>  <br/>

**Command: git commit -m "first commit"** <br/>
*Explanation:  Record a change you’ve made to a file and then store that change in the repository. Commits are referred to as “Snapshots” of your tracked files.* <br/>  <br/>

**Command: git branch -M main** <br/>
*Explanation:  Renames the master branch to main* <br/>  <br/>

**Command: git remote add origin https://github.com/YOUR_ACCOUNT/YOUR_REPO_HERE.git** <br/> 
*Explanation:  adds a reference to the remote server in your local project* <br/>  <br/>

**Command: git push -u origin main** <br/>
*Explanation:  Publish your local code changes to a remote repository, specifically the main branch* <br/> <br/>


## Local / Remote Repository Visual Representation
![alt text](https://media.dev.to/cdn-cgi/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fvpxeexqyfvf4hw3zxtbn.png)


## Section 2: How to clone a repository from Github

**Command: git clone https://github.com/YOUR_ACCOUNT/YOUR_REPO_HERE.git** <br/> 
*Explanation:  Make a clone or copy of that repo at in a new directory, or at another location.* <br/> 
*Note: Navigate to the desired directory on your computer before cloning repository* <br/> 
*Example Directory: C:\Dev\Java*  <br/>  <br/>

## Picture for reference
![alt text](https://docs.github.com/assets/cb-60499/images/help/repository/https-url-clone-cli.png)
 <br/>  <br/>
**Steps to clone a repository**  <br/>
- Go to the Github repository you wish to clone  <br/>
- Click on "Code"  <br/>
- Copy and paste the HTTPS Web URL  <br/>
- Open up Git on your compute  <br/>
- Navigate to the desired directory  <br/>
- Use this command to clone the repository: **git clone WEB_URL_GOES_HERE**  <br/>
- Example: **git clone https://github.com/github/docs.git** <br/> <br/> 

## Section 3: How to create a .gitignore file

**Command: echo > .gitignore** <br/> 
Or <br/> 
**Command: touch .gitignore** <br/> 
*Explanation: Creates an empty .gitignore file* <br/>  <br/>

*Question: What is a .gitignore file?* <br/> 
**Answer: Specifies intentionally untracked files that Git should ignore.**  <br/>  <br/>

*More information about .gitignore files can be found here* <br/> 
https://git-scm.com/docs/gitignore <br/>  <br/>

*.gitignore file templates can be found here* <br/> 
https://github.com/github/gitignore <br/>  <br/>

*Question: Should you commit and push your .gitignore file?* <br/> 
**Answer: Yes, you should commit the .gitignore file to your remote repository. This ensures that all contributors to the project are on the same page regarding which files should not be tracked by Git.** <br/>  <br/>

*Tool to create .gitignore* <br/> 
*Enter your tech stack, then press create. Copy and paste the contents of the webpage into your .gitignore file* <br/> 
https://www.toptal.com/developers/gitignore  <br/>  <br/>

## Section 4: Working Directory

## Create files / directories in working directory

**Command: echo > FILE_NAME_HERE** <br/> 
**Example: echo > fileOne.txt** <br/> 
Or <br/> 
**Command: touch FILE_NAME_HERE** <br/> 
**Example: touch fileOne.txt** <br/>
*Explanation: Creates a file in the current directory with no text. This is not a git command.* <br/>  <br/>

**Command: echo Hello World! > FILE_NAME_HERE.EXTENSION** <br/> 
**Examples:** <br/> 
**Command: echo Hello World! > fileOne.txt** <br/> 
**Command: echo Hello World! > app.go** <br/> 
**Command: echo Hello World! > app.js** <br/> 
**Command: echo Hello World! > index.html** <br/>
*Explanation: Creates a file in the current directory with text “Hello World!”. You can create all different types of files* <br/> <br/>

**Command: echo Hello Again! >> FILE_NAME_HERE** <br/> 
**Example: echo Hello Again! >> fileOne.txt** <br/>
*Explanation: Appends “Hello Again!” to the end of a file in the current directory. Or, creates a new file, with the specified file name, if this file does not exist with the text “Hello Again!”* <br/>  <br/> 


**Command: git ls-files** <br/> 
*Explanation: How to view all files in directory* <br/> <br/>


**Command: mkdir FOLDER_NAME_HERE** <br/> 
**Example: mkdir all-text-files** <br/> 
*Explanation: How to create a directory (Folder) This is not a git command* <br/>  <br/>



**Command: git diff FILE_NAME_HERE.txt ** <br/> 
*Explanation: How to review the changes made to modified a file in working directory* <br/> 
**Example: git diff Main.java** <br/>  <br/>


## Remove files from working directory
**Command: rm FILE_NAME_HERE**
*Explanation: Removes a file named fileOne.txt in the current directory. This is not a git command* <br/> 
**Example: rm Main.java** <br/>  <br/>



**Command: git rm -f FILE_NAME_HERE** <br/> 
**Example: git rm -f Main.java** <br/> 
*Explanation: Removes a file in the current directory AND from the staging area. This is a git command* <br/> 
*Note: Be careful using the -f (force) flag*  <br/>  <br/>


## Move or rename a file(s)
**Command: mv ORIGINAL_FILE_NAME NEW_FILE_NAME**  <br/>
**Example: mv fileOne.txt fileTwo.txt** <br/> 
*Explanation: Rename a file from ORIGINAL_FILE_NAME to NEW_FILE_NAME . This is not a git command*  <br/>  <br/>


**Command: mv FILE_NAME DIRECTORY src/** <br/>
**Example: mv fileOne.txt notes/** <br/> 
*Explanation: Move a file to a directory. This is not a git command* <br/> <br/>



**Command: git mv ORIGINAL_FILE_NAME NEW_FILE_NAME**
**Example: git mv fileOne.txt fileTwo.txt** <br/> 
*Explanation: Rename a file from ORIGINAL_FILE_NAME to NEW_FILE_NAME. This is a git command and changes are applied to working directory and staging area* <br/>
*Note: File must be added to staging area for this command to work* <br/> <br/>


## Add file(s) from working directory to staging area
**Command: git add FILE_NAME_HERE** <br/> 
**Example: git add fileOne.txt ** <br/> 
*Explanation: Add file from working directory to staging area*

**Command: git add FIRST_FILE_NAME_HERE SECOND_FILE_NAME_HERE**  <br/> 
**Example: git add fileOne.txt fileTwo.txt** <br/> 
*Explanation: Add both files from working directory to staging area <br/>  
*Note: File names are separated by a space* <br/> <br/>


**Command: git add *.EXTENSION_HERE**<br/>
**Examples:** <br/>
**Command: git add *.txt** <br/> 
**Command: git add *.java** <br/> 
*Explanation: All files with the specified extension will be added from the working directory to the staging area* <br/> <br/>


**Command: git add .** <br/>
*Explanation: Add all the changes from working directory to staging area (Be Careful with this!)*  <br/>  <br/>


## Discarding changes from working directory

**Command: git restore FILE_NAME_HERE** <br/>
**Example: git restore fileOne.txt**  <br/>
*Explanation: This will undo any local changes in working directory for the file*  <br/>  <br/>


**Command: git restore** <br/>
*Explanation: This will undo any local changes in working directory for all files*  <br/>  <br/> 

**Command: git clean -fd** <br/>
*Explanation: This will remove any newly created files that have not been tracked *  <br/>  <br/> 


## Removing files from Staging area and returning back to working directory

**Command: git restore --staged FILE_NAME_HERE** <br/>
**Example: git restore –-staged fileOne.txt** <br/>
*Explanation: Keep your changes to the file, but return file to working directory* <br/> <br/>

**Command: git rm--cached FILE_NAME_HERE** <br/>
**Example: git rm –-cached fileOne.txt** <br/>
*Explanation: Keep your changes to the file, but return file to working directory* <br/>
*Note: cached removes from the index aka the staging area* <br/> <br/>


## How to delete a file from working directory and staging area
**Command: git rm FILE_NAME** <br/>
**Example: git rm fileOne.txt** <br/>
*Explanation: Delete a file from working directory and staging area* <br/> <br/>


## Section 5: Commits

## How to commit files that are added to staging area
**Command: git commit -m “your_commit_message_goes_here”** <br/>
**Example: git commit -m “fixed bug which printed wrong date on customer receipt”** <br/>
*Explanation: Commit a "snapshot" of your Git local repository at one point in time* <br/> 
*TIp: The first word of your commit message should be something like “added”, “fixed”, “updated”, “created”, “removed” . Essentially something with an “ed” at the end.* <br/> <br/>


## How to unstage files from a commit
**Command: git restore –-staged FILE_NAME_HERE**  <br/>
**Example: git restore –-staged fileOne.txt**  <br/>
*Explanation: Removes single file from staging. Keeps your changes and returns the modified file to working directory*  <br/>  <br/>

**Command: git restore -–staged FILE_NAME_HERE FILE_NAME_HERE**   <br/>
**Example: git restore -–staged fileOne.txt Main.java**  <br/>
*Explanation: Removes multiple files from staging. Keeps your changes and returns the modified files to working directory*  <br/>  <br/>

**Command: git restore –-staged .** <br/>
*Explanation: Removes all files from staging area.  Keeps your changes and returns the modified files to working directory*  <br/>  <br/>


## How to change file(s) and commit again but keep the same commit message
**Command: git add FILE_NAME_HERE**  <br/>
**Command: git commit --amend --no-edit**  <br/>  <br/>

**Example: git add fileOne.txt**  <br/>
**Example: git commit --amend --no-edit**  <br/>

*Explanation: Make the necessary changes to the desired files. Add the files to staging area. Then commit using amend and no edit. This will change your previous commit to include these new changes, while keeping the same commit message*  <br/>
*Note: You just committed but you noticed a typo within a file. Go ahead and make your change, then add and commit again. It will look like this exta commit never happened.*  <br/>  <br/>


## How to change / update the commit message (Not making any changes to files)
**Command: git commit --amend -m “NEW_COMMIT_MESSAGE_HERE”**  <br/>
**Example: git commit --amend -m “NEW_COMMIT_MESSAGE_HERE”**  <br/> 

*Explanation: You don't need to make any changes to files but want to update your most recent commit message*  <br/>
*Note: Your files and code are good, but you accidentally made a typo in your commit message, this is how you can fix it.*  <br/>  <br/>


## How to stash committed changes and pop changes on new branch
**Command: git reset HEAD~ --soft **    <br/>
**Command: git stash ** <br/>
**Command: git checkout name-of-the-desired-branch**  <br/>
**Command: git stash pop**  <br/>
**Command: git add . # or add individual files**  <br/>
**Command: git commit -m "COMMIT_MESSAGE_HERE"**  <br/>

*Explanation: You commited on the wrong branch (Ex: Main / Master). You need to move those changes to a different branch.*  <br/>
*Note: This example resets HEAD by 1 commit. This command can be altered OR be used multiple times. Use HEAD~num for specific commit* <br/> <br/>

## How to view commit history
**Command: git log**  <br/>
*Explanation: Commits will be sorted from latest(Top of terminal) to earliest (Bottom of terminal). Shows all Commits on all branches*  <br/>

Or   <br/>

**Command: git log –oneline**   <br/>
*Explanation: Shows commit history with a short summary*   <br/>

Or   <br/>

**Command: git log –oneline –reverse**   <br/>
*Explanation: Shows commit history in reverse (Oldest commit at the top of terminal, Newest at the bottom) with a short summary*   <br/>  <br/>


## How to view changes in a given commit
**Command: git show COMMIT_HASH_HERE**   <br/>
**Example: git show 7d4590cc6bfdde322653ec1164630803589ed349**   <br/>
*Explanation: View Changes made in specific commit within terminal*   <br/>

Or   <br/>

**Command: git show HEAD~Number of commits**  <br/>
**Example: git show HEAD~5**  <br/>
*Explanation: View Changes made in specific commit within terminal*   <br/>

## How to view all files and directories for a given commit
**Command: git ls-tree COMMIT_HASH_HERE** <br/>
**Example: git ls-tree 7d4590cc6bfdde322653ec1164630803589ed349**   <br/>
*Explanation: Shows blob’s (files), commits, Tags and tree’s (Directories) for a specific commit* <br/> <br/>

## Restoring a file to an earlier version
**Command: git restore –source=HEAD~NUMBER_OF_COMMITS FILE_NAME** <br/>
**Example: git restore --source=HEAD~3 fileOne.txt** <br/>
*Explanation: You accidentally deleted an important file. You can recover the file from an earlier commit* <br/> <br/>


## Section 6: Branches

## Section 7: Pushing

## Section 8: Pulling

## Section 9: Extra

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



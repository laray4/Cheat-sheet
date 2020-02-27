## Create branch
``git -b <branch name>``

## Delete branch localy
``git branch -d <branch name>``

## Delete branch remotely
``git push origin --delete <branch name>``

## Change your remote's URL
``git remote set-url origin <url>``

## Push your branch to the remote repository:
``git push -u origin <branch name>``

## Adding an existing project to GitHub using the command line  

Create a new repository on GitHub.
 
Change the current working directory to your local project.

Initialize the local directory as a Git repository.

``git init``

Add the files in your new local repository. This stages them for the first commit.

``git add .``

 Commit the files that you’ve staged in your local repository.
 
``git commit -m "initial commit"``

 Copy the https url of your newly created repo
 
In the Command prompt, add the URL for the remote repository where your local repository will be pushed.

``git remote add origin remote <repo_url>``

``git remote -v``

 Push the changes in your local repository to GitHub.

``git push -f origin master``

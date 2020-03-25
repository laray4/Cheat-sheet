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


## Cloning a repository that contains submodules

If you want to clone a repository including its submodules you can use the ``--recursive`` parameter.

``git clone --recursive [URL to Git repo]``

If you already have cloned a repository and now want to load it’s submodules you have to use submodule update.

``git submodule update --init``

If there are nested submodules:

``git submodule update --init --recursive``

## Rename a branch

If you are on the branch you want to rename:

``git branch -m <new-name>``

If you are on a different branch:

``git branch -m old-name <new-name>``

Delete the old-name remote branch and push the new-name local branch.

``git push origin :<old-name new-name>``


Reset the upstream branch for the new-name local branch.
Switch to the branch and then:

``git push origin -u <new-name>``

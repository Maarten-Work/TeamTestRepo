# How to deal with forks to update a repository

## 1) Fork a repository from another's project
- Navigate to the other's project in GitHub's web interface and click the **Fork** button.
This will create a new project in your own GitHub account.
- Clone the new created project on your local machine to work with.
## 2) Keep your fork synced with the original project
Each time you want to modify the project you forked, it is important to get the latest changes that other's might have created. For that, you need to synchronize your forked repository with the original.
- Type `git remote -v` to see the current configured remote repository for your fork (which is really your own repository on GitHub).
- Add the remote repository by entering the following command: `git remote add upstream <https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git>`
- Fetch the branches and their commites from the upstream repository by entering the following command: `git fetch upstream`.
- Check out your for's local master branch by entering the following command: `git checkout master`.
- Merge the changes from the upstream/master into your own local repo by entering the following command: `git merge upstream/master`
## 3) Keeping your fork on GitHub up-to-date
In step 2 you synchronized your local copy of the repo with the original repository. Do the following to synchronize your forked repository on GitHub.
- Update your fork on GitHub by pushing your local repo to it. You can do so by giving the following command: `git push remote master`
## 4) Working on a change
Typically you want to make changes on a new branch.
- The easiest way to create a new branch is to click on the master branch in Visual Studio Code and give your new branch a meaningfull name. The branch will be created and will immediately be the active branch.
- You can also create a new branch with git by typing the following command: `git branch <branch name>`
- To change to the newly created branch, type the following ncommand: `git checkout <branch name>`. This is done for you if you created the new branch inside Visual Studio Code.
## 5) Sharing changes back to the original repository
To inform the owner of the original repository about your changes, you open a pull request. Through it you can discuss your potential changes and allow the owner of the original repository to review them. If you want to do that from inside GitHub, you must first make sure that your proposed changes are commited both locally and on your own copy of the repository on GitHub.
- If you want a subset of files committed, stage them first in Visual Studio Code.
- Commit all or only staged files using Visual Studio and give your commit a meaningful (short) description.
- Synchronize your changes with your repository on GitHub. You can't synchronize to the original repository, because you only have read access to the original repository.
# Forking and Creating Pull Requests

## Part A: Creating Fork and Local Repository
1. Goto the Original github repository (called as **Upstream**) and press the fork button.
2. Goto your repository. There you can find the fork (i.e., copy of upstream called as **Origin**).
3. Open terminal and goto your desired folder. Clone the fork to your local machine
```
git clone <repo_url/repo.git>
```

## Part B: Syncing your fork
This Part effectively contains two sub-steps:
1. Syncing local repository
2. Syncing fork or remote

### 1. Syncing local repository
1. Add upstream(Original repository) as a remote repository. In terminal type
```
git remote add upstream <original_repo/repo.git>
```
2. Verify added remote repo using following command. There should be atleast two remote repos.
```
git remote -v
```
3. Fetch the branches and their respective commits
```
git fetch upstream
```
4. Make sure you are in the master branch
```
git checkout master
```
5. Merge changes to local repo
```
git merge upstream/master
```
Now your local repository is upto-date with Upstream

### 2.Syncing origin/fork/GitHub repository
1. Push the changes to Origin
```
git push origin master
```

## Part C: Creating a Pull request
1. Edit or add desired files
2. Stage the changes
```
git add *
or 
git add <changed_file>
```
3. Save your changes to the local repository
```
git commit -m "<Commit message>"
```
4. Push changes to Origin/Fork
```
git push origin master
```
5. Goto Github repository. Go to compare changes. Initiate pull request.
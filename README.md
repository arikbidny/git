# GIT

## Content

- [Configuration](#configuration)
- [Making changes to your files](#making-changes-to-your-files)
- [Going back to a previous commit version](#going-back-to-a-previous-commit-version)
- [Working with branches](#working-with-branches)

## Configuration

- Get config list

```
git config --list
```

- Configure user name

```
git config --global user.name "Full Name"
```

- Configure user email

```
git config --global user.email "youremail@email"
```

## Making changes to your files

- Show commit log

```
git log
```

- Check status

```
git status
```

- Add file/files to staging area

```
git add .
git add fileName
```

- Commit the changes

```
git commit -m "initial commit"
```

- Check differences

```
git diff
```

## Going back to a previous commit version

- Get back to previous commit

```
git checkout commitId
```

## Working with branches

- Good Practices
  - Create many short-lived feature branches
  - Delete the branches once they are not required

- Create a branch 
```
git branch feature
```

- Checkout the branch 
```
git checkout feature
```

## Merges in git 

### Fast forward merge 
Using fast farward merge when our changes made only on feature branch and not in master branch 
- In master branch run:
```
git merge feature
```

- Show graph process of commits 
```
git log --graph
```

### Recursive strategy 
If we made a changes in master branch and then in feature branch and then running a merge from master
```
git merge feature
```
We getting recursive strategy merge

```
git log --graph --decorate --oneline 
```

### Squash merge
- This is used to condense the git history of the feature branches when a merge is carried out. 
- Here instead of each commit history of the feature branch being added to the commit history of the master branch, the squash merge will take all the file changes and then just create one single new commit on the master branch 
- This helps to keep the commit history clean when it comes to the master branch.

- From master branch run:
```
git merge --squash feature
```


## Push changes to central 

- Push from all branches 
```
git push --all origin
```

## Pull requests
- Create new feature branch 
```
git branch new-feature
```
- Go to new-feature branch 
```
git checkout new-feature
```
- Making some changes
- Commit the file 
- In azure devops branches go to branch you want -> branch policies -> Require minimum number of reviewers
- From azure devops ui create a pool request

## Gitignore

- Create git ignore file
```
touch .gitignore
```
- Add files you want to ignore to gitignore
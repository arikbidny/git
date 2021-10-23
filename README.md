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

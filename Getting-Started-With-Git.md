#Getting Started with Git
##Core Concepts
### Commands
#### Getting Started

`git init`

or 

`git clone url`

#### Configuration

```
git config --global color.ui true
git config --global push.default current
git config --global core.editor vim
git config --global user.name "John Doe"
git config --global user.email foo@citrix.com
git config --global diff.tool meld
```
#### Working with Local Branch
Branching
```
git branch
git checkout branchname
git chekcout -b
git branch
git chekcout branchname
git merge branchname
git branch -d branchname
git branch -D branchname
```
Updating Current Branch

Standard Flow
```
git log
git log
git log --pretty=format:"%h %s" --graph
git status
git status
git status -s
git add
git add filename
git add .
git add '*.txt'
git rm
git rm filename
git commit
git commit
git commit -m
git commit --amend
```

Advanced
```
git reset
git reset
git reset --hard HEAD
git reset tag
git stash
git stash
git stash pop
git checkout filename #Goes back to the way it was
```

```
git diff
git diff HEAD
git diff branch name
git difftool -d
git tag
```

#### Working with Remote
git push
git push
git push -u origin master #The -u tells Git to remember the parameters
git push origin branchname
git pull origin branchname
git remote
git remote -v
git remote add origin https://gitremote
git fetch
git fetch
git fetch -p
###	Resources
#### Reference
Try Github
lernGitBranching http://pcottle.github.io/learnGitBranching/?NODEMO
Pro Git http://git-scm.com/book
#### Viewing History
Source Tree
Command Line Setup
https://answers.atlassian.com/questions/151279/sourcetree-command-line-option
tig
brew install tig
gitk
#### Merge/Diff Tools
Meld - `brew install meld`
Open Diff
p4v Merge - http://git-scm.com/book/en/Customizing-Git-Git-Configuration#External-Merge-and-Diff-Tools
InteliJ

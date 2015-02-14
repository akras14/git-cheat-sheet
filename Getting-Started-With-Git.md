#Getting Started with Git

## Commands
### Getting Started

`git init`

or 

`git clone url`

### Configuration

```
git config --global color.ui true
git config --global push.default current
git config --global core.editor vim
git config --global user.name "John Doe"
git config --global user.email foo@citrix.com
git config --global diff.tool meld
```
### Working with Local Branch
#### Branching
```bash
# See the list of all local branches
git branch

# Switch to existing local branch
git checkout branchname

# Checkout current branch into a new branch, named new-branch-name
git chekcout -b new-branch-name

# Merge branch-name into the current branch
git merge branchname 

# Soft branch delete, will complain if the branch is not merged
git branch -d branchname

# Hard branch delete, will not complain about nothing. Like rm -rf in bash
git branch -D branchname
```

#### Updating Current Branch

**Standard Flow**
```bash
# See all commits
git log

# Pretty commit view, you can customize it as much as you want. Just google it.
git log --pretty=format:"%h %s" --graph

# See status of your current git branch. Often will have advice on command that you need to run
git status

# Short view of status. Helpful for seeing things at a glance
git status -s

# Add modified file to be commited(aka stage the file)
git add filename

# Add all modifeid files to be commited(aka stage all files)
git add .

# Add only text files, etc.
git add '*.txt'

# Tell git not to track file anymore
git rm filename

# Record changes to git. Default editor will open for a commit message. (Visible via git log)
# Once files are commited, they are history.
git commit 

# A short hand for commiting files and writing a commit message via one command
git commit -m 'Some commit message'

# Changing the history :) If you want to change your previous commit, you can, if you haven't pushed it yet to a remote repo
# Simply make new changes, add them via git add, and run the following command. Past commit will be ammended.
git commit --amend
```

**Advanced**
```bash
# Unstage pending changes, the changes will still remain on file system
git reset

# Unstage pending changes, and reset files to pre-commit state. If 
git reset --hard HEAD

# Go back to some time in history, on the current branch
git reset tag
git reset <commit-hash>

# Save current changes, without having to commit them to repo
git stash

# And lated return those changes
git stash pop

# Return file to it's previous version, if it haven't been stage yet.
# Otherwise use git reset filename or git reset --hard filename
git checkout filename 
```

```
git diff
git diff HEAD
git diff branch name
git difftool -d
git tag
```

### Working with Remote Branch
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
##	Resources
### Reference
Try Github
lernGitBranching http://pcottle.github.io/learnGitBranching/?NODEMO
Pro Git http://git-scm.com/book
### Viewing History
Source Tree
Command Line Setup
https://answers.atlassian.com/questions/151279/sourcetree-command-line-option
tig
brew install tig
gitk
### Merge/Diff Tools
Meld - `brew install meld`
Open Diff
p4v Merge - http://git-scm.com/book/en/Customizing-Git-Git-Configuration#External-Merge-and-Diff-Tools
InteliJ

# Introduction to Git and GitHub for project management and open source

## Outline
1. What is version control?
2. What is Git?
3. Structure of Git projects
4. Basic commands
5. Hosting Git projects on GitHub
6. Push and Pull
7. Working together
8. Contributing to Open Source


## Cheatsheet of git commands

### For setup and initialization
**`git init`**: initialize an existing directory as a Git repository<br>
**git clone \[url\]**: retrieve an entire repository from a hosted location via URL<br>
**git status**: show modified files in working directory, staged for your next commit<br>
**git add \[file\]**: add a file as it looks now to your next commit (stage)<br>
**git reset \[file\]**: unstage a file while retaining the changes in working directory<br>
**git diff**: diff of what is changed but not staged<br>
**git diff --staged**: diff of what is staged but not yet committed<br>
**git commit -m “\[descriptive message\]”**: commit your staged content as a new commit snapshot<br>

### Branching and merging
**git branch**: list your branches. a * will appear next to the currently active branch<br>
**git branch \[branch-name\]**: create a new branch at the current commit<br>
**git checkout/git switch**: switch to another branch and check it out into your working directory<br>
**git merge \[branch\]**: merge the specified branch’s history into the current one<br>
**git log**: show the commit history for the currently active branch<br>
**git log branchB..branchA**: show the commits on branchA that are not on branchB<br>
**git diff branchB...branchA**: show the diff of what is in branchA that is not in branchB<br>

### Tracking path changes
**git rm \[file\]**: delete the file from project and stage the removal for commit<br>
**git mv \[existing-path\] \[new-path\]**: change an existing file path and stage the move<br>

### Sharing and updating
**git remote add \[alias\] \[url\]**: add a git URL as an alias<br>
**git fetch \[alias\]**: fetch down all the branches from that Git remote<br>
**git merge \[alias\]/ \[branch\]**: merge a remote branch into your current branch to bring it up to date<br>
**git push \[alias\] \[branch\]**: Transmit local branch commits to the remote repository branch<br>
**git pull**: fetch and merge any commits from the tracking remote <br>

### Rewrite history
**git rebase \[branch\]**: apply any commits of current branch ahead of specified one<br>
**git reset --hard \[commit\]**: clear staging area, rewrite working tree from specified commit<br>
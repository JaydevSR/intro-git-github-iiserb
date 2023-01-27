# Introduction to Git and GitHub for Project Management and Open Source Development

## First steps
1. Download git for your respective Operating system by following the corresponding instructions:<br>
    ### For Linux
    If you’re on Fedora (or any closely-related RPM-based distribution, such as RHEL or CentOS), open terminal and run
    ```
    $ sudo dnf install git-all
    ```
    If you’re on a Debian-based distribution, such as Ubuntu, try apt:
    ```
    $ sudo apt install git-all
    ```
    In case you face any issues you can refer to this [page](https://git-scm.com/download/linux) for step by step procedure

    ### For Windows
    Follow this [link](https://git-scm.com/download/win) and download the installer for the version compatible for your pc. Then open the installer to complete the installation process

    ### For Mac
    PCs with mac usually come with git already installed. You can try the following command in the terminal
    ```
    $ git --version
    ```
    and if git is not already installed, it will prompt you to install it.

2. Once you complete the first step, run the following command on the terminal
    ```
    $ git
    ```
    and you should see a prompt like the one shown below
    ![](git_cmd.png)
    If this is not the case, then follow the instructions on official [git page](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) for downloading and installing git.

3. Download GitHub CLI by following the instructions from this [page](https://github.com/cli/cli)

4. Try running the following command
    ```
    $ gh
    ```
    You should see a prompt like this
    ![](gh_cmd.png)

5. In the command line, authenticate to GitHub.
    ```
    $ gh auth login
    ```
    Now you are ready to start using git and GitHub from the Terminal!
## Outline
1. What is version control?
2. What is Git?
3. Structure of Git projects
4. Basic commands
5. Hosting Git projects on GitHub
6. Push and Pull
7. Working together
8. Contributing to Open Source

## Cheatsheets 

> Whatever included within `< ... >` is a variable i.e. is upto the user to decide.

### For basic terminal commands
- **`pwd`**: fullform is _print working directory_, tells you about the current directory
- **`ls`**: fullform is _list_, tells you the contents of the current directory
- **`cd <destination>`**: fullform is _change directory_, changes the current working directory to \<destination\>
- **`cd ..`**: changes the current working directory to the parent directory i.e. move one level up
- **`cd ~`**: changes the current working directory to the home directory
- **`mkdir <directory>`**: fullform _make directory_, creates a new subdirectory with name <directory>
- **`rm <file>`**: fullform _remove_, deletes the \<file\> permanently
- **`rm -r <folder>`**: deletes the folder recursively i.e. all the subcontents including folders
- **`mv <source> <destination>`**: fullform _move_, moves the source file to destination file
- **`mv <old name> <new name>`**: used to rename the file

> For more explaination on above commands see: https://opensource.com/article/22/5/essential-linux-commands  
> For more useful commands see: https://www.hostinger.in/tutorials/linux-commands


### Git commands

1. ***For setup and initialization***
- **`git init`**: initialize an existing directory as a Git repository<br>
- **`git clone <url>`**: retrieve an entire repository from a hosted location via URL<br>
- **`git status`**: show modified files in working directory, staged for your next commit<br>
- **`git add <file>`**: add a file as it looks now to your next commit (stage)<br>
- **`git reset <file>`**: unstage a file while retaining the changes in working directory<br>
- **`git diff`**: diff of what is changed but not staged<br>
- **`git diff --staged`**: diff of what is staged but not yet committed<br>
- **`git commit -m “<descriptive message>”`**: commit your staged content as a new commit snapshot<br>

2. ***Branching and merging***
- **`git branch`**: list your branches. a * will appear next to the currently active branch<br>
- **`git branch <branch-name>`**: create a new branch at the current commit<br>
- **`git checkout <branch-name>`** or **`git switch <branch-name>`**: switch to another branch and check it out into your working directory<br>
- **`git merge <branch>`**: merge the specified branch’s history into the current one<br>
- **`git log`**: show the commit history for the currently active branch<br>
- **`git log branchB..branchA`**: show the commits on branchA that are not on branchB<br>
- **`git diff branchB...branchA`**: show the diff of what is in branchA that is not in branchB<br>

3. ***Tracking path changes***
- **`git rm <file>`**: delete the file from project and stage the removal for commit<br>
- **`git mv <existing-path> <new-path>`**: change an existing file path and stage the move<br>

4. ***Sharing and updating***
- **`git remote add <alias> <url>`**: add a git URL as an alias<br>
- **`git fetch <alias>`**: fetch down all the branches from that Git remote<br>
- **`git merge <alias> <branch>`**: merge a remote branch into your current branch to bring it up to date<br>
- **`git push <alias> <branch>`**: Transmit local branch commits to the remote repository branch<br>
- **`git pull`**: fetch and merge any commits from the tracking remote <br>

5. ***Rewrite history***
- **`git rebase <branch>`**: apply any commits of current branch ahead of specified one<br>
- **`git reset --hard <commit>`**: clear staging area, rewrite working tree from specified commit<br>

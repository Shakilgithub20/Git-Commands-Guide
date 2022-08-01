<h1 align="center">
 Basic Git Commands
</h1>



## Git-Hub:
Git is the free and open source distributed version control system that's responsible for everything GitHub
related that happens locally on your computer. This cheat sheet features the most important and commonly
used Git commands for easy reference.


## Advantages:
  - ✔️ Better teamwork
  - ✔️ Control of changes in the project
  - ✔️ Audit and reliability
  - ✔️ Return to previous versions
  - ✔️ Local & Remotes Repositories
  - ▪️▪️▪️ And much more


### INSTALLATION & GUIS:
With platform specific installers for Git, GitHub also provides the
ease of staying up-to-date with the latest releases of the command
line tool while providing a graphical user interface for day-to-day
interaction, review, and repository synchronization.
### GitHub for Windows:
```
htps://windows.github.com
```
### GitHub for Mac:
```
htps://mac.github.com
```
For Linux and Solaris platforms, the latest release is available on
the official Git web site.
### Git for All Platforms:
```
htp://git-scm.com
```
# Commands 🚀
___

### GIT Version: 🕵

```
git --version
```

### Configure tooling :

Configuring user information used across all local repositories

```
git config --global user.name “[firstname lastname]”
```
set a name that is identifiable for credit when review version history
```
git config --global user.email “[valid-email]”
```
set an email address that will be associated with each history marker
```
git config --global color.ui auto
```
set automatic command line coloring for Git for easy reviewing



### Configure & INIT :
Configuring user information, initializing and cloning repositories
```
git init
```
initialize an existing directory as a Git repository
```
git clone [url]
```
retrieve an entire repository from a hosted location via URL

### Create a Repository 👊
``` 
# navigated into your folder you want to put on Github
$ touch README.md # create a file called README.md where you can put instructions/info about your folder like what you are reading right now!
$ git init # initialize your git repository locally
$ git add . # adds everything changed from local to staging
$ git commit -m "first commit" # commits everything in staging to be ready to be pushed to Github
$ git remote add origin https://github.com/.....
$ git push -u origin master # the "-u" is so that the next time your push you don't need to type "origin master"
# put in username & password
```

### When adding on to your repository online with changes
``` 
$ git add .
$ git add -u # when you have deleted a local file you want to remove from your repository
$ git commit -m 'what has changed'
$ git push 
# put in username & password 
```

### No more username & password input for every push
```    
# Note that you must first generate a SSH key on your local computer and add it to your 
# Github account before using the following command. Follow the directions here:
# https://help.github.com/articles/generating-ssh-keys
$ git remote set-url origin git@github.com:yourUsername/yourReponame.git
```
### Working together from perspective of person that doesn't have the main repo
``` sh
# fork repo you want to work on
$ git clone https://github.com/yourUsername/yourReponame.git
# add changes to your forked repo 
# make a pull request!
$ git pull # use this after someone else has made a change to the online repo 
           # your working on and you want to make your local repo up to date
```

### Want to remove a file frome online github repo but keep it locally
``` 
$ git rm --cached localFileName
# add localFileName to .gitignore file 
# then commit these changes
# push these changes to your repo!
```

### Commands for fixing problems
``` 
# undo multiple commits  
$ git reset --hard commitSHA###... # changes staging index and 
                                   # local folder to match online 
                                   # repository commit

# removing 3 commits from online github repo
$ git push -f origin HEAD^^^:branchNameToUndoLast3Pushs
```

## Branches
| Command | Description |
| - | - |
| `git branch foo`                          | Create a new branch |
| `git branch -d foo`                       | Deletes a branch |
| `git switch foo`                          | Switch to a branch |
| `git switch -c\|--create foo`             | Create and switch to a branch |
| `git restore foo.js`                      | Undo all changes on the foo.js file |
| `git checkout foo.js`                     | Undo all changes on the foo.js file |
| `git checkout foo`                        | Use `git switch` instead |
| `git checkout -b foo`                     | Use `git switch -c` instead |
| `git merge foo`                           | Merge branch into current branch |



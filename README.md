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

### Creating a repository online for the <b>1st time</b>!
``` 
# navigated into your folder you want to put on Github
$ touch README.md # create a file called README.md where you can put instructions/info about your folder like what you are reading right now!
$ git init # initialize your git repository locally
$ git add . # adds everything changed from local to staging
$ git commit -m "first commit" # commits everything in staging to be ready to be pushed to Github
$ git remote add origin https://github.com/quinnliu/GitCommands.git
$ git push -u origin master # the "-u" is so that the next time your push you don't need to type "origin master"
# put in username & password
```


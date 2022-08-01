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

### Configure tooling 🌍 :

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
``` 
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
### Help Command 🙏

```
git help  
```

### Get help from a specific command 👏

<pre>
git help <b>commit</b>
</pre>


## Branches
| Command | Description |
| - | - |
| `git branch foo`                          | Create a new branch |
| `git switch foo`                          | Switch to a branch |
| `git switch -c\|--create foo`             | Create and switch to a branch |
| `git restore foo.js`                      | Undo all changes on the foo.js file |
| `git checkout foo.js`                     | Undo all changes on the foo.js file |
| `git checkout foo`                        | Use `git switch` instead |
| `git checkout -b foo`                     | Use `git switch -c` instead |
| `git merge foo`                           | Merge branch into current branch |


## Delete 
| Command | Description |
| - | - |
| `git branch -d <branchname> `                       | Delete the local branch, show a warning|
| `git branch -D <branhcname> `                       | Force to delete branch|
| `git remote prune origin `                          | Cleanup remote deleted branch |



## Pulling
| Command | Description |
| - | - |
| `git pull --rebase --prune`               | Get latest, rebase any changes not checked in and delete branches that no longer exist | 

## Staged Changes
| Command | Description |
| - | - |
| `git add file.txt`                        | Stage file |
| `git add -p`|--patch file.txt`            | Stage some but not all changes in a file |
| `git mv file1.txt file2.txt`              | Move/rename file |
| `git rm --cached file.txt`                | Unstage file |
| `git rm --force file.txt`                 | Unstage and delete file |
| `git reset HEAD`                          | Unstage changes |
| `git reset --hard HEAD`                   | Unstage and delete changes |
| `git clean -f\|--force -d`                | Recursively remove untracked files from the working tree |
| `git clean -f\|--force -d -x`             | Recursively remove untracked and ignored files from the working tree |

## Changing Commits
| Command | Description |
| - | - |
| `git reset 5720fdf`                           | Reset current branch but not working area to commit |
| `git reset HEAD~1`                            | Reset the current branch but not working area to the previous commit |
| `git reset --hard 5720fdf`                    | Reset current branch and working area to commit |
| `git commit --amend -m "New message"`         | Change the last commit message |
| `git commit --fixup 5720fdf -m "New message"` | Merge into the specified commit |
| `git revert 5720fdf`                          | Revert a commit |
| `git rebase --interactive [origin/main]`      | Rebase a PR (`git pull` first) |
| `git rebase --interactive 5720fdf`            | Rebase to a particular commit |
| `git rebase --interactive --root 5720fdf`     | Rebase to the root commit |
| `git rebase --continue`                       | Continue an interactive rebase |
| `git rebase --abort`                          | Cancel an interactive rebase |
| `git cherry-pick 5720fdf`                     | Copy the commit to the current branch |

## Compare
| Command | Description |
| - | - |
| `git diff`                                | See difference between working area and current branch |
| `git diff HEAD HEAD~2`                    | See difference between te current commit and two previous commits |
| `git diff main other`                     | See difference between two branches |

## View
| Command | Description |
| - | - |
| `git log`                                 | See commit list |
| `git log --patch`                         | See commit list and line changes |
| `git log --decorate --graph --oneline`    | See commit visualization |
| `git log --grep foo`                      | See commits with foo in the message |
| `git show HEAD`                           | Show the current commit |
| `git show HEAD^` or `git show HEAD~1`     | Show the previous commit |
| `git show HEAD^^` or `git show HEAD~2`    | Show the commit going back two commits |
| `git show main`                           | Show the last commit in a branch |
| `git show 5720fdf`                        | Show named commit |
| `git blame file.txt`                      | See who changed each line and when |

## Stash
| Command | Description |
| - | - |
| `git stash push -m "Message"`             | Stash staged files |
| `git stash --include-untracked`           | Stash working area and staged files |
| `git stash --staged`                      | Stash staged files |
| `git stash list`                          | List stashes |
| `git stash apply`                         | Moved last stash to working area |
| `git stash apply 0`                       | Moved named stash to working area |
| `git stash clear`                         | Clear the stash |

## Tags
| Command | Description |
| - | - |
| `git tag`                                              | List all tags |
| `git tag -a\|--annotate 0.0.1 -m\|--message "Message"` | Create a tag |
| `git tag -d\|--delete 0.0.1`                           | Delete a tag |
| `git push --tags`                                      | Push tags to remote repository |

## Remote
| Command | Description |
| - | - |
| `git remote -v`                           | List remote repositories |
| `git remote show origin`                  | Show remote repository details |
| `git remote add upstream <url>`           | Add remote upstream repository |
| `git fetch upstream`                      | Fetch all remote branches |
| `git rebase upstream/main`                | Refresh main branch from upstream |
| `git remote -v`                           | List remote repositories |
| `git push --force`                        | Push any changes while overwriting any remote changes |
| `git push --force-with-lease`             | Push any changes but stop if there are any remote changes |
| `git push --tags`                         | Push tags to remote repository |

## Submodules
| Command | Description |
| - | - |
| `git submodule status`                    | Check status of all submodules |

- Pull submodules
  1. `git submodule sync`
  2. `git submodule init`
  3. `git submodule update`
- Change branch
  1. `cd /submodule`
  2. `git fetch origin <branch-name>`
  3. `git checkout <branch-name>`
  4. `cd /`
 
### Commit:

Add & commit
 ```
git commit -am 'commit message'   
```
Commit empty change
```
git commit --allow-empty -m k3;
```
Take a commit change of another branch 
```
git cherry-pick <commit-hash>  
```
### Amend
 Add any file
 ```
 git add task2.txt 
 ```
 Merge current change to previous commit and will also change the commit hash
 ```
 git commit --amend -m 'new message'
 ```
 ### Merge
 Merge remote 'branch-1' with current branch
 ```
 git merge origin <branch-1>   
 ```
 git mergetool
 ```
 git merge --squash <privateFeatureBranch>
 ```

# Appalacian Skydive
You get to skydive inside the Appalachian Mountains, which are inexplicably hollow. You mine stuff on the way down. No parachutes. 
This is the second edition of the zero-indexed series called Appalachian Skydive.

## Installallation Instructions for Contributors (Windows only)

### What you need
* Git: https://git-scm.com/downloads
* Android Studio: https://developer.android.com/studio/index.html
* Java Development Kit 8: http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html

### Cloning the Repository
1. Once you have git, navigate to wherever you want to keep your code. I keep mine in a folder in My Documents.
2. Right click > "Git Bash Here"
3. Run this command (shift+insert is how you paste):
```
git clone https://github.com/mac-chaffee/appalachian-skydive.git appalachian-skydive
```
### Setting up Android Studio
1. Once you have Android Studio an JDK, open up Android studio
2. Select "Open an existing Android Studio Project"
3. Select the "appalachian-skydive" folder from wherever you installed it
4. If you don't see the project hierarchy in the sidebar, make sure the dropdown box above it says "Project" instead of "Android"

### Basic Git Commands
* `git status`

Shows what changes you have, what branch you're on, how many commits you haven't pushed yet, etc.

* `git pull`

Downloads any changes that other people have made to your current branch. This could cause conflicts, so I highly recommend running this command: `git config --global pull.rebase true` so that it will [rebase](https://git-scm.com/docs/git-rebase) every time you pull, drastically reducing the number of merges.

* `git add .`

If you've added files to your local folder and you want to make sure git keeps track of them, just go ahead and add eveything (".")

* `git commit -am "Updated readme with git instructions"`

Bundles up all your changes ("-a") under a message ("-m") that describes those changes.

* `git push` 

Takes all your commits and uploads them to the remote server (by default).

### Advance Git Commands
Using git "the right way (tm)": Whenever you're working on a big feature, it's good practice to do it on your own branch (not master) named after that feature. For example, if you're fixing hitboxes, checkout the 'hitboxes' branch, made a couple commits, rebase if you need to, and then merge it back into master. It makes for prettier [git trees](https://imgs.xkcd.com/comics/git_commit.png)

* `git checkout -b nameofnewbranch`

Changes to a brand new branch of your choosing. To switch to one that already exists, just don't include the `-b`.

* `git branch -d nameofbranchtodelete`

Deletes a branch. Careful.

* `git push origin nameofbranch`

Pushes your changes to the server ("origin"), but on a specific branch. `git push` by itself while on a different branch will try to push to master, which would be messy.

* `git rebase nameofotherbranch`

Say you're working on a featur on your own branch. Suddenly someone pushes changes to master, and you want those changes. You can move the "base" of your branch up the tree so that it sprouts off of their changes. This will add their changes to your branch.

* `git merge --no-ff -log nameofbranchtomergein`

When you finish working on your local branch and you want to add those changes to master, checkout the master branch and run this command with the name of your local branch. `--no-ff` to keep our tree looking pretty, and `-log` to include some helpful text in the merge commit.


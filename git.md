#Git

//the Github workflow//
## After you make a github account online
0. First for real open the computer's command line
  - for windows click on the start and type "cmd"
    - this black box is where you type commands and this is how you talk to your computer and begin your journey with git, coding, and making stuff happen.
  - once you have a github set up and you want to keep working you are going to use another command line that is more customized for git and it has fun colors. This is called git bash and is a command line. You type commands where the dollar sign is.
1. b `cd` change directory aka folder to your desired workspace
  - to find directories type `ls` then type `cd [directory]`
    - like opening a folder in windows explorer
  - `mk dir` makes a new directory aka folder
  - pay attention the yellow filepath so you know you are in the place/ folder you want to be in.
1. b  First thing you need to do when starting a new repo is `git init`.
  - a repo is a repository. This is like a folder
  - `git init` will make a git repository in your current directory location that is why you change directory to your workspace/directory/folder first
2. open your git in atom `atom .`
  - atom is a text editor. This is where you write your code then use git bash to make commands to view the status of the code, to confirm edits to the code, and to push the edits up to git hub.
  - You can create a new file in this directory using one of 2 methods.  Both methods do the same thing, add a file to the directory on your operating system.
  * another good text editor is sublime. You can also write code in an IDE - Integrated Desktop Environment. You can have your larger code file and a practice input output space and your terminal in one application. In short you can open up applications from the command line as well.
  - non IDE the code you write can run in your command line which is the terminal. for example to run python code type `python filename.file` to run the functions/ code etc.
    2. in your command line terminal (git bash) type the command from within your directory `touch [filename].file`
      - `.file` meaning like `.py` or `.md` or `.html` or whatever file type you need to create.
      - this is a weird name `¯\_(ツ)_/¯`
      - .md stands for markdown it is like metadata for code. like a text document.
3. make code or just type stuff in your .md file then version management steps below
4. check status of git directory `git status`
  - if you did not save
  - if you did not make any changes
      then then it will say "your branch is up-to-date with 'origin master' nothing to commit, working tree clean"
  - after you save your code in your text editor git status will show you "modified: [fielname].md" in red text new files will be in red under text that says "Untracked files:"
2. add all files `git add .` then check status again in 1.
  - this is like saving/updating the changes in the command line space.
  - `git add.` adds all the new files in your current path.
  - after you check the status again with `git status`
  - this time it should be green and will say "modified: [filename].file"
3. `git commit -m "info about edits"`
  - this is like a little packet of edits you are ready to push up to github and you give the edits a little name
  - if you added new files but did not `git .` added them the new file will not be included in the commit.
  - once the file is up in the remote repo online you don't need to do `git add filename.file` after the file is there you just commit changes to it going forward. *or you still do git add??*
4. you can `git push` to move your local changes up to the remote Github
 - yay! see your changes on github!
 On the same repo- going forward first thing to continue on project:
5. pull git down `git pull origin master`
  - pulls down the latest changes to your git/code/repository;
  - makes local master current with remote master
*5* also note that you need to accept/deal with any other changes that have happened to your remote githup repository before you push your local changes to origin master.


##### if you want to start a new project from scratch, where no one has anything yet
  1. create a new directory, `cd` into it, and initialize it as a git repository with the command `git init` (you will automatically be on the master branch)
    - in text editor files tree in your new repo/project folder you see a .git Folder. like making your local folder git enabled
  2. make some files, write some stuff
  3. `git add <files you want to commit>` to add the changes to staging
  4. `git commit -m <some message that describes the changes>` to commit those changes to your local repo.  Imagine an invisible set of files that you want to send up to the remote repo.
  4. Go to github and start a new project
  4. in your command line do what it says on github, something like `git remote add origin https://github.com/user/newrepo.git`
    - making the new repo on github
    - no < >
    - ends in `.git`
    - `newrepo` is the same name of your project folder
    - `newrepo` is the
  5. `git push origin master` pushes your local repo up to your remote repo
  6. if someone else does something to the repo you want to make your local repo reflect that, so you `git pull` to "pull" down the changes they made from the remote repo.

###### Pull your own repo down to your computer
 1. 'git clone /path/to/repository'
 ???

###### If you're starting on someone else's project
  1. Go to github and find their project
  2. copy the url github provides you (not what you see in the address bar)
  3. in the command line `git clone <project url>`
  4. `ls` to find the name of the repo that just got cloned
  5. `cd` into the newly cloned repo
  6. do steps 1 - 6 from above

#### Merge pull request
  1. `git branch` lists out other branches which include pull requests
  2. make local branch `git checkout -b [branch name]`
  3. `git pull origin [branch name]`
    Example Returns: From https://github.com/akell47/amber_aid
      * branch            improves-git-flow -> FETCH_HEAD
        Merge made by the 'recursive' strategy.
        git.md | 25 +++++++++++++++++++++++--
        1 file changed, 23 insertions(+), 2 deletions(-)
  4. `git checkout master` change over to master branch because will    merge the pull request into master branch      
  4. `git merge [branch name]` merges other branch to master branch locally
  5. `git push origin` pushes merged master branch back up to github
  yay!


### Branches
  versions of repo called branches
  don't make a change to the master branch directly
  1. `get checkout -b "branchname git URL"``
  2. `clone`
  3. `git branch` list the current branch you are on
  3. `git branch branchname` create a branch

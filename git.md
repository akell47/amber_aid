#Git

//the Github workflow//

0. First for real open the computer's command line
  - for windows click on the start and type "cmd"
    - this black box is where you type commands and this is how you begin your journey with git. Now you can start the "git guide."
  - once you have a git set up and you want to keep working you are going   to use another command line that is more customized for git and it has fun colors. This is called git bash and is a command line. You type commands where the dollar sign is.
1. `cd` change directory aka folder to your desired workspace
  - to find directories type `ls` then type `cd [directory]`
    - like opening a folder in windows explorer
  - `mk dir` makes a new directory aka folder
1.  First thing you need to do when starting a new repo is `git init`.
  - a repo is a repository. This is like a folder
  - `git init` will make a git repository in your current directory location that is why you change directory to your workspace/directory/folder first
2. open your git in atom `atom .`
  - atom is a text editor. This is where you write your code then use git bash to make commands to view the status of the code, to confirm edits to the code, and to push the edits up to git hub.
  - You can create a new file in this directory using one of 2 methods.  Both methods do the same thing, add a file to the directory on your operating system.
    1. left click on the directory in the gutter of atom and choose to create a file.
    2. in your command line terminal (git bash) type the command from within your directory `touch [filename].md`
      - this is a weird name that does create the file but the name doesn't really make sense here `¯\_(ツ)_/¯`
    - .md stands for markdown it is like metadata for code. like a text document.
3. make code or just type stuff in your .md file then version management steps below
4. check status of git directory `git status`
  - if you did not save
  - if you did not make any changes
      then then it will say "your branch is up-to-date with 'origin master' nothing to commit, working tree clean"
  - after you save your code in your text editor git status will show you "modified: [fielname].md" in red text
2. add all files `git add .` then check status again in 1.
  - this is like saving/updating the changes in the command line space.
  - after you check the status again with `git status`
  - this time it should be green and will say "modified: [filename].md"
3. `git commit -m "info about edits"`
  - this is like a little packet of edits you are ready to push up to github and you give the edits a little name
4. you can `git push` to move your local changes up to the remote Github
 - yay! see your changes on github!
 On the same repo- going forward first thing to continue on project:
5. pull git down `git pull origin master`
  - pulls down the latest changes to your git/code/repository;
  - makes local master current with remote master

#### The general flow is this.
###### if you want to start a new project from scratch, where no one has anything yet
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

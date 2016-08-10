#Git

//the Github workflow//

0. First for real open the computer's command line
  - for windows click on the start and type "cmd"
    - this black box is where you type commands and this is how you begin your journey with git. Now you can start the "git guide."
  - once you have a git set up and you want to keep working you are going   to use another command line that is more customized for git and it has nice colors. This is called git bash and is a command line.
1.  First thing you need to do when starting a new repo is `git init`.
  - a repo is a repository. This is like a folder
2. open your git in atom `atom .`
  - atom is a text editor. This is where you write your code then use git bash to make commands to view the status of the code, to confirm edits to the code, and to push the edits up to git hub.
3. make code then version management steps below
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
5. pull git down `git pull`
  - `git pull` will tell you an update about the latest changes to your git/code/repository
  - ???? start wit `git pull` or `git init` ??

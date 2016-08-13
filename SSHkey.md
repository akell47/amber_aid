###SSH Key

Access key - how the computer connects and talks to your repository inside the command line shell. Authenticate the user to the remote computer
SSH - Secure Shell

1. Open git Bash
2. `ssh-keygen -t rsa -b 4906 -C "youremail@email.com"`
  makes new ssh key
  Returns: "generating public/private rsa key pair"
  Enter file in which to save the key (/c/Users/amber.keller/.ssh/id_rsa):
3. Press Enter
4. Enter passphrase (empty for no passphrase):
5. Type a password then type it again
  Returns: Makes a "random art image" - fancy!
6. Turn on ssh-agent `eval "$(ssh-agent -s)"`
  turns on ssh-agent
7. add ssh key to the ssh-agent `ssh-add ~/.ssh/id_rsa`
  Returns: Identity added: /c/Users/amber.keller/.ssh/id_rsa (/c/Users/amber.keller/.ssh/id_rsa)

add ssh key to github
8. bash version of `ctrl + c` copy ssh key to your clipboard `clip < ~/.ssh/id_rsa.pub`
9. in the browser in github go to Profile > Settings > click `SSH and GPC keys` > click > `New SSH Key` paste into the Key box.

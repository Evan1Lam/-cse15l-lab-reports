# Lab report 3
## streamlining ssh Configuration

* create a file called config in VScode, with the following lines of code to set up a new hostname `ieng6` for remote computer account. 

![Image](sshConfig.png)

* we can now ssh by just typing `ssh ieng6` instead of having to type out the entire username `cs15lsp22auq@ieng.ucsd.edu`.

![Image](shhCommand.png)

* we can also scp with this abreviated new hostname, by just typing `scp <file name> ieng6:~/`. As seen in the image this successfully copies a file into our remote computer.

![Image](scpCommand.png)


## Setup Github Access from ieng6

**public key stored on Github**

* enter `pbcopy < ~/.ssh/id_rsa.pub` in terminal to copy the public key, go to user settings on GitHub, click on SSH and GPG keys in the side bar, click on New SSH key, name your key, and then paste the public key into box and save it. This allows us to use git commands to commit and push to main in the terminal without having to enter username or password. 

![Image](GitHubKeys.png)

**public key stored in user account**

* to view this, ssh into remote computer, enter `cd .ssh`, then enter `ls -al`, and the ssh keys will display. `id-rsa.pub` is the public key, and we can enter `more id_rsa.pub` to view the key itself 

![Image](publicKeyUserAccount.png)

**private key stored in user account**

* follow the steps to view public key and the private key is `id-rsa`. Or, instead of entering `ls -al`, enter `ls -al id_rsa` to view the key on its own.

![Image](privateKeyUserAccount.png)

**running git commands to commit and push a change to Github while logged into ieng6**

* using the public key created for ieng6, we can commit changes to files from the command line. `git status` informs us if a change has been made, then to commit and push a file, enter in the following commands: `git add <file name>`, then `git commit -m "<insert whatever commit message>"`,then `git push origin main`. Because the public key has been stored on gitHub there will be no prompt for username or password.

![Image](gitCommandsCommitieng6.png)

**link for resulting commit**

* we can view the commit on gitHub by clicking on commits. Here is the link to a commit made on MarkdownParse.java, where a comment was added.

[MardownParse.java commit Link](https://github.com/Evan1Lam/markdown-parser/commit/b82543af9e48dddc7c064757126b928151bca015)






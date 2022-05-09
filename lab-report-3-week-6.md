# Lab report 3
## streamlining ssh Configuration

![Image](sshConfig.png)

* create a file called config in VScode, with the following lines of code to set up a new hostname `ieng6` for remote computer account. 

![Image](shhCommand.png)

* we can now ssh by just typing `ssh ieng6` instead of having to type out the entire username `cs15lsp22auq@ieng.ucsd.edu`.

![Image](scpCommand.png)

* we can also scp with this abreviated new hostname, by just typing `scp <file name> ieng6:~/`. As seen in the image this successfully copies a file into our remote computer.

## Setup Github Access from ieng6


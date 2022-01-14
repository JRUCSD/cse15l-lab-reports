# CSE 15L Lab Report 1
## How to Access a Remote Server

### Installing VSCode
Visit [code.visualstudio.com](https://code.visualstudio.com/), download & install Visual Studio Code on your device. When complete, open VSCode if it does not automatically. The first thing you should see is the *Getting Started* page, but after clearing it you should see a screen like this:
(The colors may be different depending on your display settings in VSCode)
![VSCode Getting Started](VSCodeStart.png) 
![VSCode Empty](VSCodeEmpty.png)
### Remotely Connecting
**For Windows Users**, Before actually connecting to a server, another install is required. Install OpenSSH by opening the Settings, navigating to Apps > Apps & Features, and selecting Optional Features. From there find Open SSH Client & Open SSH Server and install them if they aren't already installed.


### Testing Some Commands
### Moving Files with `scp`
### Setting an SSH Key
To skip typing out your password every time you want to log in remotely, use SSH Keys. Simply type `ssh-keygen` in the terminal, enter where you want to store the file that contains your key and your done. Don't worry about memorizing the generated randomart image, you won't need to type it in for login. `ssh-keygen` generates 2 keys, one public and one private. The public key is stored on the server and the private key is stored on the client. Don't share the private key, it's called a private key for a reason. When you want to login again with `ssh` or copy files with `scp`, the two keys are compared and if they match, you are logged into the remote server, no password necessary.
### Optimizing Remote Running
Helpful shortcuts in the terminal:
- Wrapping a command in quotes after an ssh command will run the command remotely and exit the remote connection
- Using semicolons allows for multiple commands to be run on one line in the terminal
    - Combining the above steps allows multiple commands to be run remotely
- Use the up arrow to recall the most recent commands

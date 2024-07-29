# Getting Started

Now when it comes to programming of any kind I would suggest to use a linux operating system as it is easier to program in Linux for a few reasons: the command line interface is a little more flexible than windows, there are many text editors in linux you can use to code with, and there are built in development tools just to name a few. The next few headers are dedicated to using the command line in linux to set up git and to connect a local repository to github. Now for those who want to use linux and do not want to use a virtual machine to install linux then there is Windows subsystem for Linux which will create a version of linux as a subsystem on Windows. Meaning you can use linux within the Windows OS. I would suggest using this for most people. 

But for those who do not really want to use Linux, although I do not advise it, and want to just use Windows you can use Github Desktop. Github Desktop is the desktop application to interact with Git and Github in a GUI. Although Git already has a GUI with it, however it does not have an easy way to connect to Github like Github Desktop does. But there is a header dedicated to using Github Desktop you can go to below. 

## Command Console - For Linux and WSL

Here I'll explain how to just use Git locally. We are not connecting anything yet to Github just yet. But let's start off with some basics and start with initializing a repository for a test project. First make sure to create a folder to hold your project and the use ```git init```. This will initialize your repository. To commit all your files you have to use ```git add.``` and then ```git commit -m "Initial commit"```. 

Here are the commands in order with comments:

```bash
# 1. Create project directory
mkdir myProject

# 2. Change directory into myProject directory
cd myProject

# 3. Initialize repository
git init

# 4. Stage files to commit
git add .

# 5. Commit files with a message that says "Initial commit"
git commit -m "Initial commit"
```

### SSH Keys - Linux and WSL

Now in order to get your projects to your github you need to create a public key for your Github and a private key for your device. I am going to follow the github page here: ```https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent```

The first step on you have to do is use this command to create a public/private pair:

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

The second step is to enter a passkey for the public/private pair

Third, start the ssh-agent in the background with this command:

```bash
eval "$(ssh-agent -s)"
```

Fourth, add the private key to the ssh-agent:

```bash
ssh-add ~/.ssh/id_ed25519
```
Fifth, add the public key to github under Profile settings -> SSH keys -> New SSH key, then past the public key from the .ssh directory

## GUI With Github Desktop - More Practical for Inexperienced Users

### How to Create a Repository With Github Desktop

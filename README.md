# How to Connect VSCode to GitHub Using SSH Key

 This repository contains a comprehensive step-by-step guide on connecting Visual Studio Code (VSCode) to GitHub using SSH keys. This guide is designed to help you clone a repository, make changes, and commit those changes back to GitHub securely.

## What You'll Learn
- Generating an SSH key
- Adding the SSH key to your GitHub account
- Cloning a GitHub repository using SSH
- Making changes to the repository in VSCode
- Committing and pushing changes to GitHub

## Step-by-Step Guide

### Step 1: Generate SSH Key

In Windows PowerShell, issue the following `ssh-keygen` command to create a GitHub SSH key:

```powershell
PS C:\github\ssh\example> ssh-keygen -o -t rsa -C "example@gmail.com"
```

### Step 2: Locate SSH Key

You will get the location of your SSH key after executing the above command. For example, the location might be C:\Users\Lenovo\.ssh.

### Step 3: Copy SSH Key

Open the file named id_rsa and copy all the text written in the file. If the file is not opening, you can use VSCode to open the file. Remember, there are two id_rsa files; copy the text that contains your email that you provided above, i.e., example@gmail.com.

![Alt text](https://itknowledgeexchange.techtarget.com/coffee-talk/files/2022/01/github-ssh-keygen-key-pub.jpg)

### Step 4: Add SSH Key to GitHub

1. Open your GitHub account.
2. Go to Settings > SSH and GPG keys.
3. Click on New SSH key.
4. In the key section, paste the key that you copied earlier.

![Alt text](https://itknowledgeexchange.techtarget.com/coffee-talk/files/2022/01/github-ssh-key-config.jpg)

### Step 5: Clone Repository

1. Go to the repository that you want to clone.
2. Click on Code.
3. Click on SSH and copy the link.

### Step 6: Open the vscode terminal 

Open the desired folder where you want the clone of repository

1. To start the git bash
```powershell
git init
```
2. To clone the repository
```powershell
git clone "paste the copied link"
```
3. To add all the changes made in the files
```powershell
git add .
```
4. To finally commit all the changes locally on the system
```powershell
git commit -m "changes made"
```
5. To push the changes back to Github
```powershell
git push -u origin main
```

# Repro - Training

The following is for macOS. 

## Required Installation

Github: 

[Set up Git - GitHub Docs](https://docs.github.com/en/get-started/quickstart/set-up-git)

anaconda: 

[Free Download | Anaconda](https://www.anaconda.com/download)

## [1] Check versions of Software

```bash
>git --version
git version 2.37.0 (Apple Git-136)
>conda -V
conda 4.12.0l
>python
Python 3.8.8 (default, Apr 13 2021, 12:59:45) 
```

## [2] Fork Repository

Fork my repository in Github to your personal account

[https://github.com/therapeutic-ultrasound/template](https://github.com/therapeutic-ultrasound/template)

## [2.1] Create a Personal Access Token

Use a [Personal Access Token (PAT)](https://github.com/settings/tokens) 

- You can access this by creating a new token in your Github Account (User>Setting>Developer Settings>PAT)
- Copy the token and use it in place of a password

## [3] Clone Repository

Clone the forked repo on your local machine 

```jsx
>git clone https://github.com/paulina-rodriguez/repro-template.git
```

You will be prompted to enter your Github Account USERNAME 

You will be prompted to enter your password but you will use the **Personal Access Token**

Enter the repository 

## [4] Modify Jupyter Notebook

If necessary enable anaconda environment. Not necessary by default.

```jsx
conda activate
```

Open Jupyter notebooks (this will open the directory you are currently in on a browser 

```jsx
jupyter notebook
```

Edit the Jupyter Notebook in a locally rendered browser. 

To render/compile a cell use `shift`  + `enter`

Save and close notebook in browser tab and close session in the terminal with:

```jsx
ctr+c
```

Note: To finalize the report create a pdf of the current jupyter notebook and create a python script of the jupyter notebook. (Tentative?????) 

## [7] Store & Push Git changes

```bash
>git add .  
>git add filename.txt
>git commit -m 'Describe what changes you made'
>git push 
>git pull
```

Remember that git doesn’t automatically save changes in your local repository only. Commit frequently to keep track of important checkpoints in your project. When pushing changes, the changes will be available to everyone on that repository. 

Approach: 

1) `git status` to see what files are changed (will be red)

2) `git add .` (all files) or `git add fileName.txt` in order to choose which file changes you are going to save. 

3) `git status` to make sure the right files are staged/ready to be saved (will be green)

4) `git commit -m "describe what changes you made"` in order to save the changes that were made. This will create a unique identifier and the comment will be used as a descriptor. 

5) `git status` to make sure that all necessary changes were saved. 

6) `git push` to send changes to the Github repository, project repository. 

Extra: If there were additional changes you don’t want to keep, you can `git add` the specific files and then `git stash` to move them out of sight, but if you don’t need to recover them at some point then you can `git stash drop` to permanently delete those changes. 

Additional useful commands: 

- To see what’s going on in your local repository: `git status`
- To clean your local repository and remove unwanted changes (aka untracked files): `git stash` and then to permanently delete these unwanted tracked changes `git stash drop`

## Useful bash commands

```bash
pwd # shows the path to the current directory
ls  # lists what's in the current directory/folder
ls -al # lists what's in the current directory with more info.
cd Desktop/folderName # enters the directory located in this path 
mkdir NewFolder # create a new folder and call it NewFolder
cd ~ # enters the home directory
history # shows the last few terminal commands 
```

## Resources:

[GitHub - paulina-rodriguez/repro-template: General Reproducibility Package](https://github.com/paulina-rodriguez/repro-template)

[git - Essential skills for reproducible research computing](https://barbagroup.github.io/essential_skills_RRC/git/git/)

[Creating a personal access token - GitHub Docs](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)

[Build software better, together](https://github.com/settings/tokens)

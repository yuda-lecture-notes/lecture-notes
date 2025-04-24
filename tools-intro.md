# Tools Introduction

## Table of Contents
- [Terminal/CMD](#terminalcmd)
- [Anaconda](#anaconda)
- [VSCode](#vscode)
- [Git](#git)
- [GitHub](#github)
- [Videos to Watch](#videos-to-watch)

## Terminal/CMD
### Shell Commands
- For Windows, learn more about some useful commands [here](https://www.ninjaone.com/blog/windows-cmd-commands/)
- For Mac/Linux, learn more [here](https://www.techrepublic.com/article/16-terminal-commands-every-user-should-know/) or [here](https://www.digitalocean.com/community/tutorials/linux-commands#top-50-linux-commands-you-must-know-as-a-regular-user)

### Keyboard Shortcuts
- For Windows, learn more about some useful shortcuts [here](https://www.howtogeek.com/254401/34-useful-keyboard-shortcuts-for-the-windows-command-prompt/)
- For Mac/Linux, learn more [here](https://www.idownloadblog.com/2020/03/10/mac-keyboard-shortcuts-terminal/) or [here](https://itsfoss.com/linux-terminal-shortcuts/)

## Anaconda
### Definition
- **Anaconda** is an open-source distribution of Python and R programming languages, mainly suitable for Data Science projects.
- Miniconda is a smaller version of Anaconda, both have same functionality and features.
- **Conda** is a CLI app that enables user to manage packages and environments.
- Conda can be accessed with **Anaconda Prompt** or with built-in **Terminal** (MacOS/Linux) and **CMD** (Windows)
- **Environment** is an isolated workspace that contains a specific collection of packages. ([reference](https://carpentries-incubator.github.io/introduction-to-conda-for-data-scientists/02-working-with-environments/index.html#what-is-a-conda-environment))
  ![image](https://github.com/user-attachments/assets/17222b6b-68d2-4a8a-a940-cbbcc11bf8ad)

### Conda Cheatsheet ([reference](https://docs.conda.io/projects/conda/en/latest/_downloads/843d9e0198f2a193a3484886fa28163c/conda-cheatsheet.pdf))
```shell
# verify conda installation or check version
conda --version

# check current environment
conda info

# Display list of environments. The active environment will be labeled with asterisk (*) symbol
conda info --envs

# install package named "Pandas"
conda install pandas

# install package with specific version
conda install selenium=1.2

# remove/uninstall package
conda remove scipy

# Display list of installed packages in current environment
conda list

# create new environment named "Env1"
conda create --name Env1

# create new environment with python and pandas package installed
conda create --name Env1 python pandas

# delete specific environment
conda remove --name Env1 --all

# activate specific environment
conda activate Env1

# deactivate environment (base)
conda deactivate

# update conda to the latest version (if available)
conda update conda
```

### Pip Cheatsheet ([reference](https://opensource.com/sites/default/files/gated-content/cheat_sheet_pip.pdf))

- Just like `conda`, `pip` command is also can be used to manage packages within the environment.
- To use `pip` command it is required to have python installed in the environment.

```shell
# install package with latest version
pip install pandas

# install package with specific version
pip install pandas==2.0.0

# remove/uninstall package
pip uninstall scipy

# Display list of installed packages in current environment
pip list
```

### Troubleshoot `conda command not recognized` (**Windows only**) ([reference](https://saturncloud.io/blog/solving-the-conda-command-not-recognized-issue-on-windows-10/))
1. Open Terminal/CMD
2. Execute `conda --version`, it should display the version number.
3. If it displays `conda command not recognized`, open the Start Menu and search for "Environment Variables".
4. Click on "Edit the system environment variables".
5. In the System Properties window, click on "Environment Variables". <br>
   ![image](https://github.com/user-attachments/assets/93a65a8b-c5a4-4b1d-ba50-0a460462ac8d)
6. In the Environment Variables window, under "System variables", find and select "Path", then click on "Edit". <br>
   ![image](https://github.com/user-attachments/assets/f0d1d61a-58ef-4d99-be3a-1d7f5b3ed04d)
7. In the Edit Environment Variable window, click on "New". <br>
   ![image](https://github.com/user-attachments/assets/142cdbda-b908-4bd8-9659-b33afb77c8e2)
8. Add the path to the directory where Anaconda/Miniconda is installed, usually in `C:\Users\YourUsername\Anaconda3\Scripts`.
   - You can verify this by opening Anaconda Prompt and execute `where conda` command. It will give you the same output like above.
9. Click "OK" on all windows to save the changes.
10. Close and reopen Terminal/CMD.

## VSCode
### Select Default Profile (**Windows only**) ([reference](https://www.shanebart.com/set-default-vscode-terminal/))
1. Press `CTRL + SHIFT + P` to open the Command Palette
2. Search for `Terminal: Select Default Profile`
   ![image](https://github.com/user-attachments/assets/f94c4b98-5f78-4dd8-9f61-e3643ef50051)
3. Select `Command Prompt` <br>
   ![image](https://github.com/user-attachments/assets/570e01e8-76c3-40ad-b5ce-12e458aa210c)
4. Close and reopen the VSCode.

### Python Quickstart
- There are 2 file extensions that can be used to run python
   - Script file: `.py`
     - To run a script file, execute the following command in the Terminal
       ```shell
       python filename.py
       ```
       > **Notes**
       > - Make sure to have Conda installed and is using `base` environment.
       > - Make sure that the file exist within the current directory.
   - Notebook file: `.ipynb`
     - Notebook is a special extension that can be used to create a report, analysis, or summary using python.
     - Notebook consist of 2 cells component, **markdown/text** and **code**.
     - Markdown/Text cell is used to add narration, explanation, or insight. It is also can be used to give heading for separating each section of the content.
     - Code cell is used to execute a python script within the file.
     - To run a code inside the notebook, we can use the **Run All** button or **Execute** button in each code cell.
    
### `readme.md` File
- **readme.md** file contains information to understand what the project is about.
- This file is written using Markdown syntax. You check out these references to get familiarized with it:
   - [Basic Writing and Formatting - GitHub](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
   - [CommonMark](https://commonmark.org/help/)

## Git
### Definition
- **Git** is a Version Control System (VCS) that helps **track code changes** and **collaborate** with others.
  <img src="https://cdn.idntimes.com/content-images/community/2021/08/screenshot-20210816-170647-6ff4389e5b5ccef71e70121535467561-0c3e9947ed9df8a18cdf77be3f9c9175_600x400.jpg" width="500">

### Initial Config ([reference](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup))
1. Open Terminal/CMD
2. Execute the following command line by line:
   ```shell
   git config --global user.name "John Doe"
   git config --global user.email "johndoe@example.com"
   ```

### Git Cheatsheet ([reference](https://education.github.com/git-cheat-sheet-education.pdf))
```shell
# setup git config - set user name
git config --global user.name "your_github_username"

# setup git config - set user email
git config --global user.email "your_github_email@domain.com"

# verify git installation or check version
git -v

# initialize git project
git init

# clone repo from github
git clone repo_url

# track all changes in git
git add .

# track specific changes from specific file
git add file.txt

# track specific changes from specific folder
git add /folder1

# monitor changes
git status

# save/commit changes in git
git commit -m "your_commit_message"

# push/upload commited changes to github repo
git push

# or if it's the first time you cloned
git push --set-upstream origin main
```

### Create New Project
```shell
# create new folder
mkdir project1

# change directory to your newly created folder
cd project1

# initialize git
git init

# make changes to your project, after that you can track those changes with this command
git add .

# before tracking changes, you can also monitor changes to see which file/folder(s) has changed using this command
git status

# if you want to track changes from specific file(s) or folder(s) you can use this command
git add [filename.ext]
git add folder_name

# save your changes, put a clear message to your commit
git
```

## GitHub
### Definition
- **GitHub** is a cloud-based platform where you can store, share, and work together with others to write code. ([reference](https://docs.github.com/en/get-started/start-your-journey/about-github-and-git#about-github))
- Each source code is stored within a repository.

### Create Empty Repository ([reference](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository))
1. Open GitHub and click "Create New Repository" button.
2. Type a name for your repository, and an optional description. <br>
   <img src="https://github.com/user-attachments/assets/23971940-10a2-4483-9216-f62310f1c753" alt="drawing" width="500">
4. Choose a repository visibility (Public/Private)
5. Select "Initialize this repository with a README".
6. Click "Create repository".

### Clone Repository ([reference](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository))
1. After creating new repository or if you have existing repository, you can clone your repository to create a local copy on your computer and sync between the two locations.
2. First, navigate to the main page of the repository.
3. Above the list of files, click "Code" button. <br>
   <img src="https://github.com/user-attachments/assets/301165c1-2fcd-4e30-af2d-91f2365f0980" alt="drawing" width="500">
4. Select "HTTPS" and copy the URL for the repository. <br>
   <img src="https://github.com/user-attachments/assets/0cf23414-86ae-4429-8ffb-0ff5cdb8f8e3" alt="drawing" width="500">
5. Open Terminal/CMD and execute the following command to clone a repository
   ```shell
   git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
   ```

### Accepting Assignment From GitHub Classroom ([reference](https://sdsu-research-ci.github.io/github/students/accepting-assignment))
1. Click [here](https://classroom.github.com/a/hSnP3gZD) to accept demo assignment from Classroom.
2. You may be prompted to sign in. <br>
   <img src="https://github.com/user-attachments/assets/3f1dca1b-2c47-422e-8ce1-e58dddee144f" alt="drawing" width="500">
3. If this is your first time using GitHub Classroom, you may be prompted to authorize GitHub Classroom. <br>
   <img src="https://github.com/user-attachments/assets/c2830987-b004-4e36-b8c2-81f18cc35d70" alt="drawing" width="500">
4. If this is your first time accepting an assignment for a classroom, you may be prompted to associate your GitHub account to your registered name. <br>
   <img src="https://github.com/user-attachments/assets/6a1aa07e-4cc6-40ec-b023-d1cbcc1cb159" alt="drawing" width="500"> <br>
   > Carefully select your name, if you click the wrong name please notify your instructor so they can unlink the account.
5. Click the “Accept this assignment” button <br>
   <img src="https://github.com/user-attachments/assets/9e82cb9c-b454-407b-9777-c88d35ddc6d5" alt="drawing" width="500">
6. Click the link to view you repository <br>
   <img src="https://github.com/user-attachments/assets/c35a21a6-1573-413b-9583-21902fadec4d" alt="drawing" width="500">
7. You can clone this repository as usual.

### Learn More About Git
- Beginner's Guide to Git [here](https://github.blog/developer-skills/programming-languages-and-frameworks/what-is-git-our-beginners-guide-to-version-control/)
- Basic Git Command [here](https://www.earthdatascience.org/workshops/intro-version-control-git/basic-git-commands/)
- Introduction to Git Branch [here](https://www.geeksforgeeks.org/introduction-to-git-branch/)
- Learn more about Git Workflow [here](https://dev.to/ajmal_hasan/beginner-friendly-git-workflow-for-developers-2g3g)

## Videos to Watch
- [What is Anaconda](https://youtu.be/iaNEQglCF-I?feature=shared)
- [What is Git](https://youtu.be/2ReR1YJrNOM?feature=shared)
- [How Git Works](https://youtu.be/e9lnsKot_SQ?feature=shared)

# GitHub Tutorial

_by Joanne Fung_

---
## Git vs. GitHub
* ### What is Git?

 **Git** is a workspace that is for _your own self_. It's a place where you can keep different versions of the code that you type. This is _different_ because Git is a workspace that is mainly for you to keep track of what you have commited or edited to the project.

* ### What is GitHub?

 **GitHub** is a workspace that is used so that other people can _contribute_ to your project or _see the changes_ that you have made to the project itself. People can contribute by cloning, forking or sending you pull requests if they have anything they would want to add to your project. Also, **Git** is needed in order for **GitHub** to work.
    
---
## Initial Setup

#### Materials:
* [GitHub Account](https://github.com/join)
* [Cloud 9 Account (Or click the GitHub icon on upper right hand corner to sign in with your Git Hub)](https://c9.io)


###Adding SSH Keys- 
SSH Keys are what connects your remote file to your local file
#### Steps:

1. Go to the settings icon on the upper right hand corner in Cloud 9 once you have logged into Cloud 9
2. Go to the **SSH Keys** tab, there, you will find your default SSH key, where you copy and paste into GitHub
    * Click on your profile icon and scroll down to settings and then click the **SSH Keys** tab
    * Click the button that says **Add SSH key**
    * Title it Cloud 9
    * Paste the SSH Keys that you copied from Cloud 9 and paste it into the box that says **Key**
    * Click **Add Key** and now your local file is connected to your remote file!

##Initializing Git in Cloud 9

#### Steps:

1. Make 2 directories in your local machine, Cloud 9.
    * `mkdir github-learning`
    * `mkdir first-practice`
2. Make a `README.md` file (**!!!!CD INTO THE DIRECTORIES FIRST!!!!**)
    * `cd github-learning`
    * `cd first-practice`
    * `touch README.md`

3. Initialize the directory in your local machine  
    * `git init` - this is the only way you can use your git commands
    * You should see (username)`@github-learning:~/workspace/github-tutorial (master) $`
    * Because your cloud 9 is connected to your GitHub, you don't need to do `git config`, which is how the local machine can recognize the account that is being used.

---
## Repository Setup

1. Go into GitHub and on your home page, click the green button that says '** + New repository**'
2. Name file name in the '** Repository name**' box
    * _MAKE SURE THAT YOU NAME IT THE **EXACT** SAME NAME AS THE FILE NAME IS IN YOUR LOCAL_
3. Click the green button the says '**Create repository**'
4. Because you have a local file, you can copy and paste the code that says
    * This code basically connects your remote(GitHub) to your local(Cloud 9) and when you push a change from your local file, it will automatically change as well in the remote file.
    ```
    git remote add origin git@github.com:(your username)/README.md
    git push -u origin master
    ```
5. Go back to Cloud 9 now and click open the _first-practice_ folder and click open the _README.md_ file
6. Type "Hello World!" into the file
    * Make sure that the circle dot next to the file name in the tab is changed into an x by saving the file through file->save or hold the command key and press s.
7. Now type `git add .` to add all the files, in this case the only file, that you edited to the stage of the git, ready to be kept a copy of what you added into your file


---
## Workflow & Commands
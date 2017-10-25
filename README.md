# GitHub Tutorial

_by **Marko Henien**_

---

## Git vs. GitHub
![alt text](http://1.bp.blogspot.com/-WY2YpNr3W6g/UY6tZAc-H3I/AAAAAAAABLY/xJ9x3wIY8V8/s800/Github2.png)


Git and GitHub are 2 very usefull things. Git is a distributed version control system, and GutHub is a cloud baased website used for storing things such as git "snap shots"      

|   Git      | Simalities   |  GitHub  |   
|-----------|--------------|----------|
|1. Can keep different versoions of things such as code with so called "snap shots"  | -Both are comatible with one another |1.  Takes snapshot and stores things such as code in servers that are part of the larger cloud   |   
|2. Does not require github inorder to run | -Anyone can use both |2. Needs git in order to run  |  
|          |   | 3. One can callaborate on a project easily  |  
| | |4. Changes can easily be tracked via a visual interface  |

---
## Initial Setup
In order to get started you'll need a Github account and an SSH key. In order to obtain the SSH key you'll need a GitHub account so lets do that first.
1. Start by heading over to the [GitHub website](https://github.com/)
2. Then hit the sign up for GitHub button, you should then see a screen like this:
![alt text](https://www.wikihow.com/images/2/2c/Join-github-1.jpg)
go ahead, follow the prompts, enter your information, and hit submit.
3. If you followed everything correctly you should be at this page:
![alt tet](https://www.wikihow.com/images/2/20/Join-github-4.jpg)                      
You can choose between paying for a private repository or using a public one for free. Once you've made up your mind head over to the next and last page.
4. This is what you should see:
![alt tet](https://www.wikihow.com/images/8/88/Join-github-5.jpg)                                   
Here you can taylor your account to your coding needs, and once you hit submit you should have your own GitHub account!!!
5. Now that we have a GitHub account we can access an SSH key
* We can start by navigating to settings through the profle icon, Once in setings hit SSH and CPG
* Now here we can create a new SSH, All we have to do is name it Cloud9 (you can name it what you'd like but this is for the sake of simplicity), and make sure it says SSH key, copy it, and we are good to go. 
* Once we have the key we can head over to Cloud9 to establish a connection. In Cloud9 you'll have to make a new workspace. In the proccess of making a workspace you'll be asked to enter an SSH key. Enter the key we obtained from GitHub. Once entered complete the workspace setup . Next open the workspace and head over to the IDE. In the IDE type ```ssh -T git@github.com```. This will establish a connection. You should see somethings like this, ```Hi <your username>! You've successfully authenticated, but GitHub does not provide shell access.```,
Now we are done with the initial setup.
---
## Repository Setup
1. In order to setup a repository you first have to create a repository, so head over to your GitHub account and create a repository. You can do this by hitting the big green button on the home page . It will ask you for a name and other details . Once you're done you'll have a repository. Now that we have a repository we'll want to head back to Cloud9 
2. Once there you'll want to create a directory in your recently created workspace. Now that we have a directory we can begin to setup GitHub.
3. Now go back to GitHub and your Repo. Hit the SSH key button and you'll see a few thongs copy down the box with 2 lines of code.```Git remote add orgin [lnk]``` ( this tells c9 where to find repository) & ``` git push -u origin master ```
4. Once you have the 2 lines head back to C9.io and paste each line one by one.
5. Now you have set up GitHub, but there are some commmads you'll have to learn to use ( use them in this order) :
* ` Git Init` - Intializes Git, this means a repository has been created in that workspace and you can begin working with Git.  
* ` Git add` [Insert exact name of file here]- Here you select the files you want to save or take a snap shot of 
* ` Git commit` - In Git commit you commit the the files you selected or take the picture.  
Now you know the commands to set up Git!!!!


---
## Workflow & Commands
When working With Git there are 4 key commands you'll need in addition to the 3 we just learned :
* `Git status `- This is a very important function it allows you to see whats happening. It will come in handy when you're troubleshooting. For example if you're not sure what files have been added you use Git status to wee which files have been added.
* `Git add`: So we learned about this previously but we'll now go into more depth. With git add you take the files you would like to save or store and add them to a staging area or you put them in the frame. The stuff thats going to be commited is selected.
* `Git commit`: Now with Git commit like I said earlier you take the picture. The most recent changes have been recognized and noted.
* `Git push` : With Git push you are sending your commit to the cloud or back to GitHub there it will be stored and you can access the commit from other computers.
---
## Rolling Back Changes
So when working on a project you might have made a mistake and want to revert back to and older version. This is possible.    

| |
|---------|
| Edit------------->add-------------->commit------------->push| 
|<-----`git checkout -- filename`----Edit<--- `git reset HEAD file name`---add<----`git reset --soft HEAD~1`<-------commit<-----`git revert [version 1] [version 2]..[version you want]` --------push|   
|---|
pre-edit<------------`git reset --hard HEAD~1`-----------------commit|
|-|
|edit<-----`git reset HEAD~1`----commit  |          
## EXTRA:
Here are some cool thims you might want to use but dont have to know:
* if you init git in the wrong folder you can type `rm -rf .git` and that will uninitialize git
* If you want to delete a repository you go one space above the repository then type `rf -rf [repo name]`
   * If you want to get rid of it in the remote you headover to GitHub, then go to the repositorys settings scroll to the bottom and hit delte. Then say yes to the pop up box and it will be deleted.
* If you would like to edit someones repo you can do 2 things . You can fork or clone the repo.
    * Forking: with forking you make a copy of the repo for your own use , so you have the same repo , but you can edit it 
         * You can do this by clicking fork on the desired repo
         * Once you have the repo and make changes you can do something called a pull request. If you made changes to the repo and you want the original repo to show those changes you can submit a pull request. It asks the admin to allow the repo to be changed with your changes
    * `git clone`: you can use this if you want to copy code from a repo to your local repo. You take the link from GitHub by cliccking clone . Then you enter `git clone [link]`
* If you want to copy what is currently on the remote repo to your local repo you use `git pull`








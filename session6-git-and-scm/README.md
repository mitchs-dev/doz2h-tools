_Idea from: https://www.geeksforgeeks.org/python-program-implement-rock-paper-scissor-game/_
# SESSION 6: LAB INFORMATION

## Overview
For this lab we are going to play a game of Rock, Paper, Scissor!
Since we are going to automate this project, we want to "simulate" a user
So for this example, we are just going to include a "simulated user" by adding an additional `random.randint()` function

## Prerequisites for all participants

* Git - https://git-scm.com/downloads
* GitHub Personal Access Token (PAT). You can follow [this guide](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token) for configuring a PAT.
* A Code Editor is something that is optional but can be useful. You will only need to install one. Also, don't forget "Vim"  is also an editor. Here are a few that are quite popular: 
  * VSCode - https://code.visualstudio.com/download
  * Atom - https://atom.io/



## What you'll do
In more detail, we are going to be doing a few things:

1. Working together to collaborate on creating a fun python program
2. Use Jenkins to automate our deployment
3. Learning how Source Control Management works
4. Use Git to manage our commits

## Files in this lab
For this lab we will have a total of three files:

1. `session6.py` - Our 'Source code' that will be our Rock, Paper, Scissor program
   * This will have **9** sections to be committed
2. `Dockerfile` - Used to package our source code with the Python Docker image
   * This will have **1** section to be committed
3. `Jenkinsfile` - Our pipeline code that will be used to build our Dockerfile and then run our Python program
   * This will have **1** section to be committed

## Order of work
Since we are  working on multiple files together, we do need to follow a order for work on `session6.py`. You will see in  this repository nine files with the name of `CodeBlock_<NUMBER>.md`. These are all of the instructions for each of the 9 sections for `session6.py`. These **must** be done in order for the purpose of this lab (I.e 1 -> 9)

For the `Dockerfile` and `Jenkinsfile`, these can be done at anytime after `CodeBlock_1.md` has bee completed.

## How to use lab

Each person will be assigned one (or more) file(s) to complete. For `session6.py` you need to follow the **Order of work** before you begin working on your section(s). 

The person who is responsible for `CodeBlock_1.md` will be also responsible for creating and owning the source repository in GitHub (Instruction in `CodeBlock_1.md`).

The person who is responsible for `Jenkinsfile.md` will be also repsonsible for managing the Jenkins controller, agent, and creating the Pipeline job to run our program. 

## Example repository

You can find a completed example repository here: https://github.com/stantonmitchell/stunning-potato/tree/session6-testing

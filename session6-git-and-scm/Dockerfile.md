__Idea from: https://www.geeksforgeeks.org/python-program-implement-rock-paper-scissor-game/__
# LAB INFORMATION
For this lab we are going to play a game of Rock, Paper, Scissor!
Since we are going to automate this project, we want to "simulate" a user
So for this example, we are just going to include a "simulated user" by adding an additional 'random.randint()' function

You are going to be responsible for creating the Dockerfile for this program! Don't worry, you only need to create the file.

**Before you start** make sure to `Fork` the source repository so that you can actually work on this. See [this doc](https://docs.github.com/en/get-started/quickstart/fork-a-repo) for information on forking in GitHub

To get started on your section, wait for the previous section to be completed, then run the commands:

1. `git  clone <Repo URL>`
   * Make sure ot replace `<Repo URL>`  with the actual URL of the repository you received from the person who is working `CodeBlock_1.md`
1. `cd <Repo Name>`
   * Make sure to replace `<Repo Name>` of the actual name of the repository you received from the person who is working `CodeBlock_1.md`
1. `git remote add upstream <Source Repo Url>`
  * Replace `<Source Repo URL>` with the actual repository created by the person who is responsible for `CodeBlock_1.md`
1. `git pull upstream main`
   * Since you are pulling from the 'source' you will want  to use `upstream`
1. `git checkout -b section-<Section number>`
   * Make sure to replace section number with this section's number. (I.e if you are doing section 1, you'd put `section-one`)
1. You will be working on this by yourself so go ahead and make the `Dockerfile` file

Then you will be able to work on this section. **Once you have added your section** to the `Dockerfile` file, run these commands:

1. `git commit  session6.py -m "Adding section <Section Number>"`
* Make sure to replace `<Section Number>` with the number of your actual section
1. `git push -u  origin <branch>`
* Since you are pushing to your fork, you will want to use 'origin'

For this section, you can adding the following file in the repository as the file named `Dockerfile`:

```Dockerfile
# We are using 'python:3.9.10' for our base image
FROM python:3.9.10

# This sets our working directory for the image
WORKDIR /usr/src/app

# Next we need to copy our `.py` file  to our image
COPY session6.py .

# Now we set our  command
CMD [ "python", "./session6.py" ]
```

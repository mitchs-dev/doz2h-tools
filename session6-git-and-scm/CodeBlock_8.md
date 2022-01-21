__Idea from: https://www.geeksforgeeks.org/python-program-implement-rock-paper-scissor-game/__
# LAB INFORMATION
For this lab we are going to play a game of Rock, Paper, Scissor!
Since we are going to automate this project, we want to "simulate" a user
So for this example, we are just going to include a "simulated user" by adding an additional 'random.randint()' function

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

Then you will be able to work on this section. **Once you have added your section** to the `session6.py` file, run these commands:

1. `git commit  session6.py -m "Adding section <Section Number>"`
   * Make sure to replace `<Section Number>` with the number of your actual section
1. `git push -u  origin <branch>`
   * Since you are pushing to your fork, you will want to use 'origin'

For this section, you will be adding the following sections **EIGHTH:**

```python
# if 'goAgain' is equal to '3' break
    if goAgain == 2:
        if userWin > compWin:
            print("##############\n" +
                  "THE USER HAS WON! :D\n" + "Final Score:\n" + "User:" + str(userWin) + "\nComputer: " + str(compWin) + "\n##############\n")
            break
        if userWin == compWin:
            print("##############\n" +
                  "IT'S A TIE! :O\n" + "Final Score:\n" + "User:" + str(userWin) + "\nComputer: " + str(compWin) + "\n##############\n")
            break
        else:
            print("##############\n" +
                  "THE USER HAS LOST! :(\n" + "Final Score:\n" + "User:" + str(userWin) + "\nComputer: " + str(compWin) + "\n##############\n")
            break
```
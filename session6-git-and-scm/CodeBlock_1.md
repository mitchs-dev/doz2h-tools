__Idea from: https://www.geeksforgeeks.org/python-program-implement-rock-paper-scissor-game/__
# LAB INFORMATION
For this lab we are going to play a game of Rock, Paper, Scissor!
Since we are going to automate this project, we want to "simulate" a user
So for this example, we are just going to include a "simulated user" by adding an additional 'random.randint()' function

You are going to be responsible for actually created the source repository for everyone to commit to! Don't worry, you  can follow these steps: 

1. Navigate in your browser to: `https://github.com/new`
1. Fill in the `Repository Name` section
   * Note you can also click  the green text in the `Great repository names are short and memorable. Need inspiration? How about <Green Text>?` section to choose a randomly generated repository name.
1. Make sure to select `Public`
1. Click `Create repository` at the bottom of the page

To get started on your section, Run the commands:

1. Create the initial file: `session6.py`
2. `git init`
3. `git remote add origin <Repository URL>`
   * Make sure to replace ` <Repository URL>` with your actual repositiories URL

Then you will be able to work on this section. **Once you have added your section** to the `session6.py` file, run these commands:

1. `git add .`
1. `git commit  session6.py -m "Adding section <Section Number>"`
   * Make sure to replace `<Section Number>` with the number of your actual section
1. `git branch -M main`
   * Since you are the first person to contribute, and it's your repository, you will use the `main` branch
1. `git push origin main`
   * Since you own the 'source' repository, you will only be using 'origin'  as your remote and 'main' as your branch

For this section, you will be adding the following sections **FIRST:**

```python
# Here are out imports
import random
import argparse
```
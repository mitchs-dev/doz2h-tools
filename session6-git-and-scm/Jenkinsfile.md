__Idea from: https://www.geeksforgeeks.org/python-program-implement-rock-paper-scissor-game/__
# LAB INFORMATION
For this lab we are going to play a game of Rock, Paper, Scissor!
Since we are going to automate this project, we want to "simulate" a user
So for this example, we are just going to include a "simulated user" by adding an additional 'random.randint()' function

You are going to be responsible for creating the Jenkinsfile for this program! Let's go ahead and make sure our enviornment is set up so we can run our program successfully.

1. Start your Jenkins environment.
   * In the [session 5  lab](https://docs.google.com/presentation/d/1rZeir4u4SszRJ1ckBQLNhitRTFdQ7gz7wb8y3pa_0po/edit?usp=sharing) we created this
1.  Add credentials
    1.  Go to `http://<JENKINS URL>:</JENKINS PORT>/credentials/store/system/domain/_/`
        1.  `<JENKINS URL>`- This will probably be `localhost` or your private IP address
        2.  `<JENNKINS PORT>` - This will be the port you use to connect to jenkins. The default port is `8080`
    2. In the top-left, click `Add Credentials`
    3. Add  your GitHub username and GitHub personal access token (PAT) (Follow [this guide](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token) if you need to generate a PAT)
    4. Set an ID (`github-pat`) and a Description (`GitHub PAT`)
    5. Click "OK"
2. Create a pipeline job
   1. From the Jenkins Dashboard, click "New Item" on the top-right
   2. For name, put "Session 6" and select "Pipeline" then click "OK"
   3. Scroll down to **Pipeline** and change **Definition** to `Pipeline script from SCM`
   4. Set the **Souce repository URL** in the `Repository URL` section.
   5. Provide your "GitHub PAT" credential in the `Credentials` section
   6. Scroll down to **Brances to build** and for **Branch Specifier (blank for 'any')** set this as `main`
   7. Click "Save"
3. For now we will wait until the "code" portion of this lab is completed 




**Before you start** make sure to `Fork` the source repository so that you can actually work on this. See [this doc](https://docs.github.com/en/get-started/quickstart/fork-a-repo) for information on forking in GitHub

To get started on your section, wait for the previous section to be completed, then run the commands:

1. `git  clone <Repo URL>`
   * Make sure ot replace `<Repo URL>`  with the actual URL of the repository you received from the person who is working `CodeBlock_1.md`
2. `cd <Repo Name>`
   * Make sure to replace `<Repo Name>` of the actual name of the repository you received from the person who is working `CodeBlock_1.md`
3. `git remote add upstream <Source Repo Url>`
  * Replace `<Source Repo URL>` with the actual repository created by the person who is responsible for `CodeBlock_1.md`
1. `git pull upstream main`
   * Since you are pulling from the 'source' you will want  to use `upstream`
1. `git checkout -b section-<Section number>`
   * Make sure to replace section number with this section's number. (I.e if you are doing section 1, you'd put `section-one`)
1. You will be working on this by yourself so go ahead and make the `Jenkinsfile` file

Then you will be able to work on this section. **Once you have added your section** to the `Jenkinsfile` file, run these commands:

1. `git commit  session6.py -m "Adding section <Section Number>"`
* Make sure to replace `<Section Number>` with the number of your actual section
1. `git push -u  origin <branch>`
* Since you are pushing to your fork, you will want to use 'origin'

For this section, you can adding the following file in the repository as the file named `Jenkinsfile`:

```groovy
pipeline {
    agent {
        node {
            label 'MyAgent'
        }
    }
    options {
        timestamps()
    }
    stages {
        stage('Checkout code from SCM') {
            steps {
                // This step checks out the code
                checkout scm
            }
        }
        stage('Build Image') {
            steps {
                sh 'docker image rm -f doz2h:session6'
                sh 'docker build -t doz2h:session6 .'
            }
        }
        stage('Run Program') {
            steps {
                // This is going to display the rules for our Rock, Paper, Scissor game
                sh 'docker run --rm --name doz2h-session6-rules-container doz2h:session6 python session6.py --rules'
                // This is going to actually run our program
                sh 'docker run --rm --name doz2h-session-6-container doz2h:session6'
            }
        }
        stage('Cleanup') {
            steps {
                sh 'docker image rm -f doz2h:session6'
                sh 'docker image rm -f python:3.9.10'
                cleanWs()
            }
        }
    }

}
```

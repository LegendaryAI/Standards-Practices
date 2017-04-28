## Github Workflow - Feature Branch Workflow
* All feature development should take place in a dedicated branch instead of the master branch.
* Discuss changes and issues via pull requests.
* Master branch -> Feature branches (Features will be developed in branched and merged into master.
* Master branch represents the official project history.
* Once you complete a features, don't immediately merge it into master, file a pull request asking to merge your additions to the master.


## Workflow- Adding a new feature
#### 1. Request a new branch( be descritpive)
* CMD: git checkout -b new-feature master

* Build your features in this branch- stages and commits
* CMD: git add <some-file> || git commit -m"message

* Push your feature branch to central repository( For backup and for intial access to other developers).
* CMD: git push origin branch-name

#### 2. Once you are done working on the feature, push your code and file a pull request in GIT GUI asking to merge new-feature into master.
* CMD: git push
* If someone wants to add some changes, can notify via pull requests or pull new-feature branch into their local repository and do the changes.

#### 3. Once everyone is convinced, merge the feature into the master(To merge, checkout the master branch and make sure it's up to date.)
* CMD: git checkout master
* git pull
* git pull origin new-feature
* git push
* Requests that are green on CI and have been reviewed can only be merged.

**NOTE:** Developer Role - Step 1 and Step 2
... Repo Owner's Role - Step 3

**NOTE:** For each step make sure all the test cases are running before pushing the code to server.

## More about pull requests
* You can open a pull request at any point during the development process.
* When you're stuck, and need any help or advice, or when you're ready for someone to review your work.
* By using Github's @mention system in your pull request message you can ask for feedback from specific people or teams.


## Issue Tracker/ Bug fixes:
* Once an issue has been raised in the Github anyone can work on it.
* Create a branch called myfix.
* Work on the bug in this topic branch until it is fixed.
* Run tests.
* File for pull requests.
* If your fix conflicts with another topic topic branch hasfix that your co-worker merged into Master while you were working on your fix.
* Make more changes in the myfix branch to deal with these conflicts and run the tests again.
* Merge myfix to Master.

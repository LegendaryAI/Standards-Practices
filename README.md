# Standards-Practices
## H2 Github Workflow - Feature Branch Workflow
* All feature development should take place in a dedicated branch instead of the master branch.
* Discuss changes and issues via pull requests.
* Master branch -> Feature branches (Features will be developed in branched and merged into master.
* Master branch represents the official project history.
* Once you complete a features, don't immediately merge it into master, file a pull request asking to merge your additions to the master.


## H2 Workflow- Adding a new feature
1. Request a new branch( be descritpive)
...CMD: git checkout -b new-feature master

..1. Build your features in this branch- stages and commits
...CMD: git add <some-file> || git commit -m"message"
..2. Push your feature branch to central repository( For backup and for intial access to other developers).
...CMD: git push

2. Once you are done working on the feature, push your code and file a pull request in GIT GUI asking to merge new-feature into master.
...CMD: git push
..1. If someone wants to add some changes, can notify via pull requests or pull new-feature branch into their local repository and do the changes.

3. Once everyone is convinced, merge the feature into the master(To merge, checkout the master branch and make sure it's up to date.)
...CMD: git checkout master
... git pull
... git pull origin new-feature
... git push
... Requests that are green on CI and have been reviewed can only be merged.

**NOTE:** Developer Role - Step 1 and Step 2
... Repo Owner's Role - Step 3

**NOTE:** For each step make sure all the test cases are running before pushing the code to server.

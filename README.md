# Example Repository
This is a sample repo.

Git is distributed version control system.

The following are few notes on git operations and work flow:

Git allows derivatives, or branches, to be made from the main source document. The initial branch is the "master" branch and is typically used as the stable or published version of the source. The secondary branch is the "develop" branch, or current in-development version of the master. Feature branches can then be made from the develop branch to support work on individual features or components. Changes in feature branches should then be merged into the develop branch before forking / merging the develop branch into a release or the master branch. When the develop branch seems ready to be merged in to the master, a release branch can be created. To optimize the work flow, only bug fixes, documentation generation, and release prepation tasks should be made to the release branch.

    To add a "develop" branch:
        git branch develop

    To push the "develop" branch to origin:
        git push -u origin develop

    To create a "feature" branch:
        git checkout develop
        git checkout -b feature_branch

    To merge the "feature" branch into develop:
        git checkout develop
        git merge feature_branch

    To create the "release" version 0.1.0 branch:
        git checkout develop
        git chekcout -b release / 0.1.0

    To push the release to master:
        git checkout master
        git merge release / 0.1.0

Common Commands:
    Initialize a repo: 
        Git init 

    Check the current status:
        Git status

    Commit the changes to someFile.fileExtension to the local version:
        Git commit someFile.fileExtension -m "Add notes for you commit."

    Push the changes to the master branch:
        Git push origin master
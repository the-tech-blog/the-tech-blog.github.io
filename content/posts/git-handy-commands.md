+++
ShowToc = true
TocOpen = false
aliases = []
author = "Ashish Mishra"
categories = []
date = 2020-09-29T18:30:00Z
description = "This Post talks about some of the git handy commands"
series = ["Git"]
tags = ["git", "github"]
title = "Git handy commands"
weight = 2

+++
#### Scenario 1: Remove a Modified File from Git pull request

Switch to the branch from which you created the pull request:

    $ git checkout pull-request-branch

Overwrite the modified file(s) with the file in another branch, let's consider it's **master**:

    git checkout origin/master -- src/main/java/HelloWorld.java

Commit and push it to the remote:

    git commit -m "Removed a modified file from pull request"
    git push origin pull-request-branch

#### Scenario 2: Update the commit user name and email in Git repo

    git config user.name user-name
    git config user.email username-git@gmail.com

#### Scenario 3: Git updating the buffer size in Git repo

    git config --global http.postBuffer 1048576000

#### Scenario 4: Stop tracking changes to a file in Sourcetree

I guess, This is the issue which troubled me most in git. So, the issue is i have a file in my code base which i dont want to commit as this is specific to my local. But still sourcetree show this file to me, everytime i go for making a commit. This is really very annoying. to fix this run the below command in the repo folder and sourcetre will understand our feelings.

	git update-index --assume-unchanged file.filename

For folder use this

	git rm -r --cached path_to_your_folder/

To get undo/show dir's/files that are set to assume-unchanged run this:

    git update-index --no-assume-unchanged file.filename

To get a list of dir's/files that are assume-unchanged run this:

    git ls-files -v|grep '^h'
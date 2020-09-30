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
title = "git-handy-commands"
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
    
#### Scenario 2: Update the commit user name and email in git repo
    git config user.name boring-baba
    git config user.email boringbabainfo+fiverr@gmail.com

#### Scenario 3: Git updating the buffer size in git repo
	git config --global http.postBuffer 1048576000
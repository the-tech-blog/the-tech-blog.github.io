+++
ShowToc = true
TocOpen = false
aliases = []
author = "Ashish Mishra"
categories = []
date = 2020-09-29T18:30:00Z
description = "This Post talks about some of the git handy commands"
draft = true
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
+++
ShowToc = true
TocOpen = true
aliases = []
author = "Ashish Mishra"
categories = ["couchbase"]
date = 2020-10-17T18:30:00Z
description = "This post includes useful couch base commands, such as delete, insert, copy and retrieve command"
tags = ["couchbase"]
title = "CouchBase - Commands"
weight = 3

+++
### Scenario 1: Copy all document from One Bucket to another

		INSERT INTO \`bucket-name\` (KEY _k, VALUE _v) SELECT META().id _k, _v from \`bucket-name\` _v

### Scenario 2: Deleting everything from bucket

		DELETE FROM \`bucket-name\`

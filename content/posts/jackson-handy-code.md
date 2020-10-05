+++
ShowToc = true
TocOpen = true
aliases = []
author = "Ashish Mishra"
categories = []
date = 2020-10-04T18:30:00Z
description = "Code snippet which i found useful in Implementing Jackson API"
draft = true
series = []
tags = ["json", "jackson"]
title = "Jackson Handy Code"
weight = 2

+++
### Section 1: converting JSON to POJO class, using a generalize method

By using this method we can pass a JSON Object to the method as a parameter, and the second parameter is the class reference, which needs to be mapped.

    @SneakyThrows
    public <T> T getObjectFromData(Class<T> objClass, JsonObject jsonObject) {
    return mapper.readValue(jsonObject.toString(),objClass);
    }
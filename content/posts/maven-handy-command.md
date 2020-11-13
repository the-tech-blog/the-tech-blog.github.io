+++
ShowToc = true
TocOpen = true
aliases = []
author = "Ashish Mishra"
categories = ["maven"]
date = 2020-11-12T18:30:00Z
description = "This page comprise of few maven commands which i have used in my projects"
draft = true
series = []
tags = ["maven"]
title = "Maven Handy Command"
weight = nil

+++
Scenario 1: Start the AEM in debug mode

> java -Xdebug -Xnoagent -Djava.compiler=NONE -Xrunjdwp:transport=dt_socket,server=y,suspend=n,address=127.0.0.1:8765 -XX:+HeapDumpOnOutOfMemoryError -XX:MaxPermSize=256M -Xmx1024m -Dorg.apache.sling.commons.log.level=INFO -jar cq-quickstart-6.5.0.jar

Scenario 2: Start the Spring boot application 

mvn clean spring-boot:run

Scenario 3: Start Spring boot in specific mode

mvn clean spring-boot:run -Dspring-boot.run.profiles=local

Scenario 4: Skip J-Unit test

\-Dmaven.test.skip=true

Scenario 5: Start Redis Server

redis-server

Scenario 6: Clear redis cache

**redis-cli flushall**

Scenario 7: Start Spring boot in debug mode and also run a specific profile and skip j unit test compilation 

mvn spring-boot:run -Dspring-boot.run.jvmArguments="-agentlib:jdwp=transport=dt_socket,server=y,suspend=n,address=5005" -Dspring-boot.run.profiles=local -Dmaven.test.skip=true
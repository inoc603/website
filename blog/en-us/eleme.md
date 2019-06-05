---
hidden: false
title: Using Dragonfly at Eleme
# keywords: keywords1,keywords2
description: TODO
author: inoc603
date: 2019-06-06
---

# Using Dragonfly at Eleme

TODO: Description of eleme

Eleme has a very complex production envoironment. We run apps on both directly on VMs and in docker containers, in a mixture of private IDCs and public cloud. We have 2 orchestration systems for our containers. One is an in-house mesos based system with custom scheduler, deveploped in the early days when kubernetes hasn't win the container orchestration war. The other one is Sigma, a kubernetes based solution from Alibaba, adpoted after Eleme was acquired by Alibaba in 2018.

We currently run around 30000 containers and 5000 VMs in all of our production environment, and deploy applications 1000 times each day on average. Distributing docker images, packages and large files like machine learning models across multiple IDCs has become quite challenging.

Most of our file services are deployed on public cloud, including docker registry, package repo for our application, yum repo etc. Other IDCs access these services through dedicated network lines.

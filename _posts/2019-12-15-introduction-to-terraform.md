---
layout:     post
title:      Introduction to Terraform
date:       2019-12-15 23:32:18
summary:    Introduction to Terraform in age of rising Infrastructure as Code approach
categories: personal
---


## Introduction to Terraform

Terraform is an open-source infrastructure automation tool by HashiCorp. It has been gaining more ground towards being a defacto choice for creating and managing cloud infrastructures by writing declarative definitions. By enabling "Infrastructure as Code", Terraform provides repeatability and consistency, which is very useful when setting up complicated infrastructures, such as a cluster of containers with its underlying infrastructure on AWS.

Terraform supports [many cloud providers](https://www.terraform.io/docs/providers/index.html) for IaaS (e.g. AWS, GCP, Microsoft Azure, OpenStack, Alibaba Cloud), PaaS (e.g. Heroku), and SaaS services (e.g. Terraform Cloud, DNSimple, CloudFlare).


Terraform provides a native syntax, which is a rich language designed to be easy for humans to read and write.[1]


Terraform stores state about managed infrastructure and configuration. It uses the state to map the resources to the configuration and keep track of metadata. The state is stored locally by default but Terraform supports "remote state backend", which works better in a team environment and  helps keeping sensitive information off disk. The state is retrieved from backends on demand and only stored in memory. For example, Amazon S3 can be used as backend.

Where to start learning about Terraform?

Although Terraform has good [documentation](https://www.terraform.io/docs/index.html), I think [this introduction blog post](https://blog.gruntwork.io/an-introduction-to-terraform-f17df9c6d180) provides a quick and good start to have a grasp of Terraform.


[1] https://www.terraform.io/docs/configuration/syntax.html

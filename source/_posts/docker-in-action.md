---
title: docker in action
date: 2017-05-10 16:52:29
tags: docker
---

## 什么是容器云

容器云是以容器为资源分割和调度的基本单位，封装整个软件运行时环境，为开发者和系统管理员提供用于构建，发布和运行分布式应用的平台。当容器云专注于资源共享与隔离，容器编排与部署时，它更接近于传统的IaaS；当容器云渗透到应用支撑与运行时环境时，它更接近传统的PaaS；

启动容器

	docker run -it --name mytest ubuntu:latest /bin/bash

从其他服务器拉取镜像
	
	docker pull 10.10.111.121:5000/sshd

查看容器内部ip

	docker inspect --format='{{.NetworkSettings.IPAddress}}' container

查看镜像的历史版本信息

	docker history IMAGE

开发，测试和发布一体化
Docker以镜像和在镜像基础上构建的容器为基础，以容器为开发，测试和发布的单元，将与应用相关的所有组件和环境进行封装，避免了应用在不同平台间迁移时所带来的依赖性问题，确保应用在生产环境的各阶段达到高度一致的实际效果。

Docker通过namespace实现了资源隔离，通过cgroups实现资源限制，通过写时复制机制copy-on-write实现了高效的文件操作。
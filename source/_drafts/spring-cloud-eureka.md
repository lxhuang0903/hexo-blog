---
title: spring_cloud_eureka
tags: spring_cloud eureka
---

### How to set up an Eureka Server

import dependency in pom.xml file

		<dependency>
			<groupId>org.springframework.cloud</groupId>
			<artifactId>spring-cloud-starter-eureka-server</artifactId>
		</dependency>


bootstrap.yml

	spring:
  		application:
    		name: eureka-server
	server:
  		port: 8761
	eureka:
  		client:
    		registerWithEureka: false
    		fetchRegistry: false
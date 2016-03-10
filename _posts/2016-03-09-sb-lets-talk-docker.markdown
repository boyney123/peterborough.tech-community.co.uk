---
layout: post
title:  "Lets talk Docker"
cover: http://exportpackers.co.uk/blog/wp-content/uploads/2014/10/shipping-containers.jpg
date:   2016-03-09 22:29:44 +0000
categories: tech
subtitle: Docker
blurb: Musings on the benefits of using Docker in your environment

author: Stewart Barrett
---
I had a conversation the other day with some guys who manage the on-premise infrastructure and I mentioned we were using Docker. This produced a raft of questions like "What's Docker?", "What's the point of Docker"?, "Isn't that just what VM's are?", "What's a Container?" etc etc.

I had to hold back on diving into the technical benefits of Micro-services, Containerization, and Docker as I mentally recalled a similar conversation I had with a non-technical colleague who's eyes quickly glazed over as I barreled headlong into described everything I know about this kind of stuff.

I started with a quick sketch about the differences between deploying an application on a regular server to what that looks like if it's
deployed in a container and how all this is different to what these guys see every day. I talked about it being open-source and described how quick it was to get started and deploy a basic "Hello World" app and see the results in a browser.

This was great because they were bought in enough at this point to organize some time to see how it worked and deploy that "Hello World" app for themselves. What was really interesting was the spin off conversation it sparked about a whole bunch of other stuff that I really wasn't expecting. Stuff like cost savings, standardization, utilization of resources and speed to deploy and the like. Wow! Half an hour ago these guys had no idea that Docker even existed!

It's that conversation that prompted me to write this post; I take it for granted that people know what Docker is because I live and breathe it everyday but that's (obviously) not true for everyone.

Ok, lets talk Docker. So the guys at Docker have kind of a mantra which is BUILD, SHIP, RUN. You can BUILD your application without worrying about stuff like environment, operating system or language. It lets you SHIP that application from the registry managing it through to distribution via a consistent UI and finally RUN and deploy that application at scale on whatever platform or provider you feel like. Cool right?

But what is of real interest is that Docker allows you to concentrate on what you as a developer are good at i.e. writing great code, while it takes care of the infrastructure bit allowing you to use whatever platform suits you best to optimize infrastructure resources, standardize environments and at a stroke reduce that all important time to market thus increasing the 'heartbeat' of a tech company - i.e. how often it deploys new features to its customers.

Docker enables users to run their containers wherever they please either in a Cloud or on-premise, so you're not locked into a vendor or Cloud provider. You can deploy your containers to any Docker host on any infrastructure from Amazon, Google, or Azure to your datacenter servers or even your laptop!

Standardization and Resource Consolidation are also a major advantages; easily setup, reproduce, manage, update and distribute new environments. With Docker you can run as many containers as your infrastructure can handle. Just package your application and all it's dependencies into a single container and it removes all the usual inconsistencies between environments allowing you to run the same container in any environment. Docker also plays nicely with all the popular CI/CD pipelines which is great for productivity and efficient deployments.

So whatever the problem is you're trying to solve, large or small, Docker is a great way to spike out that mini project or deploy your enterprise web application. Google uses Docker extensively and spins up millions of containers a week.

So like the guys I was talking to I hope this has sparked your interest to go find out more about Docker and Containerization. It's a really cool way to get your application out there but it also has a bunch of added benefits that can help drive down your infrastructure & deployment costs, standardize your environments and reduce the time it takes to get those cool new features in front of your customers.

Find out more at: 

[https://www.docker.com/](https://www.docker.com/)

[https://docs.docker.com/](https://docs.docker.com/)

+++
description = "Which technologies will I be using to develop Birdr"
title = "Tools of the trade"
date = "2016-12-22T16:51:47Z"
draft = true
+++

![A set of old wood working tools... totally unsuitable for web development](/images/post/tools-of-the-trade.jpg)

When I initially built Birdr in 2011 I built it using [Ruby on Rails](http://rubyonrails.org/). These were new technologies to me at the time and required a substantial amount of learning. Birdr is a great project to learn new technologies. It is complex enough to require me to have a firm grasp on a language, yet remains simple enough to allow me to produce _something_ relatively quickly.

To this day, Ruby remains my favourite programming language. It has a satisfying syntax and malleable design that lets you create code that reads almost like prose. I haven't had the opportunity to use it in my day job yet, but it is my goto tool for personal projects. If you are interested in programming and haven't yet tried Ruby I would [strongly encourage you to do so](https://pragprog.com/book/rails5/agile-web-development-with-rails-5)... you won't regret it.

Rails is a framework built on Ruby that allows a developer to get up and running extremely quickly. It became famous for it's "How to build a blog in 15 minutes" tutorial. However, the best thing about Rails, in my opinion, is the community. There is a strong focus on testing and [TDD](https://en.wikipedia.org/wiki/Test-driven_development) within the Rails community - both good practices and something I strongly believe in. Furthermore, there are packages, or [Gems](https://rubygems.org/), for nearly anything. From [user authentication](https://rubygems.org/gems/devise/versions/4.2.0) to [weather reports](https://rubygems.org/gems/darksky/versions/1.0.5) - Rails has it all.

### Out with the old and in with the new

Ruby on Rails is very much the kitchen sink of development. This time around I am looking to adopt a pattern that I used successfully at the BBC - [Microservices](http://www.martinfowler.com/articles/microservices.html). At a high level, the idea behind Microservices is that you split your application up into smaller, logical chunks. What used to be a single monolithic application becomes a loosely coupled web of services that form a whole. For an architecture such as this Rails does not make sense.

There are a number of problems posed by using Microservices too. Deploying, monitoring and maintaining multiple services rather than 1 can be a large burden on a team. These are all things that I will try to solve and document during the development of Birdr. To help me I have provisionally selected a number of technologies.

#### Docker & Kubernetes

Containers. You can't avoid them nowadays. The rise of [Docker](https://www.docker.com/) has been one of the quickest in modern times. I didn't use it at the BBC. Partly due to the maturity of the project and partly due to other constraints. However, with tools such as [Kubernetes](http://kubernetes.io/) (k8s) emerging, containers have become a far more compelling proposition. I will use Birdr as an opportunity to work with k8s and Docker to host the Microservices I develop.

#### Go

Another popular technology at the moment is [Go](https://golang.org/) (or Golang). Developed by Google, it is a compiled statically typed language. For the non-techies among you, this means it is worlds apart from Ruby - which is a interpreted dynamically typed language. As it is substantially different to any language I have used recently it will place me firmly outside of my comfort zone.

#### linkerd

Building a Microservice architecture introduces a lot more communication. What was once an internal function call becomes a network request. And, as anyone will tell you, networks are inherently unreliable. Requests will fail or slow down seemingly randomly which can cause catastrophic failures when you're operating at scale. There are a number of tools at your disposal to help you build a _robust_ system such as circuit breakers, retries and bulkheads. At the BBC we built a Node.js library ([which has since been open sourced](https://github.com/bbc/flashheart)) to handle this for us. The downside of this approach is that it limits you to using Node.js. To create a Microservice in another language would require you to write a similar library. This is an anti-pattern covered in detail in [this talk by Ben Christensen](https://www.microservices.com/talks/dont-build-a-distributed-monolith/).

An alternative approach I [discovered being used by Monzo](https://monzo.com/blog/2016/09/19/building-a-modern-bank-backend/) is to use a service called [linkerd](https://linkerd.io/). Essentially, your services communicate with linkerd which is running locally and _it_ handles communication across the network - including retries, circuit breakers and monitoring.

I had never heard about this before so I am really excited to try it out and see how it works.

#### Prometheus

The last technology I want to call out is [Prometheus](https://prometheus.io/). When you're running 20+ services in production monitoring is essential. I've had great success using [StatsD](https://github.com/etsy/statsd) and [Graphite](https://graphiteapp.org/) before but wanted to take this opportunity to try something different.

No doubt there will be other technologies I want or need to use during the next year. One of the benefits of building using Microservices and linkerd is that I am free to choose the language of my choice. I hope I manage to avoid the inevitable lure of returning to Ruby.

**_Note: If you're reading this and don't understand a word I've just said - fear not. I hope to blog about each of these technologies individually at a level that even my dad could understand... and he's about as technical as a Woodpigeon!_**




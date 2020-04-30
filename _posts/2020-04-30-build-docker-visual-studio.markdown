---
layout: post
title: "Building Dotnet Core Docker Images From Visual Studio"
date: 2020-04-30 10:37:53 -0400
categories: webapi dotnetcore docker
---

When you create a new DotNetCore Web API with Visual Studio 2019, and enable Docker support, a `Dockerfile` is created for you, using the multi-stage build technique described at the link at the top of the Dockerfile.

To build, from the command prompt, the image, issue the `docker build` command from the parent directory (the directory containing the solution), passing the path to the `Dockerfile` as follows:

{% highlight bash %}
docker build -f ".\WebApplication1\Dockerfile" .
{% endhighlight %}


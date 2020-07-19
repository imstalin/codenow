---
layout: post
title: Create Windows Service - Dot Net Core 
subtitle: learn by example 
tags: [dotnet, core,programming,C#,Background service,sc utility]
---

Create windows service in dot net core become easier. We will see how to create window service in worker template and install the service by using SC utility.

Let's create a worker project by using command dotnet 

```
dotnet new worker -n SampleService
```

The above command will create the worker template then we need to include the windows hosting services package from Nuget manager.

```
dotnet add package Microsoft.Extensions.Hosting.WindowsServices --version 3.1.4
```


Make sure the version are the same in your worker template.

Now in worker template, We configure the service name and mention it as windows service.

Here is the snippet to configure the worker application as windows service in program.cs

```
public static IHostBuilder CreateHostBuilder(string[] args) =>
                Host.CreateDefaultBuilder(args) 
                .ConfigureServices((hostContext, services) =>
                {
                services.AddHostedService<Worker>()
                    .Configure<EventLogSettings>(config =>
                {
                    config.LogName = "Sample Service";
                    config.SourceName = "Sample Service Source";
                });
                }).UseWindowsService();
```

Let's build this application and test and the build command as follows below.

```
dotnet publish -o  <output directory>
```

### Install Window Service - SC Uitlity 

Now let's install the sample service program by using SC create command as follows below.

Open your command prompt in administrative mode. 

```
sc create SampleService binPath=<output directory>
```
Once services are created. Let us query service to check the status by below command.

```
sc query SampleService
```
Let us start and stop the service by using start and stop command from SC utility.

```
SC start SampleService
```
```
SC stop SampleService
```

You can refer to the video source for details and demonstration. 

[![Dot Net Core - Windows Service](http://img.youtube.com/vi/a7d1iYhUCnc/0.jpg)](http://www.youtube.com/watch?v=a7d1iYhUCnc)

GitHub:
[https://github.com/imstalin/windowservicedotnetcore](https://github.com/imstalin/windowservicedotnetcore)


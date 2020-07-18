---
layout: post
title: Folder Watcher - Dot Net Core
subtitle: learn by example 
tags: [dotnet, core,programming,C#,Background service]
---

We might come across this situation to monitor the files from your server or local machine, if there are any changes in the existing file or any new files are created in a particular location.

In that case, I would like to share small C# code snippet to monitor the files, when any File System events occurred and this might be very useful to organize Files in many scenarios.  

We will use Dot Net Core 3.0 to demonstrate this example.

We can create the sample worker application from the below in your command prompt window or terminal.

```
dotnet new worker -n myfolderwatcher

```

After the worker template created, Let's go to the code editor for developing the folder watcher utility.

Here is the code snippet for folder watcher with explantation. Now I am creating the creating instance for FileSystem watcher.

~~~

FileSystemWatcher watcher = new FileSystemWatcher();

//Mention the Path that you want to monitor file events.

watcher.Path = @"C:\Users\stali\Desktop\files"; 
watcher.IncludeSubdirectories = true;  
watcher.NotifyFilter = NotifyFilters.Attributes |  
NotifyFilters.CreationTime |  
NotifyFilters.DirectoryName |  
NotifyFilters.FileName |  
NotifyFilters.LastAccess |  
NotifyFilters.LastWrite |  
NotifyFilters.Security |  
NotifyFilters.Size;   
watcher.Filter = "*.*"; 

//File System Events to listen them
watcher.Changed += new FileSystemEventHandler(OnChanged);  
watcher.Created += new FileSystemEventHandler(OnChanged);  
watcher.Deleted += new FileSystemEventHandler(OnChanged);  
watcher.Renamed += new RenamedEventHandler(OnRenamed);  

// Starting monitoring the folder.
watcher.EnableRaisingEvents = true; 

~~~

FileSystem Events are like Created, Changed,  Renamed and Deleted.

From those events trigged, We can able to capture the source information and perform the action as you want.

Let's say for an example. We may be required to monitor the files and categories them according to the file format.

The folder has many files like excel , text and JSON.  We want to move them into the corresponding folder.

Let's create a utility program with the demonstration. Please watch video below

[![Dot Net Core - Folder Watcher](http://img.youtube.com/vi/ki-vHc1VaeQ/0.jpg)](http://www.youtube.com/watch?v=ki-vHc1VaeQ)


Github Repository

https://github.com/imstalin/myWatcher


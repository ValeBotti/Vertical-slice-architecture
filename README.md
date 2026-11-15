# Vertical Slice Architecture

[![C#](https://img.shields.io/badge/C%23-C%23-512BD4?style=flat-square)](https://learn.microsoft.com/en-us/dotnet/csharp/)
[![.NET 10](https://img.shields.io/badge/.NET-10-512BD4?logo=dotnet&logoColor=white)](https://learn.microsoft.com/en-us/dotnet/core/whats-new/dotnet-10/overview)
[![Blazor Web App](https://img.shields.io/badge/Blazor-Web%20App-512BD4?logo=blazor&logoColor=white)](https://learn.microsoft.com/en-us/aspnet/core/blazor/?view=aspnetcore-10.0)
[![Interactive Server](https://img.shields.io/badge/Render%20mode-Interactive%20Server-512BD4)](https://learn.microsoft.com/en-us/aspnet/core/blazor/components/render-modes?view=aspnetcore-10.0)

The first step is creating the Blazor Web App project in Visual Studio, and then you hit a wall: you need to decide how to organize the project's directories and files.

Firstly, it's nice to study a little bit of what a vertical slice architecture is; then, having vaguely grasped the meaning of it, you start wondering how to distribute files and directories.
One objection that came to mind when I first read about vertical slice architecture is the MainLayer; by definition, the MainLayer destroys the separation between layers. You need it to be shared, and then you think about the spinner, and probably most UI are components that must be reused, and routes, and imports...

You need more time than expected to think this through, because you can be choosing single files and directories and classifying them as shared; you need a general rule: what and why.

And then you reach an uncanny stage where nothing makes sense, and you start wondering what your files and directories actually do.

And that's where I'm starting this stream of consciousness.

## Defining purposes and roles of each file and directory
Here I describe the role of each element and pick candidates for shared features and low-coupling features.

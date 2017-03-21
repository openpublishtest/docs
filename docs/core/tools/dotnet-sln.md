---
title: dotnet-sln command | Microsoft Docs
description: The dotnet-sln command provides a convenient option to add, remove, and list projects in a solution file.
keywords: dotnet-sln, CLI, CLI command, .NET Core
author: spboyer
ms.author: mairaw
ms.date: 03/15/2017
ms.topic: article
ms.prod: .net-core
ms.technology: dotnet-cli
ms.devlang: dotnet
ms.assetid: e5a72d3e-c14b-4b0a-a978-c5e54a0988c6
---

# dotnet-sln

## Name

`dotnet-sln` - Modifies a .NET Core solution file.

## Synopsis

```
dotnet sln [<SOLUTION_NAME>] add <PROJECT> <PROJECT> ...
dotnet sln [<SOLUTION_NAME>] add **/**
dotnet sln [<SOLUTION_NAME>] remove <PROJECT> <PROJECT> ...
dotnet sln [<SOLUTION_NAME>] remove **/**
dotnet sln [<SOLUTION_NAME>] list
dotnet sln [-h|--help]
```

## Description

The `dotnet sln` command provides a convenient way to add, remove, and list projects in a solution file.

## Commands

`add <PROJECT> ...`

`add **/*`

Adds a project or multiple projects to the solution file. [Globbing patterns](https://en.wikipedia.org/wiki/Glob_(programming)) are supported on Unix/Linux based terminals.

`remove <PROJECT> ...`

`remove **/*`

Remove a project or multiple projects from the solution file. [Globbing patterns](https://en.wikipedia.org/wiki/Glob_(programming)) are supported on Unix/Linux based terminals.

`list`

List all projects in a solution file.

## Arguments

`SOLUTION_NAME`

Solution file to use. If not specified, the command searches the current directory for one. If there are multiple solution files in the directory, one must be specified.

## Options

`-h|--help`

Prints out a short help for the command.

## Examples

Add a project to a solution:

`dotnet sln todo.sln add todo-app/todo-app.csproj`

Add a project to the solution in the current directory:

`dotnet sln add todo-app.csproj`

Remove a project from a solution:

`dotnet sln todo.sln remove todo-app/todo-app.csproj`

Add multiple projects to a solution using a globbing pattern:

`dotnet sln add **/**/*.fsproj`

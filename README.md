# MSBuild.PublishNuget.Target

[![Build status](https://ci.appveyor.com/api/projects/status/3n59qsn8u5bxjto6?svg=true)](https://ci.appveyor.com/project/guibranco/msbuild-publishnuget-target)
[![MSBuild.PublishNuget.Target NuGet Version](https://img.shields.io/nuget/v/MSBuild.PublishNuget.Target.svg)](https://www.nuget.org/packages/MSBuild.PublishNuget.Target/)
[![MSBuild.PublishNuget.Target NuGet Downloads](https://img.shields.io/nuget/dt/MSBuild.PublishNuget.Target.svg)](https://www.nuget.org/packages/MSBuild.PublishNuget.Target/)

Provides a NuGet package that adds functionality to your project to auto pack and publish to a private nuget server the project as a nuget package.

**Remarks:** This works only with `nuget.exe` executable and is designed for **.NET Framework** projects. Not for **.NET Core**

----------

## Installation

Nuget package: https://www.nuget.org/packages/MSBuild.PublishNuget.Target

```ps

Install-Package MSBuild.PublishNuget.Target

```

## Instructions

- Add the package to the project.
- Make sure you have the `nuget.exe` executable in your path (i.e. Open a command prompt and type `nuget help` and check if the version of nuget is displayed).
- You can download the most recent version of `nuget.exe`at [NuGet downloads page](https://www.nuget.org/downloads).
- Open your `.csproj` and add the following property group to the file:

```xml

<PropertyGroup>
    <PackageAPIKey>{{YOUR PRIVATE NUGET FEED KEY}}</PackageAPIKey>
    <PackageServer>{{YOUR PRIVATE NUGET FEED URL}}</PackageServer>
</PropertyGroup>

```
- Put your own data (Feed API Key and Feed Url).
- Save the `.csproj`.
- On Visual Studio, change the current configuration to `Release` if isn't yet.
- Build!

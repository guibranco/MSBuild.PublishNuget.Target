# MSBuild.PublishNuget.Target

[![Wakatime](https://wakatime.com/badge/github/guibranco/MSBuild.PublishNuget.Target.svg)](https://wakatime.com/badge/github/guibranco/MSBuild.PublishNuget.Target)
[![Build Status](https://ci.appveyor.com/api/projects/status/3n59qsn8u5bxjto6?svg=true)](https://ci.appveyor.com/project/guibranco/msbuild-publishnuget-target)
[![NuGet Version](https://img.shields.io/nuget/v/MSBuild.PublishNuget.Target.svg)](https://www.nuget.org/packages/MSBuild.PublishNuget.Target/)
[![NuGet Downloads](https://img.shields.io/nuget/dt/MSBuild.PublishNuget.Target.svg)](https://www.nuget.org/packages/MSBuild.PublishNuget.Target/)
[![CodeFactor](https://www.codefactor.io/repository/github/guibranco/MSBuild.PublishNuget.Target/badge)](https://www.codefactor.io/repository/github/guibranco/MSBuild.PublishNuget.Target)

🎯⚙️ **MSBuild.PublishNuget.Target** is a NuGet package that automates the process of packing and publishing your .NET Framework project as a NuGet package to a private NuGet server.

> **Note:**  
> - This package is designed for **.NET Framework** projects and does not support **.NET Core** or newer frameworks.  
> - It requires the `nuget.exe` executable to be available in your system's PATH.

---

## 🚀 Features
- Automatically generates `.nupkg` files during the build process.
- Publishes the generated package to a specified private NuGet feed.
- Configurable options for package directory, referenced projects, and more.

---

## 📦 Installation

Install the package via NuGet Package Manager Console:

```ps
Install-Package MSBuild.PublishNuget.Target
```

Or visit the [NuGet package page](https://www.nuget.org/packages/MSBuild.PublishNuget.Target/) for more information.

---

## 🛠️ Configuration Instructions

### Prerequisites
1. Ensure the `nuget.exe` executable is installed and available in your system's PATH.  
   - Open a command prompt and type `nuget help`. If the version information is displayed, you're ready to go.
   - If `nuget.exe` is not installed, download the latest version from the [NuGet Downloads Page](https://www.nuget.org/downloads).

### Setup
1. Add the NuGet package to your project.

2. Open your `.csproj` file and add the following `<PropertyGroup>` configuration:

   ```xml
   <PropertyGroup>
       <PackageAPIKey>{{YOUR PRIVATE NUGET FEED KEY}}</PackageAPIKey>
       <PackageServer>{{YOUR PRIVATE NUGET FEED URL}}</PackageServer>
       <PackageDir>{{DIRECTORY TO GENERATE THE .NUPKG}}</PackageDir>
       <PackageIncludeReferencedProjects>true</PackageIncludeReferencedProjects>
   </PropertyGroup>
   ```

   Replace the placeholders with the following:
   - **`PackageAPIKey`**: Your private NuGet feed API key.
   - **`PackageServer`**: The URL of your private NuGet feed.
   - **`PackageDir`**: Directory where the `.nupkg` file will be generated.
   - **`PackageIncludeReferencedProjects`**: Set to `true` to include referenced projects, or `false` to exclude them (defaults to `false` if omitted).

3. Save the `.csproj` file.

4. In Visual Studio, set the current build configuration to `Release`.

5. Build the project.

---

## 🎉 Example Workflow

1. Install the NuGet package and configure your `.csproj` file as described.
2. Build your project in `Release` mode.
3. The generated `.nupkg` file will be published to your private NuGet feed.

---

## 🔗 Resources
- [NuGet Downloads](https://www.nuget.org/downloads)  
- [GitHub Repository](https://github.com/guibranco/MSBuild.PublishNuget.Target)

---

## 🧩 Contributing

Contributions are welcome!  
Feel free to submit issues, feature requests, or pull requests to improve this project.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

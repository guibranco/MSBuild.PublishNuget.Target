--------------------------------------------------------------------------------------------
-------------------------------- MSBuild.PublishNuget.Target --------------------------------
--------------------------------------------------------------------------------------------

Thank you for using MSBuild.PublishNuget.Target! 🎯⚙️  

This NuGet package simplifies the process of packing and publishing your .NET Framework project as a NuGet package to a private NuGet feed.

--------------------------------------------------------------------------------------------
## Overview

- Automatically generates a `.nupkg` file during the build process.
- Publishes the generated package to a specified private NuGet server.
- Designed specifically for **.NET Framework** projects (not compatible with .NET Core or newer frameworks).
- Requires the `nuget.exe` executable to be available in your system's PATH.

--------------------------------------------------------------------------------------------
## Getting Started

1. **Install `nuget.exe`:**  
   Ensure the `nuget.exe` executable is installed and accessible via your system's PATH.  
   - Open a command prompt and type `nuget help`. If the version information is displayed, you're ready to proceed.
   - If `nuget.exe` is not installed, download the latest version from the NuGet downloads page:  
     https://www.nuget.org/downloads  

2. **Add the Package:**  
   Install this package into your project using the NuGet Package Manager Console:  
   ```ps
   Install-Package MSBuild.PublishNuget.Target
   ```

3. **Configure Your Project:**  
   Open your `.csproj` file and add the following `<PropertyGroup>`:  

   ```xml
   <PropertyGroup>
       <PackageAPIKey>{{YOUR PRIVATE NUGET FEED KEY}}</PackageAPIKey>
       <PackageServer>{{YOUR PRIVATE NUGET FEED URL}}</PackageServer>
       <PackageDir>{{DIRECTORY TO GENERATE THE .NUPKG}}</PackageDir>
       <PackageIncludeReferencedProjects>true</PackageIncludeReferencedProjects>
   </PropertyGroup>
   ```

   Replace the placeholders with your specific values:  
   - **`PackageAPIKey`**: Your private NuGet feed API key.  
   - **`PackageServer`**: The URL of your private NuGet feed.  
   - **`PackageDir`**: Directory where the `.nupkg` file will be generated.  
   - **`PackageIncludeReferencedProjects`**: Set to `true` to include referenced projects or `false` to exclude them (defaults to `false` if omitted).  

4. **Build Your Project:**  
   - Set the build configuration to `Release`.  
   - Build your project in Visual Studio or your CI pipeline.

--------------------------------------------------------------------------------------------
## Example Workflow

1. Install the NuGet package and configure your `.csproj` as described above.
2. Build your project in `Release` mode.
3. The `.nupkg` file is created and published to the private NuGet feed.

--------------------------------------------------------------------------------------------
## Additional Resources

- [NuGet Downloads](https://www.nuget.org/downloads)  
- [GitHub Repository](https://github.com/guibranco/MSBuild.PublishNuget.Target)

--------------------------------------------------------------------------------------------
## Notes

- This package only works with `.NET Framework` projects and requires `nuget.exe`.  
- Contributions and feedback are welcome! Visit the GitHub repository for more information.

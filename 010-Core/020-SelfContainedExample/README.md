# .NET Core Console Self Contained Example

## Steps

### Update SelfContainedExample.csproj

```
<Project Sdk="Microsoft.NET.Sdk">

  <PropertyGroup>
    <OutputType>Exe</OutputType>
    <TargetFramework>netcoreapp2.0</TargetFramework>
	<RuntimeIdentifier>win-x64</RuntimeIdentifier>
	<OutputPath>dist</OutputPath>
  </PropertyGroup>

</Project>

```

### Build 

```
dotnet build
```

The built files are generated on dist\netcoreapp2.0\win-x64\SelfContainedExample.exe

# Reference
* https://docs.microsoft.com/en-us/dotnet/core/tools/csproj
* https://msdn.microsoft.com/en-us/library/bb629394.aspx
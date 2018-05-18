# C# .NET Framework MSBuild Hello World Example

MSBuild is shipped with .NET Framework. It can be used to compile .cs file into .exe.

**Path**
```
<NET Framework Folder>/MSBuild.exe
```

Usually, the path is 
```
C:/Windows/Microsoft.NET/Framework/<Framework Version>/MSBuild.exe
```

Also, you can add the framework path into Path of System Variable.

```
msbuild
```

It would create dist/NETFrameworkMSBulidExample.exe


# Configuration

```
<Project DefaultTargets="Build" xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
	
	<PropertyGroup>  
		<AssemblyName>NETFrameworkMSBulidExample</AssemblyName>
		<OutputPath>dist\</OutputPath>  
		<OutputType>Exe</OutputType>
	</PropertyGroup>  
	
	<ItemGroup>
		<Compile Include="*.cs"/>
	</ItemGroup>
	
	<Target Name="Build">
		<MakeDir Directories="$(OutputPath)" Condition="!Exists('$(OutputPath)')" />
		<Csc Sources="@(Compile)" OutputAssembly="$(OutputPath)$(AssemblyName).exe" />
	</Target>
	
</Project>  

```

# Reference

* https://msdn.microsoft.com/en-us/library/dd576348.aspx
* https://msdn.microsoft.com/en-us/library/t4w159bs.aspx
# .NET Core Console Hello World Example

## Steps

### 1. Initialize Application**
```
dotnet new console
```

**List Files**
```
dir /b
```

**Console Output**
```
010-NETCoreExample.csproj
obj
Program.cs
README.md
```

### Rename 010-NETCoreExample.csproj to NETCoreExample.csproj 

```
rename 010-NETCoreExample.csproj NETCoreExample.csproj 
```

### Update Program.cs
```
namespace NETCoreExample
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello World!");
        }
    }
}
```

### Build Project

```
dotnet build
```

Alternatively,
```
dotnet msbuild
```

The binary would be generated in bin\Debug\netcoreapp2.0\NETCoreExample.dll

### Run Application on .NET Core Runtime

```
dotnet bin\Debug\netcoreapp2.0\NETCoreExample.dll
```

**Console Output**
```
Hello World!
```


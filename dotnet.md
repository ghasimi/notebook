# .NET 
Summary notes on [.NET](https://en.wikipedia.org/wiki/.NET) installation, sample codes, etc.

## Installation

Microsot .NET [download page] (https://dotnet.microsoft.com/en-us/download) provides two options for Linux systems:

1. Manual: "commonly used as part of continuous integration testing or on an unsupported Linux distribution.
2. Packages: Convenient and recommended for developers.

### Example:.NET Package installation on Ubuntu

1. Checking Ubuntu release to select the supported package:
```
$ lsb_release

No LSB modules are available.
Distributor ID:	Ubuntu
Description:	Ubuntu 22.04.1 LTS
Release:	22.04
```
2. Installation using `apt`:
```
sudo apt-get update && \
  sudo apt-get install -y dotnet6
```

3. Checking the SDKs and runtimes:

```
$ dotnet --list-sdks
6.0.110 [/usr/lib/dotnet/dotnet6-6.0.110/sdk]
```

```
$ dotnet --list-runtimes

Microsoft.AspNetCore.App 6.0.10 [/usr/lib/dotnet/dotnet6-6.0.110/shared/Microsoft.AspNetCore.App]
Microsoft.NETCore.App 6.0.10 [/usr/lib/dotnet/dotnet6-6.0.110/shared/Microsoft.NETCore.App]
```
### SDK vs Runtime 
Microsoft's advice:
> Install the SDK (which includes the runtime) if you want to develop .NET apps. 
Or, if you only need to run apps, install the Runtime. 
If you're installing the Runtime, we suggest you install the ASP.NET Core Runtime as it includes both .NET and ASP.NET Core runtimes.

## "Hello World"

A simple "Hello World" console app in `C#` to test the `.NET` framework. 

1.  App's directory. 
```
mkdir HelloWorld && \ 
  cd HelloWorld  
```
2. Create the app. 

```
dotnet new console --framework net6.0
```
Now the app's directory looks like this:

```
+ HelloWorld
  |  
  + HelloWorld.csproj
  + obj   
  + Program.cs
```
And the content of `Program.cs`:
```c#
// See https://aka.ms/new-console-template for more information
Console.WriteLine("Hello, World!");
```

3. Running the app.

```
dot net run
```
Which will print `Hello, World!` in the terminal. 





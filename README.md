# Demonstrating Swashbuckle.AspNetCore.Cli System.IO.FileLoadException

## Qucikstart

```
dotnet build
dotnet swagger tofile Webapi.NetCore31/bin/Debug/netcoreapp3.1/Webapi.NetCore31.dll v1 # prints extracted openapi spec to stdout
dotnet swagger tofile Webapi.NetCore22/bin/Debug/netcoreapp2.2/Webapi.NetCore22.dll v1 # gives System.IO.FileLoadException
```

## Stacktrace
```
Unhandled Exception: System.IO.FileLoadException: Could not load file or assembly 'System.Runtime.Loader, Version=4.1.0.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a'. The located assembly's manifest definition does not match the assembly reference. (Exception from HRESULT: 0x80131040)
   at Swashbuckle.AspNetCore.Cli.Program.<>c.<Main>b__0_3(IDictionary`2 namedArgs)
   at Swashbuckle.AspNetCore.Cli.CommandRunner.Run(IEnumerable`1 args) in C:\projects\ahoy\src\Swashbuckle.AspNetCore.Cli\CommandRunner.cs:line 68
   at Swashbuckle.AspNetCore.Cli.CommandRunner.Run(IEnumerable`1 args) in C:\projects\ahoy\src\Swashbuckle.AspNetCore.Cli\CommandRunner.cs:line 68
   at Swashbuckle.AspNetCore.Cli.Program.Main(String[] args) in C:\projects\ahoy\src\Swashbuckle.AspNetCore.Cli\Program.cs:line 108
```

## dotnet --info
```
.NET Core SDK (reflecting any global.json):
 Version:   3.1.201
 Commit:    b1768b4ae7

Runtime Environment:
 OS Name:     debian
 OS Version:  10
 OS Platform: Linux
 RID:         debian.10-x64
 Base Path:   /usr/share/dotnet/sdk/3.1.201/

Host (useful for support):
  Version: 3.1.3
  Commit:  4a9f85e9f8

.NET Core SDKs installed:
  2.1.805 [/usr/share/dotnet/sdk]
  2.2.402 [/usr/share/dotnet/sdk]
  3.0.103 [/usr/share/dotnet/sdk]
  3.1.201 [/usr/share/dotnet/sdk]

.NET Core runtimes installed:
  Microsoft.AspNetCore.All 2.1.17 [/usr/share/dotnet/shared/Microsoft.AspNetCore.All]
  Microsoft.AspNetCore.All 2.2.8 [/usr/share/dotnet/shared/Microsoft.AspNetCore.All]
  Microsoft.AspNetCore.App 2.1.17 [/usr/share/dotnet/shared/Microsoft.AspNetCore.App]
  Microsoft.AspNetCore.App 2.2.8 [/usr/share/dotnet/shared/Microsoft.AspNetCore.App]
  Microsoft.AspNetCore.App 3.0.3 [/usr/share/dotnet/shared/Microsoft.AspNetCore.App]
  Microsoft.AspNetCore.App 3.1.3 [/usr/share/dotnet/shared/Microsoft.AspNetCore.App]
  Microsoft.NETCore.App 2.1.17 [/usr/share/dotnet/shared/Microsoft.NETCore.App]
  Microsoft.NETCore.App 2.2.8 [/usr/share/dotnet/shared/Microsoft.NETCore.App]
  Microsoft.NETCore.App 3.0.3 [/usr/share/dotnet/shared/Microsoft.NETCore.App]
  Microsoft.NETCore.App 3.1.3 [/usr/share/dotnet/shared/Microsoft.NETCore.App]
```

error : [Unable to load the service index for source](https://github.com/DarkSystemCD/.NET_CSHARP/blob/SOLUTION/ISSUES/NUGET.MD#unable-to-load-the-service-index-for-source)


## :x: Unable to load the service index for source

- after updating dotnet version the error appeared;

**to fix-it**, in File Explorer by enabling View > Hidden Files , navigate to the following directory<br>
`C:\Users\-UserName-\AppData\Roaming\NuGet\` then open the file `NuGet.Config`

``` xml
<?xml version="1.0" encoding="utf-8"?>
<configuration>
  <packageSources>
    <!-- Comment the Following Line -->
    <!-- <add key="nuget.org" value="https://api.nuget.org/v3/index.json" protocolVersion="3" /> -->
  </packageSources>
</configuration>
```

[?] tested in a offline environment<br>
[?] issue solution found on the internet<br>
[?] vscode should now returning building projects;

@microsoft @dotnet @vscode

``` csproj
    <Project Sdk="Microsoft.NET.Sdk">

    <PropertyGroup>
```

### Framework Properties<br>
`<UseWPF>` is a flag in the project file that enables WPF features and tooling during the build process, ensuring the project is correctly configured to build and run WPF applications.<br><br>
`<Nullable>` in a .csproj file configures the compiler's handling of nullable reference types, improving code safety by providing compile-time nullability checks.<br><br>
`<LangVersion>` in a .csproj file sets the C# language version for the project, controlling which language features are available during compilation to ensure compatibility or to leverage new language capabilities.<br><br>
`<OutputType>` in a .csproj file tells the build system what kind of output to create—whether it's a console app, a Windows GUI app, or a class library—guiding how the project is compiled and packaged.<br><br>
`<NoWarn>` in a .csproj file allows you to selectively disable specific compiler warnings by listing their codes, helping to keep the build output cleaner and focused on relevant issues.<br><br>
`<TargetFramework>` in a .csproj file specifies which .NET framework version the project is intended to run on, guiding the compiler and runtime to use the appropriate libraries and features.<br><br>
            
``` csproj

            <!-- Framework Properties ============================================= -->
                <UseWPF>true</UseWPF>
                <Nullable>disable</Nullable>
                <LangVersion>11.0</LangVersion>
                <OutputType>WinExe</OutputType>
                <NoWarn> 0219; 0414; 8321; </NoWarn>
                <TargetFramework>net10-windows</TargetFramework>
```

### Assembly Attribute Properties
`<NeutralLanguage>` in a .csproj file defines the default culture of the assembly’s neutral resources, aiding in resource management and localization performance.<br><br>
`<RootNamespace>` in a .csproj file sets the default namespace for the project’s code, providing a consistent naming scope for all types within the project.<br><br>
`<StartupObject>` in a .csproj file defines the class that contains the Main method to be used as the program’s entry point, ensuring the correct startup behavior when multiple entry points exist.<br><br>
`<ApplicationIcon />` in a .csproj file defines the icon file to be used as the application’s visual icon, embedding it into the executable for display in the OS interface.<br><br>
`<GenerateAssemblyInfo>` in a .csproj file specifies whether the build automatically generates assembly metadata attributes, simplifying assembly info management or allowing manual control when disabled.<br><br>
`<GenerateAssemblyInfoFile>` in a .csproj file sets the filename and path for the auto-generated assembly info source file, allowing control over where the build outputs the generated assembly metadata code.<br><br>
`<IncludeSourceRevisionInInformationalVersion>` in a .csproj file enables embedding the source control revision identifier into the assembly's informational version metadata, improving build traceability and version tracking.<br><br>

`<Product>` in a .csproj file sets the product name metadata for the assembly, helping to identify the software product associated with the compiled output.<br><br>
`<AssemblyTitle>` in a .csproj file sets the assembly’s title metadata, providing a readable name for the assembly that appears in file properties and other metadata displays.<br><br>

``` csproj
            <!-- Assembly Attribute Properties ==================================== -->
                <NeutralLanguage>en-US</NeutralLanguage>
                <RootNamespace>MainSpace</RootNamespace>
                <StartupObject>MainSpace.MainClass</StartupObject>
                <ApplicationIcon />
                <GenerateAssemblyInfo>true</GenerateAssemblyInfo>
                <GenerateAssemblyInfoFile>false</GenerateAssemblyInfoFile>
                <IncludeSourceRevisionInInformationalVersion>false</IncludeSourceRevisionInInformationalVersion>

                <Product>MyApplicationName</Product>
                <AssemblyTitle>MyApplicationTaskManagerTitle</AssemblyTitle>
                <AssemblyName>MyApplicationFileName</AssemblyName>
                <Company>MyApplicationBrand</Company>
                <Copyright>All Rights Reserved.</Copyright>
                <Description>MyApplicationQuoteLine</Description>

                <AssemblyVersion></AssemblyVersion>
                <InformalVersion></InformalVersion>
                <FileVersion>1.0.0.0</FileVersion>

                <Configuration></Configuration>
```
### Publish-Related Properties

``` csproj
            <!-- Publish-Related Properties ======================================= -->
                <AppendTargetFrameworkToOutputPath>false</AppendTargetFrameworkToOutputPath>
                <AppendRuntimeIdentifierToOutputPath>false</AppendRuntimeIdentifierToOutputPath>
                <CopyLocalLockFileAssemblies>false</CopyLocalLockFileAssemblies>
                <ErrorOnDuplicatePublishOutputFiles>false</ErrorOnDuplicatePublishOutputFiles>
                <PreserveCompilationContext>false</PreserveCompilationContext>
                <PreserveCompilationReferences>false</PreserveCompilationReferences>
                <SatelliteResourceLanguages>en-US</SatelliteResourceLanguages>
```
### Compilation-Related Properties 
            
``` csproj
            <!-- Compilation-Related Properties =================================== -->
                <GenerateSerializationAssemblies>Off</GenerateSerializationAssemblies>
                <GenerateDocumentationFile>false</GenerateDocumentationFile>
                <EnablePreviewFeatures>false</EnablePreviewFeatures>
                <AllowUnsafeBlocks>false</AllowUnsafeBlocks>

                    <!-- Debug ==================================================== -->
                    <DebugSymbols>false</DebugSymbols>
                    <DebugType>none</DebugType>
                    <Optimize>false</Optimize>

                <ErrorReport>none</ErrorReport>
                <CodeAnalysisRuleSet />
                <DefineConstants />

            <!-- Default Item Inclusion Properties ================================ -->

            <!-- Code Analysis Properties ========================================= -->

            <!-- Runtime Configuration Properties ================================= -->
```
### Reference Properties

``` csproj

            <!-- Reference Properties ============================================= -->
                <ValidateExecutableReferencesMatchSelfContained>true</ValidateExecutableReferencesMatchSelfContained>
                <IsPublishable>False</IsPublishable>
                <PlatformTarget>x64</PlatformTarget>
                <BaseOutputPath>bin\</BaseOutputPath>
                <ProduceReferenceAssembly>False</ProduceReferenceAssembly>
                <PackageTags />
                <EnableNETAnalyzers>False</EnableNETAnalyzers>

            <!-- Run-Related Properties =========================================== -->
                <!-- <RunArguments>-mode none</RunArguments> -->

            <!-- Hosting-Related Properties ======================================= -->

            <!-- Generated File Properties ======================================== -->
```
``` csproj
            </PropertyGroup>
```
### Condition

``` csproj

            <PropertyGroup Condition="'$(Configuration)|$(Platform)'=='Debug|AnyCPU'">
                <WarningLevel>5</WarningLevel>
                <CheckForOverflowUnderflow>True</CheckForOverflowUnderflow>
            </PropertyGroup>

            <PropertyGroup Condition="'$(Configuration)|$(Platform)'=='Release|AnyCPU'">
                <WarningLevel>5</WarningLevel>
                <CheckForOverflowUnderflow>True</CheckForOverflowUnderflow>
            </PropertyGroup>

            <!-- ============================= -->
```
### Resources

 ``` csproj

            <ItemGroup>
                <!-- Solution Default =============================================== -->

                <!-- <Compile Include="..\OTHERFILES\myfile1.cs" Link="myfile1.cs" /> -->
                <!-- <Resource Include="..\RESOURCES\*" /> -->

            </ItemGroup>
```
 ``` csproj
            </Project>
```

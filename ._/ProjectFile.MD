            <Project Sdk="Microsoft.NET.Sdk">

            <PropertyGroup>
            <!-- Framework Properties ============================================= -->
                <UseWPF>true</UseWPF>
                <Nullable>disable</Nullable>
                <LangVersion>11.0</LangVersion>
                <OutputType>WinExe</OutputType>
                <NoWarn> 0219; 0414; 8321; </NoWarn>
                <TargetFramework>net7.0-windows</TargetFramework>

            <!-- Assembly Attribute Properties ==================================== -->
                <NeutralLanguage>en-US</NeutralLanguage>
                <RootNamespace>MainSpace</RootNamespace>
                <StartupObject>MainSpace.MainClass</StartupObject>
                <ApplicationIcon />
                <GenerateAssemblyInfo>true</GenerateAssemblyInfo>
                <GenerateAssemblyInfoFile>false</GenerateAssemblyInfoFile>
                <IncludeSourceRevisionInInformationalVersion>false</IncludeSourceRevisionInInformationalVersion>

                <NeutralLanguage>en-US</NeutralLanguage>
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

            <!-- Publish-Related Properties ======================================= -->
                <AppendTargetFrameworkToOutputPath>false</AppendTargetFrameworkToOutputPath>
                <AppendRuntimeIdentifierToOutputPath>false</AppendRuntimeIdentifierToOutputPath>
                <CopyLocalLockFileAssemblies>false</CopyLocalLockFileAssemblies>
                <ErrorOnDuplicatePublishOutputFiles>false</ErrorOnDuplicatePublishOutputFiles>
                <PreserveCompilationContext>false</PreserveCompilationContext>
                <PreserveCompilationReferences>false</PreserveCompilationReferences>
                <SatelliteResourceLanguages>en-US</SatelliteResourceLanguages>

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

            </PropertyGroup>

            <PropertyGroup Condition="'$(Configuration)|$(Platform)'=='Debug|AnyCPU'">
                <WarningLevel>5</WarningLevel>
                <CheckForOverflowUnderflow>True</CheckForOverflowUnderflow>
            </PropertyGroup>

            <PropertyGroup Condition="'$(Configuration)|$(Platform)'=='Release|AnyCPU'">
                <WarningLevel>5</WarningLevel>
                <CheckForOverflowUnderflow>True</CheckForOverflowUnderflow>
            </PropertyGroup>

            <!-- ============================= -->

            <ItemGroup>
                <!-- Solution Default =============================================== -->

                <!-- <Compile Include="..\OTHERFILES\myfile1.cs" Link="myfile1.cs" /> -->
                <!-- <Resource Include="..\RESOURCES\*" /> -->

            </ItemGroup>

            </Project>

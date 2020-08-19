# templates-repro

This will work:

```
set PROJECT_NAME=TestWorks
mkdir %PROJECT_NAME% && cd %PROJECT_NAME% && dotnet new sln && dotnet new test-add-sln-works -n %PROJECT_NAME% 
```

Different behavior if  `postaction.args.primaryOutputIndexes` is omitted (tries to add "AddFailsOptIndex.csproj" instead of "TestFailsOutInd\TestFailsOutInd.csproj" as first one will do):

```
set PROJECT_NAME=TestFailsOutInd
mkdir %PROJECT_NAME% && cd %PROJECT_NAME% && dotnet new sln && dotnet new test-add-sln-outind-fails -n %PROJECT_NAME% 
```
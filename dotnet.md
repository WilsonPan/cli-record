# NET CORE CLI  

## Solution or Project

- `dotnet sln`
   
    1. `dotnet sln list`
    2. `dotnet sln add todo-app/todo-app.csproj`
    3. `dotnet sln remove todo-app/todo-app.csproj`
    4. `dotnet sln todo.sln remove **/*.csproj`

- `dotnet new`
    1. `dotnet new --list` --- *installed templates*
    2. `dotnet new --type project`
    3. `dotnet new --type it`
    4. `dotnet new -n 'project name'`
    5. `dotnet new spa -l`
   
- `dotnet clean`
    1. `dotnet clean -c Release`  
    2. `dotnet clean --runtime osx-x64`

- `dotnet add reference`
    1. `dotnet add app/app.csproj reference lib/lib.csproj`  -- add lib to app
    2. `dotnet add reference lib1/lib1.csproj lib2/lib2.csproj`  -- current project add multiple project references

- `dotnet list reference`
    1. `dotnet list reference`
    2. `dotnet list app/app.csproj reference`

- `dotnet remove reference`
    1. `dotnet remove app/app.csproj reference lib/lib.csproj`
    2. `dotnet remove reference lib1/lib1.csproj lib2/lib2.csproj`

## Building && Runing

- `dotnet store`
    1. `dotnet store --manifest packages.csproj --framework-version 2.0.0`
    2. `dotnet store --manifest packages.csproj --skip-optimization`


- `dotnet build`
    1. `dotnet build -c Release`
    2. `dotnet build -f netcoreapp3.1`
    3. `dotnet build --runtime osx-x64`
    4. `dotnet build --no-restore`

- `dotnet msbuild`
    1. `dotnet msbuild -property:Configuration=Release`
    2. `dotnet msbuild -restore`  ==  `dotnet build`

- `dotnet run`
    1. `dotnet run --project ./projects/proj1/proj1.csproj`
    2. `dotnet run --configuration Release`
    3. `dotnet watch run`

- `dotnet test`
    1. `dotnet test ~/projects/test1/test1.csproj`
    2. `dotnet test --logger trx`  --- **test & generate result**
    3. `dotnet test --logger "console;verbosity=detailed"`
   
## Package 

- `dotnet nuget`
   
    1. `dotnet nuget enable source <NAME>`
    2. `dotnet nuget disable source <NAME>`
    3. `dotnet nuget list source`
    4. `dotnet nuget remove source <NAME>`
    5. `dotnet nuget update source <NAME> --source c:\packages`
    6. `dotnet nuget delete <PACKAGE_NAME> <PACKAGE_VERSION>`
    7. `dotnet nuget push foo.nupkg -k 4003d786-cc37-4004-bfdf-c4f3e8ef9b3a -s https://customsource/`

- `dotnet pack`  *builds the project and creates NuGet packages*
   
    1. `dotnet pack`
    2. `dotnet pack ~/projects/app1/project.csproj`
    3. `dotnet pack --no-build --output nupkgs`

- `dotnet restore`
    
    1. `dotnet restore ./projects/app1/app1.csproj`
    2. `dotnet restore -s c:\packages\mypackages`

- `dotnet add package`

    1. `dotnet add package Newtonsoft.Json`
    2. `dotnet add ToDo.csproj package Microsoft.Azure.DocumentDB.Core -v 1.0.0`
    3. `dotnet add package Microsoft.AspNetCore.StaticFiles -s https://dotnet.myget.org/F/dotnet-core/api/v3/index.json`

- `dotnet list package`
    
    1. `dotnet list SentimentAnalysis.csproj package`
    2. `dotnet list package --outdated --include-prerelease`   --- **including prerelease versions**
    3. `dotnet list package --framework netcoreapp3.0`


## Tools

- `dotnet publish`
  
    1. `dotnet publish --runtime osx.10.11-x64`
    2. `dotnet publish --framework netcoreapp3.1`
    3. `dotnet publish ~/projects/app1/app1.csproj`

- `dotnet tool`
    1. `dotnet tool list`
    2. `dotnet tool list -g | --global`
    3. `dotnet tool list --local`
    4. `dotnet tool install  <PACKAGE_NAME>`
    5. `dotnet tool install -g <PACKAGE_NAME>`
    6. `dotnet tool install dotnetsay --tool-path ~/bin`
    7. `dotnet tool restore`
    8. `dotnet tool run dotnetsay`
    9. `dotnet tool uninstall <PACKAGE_NAME> -g|--global`
    10. `dotnet tool uninstall <PACKAGE_NAME> --tool-path <PATH>`
    11. `dotnet tool uninstall <PACKAGE_NAME>`
    12. `dotnet tool update -g dotnetsay`
    13. `dotnet tool update dotnetsay --tool-path ~/bin`
    14. `dotnet tool update -g dotnetsay --version 2.0.*`
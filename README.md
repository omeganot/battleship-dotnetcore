[![Build status](https://psdstewards.visualstudio.com/PSD/_apis/build/status/proscrumdev.battleship-dotnetcore-CI)](https://psdstewards.visualstudio.com/PSD/_build/latest?definitionId=13)

# Build the application 
In the root folder of the application there is a Battleship.sln which can be used to build all projects by executing
```bash
dotnet build 
```

# Run the application

## Running locally
You neet to have the dotnet core runtime installed on your local machine
https://www.microsoft.com/net/download

You can now run the game with
```bash
dotnet run --project .\Battleship.Ascii\Battleship.Ascii.csproj
```


## Running within a docker container
You can easily run the game within a docker container.

Change into the Battleship folder

```bash
docker run -it -v ${PWD}:/battleship microsoft/dotnet bash
```

This starts a new container and maps your current folder on your host machine as the folder battleship in your container and opens a bash console. In bash then change to the folder battleship/Battleship.Ascii and run
```bash
dotnet run 
```

# Execute Tests
There is a ExecuteTests.ps1 file which can be used to execute the tests. You can also run the tests by executing the tests within the test project with
```bash
dotnet test 
```



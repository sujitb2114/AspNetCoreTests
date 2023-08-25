# AspNetCoreTests

This project is ASP.NET Core application to demonstrate my work on ASP.NET Core unit and integration tests. 
Projects are thin and clean having just minimal code to show how testing related issues are solved.

## Unit tests

Unit tests project demonstrates the following features:

* Unit testing controllers
    * Checking if correct view is returned
    * Faking current user correctly
* Unit testing service classes
* Using EF Core in-memory database for unit tests
* Script to generate and display code coverage reports
    * run-tests.bat file runs tests and code coverage analytics
    * Look inside model classes to see how leave code out from coverage analysis

NB! You need to install report generator manually. Open unit tests project folder in command line and type the following command: 

```
dotnet tool install dotnet-reportgenerator-globaltool --tool-path tools
```

## Integration tests

Although there are simpler ways to get started with ASP.NET Core integration tests, the approach here is more 
flexible. Integration test examples have these important features:

* Use custom appsettings.json file for integration tests
* Use custom web application startup class
* Faking authenticated and authorized user
* Support for multiple faked user accounts and roles
* Testing with users in different roles

# .NET REST API Exercise

## Goal

The goal of this exercise is to learn how to use GitHub Copilot for building a REST API using .NET.

## Instructions

The `dotnet` folder contains the `MinimalAPI.sln` solution, with 2 projects:

- `MinimalAPI` is a minimal WebAPI project created using `dotnet new webapi -minimal`
- `MinimalAPI.Tests` is a minimal xUnit project created using `dotnet new xunit`

To run the tests, open a terminal in the `dotnet` folder and run:

``` bash
dotnet test
```

To run the app, open a terminal in the `dotnet` folder and run:

``` bash
dotnet run --project .\MinimalAPI\MinimalAPI.csproj
```

### Exercise 1

- Inside `MinimalAPI\Program.cs` add a new Hello World endpoint at `/` that returns a `Hello World!` string.
- Run `dotnet test`
- If the test passes you should see something like this:

``` bash
Microsoft (R) Test Execution Command Line Tool Version 17.6.0 (x64)
Copyright (c) Microsoft Corporation.  All rights reserved.

Starting test execution, please wait...
A total of 1 test files matched the specified pattern.

Passed!  - Failed:     0, Passed:     1, Skipped:     0, Total:     1, Duration: < 1 ms - MinimalAPI.Tests.dll
```

### Exercise 2

- Inside `MinimalAPI\Program.cs` add the following endpoints:

- **/daysBetweenDates**: 

Calculate days between two dates<br />
Retrieve two parameters `date1` and `date2` from a query string, and calculate the days between those two dates<br />

- **/validatePhoneNumber**: 

Retrieve a `phoneNumber` parameter from a query string<br />
Validate phoneNumber with Spanish format, for example `+34666777888`<br />
If phoneNumber is valid return true<br />

- **/validateSpanishDni**:

Retrieve dni parameter from a query string<br />
Validate the format of a spanish DNI (8 digits and 1 letter)<br />
If dni is valid return "valid"<br />
If dni is not valid return "invalid"<br />

- **/returnColorCode**:

Retrieve prameter color from a query string<br />
Read colors.json file and return the rgba field<br />
Iterate for each color in colors.json to find the color passed as the parameter<br />
Return the code.hex field<br />

- **/tellMeAJoke**:

Make a call to the joke api https://api.chucknorris.io/jokes/random<br />
Return a random joke using axios<br />
        
- **/moviesByDirector**:

(this will require requesting a FREE API key here https://www.omdbapi.com/apikey.aspx)

Retrieve `director` parameter from a query string<br />
Make a call to the movie api and return a list of movies of that director using axios<br />
Return the full list of movies<br />

- **/parseUrl**:

Retrieve `someurl` parameter from a query string<br />
Parse the url and return the protocol, host, port, path, query string and hash<br />

- **/listFiles**:

Get the current directory<br />
Get the list of files in the current directory<br />
Return the list of files<br />

- **/calculateMemoryConsumption**:

Return the memory consumption of the process in GB, rounded to 2 decimals

- **/randomEuropeanCountry**:

Make an array of European countries and its ISO codes<br />
Return a random country and its ISO code from the array<br />

### Exercise 3

Create a Dockerfile for the Minimal API project<br />
Build the image and run the app on port 8080

``` powershell
docker build -t dotnetapp .
docker run -d -p 8080:80 --name dotnetapp dotnetapp
```

# Node.js REST API Exercise

## Goal

The goal of this exercise is to learn how to use GitHub Copilot for building a REST API using Node.js.

## Instructions

- Open **nodeserver.js** and instruct Copilot to create a server and the first "GET" method call based on the ready-made comments
- Open **test.js** file and analyze the current test
- Open a command prompt, navigate to **node** folder, and run the test with `mocha test.js` command (you may want to use the --exit flag)
- See the result, it should display something like:

``` bash
mocha test.js
server is listening on port 3000

  Node Server
    
    √ should return "key not passed" if key is not passed

  1 passing (34ms)

```

- In the **nodeserver.js** develop the rest of the methods described in the [Exercise](#exercise) section below
- In the **test.js** file add methods to test the functionality
- Run the tests to verify that all works as expected 
- Open **dockerfile**, and fill it based on the comments in order to create a docker container with a node image that can run the web server
- Create a command to run docker on port 4000
- Test that the application is working on port 4000
- In the **nodeserver.js** file, you can type a new line like `//run a curl command to test the server`
to see how Copilot produces a curl command, based on the current file, to be executed in command line.
Also you can be more specific like: `//run a curl command to test the daysBetweenDates method` so that it will generate a test for a specific method 

## Exercise

- The exercise consist of building a web server using Node.js that serves the request of various functionality
- Make sure that the implemented functionality works as expected by covering it with tests
- Once the development is completed, build a container using Docker (see the instructions above)
- You may also want to try documenting and refactorig your code using Copilot.

The requests that the server must handle are the following:

- **/get** : 

Return a hello + key (parameter) message<br />
Please see the comments in **nodeserver.js** file<br />

- **/daysBetweenDates**: 

Calculate days between two dates<br />
Retrieve 2 parameters `date1` and `date 2` from a query string, and calculate the days between those two dates<br />

- **/validatephonenumber**: 

Retrieve `phoneNumber` parameter from a query string<br />
Validate phoneNumber with Spanish format, for example +34666777888<br />
If phoneNumber is valid return "valid"<br />
If phoneNumber is not valid return "invalid"<br />

- **/validateSpanishDNI**:

Retrieve `dni` parameter from a query string<br />
Validate the format of a spanish DNI (8 digits and 1 letter)<br />
If dni is valid return "valid"<br />
If dni is not valid return "invalid"<br />

- **/returnColorCode**:

Retrieve `color` parameter from a query string<br />
Read colors.json file and return the rgba field<br />
Iterate for each color in colors.json to find the color passed as a parameter<br />
Return the code.hex field<br />

- **/tellMeAJoke**:

Make a call to the joke api https://api.chucknorris.io/jokes/random<br />
Return a random joke using axios<br />
        
- **/parseUrl**:

Retrieve `someurl` parameter from a query string<br />
Parse the url and return the protocol, host, port, path, querystring and hash<br />

- **/listFiles**:

Get the current directory<br />
Get the list of files in the current directory<br />
Return the list of files<br />

- **/getLineByLinefromtTextFile**:

Create a **sample.txt** file in the root directory and fill it with several lines of text with a couple of them containing a word "Fusce"<br />
Create a promise to read the file line by line, and return a list of lines that contains "Fusce"<br />
Return the list of lines<br />

- **/calculateMemoryConsumption**:

Return the memory consumption of the process in GB, rounded to 2 decimals

- **/makeZipFile**:

Using zlib create a zip file called sample.gz that contains **sample.txt**

- **/randomEuropeanCountry**:

Make an array of European countries and its ISO codes<br />
Return a random country and its ISO code from the array<br />

Now it's time to make sure all the tests pass and to containerize the application.

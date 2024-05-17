### Notes on Command Line Arguments

What are Command Line Arguments?
CLI = command line interface

command line arguments are strings of text used to pass additional information to a programs when an application is run through the CLI of an operating system
these arguments include into to set configuration or property values for an application

- arguments are passed after the program name in the prompt, example 
```
$ [runtime] [script_name] [argument-1 argument-2 argument-3 ... argument-n]
```
syntax --> arguments separated by a space 

multiple command line areguments are separated by commas to help readability 

arguments can also be passed by key-value pairs depending on the program

### Why use command line arguments?

Benefits
1. pass info to an application b4 it starts (good for large number of configuration settings)
2. Command line arguments are passes as <b>strings<b>, 
strings can be easily converted to other data types in an application ... is flexbile 
3. you can pass ujnlimited number of arguments via command line
4. useful for automated testing ---> why? bc command line arguments are used in conjuntion with scripts and batch files

Disadvantage
1. steep learning curve to use the interface, need lots of experience with CLI tools to be effective
2. Command line applications are difficult to use on non desktop/computer systems, ie phone/tables = harder to use

## Passing Command Line Arguments in Node.js

Node.js can accept command line arguments

##### Using process.argv
process.argv 
- is a global object you can use without importing any additional libraries to use it
- to retrieve arguments in Node.js use the process.argv array by passing arguments to a Node.js application

#### Syntax
1. The first element of the process.argv array is the file system path point to the <b>node<b> executable
2. Second element --> the name of the JavaScript file being executed
3. The first argument passed by the user
4. *notes for beginners *'d like to remind you beginners out there that JavaScript uses zero-based indexes on arrays (like many other languages), which means that first element will be stored at "0th" index and last element will be stored at "n-1" index, where "n" is the total number of elements in the array.*

To initiate it

```
'use strict';

for (let j = 0; j < process.argv.length; j++) {
    console.log(j + ' -> ' + (process.argv[j]));
}
```
// copy and paste this to the filed names processargv.js
What does this script do?
it loops through the array to frint the indexes along with the elements stored in those indexes, it is good for debugging

run this command in the directory where the processargv.js file is saved

```
$ node processargv.js tom jack 43
```

Here we are passing three arguments to the processargv.js program. You will see that "tom" will be stored at 2nd index while "jack" and "43" will be stored at 3rd and 4th indexes, respectively. The output should look something like this:

```
$ node processargv.js tom jack 43
0 -> /Users/scott/.nvm/versions/node/v4.8.0/bin/node
1 -> /Users/scott/javascript/processargv.js
2 -> tom
3 -> jack
4 -> 43
```

first index --> contains the path to our <b>node<b> executable
second index --> path to the script file
other index--> contain the arguments we passed in sequence
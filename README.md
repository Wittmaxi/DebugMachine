# DebugMachine
## Project
Needed something of the likes for my projects - thought I'd share

## Using 
### Including 
Simply include the file "debugMachine.h" into all of the C++ files you want to use it's features in. 
It will by standard create an object of the name "d" - I't will be used to debug.
### Setting up
At first, the attribute ```writing``` of d has to be set to true or false. 
It modulates, wether d will output message or it wont. 

```
d.write = true; // output messages will be shown
d.write = false; //nothing will be shown
```

### Usage in projects
The debug machine has three basic commands. 
```out```, ```debug```, ```warn``` and ```info``` 
They all are functions of the form of ```void out (std::string toWrite, bool nl = true)```; They only change by how they output the messages: the output color. 

To use, simply use 
```
d.out ("Hello"); //normal output, new line
d.out ("Hello", false); //normal output, no new line
d.warn ("Warning"); //normal warning [red], new line
d.warn ("Warning", false); //normal warning, no new line
d.info ("Info"); //normal info [cyan], new line
d.into ("Info", false); //normal info, no new line
d.debug ("Poor Mans Debugger"); //normal debug statement [magenta], new line
d.debug ("Poor Mans Debugger", false); //normal debug statement, no new line
```
### Compatibility
Tested under GNU/Linux with Gcc-C++ of standard 11.
No guarantee given for the reliability of my work [yet you are free to use it as you want to] 

### Performance
If the debug machine is deactivated [by setting d.write to false], it should get optimized out by Gcc. 

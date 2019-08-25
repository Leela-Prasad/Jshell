JShell commands starts with /
eg: /help
    /exit
    /vars

JShell comes with auto completion (for that we have to press tab command)

If you execute an expression and doesn’t assign it to a variable then Jshell automatically  assigns it to a scratch variable that we can use it later.
eg: 10 +20
$1 ==> 30

If you want to see all the variables that are created in a  Jshell session then 
/vars

eg:
jshell> /vars
|    int i = 10
|    int j = 20
|    int $3 = 30
|    int $9 = 40


/history will give the commands that you ran in a Jshell session
eg:
int i=10
int j=20
i+j
$3
$3
i
j
$3
$3+10
/vars
"Hello " + "World!"
/vars
/history



/list also gives the commands that we ran in a Jshell session BUT IT WILL NOT GIVE JSHELL COMMANDS.
It will also gives the command execution number.
eg:
1 : int i=10;
   2 : int j=20;
   3 : i+j
   4 : $3
   5 : $3
   6 : i
   7 : j
   8 : $3
   9 : $3+10
  10 : "Hello " + "World!"


This execution number is useful as we can run the previous commands with this number suppose if i want to run command with number 6 then 
/6


To execute the last command we can run
/!


/reset will reset all the variables including scratch variables.


To do search in the previously executed commands
ctrl + r -> reverse search
ctrl + s -> forward search
ctrl + c -> to come out of search mode.

Multi Line statements:
for if block/while blocks Jshell automatically knows the termination of the block
*** in this blocks semicolon is mandatory.

to execute a block of statements then we need follow below syntax
{
 statement1
 statement2
 statement3
}

eg: 
{
 int i=10;
 int j=20;
}

*** Any variables created in this block will not be visible after execution, and we can replace/use global/session variables in this block

Methods or Functions in Jshell:
We can create user defined methods like this.
jshell> String greeting() {
   ...> return "Hello!!!";
   ...> }
|  created method greeting()

jshell> greeting()
$12 ==> "Hello!!!"

jshell> String greeting(String name) {
   ...> return "Hello " + name;
   ...> }
|  created method greeting(String)

jshell> greeting("Leela")
$14 ==> "Hello Leela"

We can also override existing methods like this
jshell> String greeting() {
   ...> return "Hola!!!";
   ...> }
|  modified method greeting()

/methods is used to list available methods in Jshell session.
jshell> /methods
|    String greeting(String)
|    String greeting()


/imports will give the list of imports that we have in Jshell session.
By Default Jshell provides below imports.
jshell> /imports
|    import java.io.*
|    import java.math.*
|    import java.net.*
|    import java.nio.file.*
|    import java.util.*
|    import java.util.concurrent.*
|    import java.util.function.*
|    import java.util.prefs.*
|    import java.util.regex.*
|    import java.util.stream.*


/edit is used to edit a code block 

/edit 49 
/edit - > will provide a editor with all the variables/ methods/ classes that are created as part of Jshell session.


/save will save all the variables/methods/classes to a file.
e.g.: /save myCommands.jsh

/open will load all the commands in the current session.
e.g.: /open myCommands.jsh


Startup Scripts:
We can have some of the variables/expressions as a startup script so that when we trigger Jshell command all these will be loaded into the session.

/set start startupScript.jsh -> this will load the script when /reset is invoked.
so for every Jshell login we have to set this startup script so that when /reset is invoked it will load the script.


To load startup script across Jshell session we need to use -retain option
/set start startupScript.jsh -retain

But this will override the Default Startup script that jshell comes with 
like /imports will be erased.
To avoid this we have to use DEFAULT so that default settings by Jshell will be retained.
/set start startupScript.jsh -retain DEFAULT



Executing code using third party jar
/env —class-path <path-to-jar-file>

Leelas-MacBook-Air:~ Leela$ jshell
|  Welcome to JShell -- Version 11.0.2
|  For an introduction type: /help intro

jshell> /env --class-path log4j-1.2.12.jar
|  Setting new options and restoring state.

jshell> import org.apache.log4j.Logger;

jshell> Logger logger = Logger.getLogger("Testclass");
logger ==> org.apache.log4j.Logger@4e7dc304

jshell> logger.error("This is Error Message");
log4j:WARN No appenders could be found for logger (Testclass).
log4j:WARN Please initialize the log4j system properly.

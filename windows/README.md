# JDK-Switch

## Description
JDK-Switch is a set of simple batch scripts that allows WINDOWS users to quickly switch their `JAVA_HOME` environment variable.

## Prequisites
Make sure that the `JAVA_HOME` environment variable does not exist.

## Installation
1) Include the `%JAVA_HOME%\bin` variable within your `PATH`
2) Using your favorite text editor, edit the batch scripts, pointing to where each version of Java is installed.

    e.g. JDK 8 is typically installed within `C:\Program Files\java\jdk1.8.0_XX`

3) Save your changes.
4) Now, all you have to do is run the batch script as an Administrator. Right-Click -> Run as Administrator.
5) A command prompt will open and then close.
6) Open a new command prompt and voila! the updated version of java is now being used.  
You can check the version you are using with `java -version`

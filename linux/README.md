# JDK-Switch

## Description
JDK-Switch is a batch script(s) that allows users to quickly switch their `JAVA_HOME` environment variable.

## Prequisites
* Make sure that the `JAVA_HOME` environment variable does not exist.

* Make sure that `bash` is being used.

## Installation
1) Using your favorite text editor, edit the `jdk-switch` script, pointing to where each version of Java is installed.

    e.g. JDK8 is typically installed within `JDK8=/usr/lib/jvm/java-8-oracle/`

3) Save your changes.

4) Place the script into a place that you can reference.  
e.g., `/home/exela/custom-scripts/`

5) Create an alias within the `~/.bashrc` file.  This alias `jdk` will be calling the `jdk-switch` script.

```
alias jdk='source /home/exela/custom-scripts/jdk-switch'
```
6) Open a new terminal and use the alias `jdk` followed with the java version number.  
Commands such as `jdk6`, `jdk7`, `jdk8`. 

7) Voila! the updated version of java is now being used.  You can check the version you are using with `java -version`

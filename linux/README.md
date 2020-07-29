# JDK-Switch

## Description
JDK-Switch is a batch script(s) that allows users to quickly switch their `JAVA_HOME` environment variable.  This variable is set only within the existing terminal session, so that means if a new terminal is opened, it will need to be run again.

## Prequisites
* Make sure that the `JAVA_HOME` environment variable does not exist within your user profile settings.

* Make sure that `bash` is being used.

## Installation

1) Using your favorite text editor, edit the `jdk-switch` script, pointing to where each version of Java is installed/extracted.  Usually this can be found in the `/usr/lib/jvm` directory.

    e.g. JDK8 is typically installed within `JDK8=/usr/lib/jvm/java-8-oracle/`

3) Save your changes.

4) Place the script into a place that you can reference.  

```
sudo mv jdk-switch /usr/local/bin/
```

5) Create an alias within the `~/.bashrc` file.  This alias `jdk` will be calling the `jdk-switch` script.

```
alias jdk='source /usr/local/bin/jdk-switch'
```

6) Open a new terminal (or `source ~/.bashrc`) and use the alias `jdk` followed with the java version number.  
Commands such as `jdk 6`, `jdk 7`, `jdk 8`. 

7) Voila! the updated version of java is now being used.  You can verify that the `JAVA_HOME` variable has been set using `echo $JAVA_HOME`

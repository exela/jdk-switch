# JDK-Switch

## Description
JDK-Switch is a batch script(s) that allows users to quickly switch their `JAVA_HOME` environment variable.

## Prequisites
* Make sure that the `JAVA_HOME` environment variable does not exist.

* Make sure that `bash` is being used.

* [jEnv](http://www.jenv.be/) must be installled via [Homebrew](https://brew.sh/).

* Java JDKs added into [jEnv](http://www.jenv.be/).

## Installation
### If you don't have [Homebrew](https://brew.sh/) installed:

`/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

### If you don't have [jEnv](http://www.jenv.be/) installed:

1. `brew install jenv`
2. `echo 'export PATH="$HOME/.jenv/bin:$PATH"' >> ~/.bash_profile`
3. `echo 'eval "$(jenv init -)"' >> ~/.bash_profile`

### To add Java JDKs to [jEnv](http://www.jenv.be/):

1. Locate where Java is installed on the machine.  Typically found in `/Library/Java/JavaVirtualMachines/`
2.  To add in the Java installation. e.g.,:

```
jenv add /System/Library/Java/JavaVirtualMachines/1.6.0.jdk/Contents/Home

jenv add /Library/Java/JavaVirtualMachines/jdk17011.jdk/Contents/Home
```

### Using JDK-Switch

1. Using your favorite text editor, edit the `jdk-switch` script, pointing to where each version of Java is installed.

    e.g. JDK8 is typically installed within `JDK8=/Library/Java/JavaVirtualMachines/jdk1.8.0_121.jdk/Contents/Home/`

3) Save your changes.

4) Place the script into a place that you can reference.  

```
sudo mv jdk-switch ~/exela/custom-scripts/
```

5) Create an alias within the `~/.bash_profile` file.  This alias `jdk` will be calling the `jdk-switch` script.

```
alias jdk='source ~/exela/custom-scripts/jdk-switch'
```

6) Open a new terminal and use the alias `jdk` followed with the java version number you will want to use.  
Commands such as `jdk 6`, `jdk 7`, `jdk 8`. 

7) Voila! the updated version of java is now being used.  You can check the version you are using with `java -version`

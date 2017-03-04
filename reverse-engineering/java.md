## Reverse Engineering Java Program

Bytecode is the compiled java-code that the Java Virtual Machine \(JVM\) executes.

[http://resources.infosecinstitute.com/java-bytecode-reverse-engineering/](http://resources.infosecinstitute.com/java-bytecode-reverse-engineering/)

### Compile java code

```
javac file.java
```

When we compile the code like this we will end up with a file called `file.class`. That file is an executable. And can be executed with the java runtime environment like this `java file`. If we run `file` on the file we get the following response:

```
file file.class
file.class: compiled Java class data, version 52.0 (Java 1.8)
```

### Investigating the binary

We can use `strings`on the binary to output the strings in the file. We can use `xxd` to look at the data has hex.





### Java Bytecode Reference



Very handy to have:

https://en.wikipedia.org/wiki/Java\_bytecode\_instruction\_listings


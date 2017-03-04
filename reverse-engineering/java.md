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

### Disassemble With Javap

Okay, so we have investigated the file with strings and maybe gotten a little clue of what it might do.

` `javap file

This will output name of classes, functions and variables. But it will not give us the content of functions and variables. But it is still very valuable to get a first understanding of what the binary might do.

```
javap -c file
```

Now this will output the function and the opcodes for each function.

It is also useful to run it in verbose mode.

```
javap -verbose file
```

### Java Bytecode Reference

So java have its own bytecodes, it does not use the x86 bytecodes that we might be used to. So they have their own mnemonics.

Very handy to have:

[https://en.wikipedia.org/wiki/Java\_bytecode\_instruction\_listings](https://en.wikipedia.org/wiki/Java_bytecode_instruction_listings)





## References



https://www.acloudtree.com/hacking-java-bytecode-for-programmers-part1-the-birds-and-the-bees-of-hex-editing/




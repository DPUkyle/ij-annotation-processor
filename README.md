# ij-annotation-processor

Sample project to try and reproduce [IDEA-342187](https://youtrack.jetbrains.com/issue/IDEA-342187) when specifying `annotationProcessorPaths` with `maven-compiler-plugin` v3.12.0+.

Assumes JDK 17 installed.

Steps to reproduce:

1. `$ ./mvnw clean install` -> should compile without error.  Lombok version is inferred from `<dependencyManagement/>`.
2. In IntelliJ, open App.java, click "play".  Main class should compile and run successfully.

Step 1 is working correctly.

Step 2 expected outcome:
```text
[main] INFO com.kylemoore.App - Hello from lombok!
```

Step 3 actual outcome:
```text
.../ij-annotation-processor/src/main/java/com/kylemoore/App.java:14:9
java: cannot find symbol
  symbol:   variable log
  location: class com.kylemoore.App
```
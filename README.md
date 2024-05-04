# ij-annotation-processor

Sample project to try and reproduce reported error when specifying `annotationProcessorPaths` with `maven-compiler-plugin`

Assumes JDK 21 installed.

Steps to reproduce:

1. `$ ./mvnw clean install` -> should compile without error
2. In IntelliJ, open App.java, click "play".  Main class should compile and run successfully.

IJ and Maven are both behaving as expected, unable to reproduce with current versions.

Let's check certain combinations of versions to reproduce the error:

* IntelliJ
* Maven
* JDK
* Lombok
* maven-compiler-plugin
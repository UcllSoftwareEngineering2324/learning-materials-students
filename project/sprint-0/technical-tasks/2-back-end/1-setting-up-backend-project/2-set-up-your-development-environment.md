# Set up your development environment

## 1. Acceptance Criteria

At the end of this task you should be able to code, build and run Java projects.

## 2. Implementation Details

1. Install [Java JDK 17](https://docs.aws.amazon.com/corretto/latest/corretto-17-ug/downloads-list.html)
    * Running `java -version` should return output similar to:

        ```console
        openjdk version "17.0.1" 
        OpenJDK Runtime Environment Corretto-17.0.1
        OpenJDK 64-Bit Server VM Corretto-17.0.1
        ```
    * If you get wrong output then make sure that your PATH and JAVA_HOME variables are correctly set, if this is not the case, [configure them manually](https://www.baeldung.com/java-home-on-windows-mac-os-x-linux)
1. Install [Apache Maven](https://maven.apache.org/install.html)
    * Running `mvn -v` should return output similar to:
    
        ```console
        Apache Maven 3.9.6 (bc0240f3c744dd6b6ec2920b3cd08dcc295161ae)
        Maven home: /opt/apache-maven-3.9.6
        Java version: 1.8.0_45, vendor: Oracle Corporation
        Java home: /Library/Java/JavaVirtualMachines/jdk1.8.0_45.jdk/Contents/Home/jre
        Default locale: en_US, platform encoding: UTF-8
        OS name: "mac os x", version: "10.8.5", arch: "x86_64", family: "mac"
        ```

1. Install and configure an IDE of your choice
    * A good option is VS Code, you can check [this link](https://code.visualstudio.com/docs/java/java-spring-boot) for a recommended extension setup
    * Another good option is IntelliJ IDEA
        * If you want to work with IntelliJ, make sure that you use the _Ultimate Edition_, a license is free for students
        * Only the Ultimate Edition has build-in Spring tooling, the free community edition only has build-in Java tooling
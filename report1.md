# DAT250 Software Technology Experiment 1

## Technical problems encountered during installation

During the installation of SDKman I received a message asking me to install zip on my system. After following the steps in the response to this [question](https://stackoverflow.com/questions/38782928/how-to-add-man-and-zip-to-git-bash-installation-on-windows) I've managed to add it and proceed further with installation.

I had to add the Gradle installation path to the PATH variable and the Java installation path to JAVA_HOME to make them usable from my Windows terminal.

## Validation that the software development environment is working

I used

```
gradle -v
git -v
java -version
javac -version
```

to make sure everything was installed properly and that it was available from my terminal. Then I used

```
.\gradlew.bat check
.\gradlew.bat build
.\gradlew.bat run
```

commands to check whether the project is building correctly. Lastly, I tried to build and compile the project using my IDE (IntelliJ) directly.

## Technical problems and how I've solved them

There was one technical problem that I encountered, and that was a little bit different from what was described in the assignment: I had to configure Logger before I was able to compile the project because I got an error instead of a warning. I solved this by adding the below line to the `build.gradle.kts`

```
implementation("org.slf4j:slf4j-simple:2.0.7")
```

## URLs to the projects

Link to the published container: https://hub.docker.com/repository/docker/jacekweg/dat250/

Link to the repository with the project: https://github.com/jacekweg/dat250assignment1
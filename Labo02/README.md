# Labo02 - Run a Spring App Locally

## Pedagogical intent
In this lab, we'll be taking the application we're going to evolve into our own hands, to discover the Spring architecture.

---

## Task 01 - Run the app

### Use Maven to package the solution

* [Maven Doc](https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html#build-the-project)

```bash
    mvn package
```

* What operation does maven perform ?

```
It downloaded all the dependencies and compiled the project.
```

* What java dependencies are needed to make this work?

```
The dependencies are in the pom.xml file:


<webjars-bootstrap.version>5.3.2</webjars-bootstrap.version>
<webjars-font-awesome.version>4.7.0</webjars-font-awesome.version>

<checkstyle.version>10.12.5</checkstyle.version>
<jacoco.version>0.8.11</jacoco.version>
<libsass.version>0.2.29</libsass.version>
<lifecycle-mapping>1.0.0</lifecycle-mapping>
<maven-checkstyle.version>3.3.1</maven-checkstyle.version>
<nohttp-checkstyle.version>0.0.11</nohttp-checkstyle.version>
<spring-format.version>0.0.40</spring-format.version>
```

* Where do we find the pre-compiled application after that?

```
In the target folder
```

* Delete the folder containing the pre-compiled application, try again to observe the process.

* Is it a build ready for prod ?

```
No, it is not a build ready for prod.
```

### Use Java to launch the application

* [The java command](https://docs.oracle.com/en/java/javase/14/docs/specs/man/java.html)

```bash
java -jar target/spring-petclinic-3.2.0-SNAPSHOT.jar
```

* Try to access to the app via your browser

```
http://localhost:8080/
```

* You should get this page

![Home Page](img/webappSample.JPG)

* Stop the app

## Use the Spring Boot Maven plugin to launch the application

* [Maven plug in to run the app](https://docs.spring.io/spring-boot/docs/current/maven-plugin/reference/htmlsingle/#run)

```bash
 mvn spring-boot:run
```

---

## Task 02 - Explore the app

### Kind of app

* How can we access a home page via our browser?

```
http://localhost:8080/
```

* Go to http://localhost:8080/owners/find and add an owner

* Using the search function, can you find it?

* Relaunch the application and try again. How is data persistence ensured?

```
Yes i can find it. The data isn't persisted in the database.
```

* How many logic layers are implemented on this application?

```
Repository, Service, Controller
```

---
## Task 03 - Docker - First Analysis

* At this stage of the analysis, can you imagine a little better what kind of needs Docker could help us with?

```
Docker could help us to deploy the application in a container and to have a database engine in another container.
```

* Try to list the tasks to be carried out to obtain two thirds, one hosting the application part locally and the second third using Docker for the database engine.

```
1. create a docker container for the database engine
2. create the database
3. configure the application to use the database
4. run the application and the database
```

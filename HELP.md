# Read Me First
The following was discovered as part of building this project:

* The following dependencies are not known to work with Spring Native: 'Spring Boot DevTools, Spring Configuration Processor, Spring Web Services, Spring Integration, Apache Freemarker, Vaadin'. As a result, your application may not work as expected.

# Getting Started

### Reference Documentation
For further reference, please consider the following sections:

* [Official Gradle documentation](https://docs.gradle.org)
* [Spring Boot Gradle Plugin Reference Guide](https://docs.spring.io/spring-boot/docs/2.5.2/gradle-plugin/reference/html/)
* [Create an OCI image](https://docs.spring.io/spring-boot/docs/2.5.2/gradle-plugin/reference/html/#build-image)
* [Spring Integration JPA Module Reference Guide](https://docs.spring.io/spring-integration/reference/html/jpa.html)
* [Spring Integration Test Module Reference Guide](https://docs.spring.io/spring-integration/reference/html/testing.html)
* [Spring Integration HTTP Module Reference Guide](https://docs.spring.io/spring-integration/reference/html/http.html)
* [Spring Integration Web Services Module Reference Guide](https://docs.spring.io/spring-integration/reference/html/ws.html)
* [Spring Boot DevTools](https://docs.spring.io/spring-boot/docs/2.5.2/reference/htmlsingle/#using-boot-devtools)
* [Spring Configuration Processor](https://docs.spring.io/spring-boot/docs/2.5.2/reference/htmlsingle/#configuration-metadata-annotation-processor)
* [Spring Web](https://docs.spring.io/spring-boot/docs/2.5.2/reference/htmlsingle/#boot-features-developing-web-applications)
* [Validation](https://docs.spring.io/spring-boot/docs/2.5.2/reference/htmlsingle/#boot-features-validation)
* [Spring Data JPA](https://docs.spring.io/spring-boot/docs/2.5.2/reference/htmlsingle/#boot-features-jpa-and-spring-data)
* [Spring Native Reference Guide](https://docs.spring.io/spring-native/docs/current/reference/htmlsingle/)
* [Spring Web Services](https://docs.spring.io/spring-boot/docs/2.5.2/reference/htmlsingle/#boot-features-webservices)
* [Spring Integration](https://docs.spring.io/spring-boot/docs/2.5.2/reference/htmlsingle/#boot-features-integration)
* [Apache Freemarker](https://docs.spring.io/spring-boot/docs/2.5.2/reference/htmlsingle/#boot-features-spring-mvc-template-engines)
* [Vaadin](https://vaadin.com/spring)

### Guides
The following guides illustrate how to use some features concretely:

* [Building a RESTful Web Service](https://spring.io/guides/gs/rest-service/)
* [Serving Web Content with Spring MVC](https://spring.io/guides/gs/serving-web-content/)
* [Building REST services with Spring](https://spring.io/guides/tutorials/bookmarks/)
* [Accessing Data with JPA](https://spring.io/guides/gs/accessing-data-jpa/)
* [Producing a SOAP web service](https://spring.io/guides/gs/producing-web-service/)
* [Integrating Data](https://spring.io/guides/gs/integration/)
* [Creating CRUD UI with Vaadin](https://spring.io/guides/gs/crud-with-vaadin/)

### Additional Links
These additional references should also help you:

* [Gradle Build Scans – insights for your project's build](https://scans.gradle.com#gradle)
* [Configure the Spring AOT Plugin](https://docs.spring.io/spring-native/docs/0.10.1/reference/htmlsingle/#spring-aot-gradle)

## Spring Native

This project has been configured to let you generate either a lightweight container or a native executable.

### Lightweight Container with Cloud Native Buildpacks
If you're already familiar with Spring Boot container images support, this is the easiest way to get started with Spring Native.
Docker should be installed and configured on your machine prior to creating the image, see [the Getting Started section of the reference guide](https://docs.spring.io/spring-native/docs/0.10.1/reference/htmlsingle/#getting-started-buildpacks).

To create the image, run the following goal:

```
$ ./gradlew bootBuildImage
```

Then, you can run the app like any other container:

```
$ docker run --rm -p 8080:8080 live:0.0.1-SNAPSHOT
```

### Executable with Native Build Tools
Use this option if you want to explore more options such as running your tests in a native image.
The GraalVM native-image compiler should be installed and configured on your machine, see [the Getting Started section of the reference guide](https://docs.spring.io/spring-native/docs/0.10.1/reference/htmlsingle/#getting-started-native-build-tools).

To create the executable, run the following goal:

```
$ ./gradlew nativeBuild
```

Then, you can run the app as follows:
```
$ build/native-image/live
```

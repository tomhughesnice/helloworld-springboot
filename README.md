# Spring Boot Hello World app for Google Flexible environment

This sample shows how to run a [Spring Boot][spring-boot] application on [Google
Cloud Platform][cloud-java]. It uses the [Google App Engine flexible
environment][App Engine-flexible].

[App Engine-flexible]: https://cloud.google.com/appengine/docs/flexible/
[cloud-java]: https://cloud.google.com/java/
[spring-boot]: http://projects.spring.io/spring-boot/

### Disclaimer 30th May 2016

This is an updated version of Googles [getting-started] hello-world springboot module.
That version would not deploy for me, I have updated to the latest spring-boot version and fixed some docker settings.

[getting-started]: https://github.com/GoogleCloudPlatform/getting-started-java

## Before you begin

This sample assumes you have [Java 8][java8] installed.

[java8]: http://www.oracle.com/technetwork/java/javase/downloads/

### Download Maven

These samples use the [Apache Maven][maven] build system. Before getting
started, be sure to [download][maven-download] and [install][maven-install] it.
When you use Maven as described here, it will automatically download the needed
client libraries.

[maven]: https://maven.apache.org
[maven-download]: https://maven.apache.org/download.cgi
[maven-install]: https://maven.apache.org/install.html

### Create a Project in the Google Cloud Platform Console

If you haven't already created a project, create one now. Projects enable you to
manage all Google Cloud Platform resources for your app, including deployment,
access control, billing, and services.

1. Open the [Cloud Platform Console][cloud-console].
1. In the drop-down menu at the top, select **Create a project**.
1. Give your project a name.
1. Make a note of the project ID, which might be different from the project
   name. The project ID is used in commands and in configurations.

[cloud-console]: https://console.cloud.google.com/

### Enable billing for your project.

If you haven't already enabled billing for your project, [enable
billing][enable-billing] now.  Enabling billing allows the application to
consume billable resources such as running instances and storing data.

[enable-billing]: https://console.cloud.google.com/project/_/settings

### Install the Google Cloud SDK.

If you haven't already installed the Google Cloud SDK, [install and initialize
the Google Cloud SDK][cloud-sdk] now. The SDK contains tools and libraries that
enable you to create and manage resources on Google Cloud Platform.

[cloud-sdk]: https://cloud.google.com/sdk/

### Install the Google App Engine SDK for Java


```
gcloud components update app-engine-java
gcloud components update
```


## Run the application locally

1. Set the correct Cloud SDK project via `gcloud config set project
   YOUR_PROJECT` to the ID of your application.
1. Run `mvn spring-boot:run`
1. Visit http://localhost:8080


## Deploy to App Engine flexible environment

1. `mvn gcloud:deploy`
1. Visit `http://YOUR_PROJECT.appspot.com`.


Java is a registered trademark of Oracle Corporation and/or its affiliates.


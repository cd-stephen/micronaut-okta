## sdkman
skdman

SDKMAN! (Software Development Kit Manager) is a tool that provides a consistent way to manage and install multiple versions of various software development kits on Unix-based systems. While its name implies it's only for SDKs, it's most commonly used to manage Java-related SDKs such as Java Development Kits (JDKs), Groovy, Gradle, Maven, and others.

Here are some key features and aspects of SDKMAN!:

1. Multiple Versions: SDKMAN! lets you install multiple versions of a given SDK. This is particularly useful for Java developers who need to test their software against different versions of the JDK.
2. Switching Versions: With a simple command, you can switch between installed versions of an SDK.
3. Platform Independence: SDKMAN! works on any UNIX-based platform such as Mac OSX, Linux, Cygwin, Solaris, and FreeBSD.
4. Automatic Updates: SDKMAN! provides notifications about available updates for installed SDKs and allows you to update them easily.
5. Installation and usage
```sh
curl -s "https://get.sdkman.io" | bash
source "$HOME/.sdkman/bin/sdkman-init.sh"
```
Usage Examples:
- 	To list all available SDKs: sdk list
- 	To install a specific version of Java: sdk install java 11.0.3-open
- 	To switch to a specific version: sdk use java 11.0.3-open
- 	To list installed versions of a particular SDK: sdk list java

6. Candidacy & Default: You can set a particular version of an SDK as the default to use every time a new terminal session starts or make a version a "candidate" for use in the current session.
7. Vendor Support: With Java, SDKMAN! allows you to choose between different distributions and vendors, such as AdoptOpenJDK, Amazon Corretto, GraalVM, and more.
8. Beyond Java: While Java-related SDKs are prominent, SDKMAN! also supports other platforms like Scala, Kotlin, and Groovy, as well as build tools like Maven, Gradle, and sbt.

In summary, SDKMAN! is an invaluable tool for developers, especially in the Java ecosystem, who need a consistent and easy way to manage multiple SDK versions. It streamlines the process of switching between SDK versions and ensures that the right tools are always at hand.

## install micronaut
```sh
sdk install micronaut
mn --version
```

## config
```sh
vim ~/.sdkman/etc/config

sdkman_auto_env=true
```



okta cli
https://cli.okta.com/manual/#installation

## install
```sh
curl https://raw.githubusercontent.com/okta/okta-cli/master/cli/src/main/scripts/install.sh | bash
```

## register - one time
```sh
okta register

First name: firstname
Last name: lastname
Email address: name@example.com
Country: US
Creating new Okta Organization, this may take a minute:
An account activation email has been sent to you.

Check your email
New Okta Account created!
Your Okta Domain: https://dev-########.okta.com
```



## Create an Okta Application (OAuth 2.0 / OIDC)
The Okta CLI tool can create Okta OAuth 2.0 / OIDC Applications for you with a few prompts. The following application types are supported:

Web - Backend applications, Java, .Net, PHP, etc
Single Page App (SPA) - Browser based applications
Native App - desktop and mobile applications
Service - Machine to Machine services

run:
```sh
okta apps create
```
and you will be prompted for the required information.



NOTE: On IntelliJ (at least), you’ll also need to add in the Lombok plugin to avoid compiler errors on getters and setters for data classes.


https://developer.okta.com/docs/guides/sign-into-web-app-redirect/spring-boot/main/#set-up-okta

## micronaut
```sh
okta apps create spa
#callback
http://localhost:8080/callback

#redirect uri
https://oidcdebugger.com/debug

#post logout redirect uri
https://oidcdebugger.com/
```


## using httpie
```sh
http :8080/hello Authorization:"Bearer $TOKEN"
```

## reference exercise
https://youtu.be/IG2uo4IP1QI
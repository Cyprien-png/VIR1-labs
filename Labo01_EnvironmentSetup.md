# Labo01 - Environment Setup

* [Labo description](https://cpnv-es-ngy.gitbook.io/vir1/labs/labo01-environment-setup)

## DevOps Stack to setup

Mention in this documentation the orders carried out and the results obtained.

If you have opted for a graphical installation, provide screenshots and describe the procedure up to the result obtained.

### Cloud cmd line interface - AWS Cli

```
> aws --version
aws-cli/2.15.39 Python/3.11.8 Windows/10 exe/AMD64 prompt/off
```

### IDE - Intellij

```
IntelliJ IDEA Ultimate 2024.1 was installed from JetBrains Toolbox with the default configuration
```

### Containers Engins - Docker

```
> docker version
Client:
 Cloud integration: v1.0.35+desktop.13
 Version:           26.0.0
 API version:       1.45
 Go version:        go1.21.8
 Git commit:        2ae903e
 Built:             Wed Mar 20 15:18:56 2024
 OS/Arch:           windows/amd64
 Context:           default

Server: Docker Desktop 4.29.0 (145265)
 Engine:
  Version:          26.0.0
  API version:      1.45 (minimum version 1.24)
  Go version:       go1.21.8
  Git commit:       8b79278
  Built:            Wed Mar 20 15:18:01 2024
  OS/Arch:          linux/amd64
  Experimental:     false
 containerd:
  Version:          1.6.28
  GitCommit:        ae07eda36dd25f8a1b98dfbf587313b99c0190bb
 runc:
  Version:          1.1.12
  GitCommit:        v1.1.12-0-g51d5e94
 docker-init:
  Version:          0.19.0
  GitCommit:        de40ad0
```

### Versioning - Git + Git flow

```
> git -v
git version 2.44.0.windows.1

> git flow version
1.12.3 (AVH Edition)
```

### IDE Plugin - Docker plugin for IntelliJ

```
Docker plugin installed from IntelliJ MarketPlace: bundled 241.14494.240 
```

### Development Kit - JDK

```
> java -version
java version "17.0.11" 2024-04-16 LTS
Java(TM) SE Runtime Environment (build 17.0.11+7-LTS-207)
Java HotSpot(TM) 64-Bit Server VM (build 17.0.11+7-LTS-207, mixed mode, sharing)
```

### Package manager - Maven

```
> mvn -v
Apache Maven 3.9.6 (bc0240f3c744dd6b6ec2920b3cd08dcc295161ae)
Maven home: C:\ProgramData\chocolatey\lib\maven\apache-maven-3.9.6
Java version: 17.0.11, vendor: Oracle Corporation, runtime: C:\Program Files\Java\jdk-17
Default locale: fr_CH, platform encoding: Cp1252
OS name: "windows 11", version: "10.0", arch: "amd64", family: "windows"
```

## Schema

Show your development environment, mentioning all the components in the stack.

Identify the links between components.

```
![image](https://github.com/Cyprien-png/VIR1-labs/assets/61788240/e35d8b1c-fe00-4ff6-9d9d-6f3a56f81f35)
```

## Analysis

Answer the questions below, giving reasons for your answer (link, source).

### AWS CLI

* How does the AWS Cli interact with the cloud ?

```
by using HTTPS on TCP port 443.
```

* What other ways do we have of dialoguing/interacting with the AWS cloud if we wanted to do without the CLI?

```
Using the web interface.
```

* What commands do I need to run in the CLI to start an ec2 instance?

```
$ aws ec2 start-instances --instance-ids i-1348636c
```

### Docker Engine

* What type of hypervisor does Docker use?

```
In the case of Windows, Docker uses Hyper-V which is in-built virtualization technology provided by Windows
```

* What role does the Docker Desktop play in the Docker architecture?

```
It's the client
```

### Java Environment

* JDK, JRE, JVM... what's the difference?

```
JDK is the development platform, while JRE is for execution. JVM is the foundation, or the heart of Java programming language.
```

### Maven

* What is the command you need to use Maven to retrieve dependencies (and only that)?

```
./mvnw versions:display-dependency-updates
```



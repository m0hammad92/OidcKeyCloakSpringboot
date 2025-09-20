<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 --><!--*** Thanks for checking out the Best-README-Template. If you have a suggestion*** that would make this better, please fork the repo and create a pull request*** or simply open an issue with the tag "enhancement".*** Don't forget to give the project a star!*** Thanks again! Now go create something AMAZING! :D-->

<!-- ############################################## PROJECT SHIELDS  ############################################## --><!--*** I'm using markdown "reference style" links for readability.*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).*** See the bottom of this document for the declaration of the reference variables*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.*** https://www.markdownguide.org/basic-syntax/#reference-style-links-->

<!-- ############################################## PROJECT LOGO & HEADING  ############################################## --><br />

<a name="readme-top"></a>

<div align="center">  <h1>Sample Project to Demonstrate Spring Authentication and Authorization and with keycloak OIDC</h1>  <div align="center">    A SpringBoot application with Data Access Object (DAO) Layer !    <br />    <a href="http://localhost:8081/swagger-ui.html"><strong>View Demo</strong></a>


<!-- ############################################## TABLE OF CONTENTS  ############################################## -->

 ### Table of Contents :bookmark_tabs:

1. [About The Project](#about-the-project-dart)
2. [Quick Start Guide](./app/docs/pages/QuickStartGuide.md)
3. [Build & Use](./app/docs/pages/Build_&_Use.md)
4. [Package Structure](./app/docs/pages/PackageStructure.md)
5. [Security Configuration](./app/docs/pages/SecurityConfiguration.md)
6. [Database and Data Access](./app/docs/pages/DatabaseAndDataAccess.md)
7. [Logging and Auditing](./app/docs/pages/LoggingAndAuditing.md)
8. [Exception Handling](./app/docs/pages/ExceptionHandling.md)
9. [Metrics](./app/docs/pages/Metrics.md)
10. [CI/CD Pipeline](./app/docs/pages/CI_CD_Pipeline.md)
11. [Troubleshooting](./app/docs/pages/Troubleshooting.md)

<!-- ############################################## ABOUT THE PROJECT ############################################## -->

## About The Project :dart:

### Introduction

    The main goal of
this [Spring Boot](https://docs.spring.io/spring-boot/docs/current/reference/html/getting-started.html)
application is to
allow  `data creation(CREATE), modification(UPDATE/PATCH), deletion(DELETE) & search with multiple IDs filter(SELECT)`
kind of operations for any microservice that needs a Ready-To-Use `RESTFUL-APIs` and `data access layer (DAO)`
implemented by `Hibernate JPA`.The application will be deployed on Kubernetes cluster,
with Istio installed and configured. However, this seed is compliant with quality & security standards to deliver bugfree, scalable and better performing application.

 You will find detailed explanations
related to entity relation, schema, execution endpoints in [Database & Data Access](./app/docs/pages/DatabaseAndDataAccess.md)
. This application is designed to work with `PostgreSQL` database or else the default _in-memory h2 database_ will be
used as a data storage option(Not recommended for production environment).


**NOTE:** :red_circle: <br>

> Liquibase : This application comes with liquibase enabled by default in application.yaml. i.e <br> `spring.liquibase.enabled=true` <br>
> To disable liquibase set `spring.liquibase.enabled=false` in application.yaml

<!-- ############################################## KEY HIGHLIGHT FEATURES ############################################## -->

<a name="key-highlights"></a>

### Key Highlight Features

- `CI/CD Automation:` Easy deployment feature through [Gitlab-CI pipeline](https://docs.gitlab.com/ee/ci/) (See
    the `gitlab-ci.yaml`.
- `Security:` Highly customizable `authentication` and `authorization` feature driven
    by [Open ID Connect with JWT token](https://openid.net/connect/)
- `Keycloak:` Application can be easily pluggable to any Identity Provider,
    however [keycloak](https://www.keycloak.org/guides#getting-started) identity provider is the default one.
- `Nexus Repository:` The docker image, generated after the successful build through Gitlab-CI pipeline is stored in
    the [Nexus Repository](https://www.sonatype.com/products/nexus-repository).
- `Data Storage:` Comes with in-memory [h2-DB](http://h2database.com/html/main.html) and also provides data storage
    for [PostgreSQL](https://www.postgresql.org/docs/current/) Database. Liquibase manages the database schema in this application.
     The `spring.liquibase.enabled` property allows users to activate or deactivate its usage.
- `SWAGGER-API Testing:` Comes with [Open-Api Swagger3](https://swagger.io/specification/) specification to leverage
    api  testing through _Open-Api Swagger3 dashboard_.
- `Log Tracing:` Application generates `traceId/spanId` as soon user hit requests, track and monitor each
    request/ response flow. Thanks to [Slf4j-MDC(Mapped Diagnostic Context)](https://www.baeldung.com/mdc-in-log4j-2-logback).
- `Customizable Logging:` Highly customizable application logs generated at Console and Rolling file appender
    through [logback](https://logback.qos.ch/documentation.html) xml file. (See the `logback.xml` for more details).
- `Code Quality Check:` Comes with set of strict rules, to avoid code quality issues & code-smell, driven
    by [JaCoCo-Sonar](https://github.com/SonarSource/sonar-scanning-examples/blob/master/doc/jacoco.md) plugin during
    the  build process (See _pom.xml_ for more setup).
- `Checkstyle` This application enforces to use [checkstyle](https://checkstyle.sourceforge.io/) plugin
    for `line & branch` coverages (See pom.xml for plugin configuration and setup).
- `Health Check:` This application comes
    with [Actuator](https://docs.spring.io/spring-boot/docs/current/actuator-api/htmlsingle/#overview) to provide
    health  check status that is being constantly monitored by spring boot provided `actuator`.## About The Project :dart:



## About The Project :dart:

<a name="introduction"></a>

### Introduction

&nbsp;&nbsp;&nbsp; The main goal ofthis [Spring Boot](https://docs.spring.io/spring-boot/docs/current/reference/html/getting-started.html)application is toallow  `data creation(CREATE), modification(UPDATE/PATCH), deletion(DELETE) & search with multiple IDs filter(SELECT)`kind of operations for any microservice that needs a Ready-To-Use `RESTFUL-APIs` and `data access layer (DAO)`implemented by `Hibernate JPA`.The application will be deployed on Kubernetes cluster,with Istio installed and configured. However, the  is compliant with quality & security standards to deliver bugfree, scalable and better performing application.
&nbsp;&nbsp;&nbsp; However, After you start this application or when you make use of this microservice along with yourown microservice as a independent piece, you can test the CRUD based operations by invoking CRUD endpoints ( _Click on 'View Demo' at the top for swagger endpoint_ )

<!-- ############################################## KEY HIGHLIGHT FEATURES ############################################## -->

<a name="key-highlights"></a>

### Key Highlight Features :mag:

<table>    <tbody>      <tr>        <td>              </td>        <td>          width="320" height="430">        </td>        </tr>    </tbody></table>
- `CI/CD Automation:` Easy deployment feature through [Jenkins-pipeline](https://www.jenkins.io/doc/) (See  the `Jenkinsfile` under the project root folder for the detailed configuration).- `Containerization:` Application supports containerization through [Docker](https://www.docker.com/why-docker/)(  See _  Dockerfile_ configuration for more details).- `Security:` Highly customizable `authentication` and `authorization` feature driven  by [Open ID Connect with JWT token](https://openid.net/connect/)- `Keycloak:` Application can be easily pluggable to any Identity Provider,  however [keycloak](https://www.keycloak.org/guides#getting-started) identity provider is the default one.- `Nexus Repository:` The docker image, generated after the successful build through Jenkins-pipeline is stored at  the [Nexus Repository](https://www.sonatype.com/products/nexus-repository).- `Data Storage:` Comes with in-memory [h2-DB](http://h2database.com/html/main.html) and also provides data storage  for [PostgreSQL](https://www.postgresql.org/docs/current/) Database.- `SWAGGER-API Testing:` Comes with [Open-Api Swagger3](https://swagger.io/specification/) specification to leverage  api  testing through _Open-Api Swagger3 dashboard_.- `Log Tracing:` Application generates `traceId/requestId` as soon user hit requests, track and monitor each  request/  response flow. Thanks to [Slf4j-MDC(Mapped Diagnostic Context)](https://www.baeldung.com/mdc-in-log4j-2-logback).- `Customizable Logging:` Highly customizable application logs generated at Console and Rolling file appender  through [logback](https://logback.qos.ch/documentation.html) xml file. (See the `logback.xml` for more details).- `Masking/Hiding Sensitive Data:` This application has _Data Masking_ feature to hide sensitive details from the  log  traces.- `Code Quality Check:` Comes with set of strict rules, to avoid code quality issues & code-smell, driven  by [JaCoCo-Sonar](https://github.com/SonarSource/sonar-scanning-examples/blob/master/doc/jacoco.md) plugin during  the  build process (See _pom.xml_ for more setup).- `Checkstyle` This application enforces to use [checkstyle](https://checkstyle.sourceforge.io/) plugin  for `line & branch` coverages (See pom.xml for plugin configuration and setup).- `Health Check:` This application comes  with [Actuator](https://docs.spring.io/spring-boot/docs/current/actuator-api/htmlsingle/#overview) to provide  health  check status that is being constantly monitored by spring boot provided `actuator`.
<div align="right"><a href="#key-highlights">:arrow_up_small:</a> : <a href="#readme-top">:arrow_double_up:</a></div>

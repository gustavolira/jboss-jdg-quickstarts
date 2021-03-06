Red Hat Data Grid Quickstarts
=============================
Red Hat Data Grid (RHDG) is an elastically scalable in-memory data store built on the open source Infinispan project.

## RHDG Modes
You can use Red Hat Data Grid in two modes:

* _Library Mode_ provides binaries to build and deploy custom runtime environments. RHDG runs alongside your application in the same JVM. Your application has local access to a single node in a distributed cluster.

* _Remote Client-Server Mode_ provides a self-contained process in a container based on JBoss EAP. RHDG runs remotely and provides access to data through `Hot Rod`, `REST`, or `Memcached` interfaces.

## About the Quickstarts
These quickstarts demonstrate Red Hat Data Grid features and capabilities with specific, working examples that you can reference in your own projects.

If you are using _Remote Client-Server Mode_, you should start with the **helloworld-jdg** quickstart to ensure that your server configuration is valid and you can start it successfully.

Quickstarts have **Beginner**, **Intermediate**, and **Advanced** levels. You should start with a level that is comfortable for you and move on to the next level as you gain expertise.

Some quickstarts are prerequisites for others that expand on certain capabilities or functionality. You should always deploy and run any prerequisite quickstarts first.

## Available Quickstarts
This distribution contains the following quickstarts:

| **Quickstart Name** | **Demonstrated Technologies** | **Shows you how to...** |
|:-----------|:-----------|:-----------|
| [carmart](carmart/README.md) | Infinispan, CDI | Use Infinispan instead of a relational database. |
| [carmart-tx](carmart-tx/README.md) | Infinispan, CDI, Transactions | Use Infinispan instead of a relational database with transactions enabled.|
| [eap-cluster-app](eap-cluster-app/README.md) | Infinispan, CDI, EJB | Access an Infinispan cache from a JBoss EAP application using JDG modules for EAP.|
| [helloworld-jdg](helloworld-jdg/README.md) | Infinispan, CDI | Use Infinispan in clustered mode with expiration.|
| [hotrod-endpoint](hotrod-endpoint/README.md) | Infinispan, Hot Rod | Access Infinispan remotely through the Hot Rod protocol. |
| [hotrod-secured](hotrod-secured/README.md) | Infinispan, Hot Rod | Securely access Infinispan remotely through the Hot Rod protocol. |
| [memcached-endpoint](memcached-endpoint/README.md) | Infinispan, Memcached | Access Infinispan remotely through the Memcached protocol. |
| [rapid-stock-market](rapid-stock-market/README.md) | Infinispan, Hot Rod, REST | Use compatibility mode to access data with multiple protocols. |
| [spring](spring/README.md) | Infinispan, Spring | Use Spring integration modules. |
| [spring](spring-session/README.md) | Infinispan, Spring Boot, Spring Session | Use of Spring Boot and Spring Session with RHDG. |
| [remote-query](remote-query/README.md) | Infinispan, Hot Rod, Remote Query | Query Infinispan remotely through the Hot Rod protocol. |
| [rest-endpoint](rest-endpoint/README.md) | Infinispan, REST | Access Infinispan remotely through the REST protocol. |
| [secure-embedded-cache](secure-embedded-cache/README.md) | Infinispan, CDI, REST | Secure Infinispan in Library (embedded) mode. |
| [cdi](cdi-jdg/README.md) | Infinispan, CDI | Use Infinispan CDI and JCache extensions. |
| [camel-jbossdatagrid-fuse](camel-jbossdatagrid-fuse/README.md) | Camel, Infinispan, REST | Use the Camel component camel-jbossdatagrid in JBoss Fuse. |
| [spark](spark/README.md) | Infinispan, Apache Spark | Read and write data to Infinispan and use streaming to react to data changes in real time. |

## System Requirements
You need the following to build and run the quickstarts:

* Java 8.0 (Java SDK 1.8) or later.
* Maven 3.0 or later. See the [Maven Getting Started Guide](http://maven.apache.org/guides/getting-started/index.html).
* JBoss EAP server distribution. Available from the [Red Hat Customer Portal](https://access.redhat.com/downloads).
* RHDG server distribution for _Remote Client-Server Mode_. Available from the [Red Hat Customer Portal](https://access.redhat.com/downloads).

You can also run the quickstarts with [JBoss Developer Studio or Eclipse](#use-jboss-developer-studio-or-eclipse-to-run-the-quickstarts).

### Configuring Maven

If you have not yet done so, you must [Configure Maven](https://github.com/jboss-developer/jboss-developer-shared-resources/blob/master/guides/CONFIGURE_MAVEN.md#configure-maven-to-build-and-deploy-the-quickstarts).

If you do not configure Maven, you must pass settings with every Maven command as follows: ` -s QUICKSTART_HOME/settings.xml`

### Setting Environment Variables
RHDG quickstarts use the following environment variables:

* `JBOSS_HOME` denotes the root JBoss server directory.
* `EAP_HOME` denotes the path to your JBoss EAP installation.

`EAP_HOME` is a *replaceable* value. When you encounter it in a RHDG quickstart, change the value as appropriate.

| Installation method | Installation directory |
|:-----------|:-----------|
| ZIP archive | Custom directory |
| RPM | `/var/lib/jbossas/` |
| Installer | `{USER_HOME}/EAP-6.3.0` |
| JBoss Developer Studio installer | `{USER_HOME}/jbdevstudio/runtimes/jboss-eap` |

Where `{USER_HOME}` is one of the following:

* Linux: `/home/USER_NAME/`
* Windows: `"C:\Users\USER_NAME\"`

## Running the Quickstarts
Refer to the `README` file in each quickstart directory for instructions on building and running the quickstart.

### Building Quickstart Archives
You can build archives without deploying the quickstarts to check for compilation errors and view the contents of the quickstart.

From the root directory of the quickstart, run `$ mvn clean install` to build the archive.

## Contributing the Quickstarts
Refer to [JBoss Developer Contributing Guide](https://github.com/jboss-developer/jboss-developer-shared-resources/blob/master/guides/CONTRIBUTING.md)

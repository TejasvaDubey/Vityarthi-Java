# Campus Course & Records Manager (CCRM)

## Open JDK Version 17

## Project Overview

Domain classes (edu.ccrm.domain)

Represents real-world entities like Course, Student, Instructor, Semester, and Enrollment, including details such as grades and personal data.

Each class generally includes fields (properties) along with corresponding getter and setter methods.

Service classes (edu.ccrm.service)

Provide the core logic for managing courses (CourseService) and students (StudentService).

They work directly with the domain model objects.

Main.java

Acts as the starting point of the application.

Usually responsible for creating objects, calling services, and running the workflow such as student registration and grading.

## Evolution of Java
1991 – Oak: Project started at Sun Microsystems for embedded devices, later renamed Java.

1995 – Java 1.0: "Write Once, Run Anywhere" – platform-independent language launched.

1998 – Java 2 (J2SE 1.2): Introduced Swing, Collections Framework, and JVM improvements.

2004 – Java 5 (J2SE 5.0): Major upgrade – Generics, Annotations, Autoboxing, Enums, for-each loop.

2006 – Java 6: Performance improvements, scripting support, JDBC 4.0.

2009 – Oracle acquires Sun Microsystems, takes over Java.

2011 – Java 7: Introduced try-with-resources, Diamond operator (<>), Fork/Join framework.

2014 – Java 8 (huge milestone): Lambdas, Streams API, Optional, new Date-Time API.

2017 – Java 9: Module System (Project Jigsaw), JShell (REPL).

2018 – Java 10/11: Local variable var, HttpClient API; Java 11 became LTS.

2021 – Java 17 (LTS): Sealed classes, Pattern Matching, modernized language.

2023 – Java 21 (LTS): Virtual Threads (Project Loom), String Templates, Record Patterns.

## Java SE vs ME vs EE
**🔹Java ME (Micro Edition)**

Designed for small devices → mobiles, IoT, embedded systems.

Lightweight libraries, subset of Java SE.

Optimized for low memory & CPU.

Example: Old Nokia apps, IoT sensors.

Mostly replaced by Android SDK / Embedded Java.

**🔹Java SE (Standard Edition)**

Core Java platform, foundation of everything.

Runs on PCs, laptops, small servers.

Includes Collections, IO, Networking, Concurrency, Swing/JavaFX.

Used for desktop apps, utilities, small server apps.

Every Java developer starts here.

**🔹Java EE (Enterprise Edition)**

Extension of Java SE for large-scale enterprise apps.

Runs on application servers (Tomcat, GlassFish, JBoss, etc.).

Provides Servlets, JSP, EJB, JPA, JMS, Web Services.

Used in banking, e-commerce, enterprise portals.

Now renamed Jakarta EE under Eclipse Foundation.

## JVM/JRE/JDK Explanation

**🔹 JVM (Java Virtual Machine)**

The core engine responsible for executing Java programs.

Transforms bytecode (.class) into machine-specific instructions for the OS and CPU.

Provides features: memory management, garbage collection, security.

Platform-dependent (different JVMs for Windows, Linux, Mac).

Think of it as the interpreter of Java.

**🔹 JRE (Java Runtime Environment)**

Contains all the essential components to execute Java applications.

Includes: JVM + core libraries + supporting files.

Does NOT contain development tools (compiler, debugger).

Used by end-users who only want to run Java apps, not develop.

**🔹 JDK (Java Development Kit)**

A complete suite used to build and execute Java programs.

Includes: JRE + development tools (compiler javac, debugger, Javadoc).

Used by developers to write, compile, and run programs.

Compiling Java code requires the JDK to be installed.

## Usage

Navigate to **src/edu/ccrm** and compile/run **CCRMApp.java** using 
`javac CCRMApp.java`
then 
`java CCRMApp`

## Installation

![alt text](https://www.eclipse.org/downloads/packages/modules/custom/eclipsefdn/eclipsefdn_packages/images/installer-instructions-02.png)

![alt_text](https://www.eclipse.org/downloads/packages/modules/custom/eclipsefdn/eclipsefdn_packages/images/installer-instructions-03.png)

![alt_text](https://www.eclipse.org/downloads/packages/modules/custom/eclipsefdn/eclipsefdn_packages/images/installer-instructions-04.png)

![alt_text](https://www.eclipse.org/downloads/packages/modules/custom/eclipsefdn/eclipsefdn_packages/images/installer-instructions-05.png)

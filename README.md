# Campus Course & Records Manager (CCRM)

## Open JDK Version 17

## Project Overview

Domain classes (edu.ccrm.domain)

Code real-world objects such as Course, Student, Instructor, Semester, and Enrollment, including grades and personal information.

Each class typically has fields (properties) along with their respective getter and setter methods.

Service classes (edu.ccrm.service)

Implement the central logic for handling courses (CourseService) and students (StudentService).

They interface directly with the domain model objects.

Main.java

Is the entry point of the application.

Normally tasked with generating objects, invoking services, and executing the workflow like student enrollment and grading.
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

## Syllabus Mapping

1. Core Java Fundamentals
This is the foundation of the entire project.

Basic Syntax & Structure: The entire codebase demonstrates proper Java class structure, main method, and code blocks.

Variables & Data Types: Extensive use of primitive types (int, double) and reference types (String).

Control Flow Statements:

Conditionals: if, else if, else statements for menu logic and input validation.

Loops: while loops for the main menu to keep the program running until the user chooses to exit. for loops are used for iterating through ResultSet objects.

Methods: The code is structured using static methods for different functionalities (e.g., addStudent(), viewStudents(), updateStudent()), promoting modularity and reusability.

Input/Output (I/O): Uses Scanner class for taking user input from the console and System.out.println for displaying output.

Exception Handling: Uses a basic try-catch block to handle SQLException, which is crucial for robust database interaction.

2. Object-Oriented Programming (OOP) Principles
While the current structure is largely procedural (focused on static methods), the domain is inherently object-oriented.

Classes and Objects: The system revolves around the concept of a Student object, even if it's not explicitly defined as a class in the main code. The database table students represents the blueprint of a Student class.

Practical Application (Potential Enhancement): A natural progression for this project would be to create a Student class with attributes like id, name, grade, etc., and then use objects to pass data around, which would be a direct application of OOP.

3. Database Programming (JDBC - Java Database Connectivity)
This is the most significant and advanced topic covered in the project.

JDBC Architecture: The project uses the standard JDBC workflow:

Load and Register Driver: Class.forName("com.mysql.cj.jdbc.Driver").

Establish Connection: DriverManager.getConnection(url, username, password).

Create Statement: connection.createStatement().

Execute Queries:

CREATE: stmt.executeUpdate(CREATE_TABLE_SQL) (in the setup script).

INSERT (Create): stmt.executeUpdate(query) in addStudent().

SELECT (Read): stmt.executeQuery(query) in viewStudents().

UPDATE (Update): stmt.executeUpdate(query) in updateStudent().

DELETE (Delete): stmt.executeUpdate(query) in deleteStudent().

Process ResultSet: Iterating through the ResultSet to display student data.

Close Connection: connection.close() (ideally in a finally block or using try-with-resources for better practice).

SQL (Structured Query Language): The project demonstrates practical use of fundamental SQL commands (INSERT, SELECT, UPDATE, DELETE) embedded within Java strings.

4. Software Engineering & Design Practices
The project demonstrates several important practical development skills.

CRUD Operations: Implements the four basic functions of persistent storage: Create, Read, Update, Delete. This is a fundamental pattern in software development.

Application Structure: Organizes code logically into a main driver class (Vityarthi.java) with separate methods for distinct functionalities.

Use of External Libraries: Manages dependencies using Maven (evident from the pom.xml file), specifically the mysql-connector-j dependency to connect to the MySQL database.


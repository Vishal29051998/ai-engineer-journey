# **Module 0.2: Environment**

## **1. What are Data Types?**

Data types define the type of data that a variable can store in a Java program. They specify what kind of value can be assigned to a variable, such as numbers, decimal values, characters, or text.

## **2. JDK, JRE, and JVM**

- **JVM (Java Virtual Machine):** JVM is responsible for executing Java programs. It allows Java bytecode (`.class` files) to run on different operating systems without making any changes to the code.
- **JRE (Java Runtime Environment):** JRE contains the JVM and the supporting libraries and tools required to run Java applications.
- **JDK (Java Development Kit):** JDK contains the JRE along with development tools such as the Java compiler and debugger. It is used to develop, compile, and run Java applications.

## **3. Why is the&#x20;**`main()`**&#x20;method static?**

Every standalone Java application requires an entry point to start its execution. The JVM looks for the `main()` method to begin executing the program.

The `main()` method is declared as `static` because the JVM can call it directly using the class name without creating an object of that class.

A static method belongs to the class rather than to an individual object.

## **4. Why should the Public Class Name and File Name Be the Same?**

In Java, if a class is declared as `public`, the file name must be the same as the public class name.

For example:

- Class name: `Student`
- File name: `Student.java`

This rule helps the Java compiler identify and organize public classes correctly.

## **5. How Do Tomcat and the Main Method Work?**

A Servlet runs inside a web server or servlet container such as Apache Tomcat.

Tomcat is itself a Java application, and it has its own startup mechanism and entry point. Therefore, we do not need to write a `main()` method inside our Servlet.

When Tomcat starts, it initializes the Servlet container. Based on the application configuration and URL mapping, Tomcat identifies the appropriate Servlet and invokes its lifecycle methods.

The Servlet lifecycle methods include:

1. `init()` – Initializes the Servlet.
2. `service()` – Handles incoming client requests.
3. `destroy()` – Performs cleanup before the Servlet is removed.

Servlet configuration can be done using `web.xml` or annotations such as `@WebServlet`.

## **6. Git Commands: Add, Commit, and Push**

Git is a version control system used to track changes in source code.

- **git add:** Used to move the modified files to the staging area in preparation for committing.
- **git commit:** Used to save the staged changes permanently in the local Git repository along with a commit message.
- **git push:** Used to upload the committed changes from the local repository to a remote repository, such as GitHub.

**Example workflow:**

```
git add .
git commit -m "Initial commit"
git push origin main
```

**Remember the difference:**

- `git add` → Stages the changes.
- `git commit` → Saves the changes locally.
- `git push` → Uploads the changes to GitHub.

**Small technical correction:** The JVM executes Java bytecode, while the Java compiler (`javac`) converts `.java` source files into `.class` bytecode files. Also, JRE is a runtime environment, whereas JDK is the complete development kit.
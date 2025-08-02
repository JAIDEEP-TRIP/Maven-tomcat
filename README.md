
```markdown
🛠️ Maven Project Overview

📌 What is Maven?

Maven is a powerful build automation and project management tool primarily used for Java projects. It simplifies dependency management, project structure, build lifecycles, and packaging. Though most commonly used with Java, Maven also supports languages like C#, Scala, and Ruby.

> Maven is maintained by the [Apache Software Foundation](https://maven.apache.org/).

---

 ✅ Maven Advantages

- Automates the build process
- Manages project dependencies
- Standardizes project structure
- Packages projects into `.jar`, `.war`, or `.ear`
- Supports lifecycle goals like `compile`, `test`, `package`, and `install`
- Generates reports and documentation
- Written in Java and easy to extend with plugins

---

 📁 Maven Project Structure

```

my-app/
│
├── pom.xml                  # Project Object Model (POM) file
└── src/
├── main/
│   ├── java/            # Main Java source code
│   └── resources/       # Resource files (config, properties)
└── test/
├── java/            # Unit tests
└── resources/       # Test-specific resources

````

> 📂 `target/` folder is generated after a build — it contains the compiled `.class` files, packaged `.jar` or `.war` artifacts.

---

 📦 Artifact Types

| Artifact Type | Description |
|---------------|-------------|
| `.jar`        | Java Archive – backend libraries/applications |
| `.war`        | Web Archive – web apps with servlets & JSP |
| `.ear`        | Enterprise Archive – a combination of `.jar` and `.war` for enterprise deployment |

---
 🔄 Maven Lifecycles

| Goal      | Description |
|-----------|-------------|
| `clean`   | Cleans up previously compiled files |
| `validate`| Checks if the project is correct |
| `compile` | Compiles the source code |
| `test`    | Runs unit tests |
| `package` | Packages code into a `.jar` or `.war` |
| `install` | Installs package to the local `.m2` repository |
| `deploy`  | Deploys to a remote repository for sharing |

---

🔧 Repositories

- Remote: [Maven Central](https://mvnrepository.com/)
- Local: Located in `~/.m2/repository`

---

📄 pom.xml Overview

POM = Project Object Model  
The `pom.xml` file defines dependencies, plugins, build instructions, and metadata.

Key Elements:
- `<dependencies>` – Add third-party libraries
- `<plugins>` – Configure build tools like compiler, test runners, etc.

 Example:
```xml
<dependencies>
  <dependency>
    <groupId>junit</groupId>
    <artifactId>junit</artifactId>
    <version>4.13.2</version>
    <scope>test</scope>
  </dependency>
</dependencies>
````

---

 🚀 Create a Sample Maven Project

```bash
mvn archetype:generate \
  -DgroupId=com.apple \
  -DartifactId=java_project \
  -DarchetypeArtifactId=maven-archetype-quickstart \
  -DinteractiveMode=false
```

 Common Archetypes:

 `maven-archetype-quickstart` → Java CLI app
`maven-archetype-webapp` → Web application template

---

🔍 Build Tools Comparison

| Language | Build Tool              |
| -------- | ----------------------- |
| Java     | Maven                   |
| Node.js  | npm / yarn              |
| Python   | Gradle / setuptools     |
| .NET     | MSBuild / Visual Studio |
| C/C++    | Makefile                |

---

🧪 Example Source Code

 ✅ Login Page (JSP)

```jsp
<!-- login.jsp -->
<html>
  <head><title>Login Form</title></head>
  <body>
    <h3>Login here</h3>
    <form action="user_login" method="post">
      <table>
        <tr>
          <td>Username</td>
          <td><input type="text" name="username" /></td>
        </tr>
        <tr>
          <td>Password</td>
          <td><input type="password" name="password" /></td>
        </tr>
      </table>
      <input type="submit" value="Login" />
    </form>
  </body>
</html>
```

---

✅ Hello World (HTML)

```html
<!-- hello.html -->
<html>
  <body>
    <h2>Hello World!</h2>
  </body>
</html>
```

---

 📎 License

This project is licensed under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0).

---

 🙌 Acknowledgements

Maintained by the **Apache Software Foundation**
Created as part of Java Maven learning.


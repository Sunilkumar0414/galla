Project Structure:
Open a terminal or command prompt.

You can just navigate to the directory where you want to create the new project.

Run the following command to generate a project using a specific archetype:
mvn archetype: generate
Follow the prompts to provide information such as groupId, artifactId, version, and more.

Once you've provided the required information, Maven will generate the project structure based on the selected archetype.

Navigate into the newly generated project directory:
cd your-project-directory
Depending on the archetype, you may need to modify the generated pom.xml to add or customize dependencies, plugins, and configurations.

After making any necessary modifications, you can build and run your project using Maven commands like:
mvn clean package
mvn exec: java  # If you have a Java application

mkdir MyMavenProject
cd MyMavenProject
mvn archetype: generate -DgroupId=com.example -DartifactId=my-maven-app -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false

Your project structure will now be:
MyMavenProject/
├── my-maven-app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/
│   │   │   │   └── com/
│   │   │   │       └── example/
│   │   │   │           └── App.java
│   │   ├── test/
│   │   │   ├── java/
│   │   │   │   └── com/
│   │   │   │       └── example/
│   │   │   │           └── AppTest.java
│   ├── target/
│   ├── pom.xml
└── pom.xml

Modify App.java:
Open src/main/java/com/example/App.java and modify the App class to something like:
package com. example;

public class App {
    public static void main(String[] args) {
        System.out.println("Hello, Maven!");
    }
}
cd my-maven-app
mvn clean package
java -cp target/my-maven-app-1.0-SNAPSHOT.jar com. example.App

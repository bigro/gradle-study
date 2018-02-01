# java-library
`gradle init --type java-library` で自動生成したもの

## tasks
```
plugins {
    // Apply the java-library plugin to add support for Java Library
    id 'java-library'
}
```
の記述によりjavaプラグインが入ってタスクが増えていることがわかる。


```
------------------------------------------------------------
All tasks runnable from root project
------------------------------------------------------------

Build tasks
-----------
assemble - Assembles the outputs of this project.
build - Assembles and tests this project.
buildDependents - Assembles and tests this project and all projects that depend on it.
buildNeeded - Assembles and tests this project and all projects it depends on.
classes - Assembles main classes.
clean - Deletes the build directory.
jar - Assembles a jar archive containing the main classes.
testClasses - Assembles test classes.

Build Setup tasks
-----------------
init - Initializes a new Gradle build.
wrapper - Generates Gradle wrapper files.

Documentation tasks
-------------------
javadoc - Generates Javadoc API documentation for the main source code.

Help tasks
----------
buildEnvironment - Displays all buildscript dependencies declared in root project 'java-library'.
components - Displays the components produced by root project 'java-library'. [incubating]
dependencies - Displays all dependencies declared in root project 'java-library'.
dependencyInsight - Displays the insight into a specific dependency in root project 'java-library'.
dependentComponents - Displays the dependent components of components in root project 'java-library'. [incubating]
help - Displays a help message.
model - Displays the configuration model of root project 'java-library'. [incubating]
projects - Displays the sub-projects of root project 'java-library'.
properties - Displays the properties of root project 'java-library'.
tasks - Displays the tasks runnable from root project 'java-library'.

Verification tasks
------------------
check - Runs all checks.
test - Runs the unit tests.

Rules
-----
Pattern: clean<TaskName>: Cleans the output files of a task.
Pattern: build<ConfigurationName>: Assembles the artifacts of a configuration.
Pattern: upload<ConfigurationName>: Assembles and uploads the artifacts belonging to a configuration.

```

Generate code based on the following requirements:

1. The package structure must be created first, based on the package-structure.
2. Create pom.xml in the root directory of the generated package structure (in the service being created, not in the project root).
3. Code must be structured using Spring Boot DDD Embedded Annotations.
4. All files must be generated based on Metadata, and should not be generated based on data not included in the Metadata.
5. If generic interfaces are needed according to Annotations, create an appropriate folder for that interface, create the file within it, and handle the import properly.
6. Once all files are completed, verify that all files necessary to run the application exist, and if not, they should be created (e.g., Application main class - Application.java).
7. Before performing any file modifications, verify that all files required to run the application (Application.java, application.yml, pom.xml, etc.) have been created and that all files required by .clinerules have been generated. Only after confirming this, proceed with mvn install test and then fix any file-related errors.

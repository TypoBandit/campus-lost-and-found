# Campus Lost and Found Management System

A Java desktop demo for recording lost and found items on campus, searching reports, and reviewing possible matches. This is a team project created by Nakul and a teammate. The supplied ZIP describes this version as a consolidated demonstration build based on the project report.

## Features

- Submit lost and found reports with item details and contact information.
- Search and filter reports by keyword, category, type, and status.
- View possible matches based on category, name, description, and location. Matches are suggestions and require manual verification.
- Use the admin panel to mark reports as claimed or recovered, reopen them, or delete them.
- Store data locally using the H2 embedded database.

## Technologies

- Java 17 or later
- Java Swing for the desktop interface
- JDBC and H2 for local database storage
- Maven for building and running

## Run the project

1. Install JDK 17 or newer and Maven.
2. Open a terminal in the project folder, where `pom.xml` is located.
3. Run:

   ```bash
   mvn clean compile
   mvn exec:java
   ```

4. The desktop window should open. The database is created locally in the `data` folder.

## Try the demo

1. Create a lost report and a similar found report in the same category.
2. Open **Search & Details**, select a report, and choose **Possible matches**.
3. For management actions, sign in through the **Admin** tab. The demonstration password is `campus123`.

## Demo limitations

This is an educational demo, not a production system. Its admin password is hard-coded and displayed in the application; it does not provide secure authentication. Avoid entering real personal data. The embedded database is local to the machine running the program.

## Team project

 Developed by Nakul and a teammate. The project brings together a Java Swing interface, a local H2 database, and features for reporting, searching and managing lost and found items. Individual responsibilities have not been documented.

## Project structure

- `src/main/java/campus/Main.java` — application source code
- `pom.xml` — Maven configuration and H2 dependency
- `README.txt` — original instructions included with the supplied demo
- `.gitignore` — excludes generated files and local database data

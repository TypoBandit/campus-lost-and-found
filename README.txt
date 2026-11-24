CAMPUS LOST AND FOUND DEMO - VS CODE

What is included
- src/main/java/campus/Main.java : one-file consolidated Java Swing + JDBC application
- pom.xml : H2 database dependency
- campus-lost-found-demo.jar : compiled classes

Requirements
- JDK 17 or newer
- VS Code with Extension Pack for Java (recommended)
- Maven installed and available as 'mvn' in the terminal

Run in VS Code
1. Open this folder in VS Code.
2. Open the Terminal.
3. Run: mvn clean compile
4. Run: mvn exec:java

The application creates a local H2 database under ./data/lost_found_db.
Admin password for the demo: campus123

Presentation flow
1. Dashboard: show totals.
2. Report Lost: submit a phone or other item.
3. Report Found: submit the matching item.
4. Search & Details: show both rows and filter by keyword/kind/category/state.
5. Select a report -> View details.
6. Select the lost report -> Possible matches. The matching score uses:
   - same category + opposite kind + OPEN state
   - name token overlap = 3 points
   - description token overlap = 2 points
   - location overlap = 1 point
7. Admin tab -> Admin Sign In -> password campus123.
8. Select the found report -> Claim / Recover -> enter claimant details and verification note.
9. Show the outcome changing to Claimed.
10. Demonstrate Reopen or Delete if needed.

Notes
- This is a consolidated demonstration build based on the supplied project report.
- It keeps the project's core behavior but places the classes into one Main.java file for easy copying.
- H2 is used as the embedded JDBC database, matching the embedded mode described in the report.

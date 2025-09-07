StudentDatabaseApp:
A Java-based console application for managing student records using MySQL. This project demonstrates core CRUD operations and database connectivity using JavaDB and JDBC.

Features:
This console-based Java application allows users to manage student records in a MySQL database. Key features include:
* Add new student records
* View all students
* Update existing student details
* Delete student entries
* Console-based user interface for interaction
* Uses JDBC best practices (PreparedStatement, exception handling, resource management)

Technologies Used:
| Technology     | Purpose                                      |
|----------------|----------------------------------------------|
| Java 8+        | Core programming language                    |
| JDBC           | Database connectivity between Java and MySQL |
| MySQL          | Relational database for storing student data |
| IntelliJ IDEA  | IDE used for development                     |
| WampServer     | Local MySQL server and phpMyAdmin interface  |

Database Schema:
The application connects to a MySQL database named `student_db` and uses a table called `students` with the following structure:

| Column Name | Data Type | Description              |
|-------------|-----------|--------------------------|
| `id`        | INT       | Primary key, auto-increment |
| `name`      | VARCHAR   | Student's full name      |
| `email`     | VARCHAR   | Student's email address  |
| `age`       | INT       | Student's age            |

SQL file for this schema is included in `/database/student_db.sql`.

Setup Instructions:
1. Make sure MySQL is running (via WampServer).
2. Import the SQL file `student_db.sql` using phpMyAdmin:
   - Go to `http://localhost/phpmyadmin`
   - Select the `student_db` database
   - Click on the **Import** tab
   - Choose the file `student_db.sql` from the `/database` folder
   - Click **Go**
3. Open the project in IntelliJ IDEA or Eclipse.
4. Update your MySQL credentials in `DBConnection.java`:
   ```java
   DriverManager.getConnection("jdbc:mysql://localhost:3306/student_db", "root", "");

## Hi there 👋
 # The two students : boukhedena rima .bousetla selsabil
 
# 📘 README.md  

Database Schema Designer (Python + PySide6)
🧑‍🎓 Project for the course: Database Design

Language: Python
Framework: PySide6 (Qt)
Project Type: Graphical Application for Database Schema Design
# 🧩 Project Description

This project is a graphical application that allows users to visually create and design a database schema (Graphical Database Designer) without manually typing SQL.

Users can:

 - Create tables

 - Add and delete attributes

 - Define primary keys

 - Create relationships between tables (1-N and N-N)

 - Generate valid SQL code from the schema

 - Execute SQL code within a temporary database
# 🖥️ App Features

 ### 1️⃣ Table Management

 - Add a new table

 - Delete a table (along with its associated relationships)

 - Each table appears as a visible element within the interface

 - Tables can be moved within the drawing area

### 2️⃣ Attribute Management

 - Add an attribute to each table

 - Specify the data type (INTEGER, TEXT, REAL, etc.)

 - Define:

 - Primary Key 🔑

 - Nullable

 - Display table properties clearly

   ### 3️⃣ Relationships

 #### Creating a relationship between two tables:

 - One-to-Many (1-N)

 - Many-to-Many (N-N)

 - Delineate the relationship with arrows, showing the relationship direction.

 - Show the relationship type above the arrow.

 - Delete the relationship by right-clicking.
   
### 4️⃣ N-N Relationships (Intermediate Tables)

 #### When an N-N relationship is created:

 - An intermediate table is automatically created

 - Containing:

 - Two foreign keys

 - One composite primary key

 - The intermediate table appears in:

 - The interface diagram

 - The list of tables

 - The final SQL code

### 5️⃣ SQL Generation and Execution

#### Generating complete and valid SQL code:

 - CREATE TABLE

 - PRIMARY KEY

 - FOREIGN KEY

 - Executing SQL within a temporary database (SQLite)

 - Validating the scheme before execution

#🗂️ Project Structure ;

##Project /:
 - ### main.py
 - ### controllers /
      - maincontroller.py
 - ### models /
      - Schemamodel.py
      - tablemodel.py
      - arributemodel.py
      - relationshipmodel.py
 - # Ui / (veiw)
      - main_window.py
      - tablename.py (add table)
      - deletetable.py
      - addattribute.py
      - deleteatt.py
      - relationship.py
        




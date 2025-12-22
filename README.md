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

# 🗂️ Project Structure ;

## Project /:
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

 # So that : 

 ## 📁 main.py

 #### ✨ Role:

This is the application's entry point.

#### What does it do?

 - It launches the Qt application.

 - It creates the main program window.

 - It starts the event loop.

 - Without it
   
 -  the program won't work.

## 📁 models/

Represents data only, without an interface or graphics.

 ### 📄 schemamodel.py
 #### ✨ Role:

Represents the complete database schema.

#### Contains:

  - All tables

  - All relationships

 #### What it does:

  - Add/delete a table

  - Add/delete a relationship

 - Generate a complete SQL statement

📌 This is the logical representation of the database.

### 📄 tablemodel.py
 #### ✨ Role:

Represents a single table

#### Contains:

  - Table name

  - List of attributes

  - What does it do?

  - Add an attribute

  - Check for a primary key

  - Generate SQL for CREATE TABLE

### 📄 attributemodel.py
#### ✨ Role:

Represents one property (column)

#### Contains:
 
  - Name

  - Type

  - Is it a Primary Key?

 - Is it a Foreign Key?

📌 Simple but essential

### 📄 relationshipmodel.py
#### ✨ Role:

Represents a relationship between two tables

#### Contains:

  - from_table

  - to_table

  - Relationship type (1-N or N-N)

## 📁 ui/
 ### Why is it there?

It contains only the graphical interface.

📌 It's often created with Qt Designer.

 ### Examples:

 #### main_window.py → Main window
 ![ Project interface] (<img width="1897" height="986" alt="Capture d&#39;écran 2025-12-22 233645" src="https://github.com/user-attachments/assets/1bc18bae-7260-4406-a882-2efbe98b2c9f" />

)

 #### tablename.py → Dialog (Enter table name)
  (<img width="1557" height="968" alt="Capture d&#39;écran 2025-12-22 234715" src="https://github.com/user-attachments/assets/fbaf7ec6-2823-4625-a102-f6d4418cafcd" />)
 
  #### addattribute.py → Dialog (Add attribute)
   (<img width="1245" height="966" alt="Capture d&#39;écran 2025-12-23 000002" src="https://github.com/user-attachments/assets/8a214b45-faf8-498e-8f62-df5f25051abc" />
)
#### dedeteatt.py -> Dialog ( remove attribute )
(<img width="1190" height="982" alt="Capture d&#39;écran 2025-12-23 000313" src="https://github.com/user-attachments/assets/aa34217c-ee09-4a4a-ab8d-43dfead40d17" />
)


relationship.py → Dialog (Select relationship)
(<img width="1242" height="976" alt="Capture d&#39;écran 2025-12-23 000627" src="https://github.com/user-attachments/assets/50031232-e5c2-464e-a1e7-48c8063b8d73" />
)

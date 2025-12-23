# Hi there 👋
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
  - ### Ui / (veiw)
      - main_window.py
      - tablename.py (add table)
      - deletetable.py
      - addattribute.py
      - deleteatt.py
      - relationship.py

 ## So that : 

  ### 📁 main.py

   #### ✨ Role:

   This is the application's entry point.

#### What does it do?

   - It launches the Qt application.

   - It creates the main program window.

   - It starts the event loop.

   - Without it
   
   -  the program won't work.

### 📁 models/

 Represents data only, without an interface or graphics.

 #### 📄 schemamodel.py
  ##### ✨ Role:

  Represents the complete database schema.

##### Contains:

   - All tables

   - All relationships

 ##### What it does:

   - Add/delete a table

   - Add/delete a relationship

   - Generate a complete SQL statement

📌 This is the logical representation of the database.

#### 📄 tablemodel.py
 ##### ✨ Role:

  Represents a single table

##### Contains:

   - Table name

   - List of attributes

   - What does it do?

   - Add an attribute

   - Check for a primary key

   - Generate SQL for CREATE TABLE

#### 📄 attributemodel.py
 ##### ✨ Role:

  Represents one property (column)

##### Contains:
 
   - Name

   - Type

   - Is it a Primary Key?

  - Is it a Foreign Key?

  📌 Simple but essential

#### 📄 relationshipmodel.py
 ##### ✨ Role:

  Represents a relationship between two tables

 ##### Contains:

   - from_table

   - to_table

   - Relationship type (1-N or N-N)

### 📁 ui/
 #### Why is it there?

  It contains only the graphical interface.

📌 It's often created with Qt Designer.

 #### Examples:

  ##### main_window.py → Main window
   ![ Project interface] 
 (<img width="1897" height="986" alt="Capture d&#39;écran 2025-12-22 233645" src="https://github.com/user-attachments/assets/1bc18bae-7260-4406-a882-2efbe98b2c9f" />

)

 ##### tablename.py → Dialog (add new table)
  (<img width="1248" height="1003" alt="Capture d&#39;écran 2025-12-23 104738" src="https://github.com/user-attachments/assets/f096d5eb-5d39-416b-a3ef-2fab76e60b52" />
)
 
  ##### addattribute.py → Dialog (Add table attribute)
   (<img width="1248" height="962" alt="Capture d&#39;écran 2025-12-23 105050" src="https://github.com/user-attachments/assets/daf0aeb2-52d1-473c-92fa-c3cd2112318a" />

)
 ##### dedeteatt.py -> Dialog ( remove attribute )
(<img width="973" height="856" alt="Capture d&#39;écran 2025-12-23 105428" src="https://github.com/user-attachments/assets/998e0129-a10b-4b6b-a0fb-ae08cb9255c3" />

)
##### deletetable.py -> Dialog (delete table) 
( <img width="1622" height="962" alt="Capture d&#39;écran 2025-12-23 110231" src="https://github.com/user-attachments/assets/eba43db6-3c11-4559-a8a0-3c32787dc01a" />

)


##### relationship.py → Dialog (ceate relationship)
(<img width="1049" height="804" alt="Capture d&#39;écran 2025-12-23 105613" src="https://github.com/user-attachments/assets/be58a03d-70f2-4027-a09c-fff2962f71fd" />

)
### 📁 controller /
 #### Maincontroller 
  ##### 🔹 MainController Description

   The MainController is the core of the application.
    It connects the user interface with the database logic
     and manages all interactions.

##### 🔹 Initialization (__init__)

  This method:

 -  Loads the UI

 - Initializes the schema

 -  Connects buttons to actions

 - Prepares drawing and interaction events
![Main Interface]
(<img width="1897" height="986" alt="Capture d&#39;écran 2025-12-22 233645" src="https://github.com/user-attachments/assets/1a27323e-1c19-47b9-8ed2-d8abe40b21d5" />
)
##### 🔹 Add Table

Allows the user to create a new table
and display it visually in the canvas.

##### 🔹 Draw Table

Draws a draggable table box
with a title and attributes.
![add table]
(<img width="1248" height="1003" alt="Capture d&#39;écran 2025-12-23 104738" src="https://github.com/user-attachments/assets/27213b39-4cd0-4d75-a458-b13f4911dd3d" />
)  --> (<img width="1330" height="950" alt="Capture d&#39;écran 2025-12-22 234800" src="https://github.com/user-attachments/assets/026e7504-388e-4707-965a-e2b8f0951a95" />
)

##### 🔹 Add Attribute

Allows adding columns with:

Data type

Primary Key

Foreign Key


 ![add attribute]
 (<img width="1248" height="962" alt="Capture d&#39;écran 2025-12-23 105050" src="https://github.com/user-attachments/assets/01e464d3-e807-40a6-a543-2cf59166e473" />

) 

 --> (<img width="1073" height="399" alt="Capture d&#39;écran 2025-12-23 115644" src="https://github.com/user-attachments/assets/9565e76a-4810-4d3e-b2af-a6fba2343902" />

)
#### Note! :

the table in whicg the attributes will be placed must be specified 
(<img width="1270" height="972" alt="Capture d&#39;écran 2025-12-22 235904" src="https://github.com/user-attachments/assets/85d1ff03-d00e-4df3-895e-cca98d775a14" />
)
##### 🔹 Relationships

Supports:

One-to-Many (1-N)

Many-to-Many (N-N)

For N-N relationships:

A join table is created automatically

Includes PK and FK

Displayed in UI and SQL

 ##### 🔹 Drawing Relationships

Relationships are drawn using arrows
with direction and type displayed.

(<img width="1049" height="804" alt="Capture d&#39;écran 2025-12-23 105613" src="https://github.com/user-attachments/assets/1a908124-aa01-4ff9-9828-4f8c22cfceba" />

) (<img width="1849" height="423" alt="Capture d&#39;écran 2025-12-23 122343" src="https://github.com/user-attachments/assets/a4a53203-b217-4f5a-b338-bc5125b8f7bd" />
)

##### 🔹 Delete Relationship

Right-click on a relationship

to delete it and its join table if exist
(<img width="1733" height="957" alt="Capture d&#39;écran 2025-12-23 105733" src="https://github.com/user-attachments/assets/1ff88019-da73-4f54-aee9-bd50cc224d5d" />
)

##### 🔹 SQL Generation

Ensures all tables have a Primary Key
and generates valid SQL code.

(<img width="1749" height="980" alt="Capture d&#39;écran 2025-12-23 122403" src="https://github.com/user-attachments/assets/b9cc916e-efdd-4517-8e72-1f1389a314be" />
)

##### ▶️ Run SQL Button

The Run SQL button executes the generated SQL code directly using an SQLite database (in-memory).

- When the button is clicked:

   - The SQL code is read from the preview area

   - Each SQL statement is executed sequentially

   - If an error occurs, an error message is displayed

   - If execution is successful, a confirmation message is shown

- This feature ensures that:

   - The database schema is valid

   - All constraints and relationships are correctly defined

   - The generated SQL is executabl

 (<img width="1718" height="985" alt="Capture d&#39;écran 2025-12-23 105811" src="https://github.com/user-attachments/assets/f2462f1d-0219-4e5d-acea-a012db1b316d" />
)
## 🔹 Conclusion

This project demonstrates:

Database design

GUI programming

MVC architecture

SQL generation 
 ## ![final result ]
 (<img width="1896" height="972" alt="Capture d&#39;écran 2025-12-23 131616" src="https://github.com/user-attachments/assets/559d0bf4-91b3-4941-932a-ec1dff6d08d3" />
)





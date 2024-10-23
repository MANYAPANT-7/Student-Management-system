# Student-Management-system


## Overview
The **Student Management System** is a Python-based application designed to manage student and teacher records. It provides functionalities to add, update, display, and delete records of students and teachers, as well as save this information to CSV files. The system connects to a MySQL database for persistent data storage.

## Features
- **Add Student**: Easily add new student records with details such as name, age, course, and fees status.
- **Update Fees Status**: Update the fees status of existing students based on their payment.
- **Assign Teacher to Student**: Assign a teacher to a specific student along with the subject they teach.
- **Display Students**: View all student records directly in the terminal.
- **Display Teacher**: View all teacher records in the terminal.
- **Delete Student**: Remove a student's record from the database.
- **Delete Teacher**: Remove a teacher's record from the database.
- **Save to CSV**: Save student and teacher records to separate CSV files for external use.

## Technology Stack
- **Programming Language**: Python
- **Database**: MySQL
- **Data Format**: CSV (Comma-Separated Values)

## Getting Started
### Prerequisites
- Python 3.x
- MySQL Server
- mysql-connector-python library (to install, use `pip install mysql-connector-python`)

### Setting Up the Database
1. Create a MySQL database named `student_management`.
2. Create the following tables:
   ```sql
   CREATE TABLE students (
       student_id INT AUTO_INCREMENT PRIMARY KEY,
       name VARCHAR(100),
       age INT,
       course VARCHAR(100),
       fees_paid BOOLEAN
   );

   CREATE TABLE teachers (
       teacher_id INT AUTO_INCREMENT PRIMARY KEY,
       name VARCHAR(100),
       subject VARCHAR(100),
       assigned_to INT,
       FOREIGN KEY (assigned_to) REFERENCES students(student_id)
   );
### How to Run

1. Clone the repository or download the project files.
2. Ensure the required libraries are installed:
  ```Python
pip install mysql-connector-python
 ```

3. Run the application:
  ```Python
python student_management_system.py
```
4. Follow the on-screen prompts to manage student records.

### Code Structure
- Add Student: Add new students to the database with their name, age, and course details.
- Update Fees Status: Update the fees status for a specific student.
- Assign Teacher: Assign a teacher to a student along with their subject.
- Display Students: View all student records in the terminal.
- Display Teachers: View all teacher records in the terminal.
- Delete Student: Remove a student's record from the database.
- Delete Teacher: Remove a teacher's record from the database.
- Save to CSV: Save student and teacher records to separate CSV files for external use.

###  Example Usage
```
--- Student Management System ---
1. Add a Student
2. Update Fees Status
3. Assign Teacher to a Student
4. Save Students to CSV
5. Save Teachers to CSV
6. Display Students
7. Display Teachers
8. Delete a Student
9. Delete a Teacher
10. Exit
Enter your choice (1-10): 1

Enter student's name: Manya
Enter student's age: 19
Enter student's course: Computer Science
Student Manya added successfully!
```
### Future Enhancements
Implement user authentication to secure access to the system.
Add functionality to delete student or teacher records.
Create a graphical user interface (GUI) for better user experience.

### Contributing
Contributions are welcome! If you have suggestions for improvements or additional features, please submit a pull request or open an issue on the GitHub repository.

### License
This project is open-source and available under the MIT License.


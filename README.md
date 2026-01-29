overview

(Normalization)
Normalization is a database design process used to organize data in a database efficiently. Its main goals are:
Eliminate data redundancy – avoid storing the same data in multiple places.
Ensure data consistency – changes in one place automatically reflect everywhere.
Improve data integrity – reduce errors and anomalies when inserting, updating, or deleting data.

Database Schema

Unnormalized Form (Initial)

```
data (StudentID, Name, Email, Majors, Majorhead, CourseID, CourseTittle, Credits, Grade, Building, room)

```

1NF(first normal form )
it has already in first normal you don't have to do in 1NF

## 2NF (Second Normal Form)

1. Students(StudentID, Name, Email, Major)
2. Courses(CourseID, CourseTitle, Credits, Building, Room)
3. Enrollments(StudentID, CourseID, Grade)

## 3NF (Third Normal Form)

1. Students(StudentID, Name, Email, Major)
2. Courses(CourseID, CourseTitle, Credits, Building, Room)
3. Enrollments(StudentID, CourseID, Grade)
4. Majors(Major, Advisor)

Usage Instructions

Running Individual SQL Scripts

Step 1: Create Unnormalized Table

```
 CREATE TABLE data (
    StudentID VARCHAR(50) PRIMARY KEY,
     Name VARCHAR(50),
    Email VARCHAR (50),
     Majors VARCHAR(50),
     Majorshead VARCHAR(50),
     CourseID VARCHAR(50),
     CourseTitle VARCHAR(50),
     Credits int,
     Grade VARCHAR(50),
     Building VARCHAR(50),
     Room VARCHAR
     );

 INSERT INTO data1
 ('S101','Alice','alice@uni.edu','CS','Dr.smith','CS301','Algorithms',4,'C','Science',205);
 ('S102','Bob','Bob@uni.edu','CS','Dr.smith','CS301','Algorithms',4,'C','Science',205);
  ('S103','carol','carol@uni.edu','physics','Dr.lee','CS301','Linear Algebra',3,'A','Math wing',101);

```

it has already in 1NF you don't have to do in 1NF (first normal form )

Step 2: Apply Normalization
## 2NF 

Table Students 
```
CREATE TABLE Students (
StudentID VARCHAR(10) PRIMARY KEY,
Name VARCHAR(100) NOT NULL,
Email VARCHAR(100) UNIQUE NOT NULL,
Major VARCHAR(50),
FOREIGN KEY (Major) REFERENCES Majors(
Major)
);

```

Inserting values

```
INSERT INTO Students VALUES
('S101', 'Alice', 'alice@uni.edu', 'CS'),
('S102', 'Bob', 'bob@uni.edu', 'CS'),
('S103', 'Carol', 'carol@uni.edu', 'Physics');

```

Table Courses 
```
CREATE TABLE Courses (
CourseID VARCHAR(10) PRIMARY KEY,
CourseTitle VARCHAR(100) NOT NULL,
Credits INT NOT NULL,
Building VARCHAR(50),
Room VARCHAR(10)
);

```

Inserting values

```
INSERT INTO Courses VALUES
('CS301', 'Algorithms', 4, 'Science', '205'),
('MATH201', 'Linear Algebra', 3, 'Math Wing',
'101'),
('PHYS101', 'Mechanics', 4, 'Science', '301');

```

Table Enrollments 

```
CREATE TABLE Enrollments (
StudentID VARCHAR(10),
CourseID VARCHAR(10),
Grade CHAR(1),
PRIMARY KEY (StudentID, CourseID),
FOREIGN KEY (StudentID) REFERENCES
Students(StudentID),
FOREIGN KEY (CourseID) REFERENCES Courses(
CourseID)
);

```

Inserting values

```
INSERT INTO Enrollments VALUES
('S101', 'CS301', 'A'),
('S101', 'MATH201', 'B'),
('S102', 'CS301', 'C'),
('S103', 'PHYS101', 'A');

```
 







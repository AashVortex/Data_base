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





overview

(Normalization)
Normalization is a database design process used to organize data in a database efficiently. Its main goals are:
Eliminate data redundancy – avoid storing the same data in multiple places.
Ensure data consistency – changes in one place automatically reflect everywhere.
Improve data integrity – reduce errors and anomalies when inserting, updating, or deleting data.

Database Schema

Unnormalized Form (Initial)

"""
data (StudentID, Name, Email, Majors, Majorhead, CourseID, CourseTittle, Credits, Grade, Building, room)

"""



```sql
CREATE TABLE data (
    StudentID INT PRIMARY KEY,
    Name VARCHAR(100),
    Email VARCHAR(100),
    Majors VARCHAR(50),
    Majorhead VARCHAR(100),
    CourseID VARCHAR(20),
    CourseTittle VARCHAR(100),
    Credits INT,
    Grade CHAR(2),
    Building VARCHAR(50),
    Room VARCHAR(10)
);
```



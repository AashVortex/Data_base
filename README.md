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





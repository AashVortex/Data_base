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

2NF(second normal form )
Students(StudentID, Name, Email, Major)
Courses(CourseID, CourseTittle, Credits, Building, Room )
Enrollments(StudentsID, CourseID, Grade)

3NF(third normal form )
Students(StudentID, Name, Email, Major)
Courses(CourseID, CourseTittle, Credits, Building, Room )
Enrollments(StudentsID, CourseID, Grade)
Majors(Major,Advisor)




# Week 3 - Day 2 - ERM Case Studies

# Case Study 1: University Enrollment System

## Entities
The main entities in this system are:
- Student
- Course
- Professor

## Attributes

**Student**
- StudentID (PK)
- Name
- Major

**Course**
- CourseID (PK)
- Name
- Credits

**Professor**
- ProfessorID (PK)
- Name
- Department

## Relationships

Students and courses have a many-to-many relationship. A student can take multiple courses, and each course can have multiple students.

Professors and courses are one-to-many. One professor can teach multiple courses, but each course is assumed to be taught by one professor.

## Keys / Structure Notes

Because students and courses are many-to-many, you would normally use a junction table like Enrollment:

**Enrollment**
- StudentID (FK)
- CourseID (FK)

For professors, the relationship is handled by adding a foreign key in Course:
- Course.ProfessorID (FK)


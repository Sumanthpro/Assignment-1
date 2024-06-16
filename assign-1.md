# Assignment-1

1. Write an SQL query to insert a new student named John Doe into the "Students" table.

query:

```sql
insert into students(student_id,first_name,last_name,date_of_birth,email,Phone_number)
values
      (107,'John','Doe','2000-04-14','johndoe@gmail.com',9177483720);
```
![alt text](image.png)

2.Write an SQL query to enroll an existing student in a course, specifying the enrollment date.

query:
```sql
insert into enrollments values(408,107,201,'2024-04-14');
```
![alt text](image-1.png)


# Assignment-1

1. Write an SQL query to insert a new student named John Doe into the "Students" table.

query:

```sql
insert into students(student_id,first_name,last_name,date_of_birth,email,Phone_number)
values
      (107,'John','Doe','2000-04-14','johndoe@gmail.com',9177483720);
```

output:

![alt text](image.png)

2.Write an SQL query to enroll an existing student in a course, specifying the enrollment date.

query:

```sql
insert into enrollments values(408,107,201,'2024-04-14');
```

output:

![alt text](image-1.png)

3. Update the email address of a teacher in the "Teachers" table.

query:

```sql
update teachers set email = 'jessicacassendra@gmail.com' where teacher_id=301;
```

output:

![alt text](image-2.png)

4. Write an SQL query to delete a specific enrollment record, choosing based on the student and course.

query:

```sql
delete from enrollments where student_id=101 and course_id=203;
```

output:
![alt text](image-3.png)

5. Update a course to assign a specific teacher using the "Courses" table.

query:

```sql
update courses set teacher_id=302 where course_id=201;
```

![alt text](image-4.png)

6. Write an SQL query to calculate the total payments made by a specific student.

query:

```sql
select *from payments where student_id=102;
```

output:

![alt text](image-5.png)

7. Retrieve a list of courses along with the count of students enrolled in each.

query:

```sql
select course_name,count(student_id) as Total_enrolls from courses as c
inner join enrollments as e
on c.course_id=e.course_id group by course_name;
```

output:

![alt text](image-6.png)

8. Find the names of students who have not enrolled in any course.

query:

```sql
select  CONCAT(first_name,' ',last_name) as Student_name  from students as e left join enrollments as s
on e.student_id = s.student_id where enrollment_id is null;
```

output:

![alt text](image-7.png)

9. Retrieve the first name and last name of students, along with the names of the courses they are enrolled in.

query:

```sql
select first_name,last_name,course_name from students as s
inner join
enrollments as e
on s.student_id=e.student_id inner join courses as c on e.course_id=c.course_id;
```

output:

![alt text](image-8.png)

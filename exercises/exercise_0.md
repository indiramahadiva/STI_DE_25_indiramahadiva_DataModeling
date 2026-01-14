# Exercise 0 - fundamental concepts of data modeling

## 0. Library Bookly

### a.Entities and Attributes:

**Entities**

- Book
- Member

**Attributes**

- Book: title, author, ISBN
- Member: membership_id, name, contact_information

### b. Relationship: The relationship is "borrows" - a Member borrows a Book.

### Conceptual ERD:

**In crow's foot notation:**

- A Member can borrow zero or many Books (one-to-many)
- A Book can be borrowed by zero or one Member at a time (one-to-one at any moment)

## 1. Conceptual ERD to Words

**Car rental entities would include:**

- Customer
- Rental
- Car

**Relationship Labels:**

- Customer places Rental
- Rental involves Car

**Relationships:**

- Customer to Rental: One-to-Many
  One customer can have zero or many rentals
  Each rental belongs to exactly one customer

- Rental to Car: Many-to-One
  Many rentals can involve the same car (at different times)
  Each rental involves exactly one car

**Relationship Statements:**

- A Customer can have zero or more Rentals
- A Rental must be placed by exactly one Customer
- A Rental must involve exactly one Car
- A Car can be involved in zero or many Rentals

## 2. University Management System - ERD Instructions

1. Student :

student_id (PK - underline)
first_name
last_name
email
enrollment_date

2. Course :

course_id (PK)
course_name
course_code
credits

3. Professor :

professor_id (PK)
first_name
last_name
department
email

4. Enrollment (junction table for many-to-many):

enrollment_id (PK)
student_id (FK)
course_id (FK)
enrollment_date
grade

- Relationships :
  Student Enrollment (Many-to-Many through Enrollment)
  Course Enrollment (Many-to-Many through Enrollment)
  Professor Course (One-to-Many: One professor teaches many courses)

- Add Business Rules :
  "Max 4 courses per student per semester"
  "Min 5 students per course"
  "Max 3 courses per professor per semester"

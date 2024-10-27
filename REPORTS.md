
# UML CLASS DIAGRAM

---

## Introduction

Introduction to Class Diagram:
A Class Diagram is a type of structural diagram used in the Unified Modelling Language [`UML`](https://en.wikipedia.org/wiki/Unified_Modeling_Language) This type of diagram focuses on the visualization of objects (Classes) and the connections between them, such as Inheritance or Aggregation. The diagram represents the system's Classes, __`Attributes`__, and __`Methods`__, as well as the __`Relationships`__ that connect these objects to each other.

![Class Diagram](/images/maxresdefault.jpg)

## Class Diagram Components

Classes: Represent the basic objects of the system that contain properties and methods:

- __`Attributes`__: These are the values or variables that an object holds.
- __`Methods`__: These are the functions that a class can implement.
- __`Relationships`__: Represent how classes are related to each other.

---

## Scenario

Imagine that we have a university system to manage the library, students, departments, courses, and fees. The role of the Class Diagram is to show all the classes involved in this system and how they interact with each other. This diagram can be used by developers to understand the relationships between the different components of the system before they start coding.

---

-__adminID__: Unique identifier for theadmin (String).
- __name__: Name of the admin (String).
- __email__: Email address of the admin (String).

### operations

- `addStudent(student:Student)`: Adds a new student to the system.
- `updateStudentInfo(studentID:String)`: Updates the information of a student based on their studentID.
- `addCourse(course:Course)`: Adds a new course to the system.
- `updateCourseInfo(courseID:String)`: Updates the information of a specific course.
- `addDepartment(department:Department)`: Adds a new department to the system.
- `updateDepartmentInfo(departmentID:String)`:Updates the setails of an existing department.
- `assignHeadOfDepartment(departmentID:String, professorID: String)`: Assigns a professor as the head of a specific department.



- __Manages__:
  - The `Admin` manages:
    - `Student`
    - `Course`
    - `Department`
   
---

 


            
- __studentID__: Unique identifier for the student(String).
- __name__: Name of the student(String).
- __email__: Email address of the student(string).
- __phone__: Contact number of the student(String).
- __address__: Address of the student(String).



- `updateInfo()`: Allows the student to update their personal information.
- `registerCourse(courseID: String)`: Enables the student to enroll in a specific course.
- `viewGrades(): List<Grade>`: Provides the student with a list of their grades.
- `payFees(amount:Double)`: Allows the student to pay their fees.




 








































 Fee Class

### Attributes

- __feeID__: Unique identifier for the fee (String).
- __studentID__: Unique identifier of the student who is charged (String).
- __amount__: Amount of the fee (Double).
- __dueDate__: The due date for fee payment (Date).
- __status__: The current payment status (String).

### Relationships

- __Managed by__
  - The `Fee` is managed by the `FeeSystem`, which is responsible for generating and updating fee details.

---

## 9. Accountant Class

### Attributes

- __accountantID__: Unique identifier for the accountant (String).
- __name__: Name of the accountant (String).
- __email__: Email address of the accountant (String).

### Operations

- `generateInvoice(studentID: String, amount: Double)`: Generates an invoice for a student.
- `updatePaymentStatus(studentID: String, status: String)`: Updates the payment status for a student.
- `viewFees(studentID: String): List<Fee>`: Allows the accountant to view the list of fees for a student.

### Relationships

- __Manages__
  - The `Accountant` manages the `FeeSystem` by generating and updating fee information.

---

## Plain Text Diagrams Classes

```c++
class Student {
    +studentID: String
    +name: String
    +email: String
    +phone: String
    +address: String
    +updateInfo()
    +registerCourse(courseID: String)
    +viewGrades(): List<Grade>
    +payFees(amount: Double)
}
```














































##__Class Accountant__

```c++
class Accountant {
    +accountantID: String
    +name: String
    +email: String
    +generateInvoice(studentID: String, amount: double)
    +updatePaymentStatus(studentID: String ,status: String)
    +viewFees(studentID: String): list<fee>
}
```
## All Classes Plain Text

```yml
@startuml
class Student {
    studentID: String
    name: String
    email: String
    phone: String
    address: String
    updateInfo()
    registerCourse(courseID: String)
    viewGrades(): List<Grade>
    payFees(amount: Double)
}
class Admin {
    adminID: String
    name: String
    email: String
    addStudent(student: Student)
    updateStudentInfo(studentID: String)
    addcourse(course: Course)
    updateCourseInfo(courseID: String)
    addDepartment(department: Department)
    updateDepartmentInfo(departmentID: String)
    assignHeadOfDepartment(departmentID: String, professorID: String)
}

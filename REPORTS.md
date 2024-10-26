
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







-__adminID__: Unique identifier for theadmin (String).
- __name__: Name of the admin (String).
- __email__: Email address of the admin (String).


            
لعلتل
عهع




---








































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

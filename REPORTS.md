
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

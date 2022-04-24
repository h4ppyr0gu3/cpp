## Prelim Project CPP

Requirements for Preliminary Project in EOOP LaboratoryEach student receives a keyword for the project during EOOP Laboratory. 
The keyword has to be name of one class and at least three other are required.
The document of Preliminary Projects has to containfour points:

1.  Description of the project (“The Story”)The description defines functionalities of the classes and relations between them. 
  Some limits and restrictions should be specified there. 
  The functionality of each class should be simple, anyway consistent and complete (considering all consequences of the particular choices). 
  Description is presented in the natural language up to one page.
2.  Case study (a memory map)It should be a drawing presenting relations between number of objects from differentclasses. 
  These relations should be representativeand should show how particular pointers are organized in a coherent way.
3. Declaration of the classesWritten in C++ declaration of the classes should present declarations of all public methodsand private data structures of each class. 
  In comments special behaviorsof methods should be explained.
4.  Testing Written in C++ scenarios of correct and incorrect cases, with explanationswhat sequences of instructions should demonstrate.

## Car garage

### Story

- Keep track of progress and inventory within a garage setting 
- Allow only admins to take new orders but keep a possible client list
- Keep track of qoutes of future customers again only made by the manager
- Admin is able to create other admins
- Admin can create Employees and customer entries
- Admin can update Customer entries
- Employee can update the status only of a customer ticket
- Employee can log additional details 

#### Classes

```c++
class Vehicle {
  private: 
    string make
    string model
    int year
    int cc
    int parking // 1..3
    string type // enum
}

class Person {
  private:
    string name
    string phone
    string email
}

class Employee : public Person {
  private:
    int id
    Ticket ticket
    Admin supervisor
}

class Admin : public Person {
  private: 
    int id
    Ticket ticket
}

class Ticket {
  private:
    int id
    Admin admin
    Employee employee
}
```


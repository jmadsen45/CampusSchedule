# CampusSchedule 
John Madsen
John Madsen
Design Patterns Assignment 1
UML Class Diagram explanation:
Worker interface and classes that realize this interface:
•	There is an Intern class and an Employee class that both realize the worker interface. 
•	An interface is used for worker because a worker does not contain any implantation on its own because any time a worker is created within the company it is either an Employee or an Intern.  
•	The manager class extends the Employee class because a Manager is also an Employee of the company and must inherit any methods and attributes the Employee class contains (such as address).
Address class:
•	The Address class is a directed composition of the Employee class.  
•	This is a composition because the Address class does not mean anything outside of the context of the Employee class.  
•	This is a directed relationship because only the employee is aware of the relationship, by holding a list of addresses that the employee has.  The Address class does cannot tell which employee has a given address.
•	The relationship from Address to Employee is a 0 to many relationship because an employee can have 0 or more addresses.
•	The relationship from Employee to Address is 1 because I assumed that multiple workers will not share an address.
Department class:
•	The Department class has three attributes:
o	Head: holds the head of the department.
o	Employees: holds a list of employees who belong to the department.
o	Interns: holds a list of interns who belong to the department.
•	Relationships:
o	There is a directed aggregation relationship from Department to intern, Department to Employee, and Department to Manager. 
o	These are aggregation relationships because these three workers make up part of the department, but the workers also make sense in a context outside of the department.
o	They are also directed relationships because the Department holds lists of all the workers within the department, but the workers do not hold an attribute of which department they are working for.
o	The Department to intern relationship is 0 to many because a department can have 0 or more Interns working within the department.
o	The Department to Employee relationship is 1 to many because a department should have at least 1 worker but can also have many more than that.
o	The Department to Manager relationship is 1 to 1 because there can only be one manager at the head of a department.
o	The relationship the other way is all 1 to 1 because an employee/intern/manager can not belong to more than one apartment (assumed).
o	I needed a direct link to Manager because I didn’t want to handle the Manager to Department relationship through my Employee to Department relationship.  This is to ensure a regular employee is not made head of a department (which would be possible without the extra relationship).
       HumanResources Class:
•	Attributes and Methods:
o	HR class has one attribute to the HumanResources class which is employeeList which maintains a list of all employees.
o	CreateEmployee and AssignEmployee methods create a dependence relationship on the Employee class.
o	CreateManager and AssignManager methods create a dependence relationship on the Manager class.
o	AssignEmployee and AssignManager created a dependence relationship on the department class.
o	Once again I drew a dependence relationship to Employee and Manager instead of just Employee to ensure the CreateManager and AssignManager methods actually took in a Manager for a parameter instead of just any Employee.


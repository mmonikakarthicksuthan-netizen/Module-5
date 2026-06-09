# # Constructors in Python: Welcome Message with Student Name

## 🎯 Aim
To write a Python program that creates a **Student** class with a **default constructor** and a method to display a welcome message along with the student’s name provided by the user.

## 🧠 Algorithm
1. **Get user input**: Accept the student's name from the user.
2. **Define the class**: Create a class `Student` with a default constructor (`__init__`).
3. **Default Constructor**: In the constructor, assign the user input (student name) to an instance variable `self.a`.
4. **Display Message**: Define a method `show` that prints "This is non-parameterized constructor" and a welcome message with the student’s name.
5. **Execute the Program**: Instantiate the `Student` class and call the `show` method.

## 🧾 Program

```
class Student:
    def __init__(self):
        self.a = input("Enter student name: ")
    def show(self):
        print("This is non-parameterized constructor")
        print("Welcome", self.a)

obj = Student()
obj.show()
```

## Output
Enter student name: Arun
This is non-parameterized constructor
Welcome Arun
## Result
The program is compeleted successfully
# Destructor in Python

This project demonstrates how to implement a **destructor** in Python using a simple class.

## 🚀 Overview

The program defines a class `Demo` with:

- A **constructor** `__init__` that initializes an instance variable and prints a message.
- A **destructor** `__del__` that prints a message when the object is destroyed.

## 🧠 Algorithm

1. Define a class named `Demo`.
2. Inside the class, define the `__init__` method:
   - Initialize an instance variable `status` with the value `"Alive"`.
   - Print the value of `status`.
3. Define the `__del__` method:
   - Print a message indicating the object is being destroyed.
4. Outside the class:
   - Create an instance of the `Demo` class.
   - Delete the object using the `del` keyword.
## Program
```
class Demo:
    def __init__(self):
        self.status = "Alive"
        print("Status:", self.status)
    
    def __del__(self):
        print("Object is being destroyed")

obj = Demo()
del obj
```

## 🧪 Output
Status: Alive
Object is being destroyed
## Result
the program is verified
# Hierarchical Inheritance in Python

This Python project demonstrates **Hierarchical Inheritance** using a base class `Details` and two derived classes `Employee` and `Patient`. The program collects and displays details for both employees and patients.

## 🎯 Aim

To write a Python program that uses **Hierarchical Inheritance** to input and display **Employee** and **Patient** details.

## 📘 Description

- **Base Class:** `Details`
  - Stores common attributes: `name`, `age`
  - Provides methods: `getName()`, `getAge()`

- **Derived Class 1:** `Employee`
  - Inherits from `Details`
  - Adds: `employee_id`, `department`
  - Method: `getEmployeeDetails()`

- **Derived Class 2:** `Patient`
  - Inherits from `Details`
  - Adds: `patient_id`, `disease`
  - Method: `getPatientDetails()`

## 🧠 Algorithm

1. Create base class `Details` with common attributes.
2. Create `Employee` class extending `Details`, adding employee-specific data.
3. Create `Patient` class extending `Details`, adding patient-specific data.
4. Get user input for employee and patient data.
5. Display collected information using class methods.

## Program
```
class Details:
    
    def getName(self):
        self.name = input("Enter Name: ")
    
    def getAge(self):
        self.age = int(input("Enter Age: "))

class Employee(Details):
    
    def getEmployeeDetails(self):
        print("\n--- Employee Details ---")
        self.getName()
        self.getAge()
        self.employee_id = input("Enter Employee ID: ")
        self.department = input("Enter Department: ")
        
    def displayEmployee(self):
        print("\nEmployee Information")
        print("Name:", self.name)
        print("Age:", self.age)
        print("Employee ID:", self.employee_id)
        print("Department:", self.department)

class Patient(Details):
    
    def getPatientDetails(self):
        print("\n--- Patient Details ---")
        self.getName()
        self.getAge()
        self.patient_id = input("Enter Patient ID: ")
        self.disease = input("Enter Disease: ")
        
    def displayPatient(self):
        print("\nPatient Information")
        print("Name:", self.name)
        print("Age:", self.age)
        print("Patient ID:", self.patient_id)
        print("Disease:", self.disease)

e = Employee()
e.getEmployeeDetails()
e.displayEmployee()

p = Patient()
p.getPatientDetails()
p.displayPatient()
```
## Sample Output
--- Employee Details ---
Enter Name: Arun
Enter Age: 30
Enter Employee ID: E101
Enter Department: IT

Employee Information
Name: Arun
Age: 30
Employee ID: E101
Department: IT

--- Patient Details ---
Enter Name: Ramesh
Enter Age: 45
Enter Patient ID: P205
Enter Disease: Fever

Patient Information
Name: Ramesh
Age: 45
Patient ID: P205
Disease: Fever
# Multilevel Inheritance Example in Python

This Python project demonstrates the concept of **Multilevel Inheritance** to collect and display the **name**, **age**, and **location** of a person.

## 🎯 Aim

To write a Python program that uses multilevel inheritance to get and display a person’s name, age, and location.

## 🧠 Algorithm

1. **Parent Class**  
   - `__init__(name)` initializes the `name` attribute.  
   - `getName()` returns the `name`.

2. **Child Class (inherits Parent)**  
   - `__init__(name, age)` initializes `name` using `super()` and adds `age`.  
   - `getAge()` returns the `age`.

3. **Grandchild Class (inherits Child)**  
   - `__init__(name, age, location)` initializes `name` and `age` using `super()` and adds `location`.  
   - `getLocation()` returns the `location`.

4. **Input & Output**  
   - Take user input for name, age, and location.  
   - Create an instance of `Grandchild`.  
   - Print all details using class methods.

## Program
```
class Person:
    def __init__(self, name):
        self.name = name
    
    def getName(self):
        return self.name
class Details(Person):
    
    def __init__(self, name, age):
        super().__init__(name)
        self.age = age
    
    def getAge(self):
        return self.age

class Location(Details):
    
    def __init__(self, name, age, location):
        super().__init__(name, age)
        self.location = location
    
    def getLocation(self):
        return self.location

name = input("Enter Name: ")
age = int(input("Enter Age: "))
location = input("Enter Location: ")

obj = Location(name, age, location)

print("\n--- Person Details ---")
print("Name:", obj.getName())
print("Age:", obj.getAge())
print("Location:", obj.getLocation())
```

## Sample Output
Enter Name: Kumar
Enter Age: 25
Enter Location: Salem

--- Person Details ---
Name: Kumar
Age: 25
Location: Salem
# Arithmetic Operations Using Multiple Inheritance in Python

This Python program demonstrates **multiple inheritance** by performing basic arithmetic operations — Addition, Subtraction, and Division — using three classes.

## 🎯 Aim

To write a Python program to calculate **Add, Sub & Division** using **Multiple Inheritance**.

## 🧠 Algorithm

1. **Define `Calculation1` class**
   - Contains `Summation(a, b)` method to return the sum of two numbers.
2. **Define `Calculation2` class**
   - Contains `Subtraction(a, b)` method to return the difference of two numbers.
3. **Define `Derived` class**
   - Inherits from both `Calculation1` and `Calculation2`.
   - Contains `Division(a, b)` method to return the division result.
4. **Input**
   - Prompt the user to enter two numbers.
5. **Process**
   - Create an object of the `Derived` class.
   - Call `Summation`, `Subtraction`, and `Division` methods.
6. **Output**
   - Display the results of the three operations.

## 💻 Program 
```
class Calculation1:
    
    def Summation(self, a, b):
        return a + b

class Calculation2:
    
    def Subtraction(self, a, b):
        return a - b

class Derived(Calculation1, Calculation2):
    
    def Division(self, a, b):
        if b != 0:
            return a / b
        else:
            return "Cannot divide by zero"

a = float(input("Enter first number: "))
b = float(input("Enter second number: "))

obj = Derived()

print("\n--- Results ---")
print("Addition:", obj.Summation(a, b))
print("Subtraction:", obj.Subtraction(a, b))
print("Division:", obj.Division(a, b))
```
## Output Example
Enter first number: 10
Enter second number: 5

--- Results ---
Addition: 15.0
Subtraction: 5.0
Division: 2.0

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
~~~
class Calculation1:  
    def Summation(self,a,b):  
        return a+b;  
class Calculation2:  
    def sub(self,a,b):  
        return a-b;  
class Derived(Calculation1,Calculation2):  
    def Mul(self,a,b):  
        return a*b;  
a=int(input())
b=int(input())
d = Derived()  
print(d.Summation(a,b))  
print(d.sub(a,b))  
print(d.Mul(a,b))
~~~
## Output Example

<img width="334" height="209" alt="image" src="https://github.com/user-attachments/assets/33a0230d-71ef-43a9-83db-de167871c1bf" />


## Result

The multiple inheritence is verified successfully.

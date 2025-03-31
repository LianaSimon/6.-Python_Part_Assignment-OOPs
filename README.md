# PYTHON ASSIGNMENT ON OOPS

## Question 1:
### Build a program to manage a university's course catalog. You want to define a base class Course that has the following properties:
#### course_code: a string representing the course code (e.g., "CS101")
#### course_name: a string representing the course name (e.g., "Introduction to Computer Science")
#### credit_hours: an integer representing the credit hours for the course (e.g., 3)
### You also want to define two subclasses CoreCourse and ElectiveCourse, which inherit from the Course class.
### CoreCourse should have an additional property required_for_major which is a boolean representing whether the course is required for a particular major.
### ElectiveCourse should have an additional property elective_type which is a string representing the type of elective (e.g., "general", "technical", "liberal arts").


# University Course Catalog Program

This program defines a Course base class and two subclasses, CoreCourse and ElectiveCourse.

## PROGRAM 1

class Course:

    def __init__(self, course_code, course_name, credit_hours):
    
        self.course_code = course_code
        
        self.course_name = course_name
        
        self.credit_hours = credit_hours
        

    def display_info(self):
    
        return f"Course Code: {self.course_code}, Name: {self.course_name}, Credit Hours: {self.credit_hours}"
        

class CoreCourse(Course):

    def __init__(self, course_code, course_name, credit_hours, required_for_major):
    
        super().__init__(course_code, course_name, credit_hours)
        
        self.required_for_major = required_for_major
        

    def display_info(self):
    
        return super().display_info() + f", Required for Major: {self.required_for_major}"
        

class ElectiveCourse(Course):

    def __init__(self, course_code, course_name, credit_hours, elective_type):
    
        super().__init__(course_code, course_name, credit_hours)
        
        self.elective_type = elective_type
        

    def display_info(self):
    
        return super().display_info() + f", Elective Type: {self.elective_type}"
        

# Example Usage

core = CoreCourse("CS101", "Introduction to Computer Science", 3, True)

elective = ElectiveCourse("HIST202", "World History", 2, "liberal arts")


print(core.display_info())

print(elective.display_info())



## OUTPUT 1

![image](https://github.com/user-attachments/assets/3f73ce53-92cf-44d3-9f2f-a5ccc8e77181)




## Question 2: (5 Marks)
### Create a Python module named employee that contains a class Employee with attributes name, salary and methods get_name() and get_salary(). Write a program to use this module to create an object of the Employee class and display its name and salary.



# Employee Module and Jupyter Notebook Usage

Create a Python module named employee.py

Save the following code in a file named employee.py:


## PROGRAM 2a

class Employee:

    def __init__(self, name, salary):
    
        self.name = name
        
        self.salary = salary
        

    def get_name(self):
    
        return self.name
        

    def get_salary(self):
    
        return self.salary



# Use the employee module in Jupyter Notebook In a Jupyter Notebook cell, write the following code to import and use the module:

## PROGRAM 2b


import employee


# Create an Employee object

emp = employee.Employee("John Doe", 50000)


# Display Employee details

print(f"Employee Name: {emp.get_name()}")

print(f"Employee Salary: {emp.get_salary()}")


## OUTPUT 2

![image](https://github.com/user-attachments/assets/55a5fd8d-cd27-4822-a0ec-6978305d2c27)




        




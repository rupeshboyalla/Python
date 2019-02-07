# Python

**1. What is differnce between Python and Java:**

  **Java is a statically typed**:  In Java, all variable names (along with their types) must be explicitly declared. Attempting to assign an object of the wrong type to a variable name triggers a type exception. That’s what it means to say that Java is a statically typed language.
  Java container objects (e.g. Strings and ArrayList) hold objects of the generic type Object, but cannot hold primitives such as int. To store an int in a Vector, you must first convert the int to an Integer. When you retrieve an object from a container, it doesn’t remember its type, and must be explicitly cast to the desired type.
  **Example**:

    int    myCounter = 0;
    String myString = String.valueOf(myCounter);
    if (myString.equals("0")) ...


**Python is Dynamically typed**: In Python, you never declare anything. An assignment statement binds a name to an object, and the object can be of any type. If a name is assigned to an object of one type, it may later be assigned to an object of a different type. That’s what it means to say that Python is a dynamically typed language.
Python container objects (e.g. lists and dictionaries) can hold objects of any type, including numbers and lists. When you retrieve an object from a container, it remembers its type, so no casting is required.
  **Example**:
  
    myCounter = 0
    myString = str(myCounter)
    if myString == "0": ...
    
 **Braces vs Indentation**
 
Java, like most other languages, uses curly braces to define the beginning and end of each function and class definition.

Python is unusual among programming languages in that it uses indentation to separate code into blocks. 

The advantage of using indentation is that it forces you to set your program out in a way that is easy to read, and there is no chance of errors resulting from a missing brace.
    
**2. Python how code is code compiling**

Python source code is automatically compiled into Python byte code by the CPython interpreter. Compiled code is usually stored in PYC (or PYO) files, and is regenerated when the source is updated, or when otherwise necessary

**3. IDE**

 PyCharm or any IDE 
 
**4. Arrays**

In python arrays and lists are same - what is that means ? array have inbuilt functions for adding, deleting and insert at position (like java list collection) 

 **Example**
 
     my_list = ["cat", "cow", "orange", "hello"]
     print(my_list)
     ["cat", "cow", "orange", "hello"]
     print(my_list[0])
     >>> cat 
     my_list[0] = "dog"
     print(my_list)
     ["dog", "cow", "orange", "hello"]
     print(my_list[0])
     >>> dog 
     my_list.append("Honda")
     print(my_list)
     [ "cat", "cow", "orange", "hello", "Honda"]
     append() -- append will add an element at end of the list, always take constant time O(1)
     **Why append() will take constant time ?**
      
    
4. control statements 

5. Strings 

6. Data structures 

7. Searching and Sorting 

8. Trees 

9. 



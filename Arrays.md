
 In python arrays and lists are same - what is that means ? array have inbuilt functions for adding, 
 deleting and insert at position (like java list collection) 
 
 **Arrays Inbuilt operations**

append() - Add an objects to the end of the list
extend() - Add all objects of a list to the another list
insert() - Insert an object at the defined index
remove() - Removes an object from the list
pop() - Removes and returns an object at the given index
clear() - Removes all objects from the list
index() - Returns the index of the first matched objects
count() - Returns the count of number of objects passed as an argument
sort() - Sort objects in a list in ascending order
reverse() - Reverse the order of objects in the list
copy() - Returns a shallow copy of the list

    my_list = ["cat", "cow", "orange", "hello"]
    print(my_list))
    ["cat", "cow", "orange", "hello"]
    print(len(my_list))
    >>> 4
    print(my_list[0])
    >>> cat 
    my_list[0] = "dog"
    print(my_list)
    ["dog", "cow", "orange", "hello"]
    print(my_list[0])
    >>> dog 
    
append()- Add an object to the end of the list

    my_list.append("Honda")
    print(my_list)
    [ "cat", "cow", "orange", "hello", "Honda"]
    append() -- append will add an object at end of the list, always take constant time O(1)
    Why append() will take constant time ?
    Algo - https://en.wikipedia.org/wiki/Amortized_analysis
    It's amortized O(1), not O(1).
    Let's say the list reserved size is 8 elements and it doubles in size when space runs out. You want to push 50 elements.
    The first 8 elements push in O(1). The nineth triggers reallocation and 8 copies, followed by an O(1) push. The next 
    7 push in O(1). The seventeenth triggers reallocation and 16 copies, followed by an O(1) push. The next 15 push in O(1).
    The thirty-third triggers reallocation and 32 copies, followed by an O(1) push. The next 17 push in O(1).
    So all of the pushes have O(1) complexity, we had 56 copies at O(1), and 3 reallocations at O(n), with n = 8, 16, and
    32. Note that this is a geometric series and asymptotically equals O(n) with n = the final size of the list. That 
    means the whole operation of pushing n objects onto the list is O(n). If we amortize that per element, it's O(n)/n = O(1).
    
extend() - Add all object of a list to the another list

    my_list = ["cat", "cow", "orange", "hello"]
    new_list.extend(my_lsit)
    print(new_list)
    >>> ["cat", "cow", "orange", "hello"]
    new_list1 = ["mac", "windows"]
    new_list1.extends(my_list)
    print(new_list1)
    >>> ["mac", "windows", "cat", "cow", "orange", "hello"]
    Time Complexity for extend O(k) where k is the number of object in list, always new list is added 
    at the end of the list.
    
insert() - Insert an object at the defined index
    
    insert(index, object) index --> position where to insert
    my_list.insert(1, "apple")
    print(my_list)
    >>> ["cat", "apple", "orange", "hello"]
    Time Complexity for insert is O(n) all the object are reshuffled 

remove() - Removes an item from the list
    
    remove(object) removes frist occurance of an object, if object is not present Raises ValueError if 
    the value is not present.
    my_list.remove("apple")
    print (my_list)
    >>> ["cat", "orange", "hello"]
    Time Complexity for remove is O(n)
    my_list.remove("apple")
    >>> valueError: list.remove(x): x not in list
    
pop() - Removes and returns an object at the at the end of list

    pop() removes last object in the list, Raises IndexError if list is empty or index is out of range
    print (my_list)
    >>> ["cat", "orange", "hello"]
    print(my_list.pop())
    >>> hello
    print (my_list)
    >>>["cat", "orange"]
    
clear() - Removes all objects from the list
   
    clear() removes all objests from the list  
    print (my_list)
    >>>["cat", "orange"]
    my_list.clear()
    print(my_list)
    >>> [] --> returns empty list 

index() - Returns the index of the first matched objects
    
     index() L.index(value, [start, [stop]]) -> integer -- return first index of value.
     returns index of an object 
     my_list = ["cat", "orange"]
     print(my_list.index("orange"))
     >>> 1
     Time complexity is O(k) where k is the index of an element 
     
count() - Returns the count of number of objects passed as an argument 
     
     count() returns number of time object in the list. 
     print(my_list.count("cat"))
     >>> 1
     Time complexity is O(n) 
     
sort() - Sort objects in a list in ascending order

     sort() -- time compelxity for a O(n log n)
     https://en.wikipedia.org/wiki/Timsort
     my_list = [5,3,4,1,2]
     my_list.sort()
     print(my_list)
     >>> [1, 2, 3, 4, 5]

reverse() - Reverse the order of objects in the list

    reverse() - reverse objects in the list 
     my_list.reverse()
     print(my_list)
     >>> [5, 4, 3, 2, 1]
     
copy() - Returns a shallow copy of the list
   
    A shallow copy means constructing a new collection object and then populating it with references to the child objects 
    found in the original. The copying process does not recurse and therefore won’t create copies of the child 
    objects themselves. In case of shallow copy, a reference of object is copied in other object. It means that any 
    changes made to a copy of object do reflect in the original object. In python, this is implemented using “copy()” 
    function.
    <img width="501" alt="screen shot 2019-02-09 at 12 32 17 pm" src="https://user-images.githubusercontent.com/11428274/52526069-49ecfe00-2c68-11e9-8bab-460d383b72cf.png">
   
     

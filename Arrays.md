
 In python arrays and lists are same - what is that means ? array have inbuilt functions for adding, 
 deleting and insert at position (like java list collection) 
 
 **Arrays Inbuilt operations**

append() - Add an element to the end of the list
extend() - Add all elements of a list to the another list
insert() - Insert an item at the defined index
remove() - Removes an item from the list
pop() - Removes and returns an element at the given index
clear() - Removes all items from the list
index() - Returns the index of the first matched item
count() - Returns the count of number of items passed as an argument
sort() - Sort items in a list in ascending order
reverse() - Reverse the order of items in the list
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
    
append()

    my_list.append("Honda")
    print(my_list)
    [ "cat", "cow", "orange", "hello", "Honda"]
    append() -- append will add an element at end of the list, always take constant time O(1)
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
    
extend()

    my_list = ["cat", "cow", "orange", "hello"]
    new_list.extend(my_lsit)
    print(new_list)
    >>> ["cat", "cow", "orange", "hello"]
    new_list1 = ["mac", "windows"]
    new_list1.extends(my_list)
    print(new_list1)
    >>> ["mac", "windows", "cat", "cow", "orange", "hello"]
    Time Complexity for extend O(k) where k is the number of elements in list, always new list is added at the end of the list.
    
insert()
    
    insert(index, object) index --> position where to insert
    my_list.insert(1, "apple")
    print(new_list)
    >>> ["cat", "apple", "orange", "hello"]
    Time Complexity for insert is O(n) all the elements are reshuffled 

remove()
    
    remove(object) removes frist occurance of an element, if element is not present Raises ValueError if 
    the value is not present.
    my_list.remove("apple")
    print (my_list)
    >>> ["cat", "orange", "hello"]
    Time Complexity for remove is O(n)

      
    

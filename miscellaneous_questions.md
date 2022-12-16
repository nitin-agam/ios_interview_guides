# Miscellaneous Questions & Answers

### Question: What is a named tuple?

In a tuple, we can provide names for each value. Using names, we can access the values by their names instead of an index. 

Named tuples eliminate the need to remember indexes. For example,

```swift
let tupleWithoutNames = ("Simon", "New York City", 24)

// Access the name
print(tupleWithoutNames.0) // print "Simon"


let tupleWithNames = (name: "Simon", city: "New York City", age: 24)

// Access the name
print(tupleWithNames.name) // print "Simon"
```

<br>
### Question: What is the difference between classes and structs?

- The difference between a class and a struct is whether it's a reference or a value. If you need to store some primitive data types (i.e. ​Ints, ​Floats​, ​Strings, etc.), use a ​struct​. 
- However, if you need custom behavior where passing by reference is preferred so that you refer to the same instance everywhere, use a class.
- The other difference is that a ​class ​supports inheritance, while a struct doesn’t.

Note: Basically in Swift, a ​struct ​is preferred over a ​class.

<br>
### Question: What is the difference between static and class functions?

- A static function can be associated with a type like a struct, class, or enum, while a class function is associated with a class type only.
- Class functions can be overridden by subclasses, while static functions cannot be overridden.
- Class functions can access the self properties of the class, which is not possible for static functions.


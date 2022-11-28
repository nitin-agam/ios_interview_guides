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

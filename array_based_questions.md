# Array Related Questions & Answers

### Question: What is the difference between Array and NSArray/NSMutableArray?

1. Array is a struct, therefore it is a value type in Swift. NSArray is an immutable Objective C class, therefore it is a reference type in Swift.
2. An array can store one type of data, whereas NSArray can hold different types of data.

In the below examples, we will try to modify the array which are mutable in both the cases. 

```swift
import Foundation

var languagesArray = ["Swift", "Objective-C", "Java", "Python"]

func modifyArray1(array: [String]) {
    var inputArray = array
    inputArray[2] = "C++"
}

modifyArray1(array: languagesArray)

print(languagesArray)
// ["Swift", "Objective-C", "Java", "Python"]
// Note: Original array `languagesArray` has not changed.


var languagesMutableArray: NSMutableArray = ["Swift", "Objective-C", "Java", "Python"]

func modifyArray2(array: NSMutableArray) {
    array[2] = "C++"
}

modifyArray2(array: languagesMutableArray)

print(languagesMutableArray)
/*
(
    Swift,
    "Objective-C",
    "C++",
    Python
)

// Note: Original array `languagesMutableArray` has been changed.
*/
```

 







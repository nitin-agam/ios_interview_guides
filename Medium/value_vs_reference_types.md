**Question**

## Describe the differences between a reference type and a value type in Swift. How to choose between them?

<br>

Swift types can be divided into two categories: value and reference types. The key difference between the two is how they are stored and passed around in memory.

Understanding the difference between value types and reference types is important for writing efficient and correct code in Swift. When deciding which type to use, consider factors like memory usage, performance, and mutability requirements.

**Values Types**

A value type is a type that is stored directly in memory where the variable is defined. When you create a new instance of a value type, a new copy of the data is created and stored in a new location in memory. Examples of value types in Swift include basic data types like Int, Float, Bool, and String, as well as more complex types like structs and enums.

**Reference Types**

A reference type is a type that is stored in memory separately from where the variable is defined. When you create a new instance of a reference type, a new reference to the same memory location is created, rather than a new copy of the data. Examples of reference types in Swift include classes and closures.

### Here are some difference between both:

**Memory management**

Value types are managed by the compiler and automatically destroyed when they go out of scope, while reference types require manual memory management using techniques like reference counting.

**Copying behavior**

Value types are copied by value, meaning that when you pass a value type to a function or assign it to a new variable, a new copy of the data is created. Reference types are copied by reference, meaning that when you pass a reference type to a function or assign it to a new variable, a new reference to the same memory location is created.

**Immutability**

Value types are often immutable, meaning that their values cannot be changed after they are created. Reference types can be mutable or immutable.

### How to choose?

**Use a value type when:**

* Comparing instance data with == makes sense
* You want copies to have independent state
* The data will be used in code across multiple threads

**Use a reference type when:**

* Comparing instance identity with === makes sense
* You want to create a shared, mutable state

# Optional Based Questions & Answers

### Question: What is optional in Swift?

An optional type acts as a container with either a wrapped value or nil. 

By syntax, an optional is an enum with two cases, .some storing a wrapped value and .none storing nil.


<br>
### Question: What is optional binding in Swift?

Optional binding is a way to bind the wrapped value of an optional variable to a new variable. You can use the if-let, and guard-let statements to unwrap the value.

```swift
var nameString: String?

// Here, we are conditionally binding the wrapped value to a new variable called name.
if let name = nameString {
    print("Name is '\(name)'")
} else {
    print("Name not found")
}
```

<br>
### Question: What is optional chaining in Swift?

The answer to be added soon.


<br>
### Question: What is the Nil-Coalescing operator in Swift?

The nil-coalescing operator (??) is a shorthand way in Swift to unwrap an optional variable and provide a default value if the variable is "nil". The operator compares the value on the left to "nil", and if it is "nil", it returns the value on the right.

The basic syntax for the nil-coalescing operator is:

optionalVariable ?? defaultValue

For example, you have an optional variable myOptionalInt: Int? and you want to use the value of this variable, but you want to provide a default value of 0 if the variable is "nil":

let myInt = myOptionalInt ?? 0

In this case, if myOptionalInt has a value, myInt will be assigned that value, otherwise myInt will be assigned 0.

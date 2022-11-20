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

The answer to be added soon.

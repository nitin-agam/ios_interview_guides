# Hey, iOS Developers 🧑‍💻👩‍💻

Our life is incomplete without interview practice. It is very important for us to practice interview questions regularly. 

It has been requested by many iOS developers to share the list of interview questions so they can prepare for their interviews. There will never be an end to this list. 

In order to provide you with important interview questions that you can access at any time, I have created this open-source repository. 

If you like my work, don't forget to click ⭐️ button and share it with your friends !!

<br>

> Note: You will get this list to be updated time to time by adding more questions and answers.

<br>
## Property Related Questions & Answers

### Question: What is a lazy property in Swift?

A lazy property is a stored property whose initial value isn’t calculated until the first time it’s used. You indicate a lazy stored property by writing the lazy modifier before its declaration. This could be a great way to optimize your code to prevent doing any unnecessary work.

```swift
class LoginController: UIViewController {
    
    lazy var alertView: UIView = {
        let view = UIView()
        // Configuration of alert in accordance with requirement
        return view
    }()
    
    override func viewDidLoad() {
        super.viewDidLoad()
    }
    
    private func loginButtonClicked() {
        // here we need to show an alert
    }
}
```
Why did we define `alertView` as lazy? Because we know that `alertView` will be needed when the login button is clicked. Before that, it might not even have been in use. 

<br>
### Question: Why should a lazy property be a variable in Swift?

You must always declare a lazy property as a variable (with the var keyword), because its initial value might not be retrieved until after instance initialization completes. Constant properties must always have a value before initialization completes, and therefore can’t be declared lazy.

```swift
lazy let alertView: UIView = {
    let view = UIView()
    // configuration of alert as per requirement
    return view
}()
```
Once you make a lazy property as a constant, you will get an error like below:

```swift
error: 'lazy' cannot be used on a let
```



<br>
### Question: What are the advantages of lazy stored properties?

There are a few advantages of using lazy property instead of stored property:

1. The statements in the closure of the lazy property execute only if you read the property. 
2. If you never read a lazy property, you can avoid unnecessary allocations and computations. 
3. You can access stored property inside the lazy property. 


<br>
### Question: What is the difference between a computed and a lazy stored property?

- Computed property would be recalculated every time while lazy property is calculated once.

Let's understand this with an example.

```swift

struct Student {
    let name: String
    let score: Double
}

struct StudentViewModel {
    
    var students: [Student]
    
    lazy var topperByLazy: Student? = {
        print("calculating topper by lazy property")
        return students.max(by: { $0.score < $1.score } )
    }()
    
    var topperByComputed: Student? {
        print("calculating topper by computed property")
        return students.max(by: { $0.score < $1.score } )
    }
    
    init(studentArray: [Student]) {
        self.students = studentArray
    }
}

var viewModel = StudentViewModel(studentArray: [Student(name: "Charlie", score: 7.9),
                                                Student(name: "Josh", score: 8.5),
                                                Student(name: "Alex", score: 9.1),
                                                Student(name: "Tina", score: 9.0)])

let _ = viewModel.topperByLazy
let _ = viewModel.topperByLazy
let _ = viewModel.topperByComputed
let _ = viewModel.topperByComputed

```

Ouput:

```swift
calculating topper by lazy property
calculating topper by computed property
calculating topper by computed property
```

- As we know, lazy properties are called once. Sometimes it may return a wrong value in case of data changes as you can see in the below example:

```swift
print("Top score: \(viewModel.topperByLazy?.score ?? 0.0)")
// calculating topper by lazy property
// Top score: 9.1

viewModel.students.append(Student(name: "Elena", score: 9.5))

print("Top score: \(viewModel.topperByLazy?.score ?? 0.0)")
// Top score: 9.1 // Wrong score, it should be 9.5
```
If this is the case, computed property will give you the correct result.

 
<br><br>

### Want to contribute?

- You can request more questions and answers on specific topics by creating an issue. I'll try to add them as soon as I can.
- If you find a typo or an incorrect answer, please create an issue. I would be happy to fix them.
- Raise a pull request with your questions and answers if you want to contribute. 



<br><br>
### ***Let's make this list bigger to help other.***




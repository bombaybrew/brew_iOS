---
title: "Minimal Swift"
date: 2020-02-08
weight: 20
draft: true
---

# Minimal Swift
---
Status: WIP

To make beautiful, peformant iOS apps we need to master Swift programming language.
In this chapter we are going to focus on minimal swift to get us started.

If you have been using swift before feel free to skip this one.

### Print
```swift
print("Ok Computer")
// Prints "Ok Computer"
```

### Variable
```swift
var myVariable = 42
myVariable = 50
```

### Constant
```swift
let myConstant = 42

let implicitDouble = 70.0
let explicitDouble: Double = 70

let apples = 3
let appleSummary = "I have \(apples) apples."
```
### Function
```swift
func greet(person: String, day: String) -> String {
    return "Hello \(person), today is \(day)."
}

greet(person: "Bob", day: "Tuesday")

// prints "Hello Bob, today is Tuesday."
```

### Class
```swift
class Shape {
    var numberOfSides = 0
    func simpleDescription() -> String {
        return "A shape with \(numberOfSides) sides."
    }
}
```


## References
https://docs.swift.org/swift-book/GuidedTour/GuidedTour.html
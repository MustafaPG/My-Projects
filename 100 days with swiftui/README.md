# My Solutions to CheckPoints

## Day 1
No CheckPoint!

## Day 2

### Question
1. Creates a constant holding any temperature in Celsius.
2. Converts it to Fahrenheit by multiplying by 9, dividing by 5, then adding 32.
3. Prints the result for the user, showing both the Celsius and Fahrenheit values.

### My Solution

```swift
let celsius: Double = 44.2
let fahrenheit = (celsiusTemperature * 9 / 5) + 32

print("Temperature in Celsius: \(celsius)°C")
print("Temperature in Fahrenheit: \(fahrenheit)°F")
```
## Day 3
No CheckPoint!

## Day 4

### Question
1. You should start by creating an array of strings, using something like let albums = ["Red", "Fearless"]
2. You can read the number of items in your array using albums.count.
3. count also exists for sets.
4. Sets can be made from arrays using Set(someArray)
5. Sets never include duplicates.


### My Solution

```swift
let names : [String] = ["ali" , "mohammed" , "omar" , "Amer" , "ali"]
print("The namse = " , names.count)
let filterNames = Set(names)
print("The unique Names = " , filterNames)
```

## Day 5
No CheckPoint!

## Day 6

### Question
1. If it’s a multiple of 3, print “Fizz”
2. If it’s a multiple of 5, print “Buzz”
3. If it’s a multiple of 3 and 5, print “FizzBuzz”
4. Otherwise, just print the number.


### My Solution

```swift
for i in 1...100{
    if i.isMultiple(of: 3) && i.isMultiple(of: 5) {
        print(i , "FizzBuzz")
    }
    else if i.isMultiple(of: 3){
        print(i , "Fizz")
    }else if i.isMultiple(of: 5) {
        print(i , "Buzz")
    }else{
        print(i)
    }
}
```

## Day 7

### Question
# do two strings contain the same letters, regardless of their order? This function should accept two string parameters, and return true if their letters are the same so, “abc” and “cab” should return true because they both contain one “a”, one “b”, and one “c”.


### My Solution

```swift
func FindTheSame(a: String , b: String) -> Bool{

    var first = a.sorted()
    var secund = b.sorted()

    if first == secund{
        return true
    }else{
        return false
    }
    
}

print(FindTheSame(a: "Ahmed", b: "Ahedm"))
```

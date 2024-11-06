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
1. do two strings contain the same letters, regardless of their order? This function should accept two string parameters, and return true if their letters are the same so, “abc” and “cab” should return true because they both contain one “a”, one “b”, and one “c”.


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

## Day 8

### Question
1. The challenge is this: write a function that accepts an integer from 1 through 10,000, and returns the integer square root of that number. That sounds easy, but there are some catches:

2. You can’t use Swift’s built-in sqrt() function or similar – you need to find the square root yourself.
3. If the number is less than 1 or greater than 10,000 you should throw an “out of bounds” error.
4. You should only consider integer square roots – don’t worry about the square root of 3 being 1.732, for example.
5. If you can’t find the square root, throw a “no root” error.



### My Solution

```swift
enum error : Error {
    case LessThanOne
    case MoreThanThosnd
    case NoSQRT
}

func FindSQRT(num: Int) throws -> Int{
    if num <= 1 {
        throw error.LessThanOne
    }else if num >= 10000 {
        throw error.MoreThanThosnd
    }else{
        for i in 1..<num{
            if i * i == num {
                return i
            }
        }
    }
    throw error.NoSQRT
}
do{
    try print(FindSQRT(num: 900))
    
}catch error.NoSQRT{
    print("No Root")
}catch error.LessThanOne{
    print("out of bounds")
}catch error.MoreThanThosnd{
    print("out of bounds")
}
```

## Day 9

### Question
1. Your input is this:
let luckyNumbers = [7, 4, 38, 21, 16, 15, 12, 33, 31, 49]
Your job is to:
2. Filter out any numbers that are even
3. Sort the array in ascending order
4. Map them to strings in the format "7 is a lucky number"
5. Print the resulting array, one item per line


### My Solution

```swift
let luckyNumbers = [7, 4, 38, 21, 16, 15, 12, 33, 31, 49]

let Even = luckyNumbers.filter{$0 % 2 == 0}

let NotEven = luckyNumbers.filter{$0 % 2 == 1}

let EvenSorted = Even.sorted()

let LuckyNumbers = NotEven.map{ "\($0)  is a Lucky number" }

let PrintItemsOnePerLine = {( Numbers :[String]) in
    for i in Numbers{
        print(i)
    }

}

PrintItemsOnePerLine(LuckyNumbers)
```
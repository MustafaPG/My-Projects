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


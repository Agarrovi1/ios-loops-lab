# Loops Lab

## Instructions for lab submission

1. Fork the assignment repo
1. Clone your Fork to your machine
1. Complete the lab
1. Push your changes to your Fork
1. Submit a Pull Request back to the assignment repo
1. Paste a link to of your Fork on Canvas and submit


## Question 1

Write code that prints all the numbers from 1 to 150, **inclusive.**

var range = 1...150
for i in range {
print(i)
}

***
## Question 2

Write code that prints all the numbers from 142 to 159, **exclusive.**

var secondRange = 142..<159
for i in secondRange where i > 142 {
print(i)
}

***
## Question 3

Write code that prints only the even numbers from 15 to 80, **inclusive.**

var range = 15...80
for a in range where a % 2 == 0 {
print(a)
}


***
## Question 4

Write code that prints only the odd numbers from 19 to 51, **inclusive.**

var aRange = 19...51
for b in aRange where b % 2 != 0 {
print(b)
}

***
## Question 5

Write code that prints all the numbers that end in a **5** from 1 to 100, **exclusive.**

var range5 = 1...100
for j in range5 where j % 5 == 0 && j % 10 != 0 {
print(j)
}

***
## Question 6

Write code that prints all the numbers that end in a 7 from 1 to 40, **inclusive.**

var range6 = 1...40
for seven in range6 {
if seven % 5 == 0 && seven % 10 != 0 {
print(seven + 2)
}
}

***
## Question 7

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 3`
var range7 = 20...150
for three in range7 where three % 3 == 0 {
print(three)
}

***
## Question 8

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that are divisible by 2 and 3`

var range8 = 20...150
for twoAndThree in range8 where twoAndThree % 2 == 0 && twoAndThree % 3 == 0 {
print(twoAndThree)
}

***
## Question 9

Given a range of numbers from 20 to 150 inclusive, print out all the numbers that follows these conditions:

`Numbers that end with a 4`

var range9 = 20...150
for four in range9 where four % 10 == 0 && four != 150 {
print(four + 4)
}

***
## Question 10

Given a range of numbers from 20 to 150, print out all the numbers that follows these conditions:

`Print out numbers: 31, 35, 40 to 60.`

var range10 = 20...150
for specific in range10 {
if specific == 31 || specific == 35 || specific >= 40 && specific <= 60 {
print(specific)
}
}

***
## Question 11

Without using Xcode, how many times will the loop below run?  Explain why.

```swift
var i = 5

while (i > 3) {
    i += 1
}

// Your explanation here
This loop will not run because the variable i is not in the i > 3 range
```

***
## Question 12

Change the code below to make the loop stop executing when i reaches 9.

```swift
var i = 5

while (i <= 9)  {
    i += 1
}
```

***
## Question 13

Change the code below to make the loop stop executing after it has run 1,000 times.

```swift
var i = 5

while (i < 1005) {
    i += 1
}
```

***
## Question 14

Change the code below to make the loop stop executing after it has run 1,000 times and also make it print out the current value of i **only if i is an even number.**

```swift
var i = 5

while (i < 1005) {
if i % 2 == 0 {
print(i)
}
i += 1
}
```

***
## Question 15

What's the difference in syntax between the following two while loops?  Will their outputs be different?  Explain why or why not.

```swift
var i = 1
//loop one
while i <= 10 {
    print("i = \(i)")
    i += 1
}

//loop two
var i = 1

repeat {
    print("i = \(i)")
    i += 1
} while i <= 10

//The two loops gives the same output because they are both loops with the same conditions so they'll start at one and end at ten. And they have the same increments.
```

***
## Question 16

What's the difference between `break` and `continue`?  Give an example that demonstrates their differences.

continues loop until conditions are met then does rest of code and break will stop the loop
Example:
var lives = 5
var points = 50

while lives > 0 {
if points == 50 {
print("yay")
break
}
if lives > 3 {
points += 30
}
print("you were hit! -1")
lives -= 1
points += 5
}

***
## Question 17

Without using Xcode, what will the loop below print? Select all that apply.

```swift
for i in 1...10 {
    if (i >= 4 && i <= 7){
        continue
    }
    print(i)
}
```
It'll print the following:
[]1
[]2
[]3
[]8
[]9
[]10

***
## Question 18

Without using Xcode, what will the loop below print? Select all that apply.

```swift
for i in 1...10 {
    if (i >= 4 && i <= 7){
        break
    }
    print(i)
}
```

[]1
[]2
[]3

***
## Question 19

Without using Xcode, what will the loop below print?  Explain below.

```swift
outerloop: for x in 1...3 {
    innerloop: for y in 1...3 {
        if y == 2{
            continue outerloop
        }
        print("x = \(x), y = \(y)")
    }
}
```
x = 1, y = 1

x = 2, y = 1

x = 3, y = 1
when y == 2 it'll skip y = 2 and y = 3 steps and continue outer loop 
***
## Question 20

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** x and y are both integers.

for x in 0...10 {
for y in 0...10 {
print("\(x),\(y)")
}
}

***
## Question 21

Write code that prints out all the points in the area bounded by (0,0), (10,0), (0,10) and (10,10) **where** the difference of x and y is at least 5, and x and y are both integers.

for x in 0...10 {
for y in 0...10 where x - y >= 5 {
print("\(x),\(y)")
}
}

***
## Question 22

Print the first `N` square numbers. A **square number**, also called perfect square, is an integer that is obtained by squaring some other integer; in other words, it is the product of some integer with itself (ex. 1 = 1*1, 4 = 2 * 2, 9 = 3* 3 …).

Example:
Input: `var N = 5`

Output:
```swift
1
4
9
16
25

N = 1
while n < 6 {
print(n * n)
n += 1
}
```

***
## Question 23

Given an integer N draw a square of N x N asterisks. Look at the examples.

Example 1:
Input: `var N = 2`

Output:
```swift
**
**
```

Example 2:
Input: `var N = 3`

Output:
```swift
***
***
***
```

Hint 1
Try printing a single line of * first.

Hint 2
You can use print("") to print an empty line.

for x in 1...n {
for y in 1...n {
print("*", separator: "", terminator: " ")
}
print("")
}
***

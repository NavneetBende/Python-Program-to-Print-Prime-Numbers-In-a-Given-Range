Python Program to Print Prime Numbers In a Given Range
Find the Prime Numbers in a Given Range in Python
Given two integer as Limits, low and high, the objective is to write a code to in Python Find Prime Numbers in a Given Range in Python Language. To do so we’ll use nested loops to check for the Prime while Iterating through the range.
Example
Input : low = 2 , high = 10
Output : 2 3 5 7
Find the Prime Numbers in a Given Interval in Python
Given two integer variables for range, the objective is to check for all the prime number that lay in the given interval. The two input integers will act as the interval limits low and high. In order to check which iterating, we’ll use nested loops. The outer loop will iterate through the numbers while the inner loop will check for Prime. Here are some of the methods used to solve the above mentioned problem in python language

Method 1: Using inner loop Range as [2, number-1].
Method 2: Using inner loop Range as [2, number/2].
Method 3: Using inner loop Range as [2, sqrt(number)].
Method 4: Using inner loop Range as [3, sqrt(number), 2].
We’ll discuss the above mentioned methods in the upcoming sections below. Check out Python Program to check for Prime. Check out the definition in the blue box below.

Prime Numbers
A prime number is a natural number greater than 1 that is not a product of two smaller natural numbers. A natural number greater than 1 that is not prime is called a composite number. For example, 5 is prime because the only ways of writing it as a product, 1 × 5 or 5 × 1, involve 5 itself.

Related Pages
Leap year

Prime Number

Sum of Digits of a number

Reverse of a number

Palindrome number

Method 1: Using inner loop Range as [2, number-1]
Working
For two integer inputs as low and high limits of the interval,

Run a for loop to iterate through all the numbers.
Run a Nested for loop to check for prime or not.
Let’s implement the above logic in Python Language.

Python Code
Run
# python find prime numbers in range 
low, high = 2, 10
primes = []

for i in range(low, high + 1):
    flag = 0

    if i < 2:
        continue
    if i == 2:
        primes.append(2)
        continue

    for x in range(2, i):
        if i % x == 0:
            flag = 1
            break

    if flag == 0:
        primes.append(i)
        
print(primes)
Output
[2, 3, 5, 7]
Method 2: Using inner loop Range as [2, number/2]
Working
For two integer inputs as limits, we perform the following main operations,

Run a for loop to iterate through the numbers in a given interval.
Run a nested while to check for prime by checking if the number has any other factors in the range [2, number/2].
Let’s implement the above logic in Python Language.

Python Code
Run
low, high = 2, 10
primes = [2]

for num in range(low, high + 1):
    flag = 0
    if num < 2:
        flag = 1
        
    if num % 2 == 0:
        continue
    iter = 2

    while iter < int(num / 2):
        if num % iter == 0:
            flag = 1
            break
        iter += 1

    if flag == 0:
        primes.append(num)

print(primes)
Output
[2, 3, 5, 7]
Method 3: Using inner loop Range as [2, sqrt(number)]
Working
For two integer inputs as low and high limits of the interval, we perform the following

Run a for loop to iterate through the number in the given interval.
Run a nested while loop to check for prime or not.
We do so by checking if the number has any factors in the range [2, sqrt(number)].
Let’s implement the above logic in Python Language.

Python Code
Run
low, high = 2, 10
primes = [2, 3]

for num in range(low, high + 1):
    flag = 0
    
    if num < 2:
        flag = 1
        
    if num % 2 == 0:
        continue
        
    if num % 3 == 0:
        continue
        
    iter = 2
    while iter < int(pow(num, 0.5)):
        if num % iter == 0:
            flag = 1
            break
        iter += 1
        
    if flag == 0:
        primes.append(num)

print(primes)
Output
[2, 3, 5, 7]
Method 4: Using inner loop Range as [3, sqrt(number), 2]
Working
This method is similar to the one above but here we’ll use 2 as a step to skip the even numbers.

For a given interval as [low, high], we do the following

Run a for loop to iterate through the numbers that lay in the input interval.
Run a nest while eith step size as 2 from 3 to the square root of number and check for factors of the number in that interval.
Let’s implement the above logic in Python Language.

Python Code
Run
low, high = 2, 10
primes = [2, 3]

for num in range(low, high + 1):
    flag = 0
    if num < 2:
        flag = 1

    if num % 2 == 0:
        continue
        
    if num % 3 == 0:
        continue

    iter = 3

    while iter < int(pow(num, 0.5)):
        if num % iter == 0:
            flag = 1
            break
        iter += 2

    if flag == 0:
        primes.append(num)

print(primes)
Output
[2, 3, 5, 7]

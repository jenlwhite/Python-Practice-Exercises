# Python-Practice-Exercises
I am using this repository to save code that I write to practice as I learn Python.

### Exercise 1
#### Instructions: Create a program that asks the user to enter their name and their age. Print out a message addressed to them that tells them the year that they will turn 100 years old.

name = input('What is your name?')
age = int(input('How old are you?'))
currentyear = 2021
yearforage100 = currentyear - age + 100
print(name + ', you will be 100 years old in the year ' + str(yearforage100) + '.')



### Exercise 2
#### Instructions: Ask the user for a number. Depending on whether the number is even or odd, print out an appropriate message to the user. Hint: how does an even / odd number react differently when divided by 2?
#### Extras: If the number is a multiple of 4, print out a different message. Ask the user for two numbers: one number to check (call it num) and one number to divide by (check). If check divides evenly into num, tell that to the user. If not, print a different appropriate message.

number = int(input('Choose an integer.'))
if number%4==0:
    print(str(number) + ' is even and divisible by 4.')    
elif number%2==0:
    print(str(number) + ' is even.') 
else:
    print(str(number) + ' is odd.')
    
num = int(input('Choose a dividend.'))
check = int(input('Choose a divisor.'))
if num%check==0:
    print(str(check) + ' is a factor of ' + str(num) + '.')
else:
    print(str(num) + ' is not a multiple of ' + str(check) + '.')    
    
    

### Exercise 3
#### Instructions: Take a list, say for example this one: a = [1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89] and write a program that prints out all the elements of the list that are less than 5.
#### Extras: Instead of printing the elements one by one, make a new list that has all the elements less than 5 from this list in it and print out this new list. Write this in one line of Python. Ask the user for a number and return a list that contains only elements from the original list a that are smaller than that number given by the user.

a = [1,1,2,3,5,8,13,21,34,55,89]
a.sort()

i=0
while (a[i] < 5):
        print(a[i])
        i=i+1
    
    
b = []

i=0

while (a[i] < 5):
        b.append(a[i])
        i=i+1
        
b


maximum = int(input('Provide a maximum value to see all elements less than the stated maximum.'))

c=[]

i=0
while (a[i]< maximum):
    c.append(a[i])
    i=i+1
    
c



### Exercise 4
#### Instructions: Create a program that asks the user for a number and then prints out a list of all the divisors of that number. (If you don’t know what a divisor is, it is a number that divides evenly into another number. For example, 13 is a divisor of 26 because 26 / 13 has no remainder.)

dividend = int(input('Provide a number to retrieve all of its divisors.'))

listofdivisors = list(range(1,dividend))
optimaldivisors = []

for divisor in listofdivisors:
    if dividend%divisor == 0:
        optimaldivisors.append(divisor)   
    
optimaldivisors



### Exercise 5
#### Instructions: Take two lists, say for example these two: a = [1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89] and b = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13] and write a program that returns a list that contains only the elements that are common between the lists (without duplicates). Make sure your program works on two lists of different sizes.
#### Extras: Randomly generate two lists to test this. Write this in one line of Python (don’t worry if you can’t figure this out at this point - we’ll get to it soon)

a = [1,1,2,3,5,8,13,21,34,55,89]
b = [1,2,3,4,5,6,7,8,9,10,11,12,12]

c = []

for number in a and b:
    if (number in a) and (number in b):
        c.append(number)
c



### Exercise 6
#### Instructions: Ask the user for a string and print out whether this string is a palindrome or not. (A palindrome is a string that reads the same forwards and backwards.)

teststring = str(input('Type a word to see if it is a palindrome.'))

length = len(teststring)

forward = teststring[0:length]
backward = teststring[length::-1]

if forward == backward:
    print(teststring + ' is a palindrome.')
else:
    print(teststring + ' is not a palindrome.')
    


### Exercise 7
#### Instructions:

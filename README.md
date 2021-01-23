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

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
#### Instructions: Let’s say I give you a list saved in a variable: a = [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]. Write one line of Python that takes this list a and makes a new list that has only the even elements of this list in it.

    a = [1,4,9,16,25,36,49,64,81,100]

    newlist = [number for number in a if number%2 == 0]



### Exercise 8
#### Instructions: Make a two-player Rock-Paper-Scissors game. (Hint: Ask for player plays (using input), compare them, print out a message of congratulations to the winner, and ask if the players want to start a new game.)

    while True:
   
        player1 = input('Player 1 Object: ')
        player2 = input('Player 2 Object: ')

        if (player1=='rock' and player2=='paper') or (player1=='scissors' and player2=='rock') or (player1=='paper' and player2=='scissors'):
            print('Player 2 wins.')
        elif (player1=='paper' and player2=='rock') or (player1=='rock' and player2=='scissors') or (player1=='scissors' and player2=='paper'):
            print('Player 1 wins.')
        elif player1==player2:
            print('Players tied.')
        else:
            print('Try again.')
        x = input('Press Enter to play again. Type Goodbye if not.')
        if x == 'Goodbye': 
            print('Thank you for visiting.')
            break



### Exercise 9
#### Instructions: Generate a random number between 1 and 9 (including 1 and 9). Ask the user to guess the number, then tell them whether they guessed too low, too high, or exactly right. (Hint: remember to use the user input lessons from the very first exercise)
#### Extras: Keep the game going until the user types “exit”. Keep track of how many guesses the user has taken, and when the game ends, print this out.

    import random

    while True:

        x = random.randint(1,9)
        userinput = int(input('Type an integer between 1 and 9.'))
        if userinput == x:
            print('You guessed the correct number!')
        elif userinput > x:
            print('You guessed a number too high.')
        elif userinput < x:
            print('You guess a number too low.')
        else:
            print('Try again.')

        userinput2 = input('Press \'Enter\' to play again, or type \'exit\' to stop.')
        if userinput2 == 'exit': 
            print('Thank you for playing.')
            break



### Exercise 10
#### Instructions: This week’s exercise is going to be revisiting an old exercise (see Exercise 5), except require the solution in a different way. Take two lists, say for example these two: a = [1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89] and b = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13] and write a program that returns a list that contains only the elements that are common between the lists (without duplicates). Make sure your program works on two lists of different sizes. Write this in one line of Python using at least one list comprehension. (Hint: Remember list comprehensions from Exercise 7).

    a = [1,1,2,3,5,8,13,21,34,55,89]
    b = [1,2,3,4,5,6,7,8,9,10,11,12,13]

    c = [number for number in a and b if number in a and number in b]
    c



### Exercise 11
#### Ask the user for a number and determine whether the number is prime or not. You can (and should!) use your answer to Exercise 4 to help you.

    while True:

    usernumber = int(input('Enter an integer to see if it is prime or composite.'))
    listofdivisors = [number for number in range(2,usernumber-1) if usernumber%number == 0]
    if len(listofdivisors) != 0:
        print('The number is composite.')
    if len(listofdivisors) == 0:
        print('The number is prime.')
    x = input('Press Enter to check another integer or type \"exit\".')
    if x == "exit":
        print('Thank you for visiting.')
        break



### Exercise 12
#### Instructions: Write a program that takes a list of numbers (for example, a = [5, 10, 15, 20, 25]) and makes a new list of only the first and last elements of the given list. For practice, write this code inside a function.

    def firstandlast (list):
        newlist = [list[0],list[-1]]
        return print(newlist)



### Exercise 13
#### Instructions: Write a program that asks the user how many Fibonnaci numbers to generate and then generates them. Take this opportunity to think about how you can use functions. Make sure to ask the user to enter the number of numbers in the sequence to generate.(Hint: The Fibonnaci seqence is a sequence of numbers where the next number in the sequence is the sum of the previous two numbers in the sequence. The sequence looks like this: 1, 1, 2, 3, 5, 8, 13, …)

    def Fibfun():
    usernum = int(input('How many Fibonnaci numbers would you like to see?'))
    i=1
    if usernum == 0:
        fiblist = []
    elif usernum == 1:
        fiblist = [1]
    elif usernum == 2:
        fiblist = [1,1]
    elif usernum > 2:
        fiblist = [1,1]
        while i < (usernum-1):
            fiblist.append(fiblist[i]+fiblist[i-1])
            i += 1
    return fiblist

    Fibfun()



### Exercise 14
#### Instructions: Write a program (function!) that takes a list and returns a new list that contains all the elements of the first list minus all the duplicates.
#### Extras: Write two different functions to do this - one using a loop and constructing a list, and another using sets. Go back and do Exercise 5 using sets, and write the solution for that in a different function.

    def RemoveDupes(somelist):
        list2set = set(somelist)
        return list(list2set)
    
    
    def UniquesOnly(someotherlist):
        newlist = []
        for element in someotherlist:
            if element not in newlist:
                newlist.append(element)
        return newlist



### Exercise 15
#### Instructions: Write a program (using functions!) that asks the user for a long string containing multiple words. Print back to the user the same string, except with the words in backwards order. For example, say I type the string: 'My name is Michele'. Then I would see the string: 'Michele is name My' shown back to me.

    userinput = str(input('Type a phrase or sentence to see it printed in reverse.'))

    def backwardphrase(userinput):
        split_userinput = userinput.split()
        return " ".join(split_userinput[::-1])

    backwardphrase(userinput)



### Exercise 16
#### Instructions: Write a password generator in Python. Be creative with how you generate passwords - strong passwords have a mix of lowercase letters, uppercase letters, numbers, and symbols. The passwords should be random, generating a new password every time the user asks for a new password. Include your run-time code in a main method.
#### Extra: Ask the user how strong they want their password to be. For weak passwords, pick a word or two from a list.

    import random
    
    lower_letters = ['a','b','c','d','e','f','g','h','i','j','k','l','m','n','o','p','q','r','s','t','u','v','w','x','y','z']
    upper_letters = ['A','B','C','D','E','F','G','H','I','J','K','L','M','N','O','P','Q','R','S','T','U','V','W','X','Y','Z']
    numbers = ['0','1','2','3','4','5','6','7','8','9']
    symbols = ['!','?','.','@','#','$','&','*','(',')','{','}','_']
    all_characters = lower_letters + upper_letters + numbers + symbols
    
    length = int(input('How many characters would you like in the password?'))
    userpassword = "".join(random.sample(all_characters,length))
    print(userpassword)

### Exercise 17
#### Instructions: Use the BeautifulSoup and requests Python packages to print out a list of all the article titles on the New York Times homepage.


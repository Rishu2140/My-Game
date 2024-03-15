I have created this game using python and then I convert the logic of my game into the Javascript with the help of Internet. 
Here's my python code for the game 


import random 
import math 

lower = int(input("Enter the lower bound")) 
upper = int(input("Enter the upper bound")) 

print("You have only ",round(math.log(upper - lower + 1,2))," chances to guesss the numeber")
number = random.randint(lower, upper) 
count = 0
while count < math.log(upper - lower + 1):
    count+=1
    x = int(input("Guess the Number"))

    if x==number:
        print("Yes the number is ",number," You did it in ",count," try")         
        break
    elif x > number:
        print("You Choose to big number") 
    elif x < number:
        print("You guess too short number") 
if count > math.log(upper - lower + 1):
    print("Better luck next time")

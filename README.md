# -Rock-Paper-Scissors-Game
#Make a rock-paper-scissors game where it is the player vs the computer.
#The computer’s answer will be randomly generated, while the program will ask the user for their input.
#This project will better your understanding of while loops and if statements.

import random
option=["rock","paper","scissor"]
user_input=input("Please type rock, paper & scissor :")
comp_input=random.choice(option)

while(user_input!=""):
    while(comp_input==user_input):
        comp_input=random.choice(option)
          
    if user_input not in option:
        print("Please enter a valid input")
        user_input=input("Please type rock, paper & scissor :")
    
    print("Computer chose {} and you chose {}".format(comp_input,user_input)) 
    
    if user_input=="scissor":
        if  comp_input=="rock": 
            print("Sorry! you loose :( -- Rock crushes scissor")
        if comp_input=="paper":
            print("Congrats! you Win :) -- Scissor cuts paper")

    if user_input=="rock":
        if comp_input=="paper": 
            print("Sorry! you loose :( -- Paper covers rock")
        if comp_input=="scissor":
            print("Congrats! you Win :) -- Rock crushes scissor")  

    if user_input=="paper":
        if comp_input=="scissor": 
            print("Sorry! you loose :( -- Scissor cuts paper")
        if comp_input=="rock":
            print("Congrats! you Win :) -- Paper covers rock")
            
    print("Press enter to exit")
    user_input=input("Please type rock, paper & scissor :")
    comp_input=random.choice(option)
    

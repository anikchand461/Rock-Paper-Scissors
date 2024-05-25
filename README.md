# Rock-Paper-Scissors

import random as r

print('''
****************************************
**** WELCOME TO ROCK-PAPER-SCISSORS ****
****************************************
''')

print('''
Rock🪨 wins against Scissors✂️
Scissors✂️ win against Paper📃
Paper📃 wins against Rock🪨

for 🪨 enter 0
for 📃 enter 1
for ✂️ enter 2
''')

while True:
    try:
        l = ['🪨', '📃', '✂️']
        n = int(input("enter 0/1/2: "))

        if n > 2 or n < 0:
            print("invalid input 😐")

        else:
            print(f"Your choice : {l[n]}")

            m = r.randint(0, 2)
            print(f'Computer choice : {l[m]}')

            if n == m:
                print("Match drawn 😏")
            elif n == 2 and m == 0:
                print("You lose 😓")
            elif n == 0 and m == 2:
                print("you won 😎")
            elif n < m:
                print("You lose 😓")
            else:
                print("You won 😎")

    except:
        print("invalid input 😐")
    ask = input("Do you want to continue? (y/n) : ").lower()
    if ask!= 'y':
        break

This is a simple Snake and Ladder game typed by using Python.

Code:-


Ihave taken import random beacause we can generate random numbers between1 to 6. 

Ihave created two dictionaries and name them 
ladder &
snake

defined where the ladders are placed in the board
# ladder = {1: 38, 4: 14, 8: 30, 21:42, 28:76, 50: 67, 71: 92, 80: 99}

defined where the snakes are placed in the board
# snake = {32: 10, 34: 6, 48: 26, 62: 18, 88: 24, 95: 56, 97: 78}


I have declared position of both the players like pos1 pos2 and initiate them 0 because it starts from 0 pos.
Then i defined a fucntion called move and in() i have created a argument of pos Inside move function dice = random.randint(1,6)
and print(f"Dice:{dice}") dice = random.randint(1,6) print(f"Dice:{dice}") pos = pos + dice if pos in snake: print("Bitten by snake") pos = snake[pos] print(f"Position:{pos}")
elif pos in ladder: print("Climbed by ladder") pos = ladder[pos] print(f"Position:{pos}") else: print(f"Position:{pos}") print("\n") return pos while True: A = input("Player 1 Enter \"A\" to throw dice")
pos1 = move(pos2) if pos1 >= 100: print("Game Over!!!\n Player 1 Wins.") break B= input("Player 1 Enter \"B\" to throw dice") pos2 = move(pos2) if pos2 >= 100: print("Game Over!!!\n Player 2 Wins.")
break


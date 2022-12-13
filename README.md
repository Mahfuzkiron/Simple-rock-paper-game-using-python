# Simple-rock-paper-game-using-python

#import module

import random

#define initial value

user_win = 0
computer_win = 0
option = ['rock', 'paper', 'scissors']

# now play a while loop

while True:

    user_input = input('Type rock/paper/scissors or q to quit:')
    if user_input == 'q':
        break
    if user_input not in option:
        continue

    random_number = random.randint(0, 2)
    computer_pick = option[random_number]
    print('computer picked', computer_pick, '.')

    if user_input == 'rock' and computer_pick == 'scissors':
        print('you win!')
        user_win += 1
        continue
    elif user_input == 'paper' and computer_pick == 'rock':
        print('you win!')
        user_win += 1
        continue
    if user_input == 'rock' and computer_pick == 'scissors':
        print('you win!')
        user_win += 1
        continue
    else:
        print('you lost!')
        computer_win += 1
        
#print output

print('you won', user_win, 'times.')
print('computer won', user_win, 'times.')
print('bye')

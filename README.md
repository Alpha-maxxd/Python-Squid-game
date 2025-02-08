# Python-Squid-game

import random
import time
num1 = (10)
num2 = (100)
rnd = (random.randint(1,456))
print('Welcome to squid game..')
time.sleep(2.5)
print('We will get you your number.')
time.sleep(0.5)
print('.')
time.sleep(1)
print('.')
time.sleep(1)
print('.')
time.sleep(1)
print('.')
time.sleep(1)
print('.')
if rnd < num1:
    print('Your number is 00' + str(rnd))
elif rnd < num2:
    print('Your number is 0' + str(rnd))
else:
    print('Your number is ' + str(rnd))
time.sleep(2)    
print('LETS START THE FIRST GAME.')
                                        
ans1 = input('Wht is 69*5?')
time.sleep(2.5)
if ans1 == ('345'):
    print('Correct ans.')
else:
    print('Wrong ans u will be elimanated.')
    quit()
time.sleep(2.5)    
123 == input('Would u like to countine?    O/X')
time.sleep(2.5)
if 123 == ('O')or('o'):
    print('You choosed to countinue.')
else:
    print('You choosed to leave.')
    quit()
time.sleep(2.5)    
321 == input('Catalonia is a region of what country?')    
if 321 == ('spain')or('Spain'):
    print('Correct ans.')
else:
    print('Wrong ans u will be elimanated.')
    quit()
time.sleep(2.5)    
12 == input('Would u like to countine?    O/X')
if 12 == ('O')or('o'):
    print('You choosed to countinue.')
else:
    print('You choosed to leave.')
    quit()
time.sleep(2.5)    
ans1 = input('Where in the world was golf invented?')
if ans1 == ('scotland')or('Scotland'):
    print('Correct ans.')
else:
    print('Wrong ans u will be elimanated.')
    quit()
time.sleep(2.5)    
1234 == input('Would u like to countine?    O/X')
if 1234 == ('O')or('o'):
    print('You choosed to countinue.')
else:
    print('You choosed to leave.')
    quit()
time.sleep(2.5)    
3214 == input('What is a female dear called?')    
if 3214 == ('Doe')or('doe'):
    print('Correct ans.')
else:
    print('Wrong ans u will be elimanated.')
    quit()
time.sleep(2.5)    
412 == input('Would u like to countine?    O/X')
if 412 == ('O')or('o'):
    print('You choosed to countinue.')
else:
    print('You choosed to leave.')
    quit()
time.sleep(2)    
print('You have finished the first game,lets start the secound game.')
time.sleep(5)
#////////////////////////////////////////////////////////////////////////////////FIRST GAME DONE////////////////////////////////////////////////////////////////////////////////////
lower_bound = 1
upper_bound = 1000
max_attempts = 10

# generate the secret number
secret_number = random.randint(lower_bound, upper_bound)

# Get the user's guess
def get_guess():
    while True:
        try:
            guess = int(input(f"Guess a number between {lower_bound} and {upper_bound}: "))
            if lower_bound <= guess <= upper_bound:
                return guess
            else:
                print("Invalid input. Please enter a number within the specified range.")
        except ValueError:
            print("Invalid input. Please enter a valid number.")

# Validate guess
def check_guess(guess, secret_number):
    if guess == secret_number:
        return "Correct"
    elif guess < secret_number:
        return "Too low"
    else:
        return "Too high"

# track the number of attempts, detect if the game is over
def play_game():
    attempts = 0
    won = False

    while attempts < max_attempts:
        attempts += 1
        guess = get_guess()
        result = check_guess(guess, secret_number)

        if result == "Correct":
            print(f"You have passed the secound game.")
            won = True
            break
        else:
            print(f"{result}. Try again!")

    if not won:
        print(f"You ran out of attempts,you wll be elimaneted,the secret number was {secret_number}.")

if __name__ == "__main__":
    print("Welcome to the Number Guessing Game!")
    play_game()
time.sleep(5)
4133 == input('Would u like to countine?    O/X')
if 4133 == ('O')or('o'):
    print('You choosed to countinue.')
else:
    print('You choosed to leave.')
    quit()
#////////////////////////////////////////////////////////SECOUND GAME DONE/////////////////////////////////////////////////////////////////////////////////////////////
print('Welcome to glass bridge..')
time.sleep(2)
print('Lets start the third game.')
time.sleep(2)
st1 = input('Will you jump right or left?')
if st1 == ('left')or('Left'):
    print('Correct ans.')
else:
    print('*CRASH*')
    quit()
time.sleep(2)
st2 = input('Will you jump right or left?')
if st2 == ('right')or('Right'):
    print('Correct ans.')
else:
    print('*CRASH*')
    quit()
time.sleep(2)
st3 = input('Will you jump right or left?')
if st3 == ('right')or('Right'):
    print('Correct ans.')
else:
    print('*CRASH*')
    quit()
time.sleep(2)
st4 = input('Will you jump right or left?')
if st4 == ('left')or('Left'):
    print('Correct ans.')
else:
    print('*CRASH*')
    quit()
time.sleep(2)
st5 = input('Will you jump right or left?')
if st5 == ('right')or('Right'):
    print('Correct ans.')
else:
    print('*CRASH*')
    quit()
time.sleep(2)
st6 = input('Will you jump right or left?')
if st6 == ('left')or('Left'):
    print('Correct ans.')
else:
    print('*CRASH*')
    quit()
time.sleep(2)
st7 = input('Will you jump right or left?')
if st7 == ('left')or('Left'):
    print('Correct ans.')
else:
    print('*CRASH*')
    quit()    
print('You have passed the third game.')
#////////////////////////////////////////////////////////THIRD GAME DONE/////////////////////////////////////////////////////////////////////////////////////////////
import tkinter as tk
import random
import os

WIDTH, HEIGHT = 600, 600
BG_COLOR = "#FFCC00"
LINE_COLOR = "red"
THRESHOLD = 15

SHAPES = {
    "circle": [(300, 150), (400, 250), (350, 350), (250, 350), (200, 250)],
    "triangle": [(200, 350), (400, 350), (300, 150)],
    "star": [(300, 150), (350, 250), (450, 250), (370, 300), 
             (400, 400), (300, 350), (200, 400), (230, 300), (150, 250), (250, 250)]
}

shape_name, shape_points = random.choice(list(SHAPES.items()))

tracing = []
fail = False

root = tk.Tk()
root.title("Squid Game Cookie Challenge")
root.geometry(f"{WIDTH}x{HEIGHT}")

canvas = tk.Canvas(root, width=WIDTH, height=HEIGHT, bg=BG_COLOR)
canvas.pack()

canvas.create_polygon(shape_points, outline="black", width=3, fill="")

label = tk.Label(root, text=f"Trace the {shape_name} without going outside!", font=("Arial", 14), bg=BG_COLOR)
label.pack()

def start_trace(event):
    global tracing, fail
    tracing = [(event.x, event.y)]
    fail = False

def trace(event):
    global fail
    if fail:
        return
    
    x, y = event.x, event.y
    closest = min(shape_points, key=lambda p: (p[0] - x) ** 2 + (p[1] - y) ** 2)
    
    if abs(closest[0] - x) > THRESHOLD or abs(closest[1] - y) > THRESHOLD:
        fail = True
        label.config(text="You Broke the Cookie! Closing...", fg="red")
        root.after(2000, lambda: (root.quit(), os._exit(0)))
    elif len(tracing) > len(shape_points):
        label.config(text="You Won! Restarting IDLE...", fg="green")
        root.after(2000, lambda: (root.quit(), os.system("python")))
    else:
        tracing.append((x, y))
        canvas.create_line(tracing[-2], tracing[-1], fill=LINE_COLOR, width=3)

canvas.bind("<Button-1>", start_trace)
canvas.bind("<B1-Motion>", trace)

root.mainloop()
#////////////////////////////////////////////////////////THIRD GAME DONE/////////////////////////////////////////////////////////////////////////////////////////////
print('Congrats you have won squid game and you also won the 46.5 won')

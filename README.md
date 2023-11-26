animal quiz
def check_guess(guess, answer):
    global score
    still_guessing = True
    attempt = 0
    while still_guessing and attempt < 3:
        if guess.lower() == answer.lower():
            print("Correct Answer")
            score = score + 1
            still_guessing = False
        else:
            if attempt < 2:
                guess = input("Sorry Wrong Answer, try again")
            attempt = attempt + 1
    if attempt == 3:
        print("The Correct answer is ",answer )
    
score = 0
print("Guess the Animal")
guess1 = input("Which bear lives at the North Pole? ")
check_guess(guess1, "polar bear")
guess2 = input("Which is the fastest land animal? ")
check_guess(guess2, "Cheetah")
guess3 = input("Which is the larget animal? ")
check_guess(guess3, "Blue Whale")
print("Your Score is "+ str(score))


build functions
def add(x,y):
  return x+y
 
print(add(3,5))

caculatorfrom tkinter import * 

root=Tk()
root.title("Simple Calculator")
root.geometry("570x600+100+200")
root.resizable(False,False)
root.configure(bg="#17161b")

equation = ""

def show(value):
    global equation
    equation+=value
    label_result.config(text=equation)

def clear():
    global equation
    equation = ""
    label_result.config(text=equation)

def calculate():
    global equation
    result =""
    if equation !="":
       try:
        result= eval(equation)
       except:
        result ="error"
        equation = ""
        label_result.config(text=result)

   
label_result= Label(root,width=25,height=2,text="",font=("arial",30))
label_result.pack()

Button(root,text= "C", width=5, height=1, font=("arial",30,"bold"),bd=1,fg="#fff",bg="#3697f5",command=lambda: clear()).place(x=10,y=100)
Button(root,text= "/", width=5, height=1, font=("arial",30,"bold"),bd=1,fg="#fff",bg="#2a2d36",command=lambda: show("/")).place(x=150,y=100)
Button(root,text= "%", width=5, height=1, font=("arial",30,"bold"),bd=1,fg="#fff",bg="#2a2d36",command=lambda: show("%")).place(x=290,y=100)
Button(root,text= "*", width=5, height=1, font=("arial",30,"bold"),bd=1,fg="#fff",bg="#2a2d36",command=lambda: show("*")).place(x=430,y=100)              

Button(root,text= "7", width=5, height=1, font=("arial",30,"bold"),bd=1,fg="#fff",bg="#2a2d36",command=lambda: show("7")).place(x=10,y=200)
Button(root,text= "8", width=5, height=1, font=("arial",30,"bold"),bd=1,fg="#fff",bg="#2a2d36",command=lambda: show("8")).place(x=150,y=200)
Button(root,text= "9", width=5, height=1, font=("arial",30,"bold"),bd=1,fg="#fff",bg="#2a2d36",command=lambda: show("9")).place(x=290,y=200)
Button(root,text= "-", width=5, height=1, font=("arial",30,"bold"),bd=1,fg="#fff",bg="#2a2d36",command=lambda: show("-")).place(x=430,y=200)              

Button(root,text= "4", width=5, height=1, font=("arial",30,"bold"),bd=1,fg="#fff",bg="#2a2d36",command=lambda: show("4")).place(x=10,y=300)
Button(root,text= "5", width=5, height=1, font=("arial",30,"bold"),bd=1,fg="#fff",bg="#2a2d36",command=lambda: show("5")).place(x=150,y=300)
Button(root,text= "6", width=5, height=1, font=("arial",30,"bold"),bd=1,fg="#fff",bg="#2a2d36",command=lambda: show("6")).place(x=290,y=300)
Button(root,text= "+", width=5, height=1, font=("arial",30,"bold"),bd=1,fg="#fff",bg="#2a2d36",command=lambda: show("+")).place(x=430,y=300)              


Button(root,text= "1", width=5, height=1, font=("arial",30,"bold"),bd=1,fg="#fff",bg="#2a2d36",command=lambda: show("1")).place(x=10,y=400)
Button(root,text= "2", width=5, height=1, font=("arial",30,"bold"),bd=1,fg="#fff",bg="#2a2d36",command=lambda: show("2")).place(x=150,y=400)
Button(root,text= "3", width=5, height=1, font=("arial",30,"bold"),bd=1,fg="#fff",bg="#2a2d36",command=lambda: show("3")).place(x=290,y=400)
Button(root,text= "0", width=11, height=1, font=("arial",30,"bold"),bd=1,fg="#fff",bg="#2a2d36",command=lambda: show("0")).place(x=10,y=500)              

Button(root,text= ".", width=5, height=1, font=("arial",30,"bold"),bd=1,fg="#fff",bg="#2a2d36",command=lambda: show(".")).place(x=290,y=500)
Button(root,text= "=", width=5, height=3, font=("arial",30,"bold"),bd=1,fg="#fff",bg="#fe9037",command=lambda: calculate()).place(x=430,y=400)              

root.mainloop()

description
name = "Seyi"
city = "Lagos"
hobby = "cook" 

# David lives in Lagos and her favourite thing to do is cooking
print(name, 'lives in',city,'and her hobby is to cook')

print(f'{name} lives in {city} and her hobby is to {hobby}')


if statements
weather = "cold"

if weather  == "raining":
    print("Take your Umbrella")
else:
    print("wear your cap")

    lists
    colors = ['red','green','blue','yellow','white','black']
colors.append('purple')

colors.remove('red')


multipication table
print("The Multiplication Table")
number = int(input("Enter a Number: "))

for x in range(1,12):
  
  product = number * x
  
  print(f'{number} * {x} = {product}')


random is fun
import random
number = random.randint(1,10)

print(number)

strings
name = "Seyi"
city = "Lagos"
hobby = "cook" 

# David lives in Lagos and her favourite thing to do is cooking
print(name, 'lives in',city,'and her hobby is to cook')

print(f'{name} lives in {city} and her hobby is to {hobby}')

while loop
for x in range(1,6):
    print("I am learning Python")


roc paper scissors
import random
choices = ["Rocc", "Paper", "Scissors"]
computer = random.choice(choices)
player = False
cpu_score = 0
player_score = 0
while True:
    player = input("Rock, Paper or  Scissors?").capitalize()
    ## Conditions of Rock,Paper and Scissors
    if player == computer:
        print("Tie!")
    elif player == "Rock":
        if computer == "Paper":
            print("You lose!", computer, "covers", player)
            cpu_score+=1
        else:
            print("You win!", player, "smashes", computer)
            player_score+=1
    elif player == "Paper":
        if computer == "Scissors":
            print("You lose!", computer, "cut", player)
            cpu_score+=1
        else:
            print("You win!", player, "covers", computer)
            player_score+=1
    elif player == "Scissors":
        if computer == "Rock":
            print("You lose...", computer, "smashes", player)
            cpu_score+=1
        else:
            print("You win!", player, "cut", computer)
            player_score+=1
    elif player=='End':
        print("Final Scores:")
        print(f"CPU:{cpu_score}")
        print(f"Plaer:{player_score}")
        break


function
print("Hello World")
print("Seyi is", 10)
name = 'Seyi'
city = 'Nigeria'
print(name,"lives in",city)
print("what is your name")
name = input("Enter your name:")
print(name)
print("I like that name")
input("Tell me about yourself:")
print("OMG I like you BYE I have to go")
input("what do you say to me")


numbers
print("ADDITION SECTION")
n1 = input("Enter a number of your choice: ")
n2 = input("Enter a 2nd number: ")

n1 = int(n1)
n2 = int(n2)


print("ANSWER = ")
print(n1 + n2)

print("SUBTRACTION SECTION")
n3 = input("Enter a number of your choice: ")
n4 = input("Enter a 2nd number: ") 

print("ANSWER = ")
n3 = int(n3)
n4 = int(n4)

print(n3 - n4)
print("MULTIPLICATION SECTION")
n5 = input("Enter a number of your choice: ")
n6 = input("Enter a 2nd number: ") 

print("ANSWER = ")
n5 = int(n5)
n6 = int(n6)

print(n5 * n6)

print("DIVISION SECTION")
n7 = input("Enter a number of your choice: ")
n8 = input("Enter a 2nd number: ") 

print("ANSWER = ")
n7 = int(n7)
n8 = int(n8)


vzriables
name = 'Seyi'
age = 10
dob = '26-10-2012'

print(name)
print(age)
print(dob)

firstname = "Seyi"
middlename = "Sharon"
lastname = "Adaramola"

print(firstname,middlename,lastname)

hot_weather = True
cold_weather = False

print(hot_weather)
print(cold_weather)












import time
lives=10
stringword="Apple"
word=list("Apple".lower())
incorrectletters=[]
guess=["_"]*len(word)
winner=False
def printscore():
    print("\n\nLives: "+str(lives))
    print("Incorrect Letters: ",end="")
    for x in range(len(incorrectletters)):
        if x==len(incorrectletters)-1:
            print(incorrectletters[x],end="")
        else:
            print(incorrectletters[x],end=",")
    print("")
    for x in range(len(guess)):
        if x==len(guess)-1:
            print(guess[x],end="")
        else:
            print(guess[x],end=",")
    print("")
def ask_user():
    user=input("Guess the letter of the word to win: ").strip().lower()
    correct=False
    for x in range(len(word)):
      
        if user==word[x]:
            guess[x]=user
            correct=True
    if correct:
        print("You got one!")
    else:
        print("Oh no! that wasn't there!")
        incorrectletters.append(user)
        global lives
        lives-=1
        time.sleep(1)
def check():
    if "_" not in guess:
        global winner
        winner=True
   
while lives>0 and winner==False:
   printscore()
   ask_user()
   check()

if lives<=0:
    print("you lost the word was" +stringword)
else:
    print("Congratulations you won with "+ str(lives) + " lives left")

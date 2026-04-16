import datetime
import time


name= input("Welcome,Enter Your Name:")
presentHour=datetime.datetime.now().hour

if 5<= presentHour <=11:
   print("Good Morning,", name)
elif 11<=presentHour<=17:
   print("Good afternooon,",name)
elif 17<= presentHour <=20:
   print("Good evening,",name)
else:
   print("Good Night,",name)





print("namaste! welcome to Tiger  Chatbot")
print("you can ask me basic questins,type 'bye' to exit from the bot")



responses ={
    "hello":"hi,welcome. how can i help you?",
    "how are you":"i am very fine. thank you",
    "who are you":"i am a smart ai chatbot",
    "motivate me" : "keep going . every bug of your project ,ales you a better devloper ",
    "happy":"freat to hear that",
    "what are functions":"go and read chapter 7",
}

def getResponseBot(userQuestion):
    userQuestion = userQuestion.lower()
    for eachkey in responses:
        if eachkey in userQuestion:
            return responses[eachkey]
        
    return "i am not able to tell that yet. ill learn fast"


while True:
    userInput= input("please ask your question:")
    reply= getResponseBot(userInput)
    print("bot response:",reply)


    if "bye" in userInput.lower():
     break

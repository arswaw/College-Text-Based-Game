#College-Text-Based-Game
#=======================

#This was based on the reddit thread at http://www.reddit.com/r/explainlikeIAmA/comments/1j2zxg/explain_college_like_an_oldschool_text_adventure/

#import math, random, sys
#from random import randint
import os
#os.system("PAUSE")

#class Wipe(object):
#    def __repr__(self):
#        return '\n'*1000

#wipe = Wipe()

#from wiper import wipe

#import tkMessageBox as tkmb
#tkmb.showinfo("Alert", "Press OK  to continue")

print 'From now on, after every line. Press enter to continue.'
raw_input("")
print 'Welcome to College!'
raw_input("")
print 'Developed by Arswaw!'
raw_input("")
print 'Based on a story written by /u/saberishungry.'
raw_input("")
print 'Read the prompts and select a command from the list WITHOUT QUOTES.'
raw_input("")
print 'Well that\'s it. Have fun!'
raw_input("")

dialogue = ['look', 'equipment', 'look at note', 'get clean clothes', 'get clothes', 'exit', 'inventory', 'say fuck', 'enter classroom', 'listen', 'whisper fuck', 'punch Robbie', 'flee']
dorm1 = ['look', 'equipment', 'look at note', 'get clean clothes', 'get clothes', 'exit']
campuswords = ['inventory', 'say fuck', 'enter classroom', 'look around', 'listen', 'whisper fuck', 'exit']
punchwords = ['punch Robbie', 'flee']

def finish():
    print 'Alright! You won! Thank you for playing the game!'
    raw_input("")
    print 'I\'d like to thank /u/saberishungry for the story. Also thank you /u/FreshNeverFrozen and /u/normalcypolice for the support!'
    raw_input("")
    print 'I hope you enjoyed the game and that it was a fun few minutes.'
    raw_input("")
    print ' -Arswaw'
    exit()

def punch():
    raw_input("")
    print 'Your commands:'
    print punchwords
    punchvar = raw_input('What do you choose? ')
    if punchvar == 'punch Robbie':
        print ''
        print 'You walk over and plant a fist squarely into his upper back as a satisfyingly loud thud resounds throughout the room. He jumps in his bed, groggily yelling "What the fuck!?" as he tries to open his droopy eyes to find his attacker.'
        raw_input("")
        finish()
    if punchvar == 'flee':
        print ''
        print 'You run out of his room and into your own. You dive into your bed, sending dirty clothes flying everywhere. Just before you fall asleep, you smile to yourself, knowing that justice had been served. Robbie will probably ask about it later, but you will just feign ignorance and ask him if he was just dreaming. Serves him right.'
        raw_input("")
        finish()
    if punchvar != punchwords:
        print ''
        print 'I didn\'t quite get that. Would you kindly try again?'
        punch()
        

def campus():
    raw_input("")
    print 'Your commands:'
    print campuswords
    campusvar = raw_input('What do you choose? ')
    if campusvar == 'inventory':
        print ''
        print 'You suddenly notice that you are walking to class bare-handed. You think hard about the situation before remembering that you left the house without grabbing your bag and laptop. They\'re probably still in your room somewhere. One of the books is probably under that pile of laundry.'
        campus()
    elif campusvar == 'say fuck':
        print ''
        print 'You curse out loud at your misfortune and berate yourself for being so forgetful. This usually never happens, but you\'re totally out of it today. And every other day, it seems. Doesn\'t matter now though, since you don\'t have time to go home and retrieve your materials. '
        campus()
    elif campusvar == 'enter classroom':
        print ''
        print 'You decide that you don\'t care anymore and go into the classroom. You don\'t need your bag to take a test anyway. Luckily for you, class just started not too long ago and a few other students are still making their way in. You look around before asking the guy two seats away from you for a pencil. He stares at you blankly before half-heartedly offering you the one he was holding. You normally wouldn\'t take other people\'s stuff, but today is an exception. He takes out another pencil and goes back to scribbling notes in his binder. He\'s probably a freshman.'
        campus()
    elif campusvar == 'look around':
        print ''
        print 'You scan the room, trying to see if you see if you can find any of your friends. A few of them spot you and wave, although they look a bit surprised to see you here, for some reason. Robbie is curiously absent even though he\'s in your class and left before you did. '
        campus()
    elif campusvar == 'listen':
        print ''
        print 'The professor, droning on in his usual monotone voice, says a bunch of things that you don\'t really want to pay attention to. You tap the pencil impatiently, wondering when the TAs will pass out your exam so you can take it already. Your ears perk up when you hear the professor say the word "final", only to be shocked when he rambles on about how today is the last day of review "before the final exam tomorrow".'
        campus()
    elif campusvar == 'whisper fuck':
        print ''
        print 'You mutter under your breath, saying hateful things about Robbie and how he made you think the final was today. Robbie not only made you go to class when you didn\'t have to, but he poked holes in one of your shirts with a staple in the process. The fact that you should have remembered the date yourself is irrelevant. You hate going to class when there\'s nothing important going on.'
        campus()
    elif campusvar == 'exit':
        print ''
        print 'You get up and leave the room. You think to yourself that you should have checked on the snoring back at the house. That was probably Robbie. You realize that he thought the final was today and got ready for it in the morning, eating one of your burritos for breakfast in the process. He then decided to "help" you out with that post-it note in case you forgot about the final, even though it wasn\'t really today. He probably went back to sleep after realizing the truth, forgetting about what he did. Must\'ve been the alcohol from last night, or the result of his tiny brain. Most likely both.'
        raw_input("")
        print '.....'
        raw_input("")
        punch()
    elif campusvar != campuswords:
        print 'I didn\'t quite get that. Would you kindly try again?'
        campus()

print 'You wake up, drowsy and disoriented. An incessant and annoying beeping resonates in the background, forcing you to open your eyes. You groan slightly as you slowly rise out of bed, gently scratching your head at a non-existent itch.'
def getup():
    raw_input("")
    print 'Your commands:'
    print dorm1
    room1 = raw_input('What do you choose? ')
    print ''
    if room1 == 'look':
        print ''
        print 'The room is rather messy, with dirty clothes piled on top of your computer chair in a misshapen heap. You remember that you were supposed to do laundry two days ago, but it\'s not important right now. You swiftly grab the pile of clothes and deposit them on your bed. Your alarm clock sits on the desk next to your bed, still beeping loudly.'
        getup()
    
    elif room1 == 'equipment':
        print ''
        print 'You are wearing boxers that should have been washed two days ago and a plain, white T-shirt with a pizza stain from last night. A post-it note is stapled to your shirt.'
        getup()
    elif room1 == 'look at note':
        print ''
        print '\"Sorry bro i was in a hurry and the note didn\'t wanna stick. I ate one of your burritos cuz i forgot to buy food. Last nite was sick btw! i think ima fail the test today but wutevr we can party after!!\" -Robbie'
        getup()
    elif room1 == 'get clean clothes':
        print ''
        print 'You search for clean clothes in order to change out of your grungy boxers and note-stapled shirt. You do not find anything suitable. Figures that you would be out on a day when something important was going on.'
        getup()
    elif room1 == 'get clothes':
        print ''
        print 'You sift through a few shirts that look clean and sniff them carefully before deciding on the black one. A pair of jeans hanging off the side of the bed goes over your boxers. You should probably do your laundry soon.'
        getup()
    elif room1 == 'exit':
        print ''
        print 'You exit your room and walk into the living room, where empty cups, paper plates, and plastic utensils lie strewn about. The mess outside surprises you briefly before you remember the party that you and your roommates threw to celebrate summer vacation even though you\'re only on the second day of Finals Week. The house is quiet, although you can kind of hear snoring coming from another room.'
        raw_input("")
        print 'You decide that you don\'t have time to investigate because the final you\'re taking today is probably going to start soon, so you put on your shoes and leave the building. Fortunately, you found a good parking spot yesterday night, so you quickly find your car and drive to school'
        raw_input("")
        print '.....'
        campus()

    elif room1 != dorm1:
        print 'I didn\'t quite get that. Would you kindly try again?'
        getup()
        


getup()


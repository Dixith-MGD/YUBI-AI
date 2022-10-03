#YUBI AI Code #

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Speech recognition:
For speech recognition we are using VOSK which is open-source model for offline speech recognition system it Supports 20+ languages and dialects - English, Indian English, German, French, Spanish, Portuguese, Chinese, Russian, Turkish, Vietnamese, Italian, Dutch, Catalan, Arabic, Greek, Farsi, Filipino, Ukrainian, Kazakh, Swedish, Japanese, Esperanto, Hindi, Czech, Polish

CODE:
def Listen():

    model = Model("DataBase\\vosk-model-small-en-us-0.15")
    recognizer = KaldiRecognizer(model, 16000)

    mic = pyaudio.PyAudio()
    stream = mic.open(format=pyaudio.paInt16, channels=1, rate=16000, input=True, frames_per_buffer=8192)
    stream.start_stream()


    print("")
    print("Listening...")
    print("")

    while True:

        data = stream.read(4096)

        if recognizer.AcceptWaveform(data):
            text = recognizer.Result()
            p = text[14:-3]
            print(f"You Said : {p}")

            if len(p)>0:
                return p
            
            else:
                break
                
    
    #THIS WILL BE THE CODE FOR SPEECH RECOGNITION SYSTEM IT TAKES ABOUT 400 MB OF THE SPACE#
    
  ---------------------------------------------------------------------------------------------------------------------------------------
    
    PYTTSX3 TEXT-TO-SPEECH
    
    FOR TEXT TO SPEECH WE ARE GONNA USE PYTTSX3 LIBRARY WE CAN CHANGE IT WHEN WE HAVE A CUSTOM VOICE PACK WE CAN CHANGE OVER 250+ VOICES AND IF WE WANT YUBI TO SPEAK OTHER LANGUAGES WE NEED TO USE GOOGLE TEXT TO SPEECH FOR BETTER SOUNDING
    CODE:
    def Say(Text):
    print(   )
    engine = pyttsx3.init('sapi5')
    speaker = pyttsx3.init('sapi5') 
    rate = speaker.getProperty('rate')
    voices = engine.getProperty('voices')
    engine.setProperty('voice', voices[0].id)
    speaker.setProperty('rate', 145)
    speaker.say(Text)
    print(f"YUBI-: {Text}")
    speaker.runAndWait()
    print(   )
    """ RATE """
 ----------------------------------------------------------------------------
    GOOGLE Text to speech CODE :

# Import the required module for text 
# to speech conversion
from gtts import gTTS
  
# This module is imported so that we can 
# play the converted audio
import os
  
# The text that you want to convert to audio
mytext = 'Welcome to geeksforgeeks!'
  
# Language in which you want to convert
language = 'en'
  
# Passing the text and language to the engine, 
# here we have marked slow=False. Which tells 
# the module that the converted audio should 
# have a high speed
myobj = gTTS(text=mytext, lang=language, slow=False)
  
# Saving the converted audio in a mp3 file named
# welcome 
myobj.save("welcome.mp3")
  
# Playing the converted file
os.system("mpg321 welcome.mp3")

WE CAN USE ANY OF THIS TEXT TO SPEECH LIBRARIES

---------------------------------------------------------------------------------------------------------------------------------------

FACE RECOGNITION SYSTEM :

FOR FACE RECOGNITION SYSTEM WE ARE USING OPENCV PYTHON PACKAGE 
WE ARE GOING TO GET USER FACIAL DATA WITH THE HELP OF YUBI AI APP AND WE WILL USE THE DATA TO TRAIN YUBI AI TO RECOGNIZE THE USER
SINCE THE CODE IS TOO LONG I WILL PROVIDE THE LINK ON GITHUB VERY SHORTLY

IN THE FACIAL RECOGNITION SYSTEM WE ARE GONNA USE 3 STEPS:
 
 1. GETTING THE DATA/IMAGES FROM THE YUBI A.I APP
 2. TRAIN THE MODEL 
 3. USE THE TRAINED FILE TO RECOGNIZE THE USER
 
 CODE LINK: WILL UPDATE SOON
 
 ---------------------------------------------------------------------------------------------------------------------------------------
 
 YUBI - AI SYSTEM
 
 AS YUBI AI SYSTEM HAS MANY FEATURES ITS STILL IN DEVELOPMENT ITS FINISHED ALMOST 65% WE NEED MMORE DATA TO TRAIN SO IM WORKING ON IT AND WILL SHARE THE CODE SHORTLY
 
 WE HAVE THE FOLLOWING THINGS IN YUBI AI :
 
 1. FACE-RECOGNITION.
 2. ALARM SYSTEM.
 3. REMEMBERING OF IMPORTANT DATES LIKE BIRTHDAYS ETC.
 4. PROACTIVE - AND HAS A UNIQUE PERSIONALITY TO EVERY USER.
 5. NAVIGATING THROUGH DESTINATIONS AND GIVES BEST SUGGESTIONS ON TRAFFIC
 6. HOME AUTOMATION SYSTEM
 7. HOME SECURITY SYSTEM - THIS HOME SECURITY SYSTEM PROTECTS HOUSES/OFFICES FROM THIEFS
 8. TIC - THE SPECIAL THING ABOUT YUBI IS ITS PROACTIVE AND HAS A SPECIAL FEATURE CALLED AS "TIC. TEACHING ITSELF CONSISTANTLY" YUBI AI USES TIC TO TRAIN ITSELF TALKING TO THE USER.
 THAT MEANS THAT THE YUBI AI TRAINS ITSELF FOR BETTER RESPONSES YUBI DONT NEED DEVELOPERS TO TRAIN IT ANYMORE IT ALWAYS LISTENS TO YOU IN THE BACKGROUND
 9. GOOGLE DUPLEX SYSTEM - OUR TEAM IS CURRENTLY WORKING ON THE SYSTEM SIMILAR TO GOOGLE DUPLEX

 
ALTHROUGH MANY FEATURES NEED TO BE COMPLETED WE HAVE FINISHED THIS IMPORTANT FEATURES OF YUBI AI

------------------------------------------------------------------------------------------------------------------------------------------

I WILL SOON SHARE THE LINKS OF EVERY FEATURE IM CURRRENTLY UPLOADING IT TO GITHUB SO I NEED MORE TIME ....

THANK YOU ❤

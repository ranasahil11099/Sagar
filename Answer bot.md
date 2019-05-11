


const Discord = required ('discord.js');
const bot = new Discord.Client();

const token ='NTc0NTE3NzY5Mzk2MTU4NDg0.XM7ETg.in9gUX6tZXnLv6wmdK9JROZmiUA';

bot.on('ready' ,()=>{
  console.log('This bot is online');
  })

bot.on('message', mgs=>{
 if(msg.content === 'HELLO'){
  msg.reply('HELLO FRIEND');
}

})

bot.login(token);


  
    "access_token": "zMndOe7jFLXGawdlxMOdNvXjjOce5X",
    "scope": "bot",
    "expires_in": 604800,
    "refresh_token": "mgp8qnvBwJcmadwgCYKyYD5CAzGAX4"
}

API_ENDPOINT = 'https://discordapp.com/api/v6'
CLIENT_ID = '574517769396158484'
CLIENT_SECRET = 'BNdTqWKDOFvB5auzEHCUa3Uj9OLlct2S'
REDIRECT_URI = 'https://nicememe.website'

def exchange_code(code):
  data = {
    'client_id': CLIENT_ID,
    'client_secret': CLIENT_SECRET,
    'grant_type': 'authorization_code',
    'code': code,
    'redirect_uri': REDIRECT_URI,
    'scope': 'identify email connections'
  }
  headers = {
    'Content-Type': 'application/x-www-form-urlencoded'
  }
  r = requests.post('%s/oauth2/token' % API_ENDPOINT, data, headers)
  r.raise_for_status()
  return r.json()

{
    "access_token":BNdTqWKDOFvB5auzEHCUa3Uj9OLlct2S",
    "token_type": "Bearer",
    "expires_in": 604800,
    "refresh_token": "zuuojf-02ygEX9hEEUCcdUXTrGgvzn87",
    "scope": "identify"
}

API_ENDPOINT = 'https://discordapp.com/api/v6'
CLIENT_ID = '574517769396158484'
CLIENT_SECRET = 'zuuojf-02ygEX9hEEUCcdUXTrGgvzn87'
REDIRECT_URI = 'https://nicememe.website'

def refresh_token(refresh_token):
  data = {
    'client_id': CLIENT_ID,
    'client_secret': CLIENT_SECRET,
    'grant_type': 'refresh_token',
    'refresh_token': refresh_token,
    'redirect_uri': REDIRECT_URI,
    'scope': 'identify email connections'
  }
  headers = {
    'Content-Type': 'application/x-www-form-urlencoded'
  }
  r = requests.post('%s/oauth2/token' % API_ENDPOINT, data, headers)
  r.raise_for_status()
  return r.json()
const Discord = required ('discord.js');
const bot = new Discord.Client();

const token ='NTc0NTE3NzY5Mzk2MTU4NDg0.XM7ETg.in9gUX6tZXnLv6wmdK9JROZmiUA';

bot.on('ready' ,()=>{
  console.log('This bot is online');
  })

bot.on('message', mgs=>{
 if(msg.content === 'HELLO'){
  msg.reply('HELLO FRIEND');
}

})

bot.login(token);

import pyscreenshot as ImageGrab
from PIL import Image
import pytesseract
import webbrowser
import requests
from bs4 import BeautifulSoup
pytesseract.pytesseract.tesseract_cmd = 'C:/Program Files (x86)/Tesseract-OCR/tesseract'

if __name__ == '__main__':
    # part of the screen
    imq = ImageGrab.grab(bbox=(990, 308, 1291, 413))  # X1,Y1,X2,Y2
    question = pytesseract.image_to_string(imq, lang = 'eng')
    webbrowser.open("http://google.com/search?q=" + question)
    imo1 = ImageGrab.grab(bbox=(1019, 425, 1256, 466))  # X1,Y1,X2,Y2
    option1 = pytesseract.image_to_string(imo1, lang = 'eng')
    imo2 = ImageGrab.grab(bbox=(1017, 495, 1256, 537))  # X1,Y1,X2,Y2
    option2 = pytesseract.image_to_string(imo2, lang = 'eng')
    imo3 = ImageGrab.grab(bbox=(1019, 565, 1256, 606))  # X1,Y1,X2,Y2
    option3 = pytesseract.image_to_string(imo3, lang = 'eng')
    # option1 = "Everest"
    # option2 = "Himalaya"
    # option3 = "Om"
    # print(text)
    r = requests.get("http://google.com/search?q=" + question)
    
    
    soup = BeautifulSoup(r.text, 'html.parser')
    # for data in soup.find_all("span", class_="st"):
    #     print(data.text.count("Everest"))
    response = soup.find_all("span", class_="st")
    res = str(r.text)
    # print(res)
    countoption1 = res.count(option1)
    countoption2 = res.count(option2)
    countoption3 = res.count(option3)
    maxcount = max(countoption1, countoption2, countoption3)
    sumcount = countoption1+countoption2+countoption3
    print("\n")
    if countoption1 == maxcount:
        print("A")
    elif countoption2 == maxcount:
        print("B")
    else:
        print("C")
    probA = round(((countoption1/sumcount)*100),2)
    probB = round(((countoption2/sumcount)*100),2)
    probC = round(((countoption3/sumcount)*100),2)
    print("\n")
    print("A: "+str(probA))
    print("B: "+str(probB))
    print("C: "+str(probC))
    # if option1 == max(option1, option2, option3):
    #     print("A")
    # elif option2 == max(option1, option2, option3):
    #     print("B")
    # else:
    #     print("C")
    # print(res.count(option1))
    # print(res.count(option2))
    # print(res.count(option3))

# r = requests.get('https://www.googleapis.com/customsearch/v1?key=xxxxxxxx-2oIz_9bfIXwUjdwyTwZ-s&cx=017576662512468239146:omuauf_lfve&q=highest+mountain')
# print(r.text)

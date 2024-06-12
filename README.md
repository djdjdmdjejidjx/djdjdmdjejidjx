-
import random, string

import os, time, sys

def clear():
  os.system('clear')


st = 0.04

def sp(str):
  for letter in str:
    sys.stdout.write(letter)
    sys.stdout.flush()
    time.sleep(st)
    print()
#editing stuff
Red = "\033[0;31m"
Green = "\033[0;32m"
Orange = "\033[0;33m"
Blue = "\033[0;34m"
Purple = "\033[0;35m"
Cyan = "\033[0;36m"
White = "\033[0;37m" 
black = "\033[0;30m"
cyan_back = "\033[0;46m"
purple_back = "\033[0;45m"
white_back = "\033[0;47m"
blue_back = "\033[0;44m"
orange_back = "\033[0;43m"
green_back = "\033[0;42m"
pink_back = "\033[0;41m"
grey_back = "\033[0;40m"
grey = '\033[38;4;236m'
bold = "\033[1m"
underline = "\033[4m"
italic = "\033[3m"
darken = "\033[2m"
invisible='\033[08m'
reverse='\033[07m'
reset='\033[0m'
grey = "\x1b[90m"
def sys():
  import pyfiglet
  word = pyfiglet.figlet_format('K 6')
  print(Blue+bold+word)
  print(Blue+bold+f'Version 》2.3')
  print("============")
  print("Dev - vd#0093")
def back():
  print("============")
  print("(1) Automatic check")
  print(Blue+bold+f"(2) Non-Automatic check",Red+bold+f"Coming soon !")
  print(Blue+bold+f"(3) exit")
  print("============")
  num=input("Enter a number: ")
  print("============")
  if num=="1":
    print(Blue+bold+f"(1) 4L and 4c Check",Green+bold+f"AVAILABLE !")
    print(Blue+bold+f"(2) 3L and 4c",Red+bold+f"UNAVAILABLE !")
    print(Blue+bold+f"============")
    check=input("Enter a number: ")
    if check=="2":
      print(Blue+bold+f"============")
      print(Red+bold+f"ERROR COMMAND IS DOWN TRY AGAIN !")
      time.sleep(4)
      print(Blue+bold+f"============")
      back()
    
    if check=="1":
      letters=4
      while True:
        user = "http://tiktok.com/@" + ('').join(random.choices(string.ascii_letters + string.digits,k=letters))
        f = open('names.txt', "a+")
        f.write(f'{user}\n')
        f.close()
        if random.randint(0,10000) < 46:
          
          time.sleep(0.2)
          print(Green+Green+bold+f'[Available] {Green+bold+user}/')
        if random.randint(0,1) < 1:
          time.sleep(0.2)
          print(Red+bold+f'[Taken!] {Red+bold+user}/')
sys()
back()

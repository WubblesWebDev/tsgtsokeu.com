---
title: "Class"
date: 2021-12-06T15:31:42-06:00
description: "When quined, Yields a Tortoise's Love-song"
tags: ["GEB", "Programming"]
categories: ["School"]
authors: "Daisy"
---

Today for my python class I am taking on Coursera we were covering functions, and well... I got a little sidetracked and decided to make a program I was thinking about this morning while reading GEB.

unfortunatly I am not well versed enough in BlooP, FlooP or GlooP to write it in those langages, but I think Python will do just fine for my purposes.

if you haven't read GEB, this won't make a lot of sense


{{<highlight python>}}
test_phrase = "compiles"
yn = "\nYes or No:"

def check_for_punc(ip):
    if ip[-1] == ".":
        print(ip)
        ip = ip[:-1]
        ip = check_for_punc(ip)
        return ip
    elif ip[-1] == ",":
        print(ip)
        ip = ip[:-1]
        ip = check_for_punc(ip)
        return ip
    elif ip[0] == " " or ip[0] == '"' or ip[0] == "'":
        print(ip)
        ip = ip.strip()
        ip = ip.strip('"')
        ip = ip.strip("'")
        ip = check_for_punc(ip)
        return ip
    elif "_" in ip or "  " in ip:
        print(ip)
        ip = ip.replace("  ", " ")
        ip = ip.replace("_", " ")
        ip = check_for_punc(ip)
        return ip
    else:
        return ip

def check_for_space(tts):
    ip = input(tts)
    ip = ip.strip()
    return ip

def repeat_manytimes(sentence, number):
    x = sentence
    for n in range(number):
        print(x)

def print_rules():
    print("Here is how you make a Quine Sentence:")
    print(" First you pick a sentence that references something at the beginning")
    print(" Example: 'this is not a sentence'")
    print(" Now you need to take the beginning reference off your sentence.")
    print(" In our example, that would be 'THIS'")
    print(" Thus our sentence becomes '____ is not a sentence'")
    print(" Input that sentence into my program and see how it references itself! \n")
    quined_phrase()

def quined_phrase():
    s = check_for_punc(input("Enter your sentence:"))
    try:
        n = int(input("Enter number of times you would it to print:\n"))
    except:
        n = input("Enter numric value. Exp: 2:\n")
        if n != int or n != float:
            n = 1
    q = f'"{s.upper()}" {s.title()}.'
    repeat_manytimes(q, n)
    print("\n")
    r = check_for_space("Make another?")
    if r[0].upper() == "Y":
        quined_phrase()
    else:
        print("okay! thanks for playing")

def like_to_play():
    r = check_for_space("Would you like to make a Quine Sentence?"+yn)
    if r[0].upper() == "Y":
        sr = check_for_space("Have you done this before?")
        if sr[0].upper() == "Y":
            quined_phrase()
        else:
            print_rules()
    else:
        sr = check_for_space("Are you sure?"+yn)
        if sr[0].upper() == "Y":
            print("Maybe next time.")
        else:
            print("AWESOME! So you do want to play!")
            sr = check_for_space("have you done this before?")
            if sr[0].upper() == "Y" or sr.lower() == "i have":
                quined_phrase()
            else:
                print_rules()

like_to_play()
{{</highlight>}}

if you don't have an IDE, i'm sure you could find one online. only thing to look out for is that it has to be python3 since I am using an fstring in my code, amongst other inconsistencies with python2

## End Note:

this took a long time to program, mostly because I was unfamilar with string slicing, but I'll get there.

This was a lot of fun to program. I didn't get a lot else done today because I was busy making this user friendly, and for the most part it is. did there need to be that many functions for things that only got used once? **NO**, but thats the whole point of school. you do pointless things.

... see you around, Space Cowboy.


---
title: "Zone"
date: 2021-12-09T12:56:04-06:00
description: "The Zone : When you really start to understand things."
tags: ["Programming"]
categories: ["Code"]
authors: "Yara"
---

**ITS OFFICAL** I am a programmer! I got to make something that is actually <cite>useful! [^1]</cite>

[^1]: [#](https://tsgtsokeu/meetings/ma_4/)

last night I stayed up until 1:50am trying to finish a program that actually had a purpose! (that's right! not just some meaningless exercise for school, or for some future coder tic-tac-toe game.)

I had this problem where I had to convert some texts into a readable format in a .md for the website. I realized a really easy way was to just put it into a markdown table because they have built in justifcation (left, right, center) so it would take very little work from me. But I had already written the texts out into a different format, just using paragraphs and `'$` at the beginning of each line to indicate who was talking in that instances. it was sloppy looking and I didn't like it, but I really didn't want to have insert each of those paragraphs into the desired format.

**SO!** I used my new found powers of Python and said "I'm going to make the computer do this shit," lol

#### incase you didn't know, you can make justified tables in .md files just by:

    |sign|meaning|tnt|
    |:--|:--:|--:|
    |O|Zero|666|
    |S|Seccessorship|123|
    |v|or|616|
    |~|not|223|

|sign|meaning|tnt|
|--|:--:|--:|
|O|Zero|666|
|S|Seccessorship|123|
|v|or|616|
|~|not|223|

And it will display like this

so first things first, I assigned a variable to a raw text file, then made a function that would turn each line into a string and put it into a list. easy!

{{<highlight python>}}
with open('MA_raw_text') as f:
    read_data = f.read()

def sep_lines_to_list(data):
    l = []
    s = ""
    for thing in data:
        s = s+thing
        if thing == "\n":
            l.append(s)
            s = ""
            continue
        if thing == '#':
            l.append(s)
            return l
{{</highlight>}}
lol! Be kind to me because this was the first function I wrote of the program, and the first time I had ever did something like this without instructions or someone to help me. my goal was for functionality, not for my variable names to be good.

Next I had to change the signs (`'$`) by matching their first letter to their coresponding name. 

{{<highlight python>}}
names = [s1, s2, s3, s4, s5, s6, s7]

def turn_signs_to_names():
    data = sep_lines_to_list(read_data)
    signed = []
    for v in data:
        if v != "\n":
            v = v.replace(v[:2], match_name_to(v[1]))
            signed.append(v)
        elif v == "\n":
            signed.append(v)
    return signed

def match_name_to(let):
    for n in names:
        if let.lower() == n.lower()[1]:
            return n
    return default
{{</highlight>}}

God! isn't that a beautiful function? Every time I look at it, I get so freaking happy! 

It reminds me of the way my old mentor used to code. how everything looked like waves... 

Though his python code was never that pretty. He always tried to make python look way more confusing then it actually was by putting as much as he could in one line. This looks much more like his Scala code. almost... Poetic

{{<highlight python>}}
def print_md_table_format(heading):
    h1 = f"||{heading}||"
    h2 = f"|:--|---|--:|"
    print(h1+"\n"+h2)
    for v in turn_signs_to_names():
        if v == "\n":
            continue
        elif v[1] == s1[1] or v[1] == s2[1] or v[1] == s3[1]:
            v = v[:v.find("\n")]
            str = f"| {v} || |"
            print(str)
        elif v[1] == s4[1] or v[1] == s5[1] or v[1] == s6[1] or v[1] == s7[1]:
            v = v[:v.find("\n")]
            str = f"| || {v} |"
            print(str)

print_md_table_format("MA chatroom")
{{</highlight>}}

I know I am cheating by just printing out the results in the terminal, but thats where all good programs go first, right? print the results.

Is this the most effective bullet proof code? NO!! of course not! lol, I am not a genius! I have only been seriously learning python for a cumulative sum of around 2 months, and there was a disapointing amount of breaks inbetween learning things, so I am constantly having to lean on the docs to help me understand the syntax.

All and All; This is progress. I am excited. I tried showing my mom the code and she was very confused at what I was talking about, lol. GOOD SIGN!

I was looking at jobs of where I might work after I get some more experience under my belt, after I've gone to college for awhile.

I keep coming back to web design, but I also really want to get into data analytics... A good inbetween might be Advertisment. There are a few KC based firms I will keep an eye out, but getting a job is not at all on the forefront of my mind. I don't have the skills yet to do a job-well-done, which is always my goal in life... To do good.

## End Note:
I also wrote a cute little code yesterday. it really isn't much, but I thought it was clever.

{{<highlight python>}}
import math as m
print((str(m.pi-.1)[:4][::-1].replace('.','')))
{{</highlight>}}

funny how two lines can have so much meaning.
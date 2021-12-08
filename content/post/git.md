---
title: "Git"
date: 2021-12-03T14:05:11-06:00
description: "Github must hate me"
tags: ["Programming"]
categories: ["Journal"]
authors: ["Iris"]
---

Well here I am. I could be doing about a dozen other things, like cleaning the house, doing school (I've got to get better at factoring quadtratics and a Python course I am taking) but noooooo. I am **battling** freaking github! 

so here is the cool, fun, awesome things I've been wasting my time on! I needed a way to connect the contents of my website to the contents on my computer easily. Luckly programmers throughout the years have been wanting to do that for a long time, so thus was born git! 

Because trying to do everything within a terminal is like... fucking annoying. vim can only get you so far, and I was sick of not having an IDE to help me highlight syntax, or broad search purposes. plus I had no way to preview my website and posts, so that definetly needed to change. so I needed to utilize this wonderful technology and create a git repo.

that part was easy... what was not easy was pushing everything up there!!!!

Oh my **GOD,** I spent hours on this.. HOURS!!! 

Here are some of the problems I was faced with.

- I had a .git file inside of the the repo I was trying to commit... causing everything to blow up!
- git recently moved over to token based authentication, and guess who forgot to set an access token for their account.. **ME**
- turned out I was using the wrong tipe of repo address so I had to switch to a SSH repo because I was communicating from an SSH terminal...
- I didn't have a public key on my server, so I needed to generate tha, then paste that into git up so I could communicate with my repo.

and all this took a very. very... **very** long time. at one point I was going crazy and just started ripping through my closet to dress up. I fould a nice jacket and fur scarf and started talking in a Russian accent because i thought it might help me channel some of their hacker energy, and funny enough, it kind of worked! I think I was getting in my head about it all a little too much, so doing something silly like wear a fur scarf and talk like I beat up bears in my free time let out some pent up stress. Highly suggest trying to problem solve while wearing funny hats. Very good.

If I had someone who was more knowledgable about these things helping me, I'm sure that I would have had this all done pretty quickly. But I don't... That's okay. I almost prefer working alone. I am learning the hard way, all on my own. And the important thing is I am actually LEARNING. like, shit. I didn't know any of this before this morning. I barely knew how to git init, much less fucking set a authenication access token from github and how to tunnel in through SSH and generate public key. 

Anyway... cloning my code base onto my computer is now complete. I even got it to submodule so I also have access to the repo inside of my repo.

...fuck. I just thought of something. if I make an edit to that git repo, and then commit this repo, will it save the changes? I'm not sure, but I suspect no.

I just checked. it doesn't. shit. suppose I could move the scc and js bootstrap files into my own static folder, but I'm not sure if the theme will load properly if they aren't in the theme folder.

what a load of bull crap! the entire reason I got this thing working was so I could edit *those* files. I don't like the way the contrast was set up for images, and I needed the images to have @Media for images on smaller screens to so they will display larger.

Well... all is not lost, I learned a lot along the way, and I did get it to somewhat work. I think if I just remove the submodule repo from the theme all together that it'll work. all the edits I've done so far over the terminal are still there.

## End Note:

This was supposed to be A HAPPY post! ugh. now it has a sour ending... I'm upset...

as much as I would love to continue working on this, I have to go clean the house and get ready for dinner with my sister's boyfriend. things are getting pretty serious with them two.

also I listened to skinny love by Bon Iver and almost started crying... really a blast from the past. thanks.
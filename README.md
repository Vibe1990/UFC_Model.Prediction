# How an MMA fan who got tired of bad commentary built a predictive model that did a better job than MMA analysts.

This repository contains code and data used in demonstrating various supervised machine learning algorithms to predict fight outcomes in the largest mixed martial arts organization in the world, the [UFC](www.ufc.com), using the R language.  


## TABLE OF CONTENTS

* Introduction
* Results
* Data Description
* Technical Overview

## Introduction

When I was growing up in the late 90's to early 2000's, everyone I knew had wanted to become a professional athlete in some form.  We all looked up to players like Kobe Bryant (R.I.P.), Brendan Shanahan, or Ronaldo.  To us, they were essentially gods personified, and we all had taken turns being like them during pick-up games at the local park or on the street in front of our homes (in between the car passing by every 5-10 minutes). 

![](https://images.unsplash.com/photo-1594623274890-6b45ce7cf44a?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80)

While the idea of being like them was great and all, I kind of knew it wasn't really going to be in the cards being one of the smallest person in my class with almost zero ability to skate backwards or dribble the ball with my feet. However, despite being ready to complete close that aspiration, there was an emerging sport that had both captured my attention and gave me a glimmer of hope in pursuing a professional atheletic career.  That was mixed martial arts.  

![](https://images.unsplash.com/photo-1615117972428-28de67cda58e?ixlib=rb-1.2.1&ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&auto=format&fit=crop&w=1050&q=80)

Mixed martial arts (or MMA) had everything I liked about sports: an array of technical skills and strategies to solve complex problems with dire consequences, a growing and passionate fandom, and be a platform to display a triumph of human will in its truest sense.  Ever since I saw it for the first time, I knew I had to give it a shot.  As I gotten older, I thought this was a realistic possibility after having wrestled in college and taking up some other necessary skills along the way in the form of Muay Thai and Brazilian Jiu-Jitsu.  While some of my like-minded wrestling teammates had since moved on to a career in sport, mine's came to a crashing halt upon the realization I didn't take too kindly to getting punched in the face as I orignally thought.  I guess Mike Tyson was right, "*Everyone has a plan until they get punched in the mouth*".  Despite dreams being dashed, I still remain an avid MMA fan and grappling hobbyist. 

Being an avid MMA fan, or anything eally, there is a dichotomy that we are aware of. That is the division between the casuals and the hardcore. While I understand that we hardcore fans are in the vast minority, we still expect some representation in the face of the general population.  However, everytime I happen to catch some commentary on an upcoming fight card or a certain match up, I'm baffled by some of the analyses more often than not (particularly the fight picks).  In recent times, it seems that for every correct fight pick there is also one upset that happened. While these outcomes are being touted as "upsets", there has been an awful lot of them throughout MMA’s history.  In fact, it is so frequent that it’s become common place for these analysts/experts to attribute it to the volatile nature of the sport.  Sure, it is fair to say that this may be the case, it still seems like a major cop out. 

With these analysts being so hit-or-miss with these outcomes, I figured I could do a better job than them.  Now before I get labelled as a "*I know better because I trained ‘UFC’*" guy, I'll be doing so through a more data-driven process.  Specifically, I’ll be analyzing at what the data has to say between winners and losers from previous fights in the UFC and build some predictive models to see how accurate I can get with predicting Winners and I can do a better job at predicing outcomes.  Also, considering the nature of this project, let's see if I can actually make more money doing so from my machine learning models compared to just using betting lines. 


***DISCLAIMER:*** Everything that is being used in this article is entirely for educational purposes and entertainment.  **DO NOT USE IT FOR THE PURPOSE OF GAMBLING OR FINANCIAL GAIN**.  You are way better off going with r/WallStreetBets on Reddit or investing in cryptocurrency than what’s shown here.  

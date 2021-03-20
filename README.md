# How a fan who got tired of bad MMA commentary built a predictive model that did a better job than MMA analysts.

This repository contains code and data used in demonstrating various supervised machine learning algorithms to predict fight outcomes in the largest mixed martial arts organization in the world, the [UFC](www.ufc.com), using the R language.  


## TABLE OF CONTENTS

* Introduction
* Results
* Data Description
* Technical Overview

## Introduction

When I was growing up in the late 90's to early 2000's, we all looked up to players like Kobe Bryant (RIP), Brendan Shanahan, or Ronaldo.  To us, they were essentially gods personified, and we all had taken turns being like them during pick-up games at the local park or on the street in front of our homes. Well, in between the cars passing by every 5-10 minutes. 

![](https://images.unsplash.com/photo-1594623274890-6b45ce7cf44a?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80)

While the idea of being like them was great and all, I knew it wasn't really going to be in the cards being one of the smallest person in my class with almost zero ability to skate backwards or dribble the ball with my feet. However, despite being ready to complete close that aspiration, there was an emerging sport that had both captured my attention and gave me a glimmer of hope in pursuing a professional atheletic career.  That was mixed martial arts.  

![](https://images.unsplash.com/photo-1615117972428-28de67cda58e?ixlib=rb-1.2.1&ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&auto=format&fit=crop&w=1050&q=80)

Mixed martial arts (or MMA) had everything I liked about sports: an array of technical skills and strategies to solve complex problems with dire consequences, a growing and passionate fandom, and be a platform to display a triumph of human will in its truest sense.  Ever since I saw it for the first time, I knew I had to give it a shot.  As I gotten older, I thought this was a realistic possibility after having wrestled in college and taking up some other necessary skills along the way in the form of Muay Thai and Brazilian Jiu-Jitsu.  While some of my like-minded wrestling teammates had since moved on to a career in sport, mine's came to a crashing halt upon the realization I didn't take too kindly to getting punched in the face as I orignally thought.  I guess Mike Tyson was right, "*Everyone has a plan until they get punched in the mouth*".  Despite dreams being dashed, I still remain an avid MMA fan and grappling hobbyist. 

![Felt Cute](https://user-images.githubusercontent.com/63363727/111885702-d0c04900-899f-11eb-9845-d1577f215af7.jpg)

**Life Pro Tip**: *If you're on the podium but didn't win, always try to be the cutest person there*

Now, being an avid MMA fan (or anything really), there is a dichotomy that we are aware of. That is the division between the casuals and the hardcore. While I understand that we hardcore fans are in the vast minority, we still expect some representation in the face of the general population.  However, everytime I happen to catch some commentary on an upcoming fight card or a certain match up, I'm baffled by some of the analyses given by these MMA experts.  This is particularly noted during their take on fight picks.  In recent times, it seems that for every correct fight pick there is also one upset that happened.  While these outcomes are being touted as "upsets", there has been an awful lot of them throughout MMA’s history.  In fact, it is so frequent that it’s become common place for these analysts/experts to attribute it to the volatile nature of the sport.  Sure, it is fair to say that this may be the case, it still seems like a major cop out. 

With these analysts being so hit-or-miss with these outcomes, I figured I could do a better job than them.  Now before I get labelled as a "*I know better because I trained ‘UFC’*" guy, I'll be doing so through a more data-driven process.  Specifically, I’ll be analyzing at what the data has to say between winners and losers from previous fights in the UFC and build some predictive models to see how accurate I can get with predicting Winners and I can do a better job at predicing outcomes.  Also, considering the nature of this project, let's see if I can actually make more money doing so from my machine learning models compared to just using betting lines. 

---
***DISCLAIMER:*** Everything that is being used in this article is entirely for educational purposes and entertainment.  **DO NOT USE IT FOR THE PURPOSE OF GAMBLING OR FINANCIAL GAIN**.  You are way better off going with r/WallStreetBets on Reddit or investing in cryptocurrency than what’s shown here.  
---

## Results

* A comparative analysis of the different modeling appraoches to outcome prediction found that (1) logistic regressions building with variables that significantly differ from winenrs and losers and (2) logistic regression bulit with variables correlated with fight outcomes were the two highest performing models. 

![](https://github.com/Vibe1990/UFC_Model.Prediction/blob/main/UFC_Outcome_Prediction_Recap.PNG)

* With reference to actual fight outcomes from [UFC 258](https://en.wikipedia.org/wiki/UFC_258), it was shown that the chosen approach of using a logistic regression model with variable selection using correlates outperformed the projected mma analysis. Under the impression of wagering $100 per fight, overall profit was $469.07 (~ 46.91% profit). 

![](https://github.com/Vibe1990/UFC_Model.Prediction/blob/main/Compare_model_picks_vs_analysis.PNG)


## Data Description 

The data consisted of data collected from the period of 2010-03-21 to 2021-02-10 that was scrapped from the UFC Stat site and made available on [Kaggle](https://www.kaggle.com/mdabbert/ultimate-ufc-dataset).  There are two data sets used in this project: 

1) [Historical data](https://github.com/Vibe1990/UFC_Model.Prediction/blob/main/ufc-master.csv)
2) [Pre-fight data for UFC 258](https://github.com/Vibe1990/UFC_Model.Prediction/blob/main/upcoming-event.csv)

| **Variable**                                                    | **Description**                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------|
| R_fighter                                                       | favorite fighter in match up                                        |
| B_fighter                                                       | underdog fighter in match up                                        |
| date                                                            | when the fight took place                                           |
| location                                                        | city where the fight took place                                     |
| country                                                         | country where the fight took place                                  |
| winner                                                          | which fighter won the fight                                         |
| weight_class                                                    | weight class where the fight took place in                          |
| gender                                                          | gender of the fighters                                              |
| R/B_Stance                                                      | fight stance of the underdog/favorite fighter                       |
| finish                                                          | how did the fight end                                               |
| finish_details                                                  | specifically how did the fight end                                  |
| finish_round_time                                               | time in the round when the fight ended                              |
| title_bout                                                      | was the fight a title bout                                          |
| R/B_odds                                                        | betting odds of the favorite/underdog                               |
| R/B_ev                                                          | payout for favorite/underdog win                                    |
| no_of_rounds                                                    | number of rounds for the fight                                      |
| R/B_current_lose_streak                                         | number of consecutive losses at time of fight                       |
| R/B_current_win_streak                                          | number of consecutive wins at time of fight                         |
| R/B_draw                                                        | total number of draw up until time of fight                         |
| R/B_losses                                                      | total number of losses up until time of fight                       |
| R/B_wins                                                        | total number of wins up until time of fight                         |
| R/B_longest_win_streak                                          | longest win streak in career up until time of fight                 |
| R/B_avg_SIG_STR_landed                                          | average number of significant strikes landed per minute             |
| R/B_avg_SIG_STR_pct                                             | accuracy of significant strikes landed vs thrown                    |
| R/B_avg_SUB_ATT                                                 | average number of submission attempts in a fight                    |
| R/B_avg_TD_landed                                               | average number of takedowns landed per minute                       |
| R/B_avg_TD_pct                                                  | accuracy of takedown landed vs attempted                            |
| R/B_Height_cms                                                  | height of respective fighter in match up                            |
| R/B_Reach_cms                                                   | reach of respective fighter in match up                             |
| R/B_weight_lbs                                                  | weight of respective fighter in match up                            |
| R/B_age                                                         | age of respective fighter in match up                               |
| R/B_total_title_bouts                                           | total number of in career up until the time of fight                |
| R/B_total_round_fought                                          | total number of rounds fought in the UFC up until fight             |
| R/B_win_by_decision                                             | total number of wins respectively by decision                       |
| R/B_win_by_submission                                           | total number of wins respectively by submission                     |
| R/B_win_by_KO.TKO                                               | total number of wins respectively by knockout                       |
| R/B_win_by_TKO_Doctor                                           | total number of wins respectively by doctor stoppage                |
| win_dif                                                         | total win differential b/t respective fighter                       |
| loss_dif                                                        | total loss differential b/t respective fighter                      |
| lose_streak_dif                                                 | losing streak differential b/t respective fighter                   |
| win_streak_dif                                                  | win streak differential b/t respective fighter                      |
| longest_win_streak_dif                                          | longest win streak differential b/t respective fighter              |
| total_round_dif                                                 | differential b/t respective fighter on total rounds fought          |
| total_title_bout_dif                                            | differential b/t fighters on total title bouts fought               |
| ko_dif                                                          | differential on total knockouts + doctor stoppage wins              |
| sub_dif                                                         | differential on total submission wins                               |
| sig_str_dif                                                     | differential on significant strikes landed                          |
| avg_sub_att_dif                                                 | differential on average submission attempts                         |
| avg_td_dif                                                      | differential on takedowns landed                                    |
| empty_arena                                                     | was the fight held in an empty arena                                |
| R/B_weightclass_rank                                            | weight class rank for respective fighter                            |
| finish_round                                                    | which round did the fight end                                       |
| total_fight_time_secs                                           | total length of fight in seconds                                    |
| R/B_kd_bout                                                     | average number of knockdowns in a bout                              |
| R/B_sig_str_landed_bout                                         | average number of significant strikes landed in a bout              |
| R/B_sig_str_attempted_bout                                      | average number of significant strikes attempted in a bout           |
| R/B_sig_str_pct_bout                                            | average accuracy of significant strikes landed in a bout            |
| R/B_tot_str_landed_bout                                         | average total number of strikes landed in a bout                    |
| R/B_tot_str_attempted_bout                                      | average total number of strikes attempted in a bout                 |
| R/B_td_landed_bout                                              | average number of takedowns landed in a bout                        |
| R/B_td_attempted_bout                                           | average number of takedowns attempted in a bout                     |
| R/B_td_pct_bout                                                 | average accuracy of takedowns landed in a bout                      |
| R/B_sub_attempts_bout                                           | average number of submissions attempted in a bout                   |
| R/B_pass_bout                                                   | average number of guard-passes in a bout                            |
| R/B_rev_bout                                                    | average number of reversals (i.e., sweeps) in a bout                |

**NOTE**: Values for the favorite is listed as a negative whilst the underdog is listed as a positive value.  This is noted with differential scores 
**NOTE**: Class ranking go from 0 (denoting champion) to 15. Blanks refer to unranked fighters 

## Technical Overview





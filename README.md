# Funnel analyse using SQL

Warby Parker is a transformative lifestyle brand with a lofty objective: to offer designer eyewear at a revolutionary price.


As a customer You can complete the survey about your eyewear  preferencies and than the company sends you some glasses to try on. Then You can return them for free or keep them and pay. 
For every pair of eyeglasses and sunglasses sold, a pair is distributed to smomeone in need. 

![image](https://github.com/GrzegorzCiepiel/Usage_Funnels_with_Warby_Parker/assets/135313652/159aab6e-546a-491f-a0d7-39eaad594082)


The company asked for answer a few questions related to the survey and the sales funnel:

1.	What is the number of responses of each question in website survey?
2.	Which question(s) of the survey have lower completion rates?
Warby Parker’s purchase funnel is:
Take the Style Survey → Home Try-On → Purchase the Warby Parker’s purchase funnel is:
Take the Style Quiz → Home Try-On → Purchase the Perfect Glasses
50% of the users will get 3 pairs to try on
50% of the users will get 5 pairs to try on
3.	Are users who get more pairs to try on at home will be more likely to make a purchase?

## What is the number of responses of each question in website survey?
## Which question(s) of the survey have lower completion rates?

Users will „give up” in different points in the survey. I analyse how many users move from
one question to another using COUNT ( DISTINCT user_id) and GROUP BY every question respectively.
Then I count percentage of answers to the answers of the previous question.

![image](https://github.com/GrzegorzCiepiel/Usage_Funnels_with_Warby_Parker/assets/135313652/9a8f0d41-ac99-41d2-93da-adbf79c782d3)

As we can see almost all responders answered
on second and fourth question. Only 75% of all
responders answered  the last question „When
Was your last eye exam?” 
Maybe they where afraid of of being charged an
extra fee for the eyetest?

## Are users who get more pairs of glasses to try on at home will be more likely to make a purchase?

At first I need to left join 3 tables: quiz, home_try_on and
purchase to visualise the funnel. Table below shows only 
four first rows.
![image](https://github.com/GrzegorzCiepiel/Usage_Funnels_with_Warby_Parker/assets/135313652/55f733d1-40a0-4a28-807a-457599275187)

Based on the previous table I count all purchases, dividing
theminto those made after receiving 3 and 5 pairs of
glasses. 

![image](https://github.com/GrzegorzCiepiel/Usage_Funnels_with_Warby_Parker/assets/135313652/c68602da-9a0e-478f-a54b-c72a7d43619d)

As we can see sending five pairs of glasses seems to be
significantly more effective.

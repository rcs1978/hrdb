# hrdb
# The High Stakes Tournament Poker Database
You ever wonder who has made the most money from poker, who made the most money playing Pot Limit Omaha tournaments, and who is one of the best all tournament poker player on the high stakes scene.  I setout to try and get a rough idea about the high stakes poker scene to get a rough estimate on the player pool, what events they enjoy the most, and what are some ROI for the average regular.  Let's dive in.

## Gathering the data
When it comes to openly publishing data, poker is different from many other games and sports.  You'll easily find all sorts of Earning List and Amount Won all over the place, what you won't find is Buy_Ins minus Amount Won.  It's a closely guarded stat that companies rarely ever publish.  I can only think of two occasions where this has happened and the utter chaos and outrage it caused.  No one wants to be known as the guy who lost 1.7 million dollars when their public profile shows they've won 11 million.  Besides ego, a lot of players rely on backing/staking to help them get the entry fee for the event.  A public list showing a player is losing money wouldn't help with them raising stakes.  Because of these reasons the 'net' is kept secret from any stat on poker.  

Curiousity though gets the best of me.  I'm also curious on a bigger scale what percent of the pool of players are actually profitable.  Not to mention I can also get a better idea of the size of these player pools and what games and buyin amounts they draw.  This is how I did it

## Scraping the news sites
Many years ago I guessed that you could probably make a database based off of reported data from poker news sites.  If you're a named pro you get reported about, people want to see if you survived day 1 and almost always they report if you busted. With the WSOP, they actually have an app now that reports your chipstack for people at home.  What I found is that they do a heck of a good job getting a good portion of the field reported on and if you're a famous or even on the fringe known poker player it is noted 'Fun Fred - 123,000 Chips' or 'Bob the Pro - BUSTED'.  If you take the list of all the players who played day1 (sometimes day2) and matched it up with the public list of those who cashed.  You could easily create a database showing what even a player played and if they cashed or busted out of it. This is straight from a poker news site reporting of day 1 chip counts during the 10k Seven Card Stud, notice some names have chips and others say busted.  
![day1chipcounts](https://github.com/rcs1978/hrdb/assets/152421676/d2331ab3-590d-4d58-ad71-764d74dc5b08)

Now here is a small sample of those who cashed or made it into the money for the event.
Now notice on the Day 1 chip counts the player named John Monnette had chips at the end of day 1
![day1payouts](https://github.com/rcs1978/hrdb/assets/152421676/7aea0821-ea38-4466-be23-fbc6676c9572)

Now notice on the payout list for day 1 it shows that he indeed cashed at the end of the event.  Using this it was easy to create a list of players who played and if they cashed.

So I sought out public data reported on a tour that has smaller player pools.  The PGT was the perfect match, most of the time the average tournament only has 30-50 people playing so its the perfect size.  In the end I got data on over 1500 indvidual players who have played these events since 2015.

## Drawbacks
1. We don't know how many times a player has rebought into an event.  The majority of these tournaments are reentry, meaning when a player busts they can buy back in up until a certian level.  Sometimes when they post a number like 45 entries, but after counting the chip counts there were only 36 names, we can assume 8 of them rebought but we don't know which players.  I have htought about adding a seperate column dividing reported_entries by counted_entries which in this case would be 1.2 percent and using that as the rebought buyin total.  But I left that alone
2. We don't know the rake.  The rake is how much is taken out of the entry fee to help pay admin costs.  PGT often lets players who buy in early free rake, also we're not sure if they do rake the rebuy money.  Rake can have a huge effect on a players net.  I have thought about taking 10% off the buy in and trying to adjust payouts in one of the columns to help show the cause of rake.  For now I left everything alone

Again these are all rough estimates.





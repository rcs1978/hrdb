# hrdb
# The High Stakes Tournament Poker Database
You ever wonder who has made the most money from poker, who made the most money playing Pot Limit Omaha tournaments, and who is one of the best all tournament poker players on the high stakes scene. I set out to try and get a rough idea about the high stakes poker scene to get a rough estimate on the player pool, what events they enjoy the most, and what are some ROI for the average regular. Let's dive in.

## Gathering the data
When it comes to openly publishing data, poker is different from many other games and sports. You'll easily find all sorts of Earning List and Amount Won all over the place, what you won't find is Buy_Ins minus Amount Won. It's a closely guarded stat that companies rarely ever publish. I can only think of two occasions where this has happened and the utter chaos and outrage it caused. No one wants to be known as the guy who lost 1.7 million dollars when their public profile shows they've won 11 million. Besides ego, a lot of players rely on backing/staking to help them get the entry fee for the event. A public list showing a player is losing money wouldn't help with them raising stakes. Because of these reasons the 'net' is kept secret from any stat on poker.

Curiosity though gets the best of me. I'm also curious on a bigger scale what percent of the pool of players is profitable. Not to mention I can also get a better idea of the size of these player pools and what games and buyin amounts they draw. This is how I did it.


## Scraping the news sites
Many years ago, I guessed that you could probably make a database based from reported data on poker news sites. If you're a named pro you get reported about and people want to see if you survived day 1 and almost always, they report if you busted. With the WSOP, they have an app now that reports your chipstack for people at home. What I found is that they do a heck of a good job getting a good portion of the field reported on and if you're a famous or even on the fringe known poker player it is noted in the report 'Fun Fred - 123,000 Chips' or 'Bob the Pro - BUSTED'. If you take the list of all the players who played day1 (sometimes day2) and match it up with the public list of those who cashed. You could easily create a database showing what even a player played and if they cashed or busted out of it. This is straight from a poker news site reporting of day 1 chip counts during the 10k Seven Card Stud, notice some names have chips and others say busted.  
![day1chipcounts](https://github.com/rcs1978/hrdb/assets/152421676/d2331ab3-590d-4d58-ad71-764d74dc5b08)

Now here is a small sample of those who cashed or made it into the money for the event.
Now notice on the Day 1 chip counts the player named John Monnette had chips at the end of day 1

![day1payouts](https://github.com/rcs1978/hrdb/assets/152421676/7aea0821-ea38-4466-be23-fbc6676c9572)

Now here is a small sample of those who cashed or made it into the money for the event. Now notice on Day 1 chip counts the player named John Monnette had chips at the end of day 1.

So, I sought out public data reported on a tour that has smaller player pools. The PGT was the perfect match, most of the time the average tournament only has 30-50 people playing so its the perfect size. In the end I got data on over 1500 individual players who have played these events since 2015.


## Drawbacks
1.	We don't know how many times a player has rebought into an event. The majority of these tournaments are reentry, meaning when a player busts, they can buy back in up until a certain level. When a tournament director post a number like 45 entries and after counting the reported chip counts and there are only 36 names, we can assume there were at least 8 reentries.  Sadly we don't know who and how many times. I have thought about adding a separate column dividing reported_entries by counted_entries which in this case would be 1.2 percent and using that as the rebought buyin total. But I left that alone.
2.	We don't know the rake. The rake is how much is taken out of the entry fee to help pay admin costs. PGT often lets players who buy in early free rake, also we're not sure if they do rake the rebuy money. Rake can have a huge effect on a player’s net. I have thought about taking 10% off the buy in and trying to adjust payouts in one of the columns to help show the cause of rake. For now, I left everything alone
Again, these are all rough estimates.


## Integrity
I don't want to cause drama. What I decided to do is take the pool of names and assign them a PlayerID. I also created a TourID, EventID, and Event_Code to be able reference specific tours and events without naming them. I don't have a desire to shame or make fun of anyone, so I tried to keep the data as anonymous as possible.

## How to
At first I was just using the old copy and paste method into Excel.  I had my main tab filed out with the information about that event, had my formuals set, and I would copy paste the table the final payouts from the [PGT News website](https://www.pgt.com/live-reporting/pokergo-cup-2024/event-1-5100-nolimit-holdem). In another tab I would copy paste the day 1 and sometimes day 2 chip counts info into another tab.  I'd paste the names from the days chip counts below the list of names of those who cashed.  Then I'd remove the duplicate names which would keep the names of those who cashed and delete their day 1 entry.  It would also keep the names of those on Day 1 who played and busted.  This process was tedius and long.  Eventually I learned how to create a Python script to that would do that work for me, cutting down my hours of copying and pasting.  I did use Power Querry in Excel, but it was still no where near as fast as making your own Python script.  

Eventually it would give me an entry like this.

![sample](https://github.com/rcs1978/hrdb/assets/152421676/6168af0e-86b0-4d81-a5f4-1d3c2737c266)










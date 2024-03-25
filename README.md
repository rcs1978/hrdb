# HRDB: The High Stakes Tournament Poker Database

Have you ever been curious about who the top earners in poker are, especially in high stakes tournaments or in games like Pot Limit Omaha? Wonder no more. The HRDB (High Stakes Tournament Poker Database) project is an ambitious endeavor aimed at shedding light on the elusive world of high stakes poker. It seeks to offer insights into the earnings, preferences, and overall performance of players in this competitive arena. Join me as we delve into the intricacies of the high stakes poker scene, exploring the player pool, preferred events, and the average return on investment for seasoned players.

## Data Collection: Unveiling the Hidden World of Poker

Poker, unlike many other sports and games, maintains a shroud of secrecy over certain data, particularly when it comes to net earnings (Buy-Ins minus Winnings). Such information is fiercely protected, with rare disclosures causing upheaval within the community. The reluctance stems from various reasons, including the preservation of professional reputations and the complexities of securing backing for tournament entries. In an industry where image and perceived success can influence one’s ability to compete, the true financial outcomes of players remain under wraps.

Driven by an insatiable curiosity and a passion for the game, I embarked on a quest to uncover the veiled aspects of high stakes poker. My goal was not only to understand the profitability landscape but also to gauge the size and dynamics of the player pool across different games and buy-in levels.

## Methodology: From News to Numbers

The breakthrough came from an unlikely source: poker news sites. These platforms, while covering the glitz and drama of tournaments, inadvertently provide pieces of a larger puzzle. By tracking reports on player performances, from Day 1 chip counts to final payouts, a database began to take shape. The process involved meticulously matching reported player appearances with official cashing lists, constructing a narrative of participation and success across various events.

One notable example is the WSOP app, which provides real-time updates on player stacks, offering a glimpse into the tournament's progression. By synthesizing this public data, I managed to compile a comprehensive database, capturing the journey of over 1,500 players in smaller-scale tours like the PGT, which proved to be an ideal data source due to its manageable player pool sizes.

## Challenges and Considerations

Despite the rich data, certain limitations persist. The inability to track re-entries and the opaque nature of tournament rakes present gaps in our understanding of true player profitability. These aspects, crucial to grasping the financial dynamics of poker tournaments, remain elusive due to the nature of the data available. Nevertheless, the database offers valuable insights, albeit with a degree of approximation.

## Ethical Considerations: Maintaining Anonymity

In constructing this database, I was acutely aware of the potential for controversy and the sensitivity surrounding player earnings and reputations. To navigate these concerns, I adopted a system of anonymization, assigning unique identifiers to players, tours, and events. This approach ensures the integrity of the data while respecting the privacy and dignity of the individuals involved.

The HRDB project is more than just a compilation of statistics; it's a window into the nuanced and often hidden world of high stakes poker. It serves as a resource for enthusiasts, analysts, and perhaps even players themselves, offering a new perspective on the game's competitive landscape.


## How to
At first I was just using the old copy and paste method into Excel.  I had my main tab filed out with the information about that event, had my formuals set, and I would copy paste the table the final payouts from the [PGT News website](https://www.pgt.com/live-reporting/pokergo-cup-2024/event-1-5100-nolimit-holdem). In another tab I would copy paste the day 1 and sometimes day 2 chip counts info into another tab.  I'd paste the names from the days chip counts below the list of names of those who cashed.  Then I'd remove the duplicate names which would keep the names of those who cashed and delete their day 1 entry.  It would also keep the names of those on Day 1 who played and busted.  This process was tedius and long.  Eventually I learned how to create a Python script to that would do that work for me, cutting down my hours of copying and pasting.  I did use Power Querry in Excel, but it was still no where near as fast as making your own Python script.  

Eventually it would give me an entry like this.

![sample](https://github.com/rcs1978/hrdb/assets/152421676/6168af0e-86b0-4d81-a5f4-1d3c2737c266)

## Entering into database
After gathering years of data into Excel we imported that data into Microsoft SQL Serve Managment Studio.  Its the only SQL database program I have and can be a bit touchy to get data stored correctly but eventually we got these tables

![table](https://github.com/rcs1978/hrdb/assets/152421676/b02d816a-34f6-4e20-9028-cd168405739a)

## Running a few querrys

Unique Player Count

![playercount](https://github.com/rcs1978/hrdb/assets/152421676/c9d31ec3-b986-493a-8c69-c84615360c4e)

How many poker series have run

![seriescount](https://github.com/rcs1978/hrdb/assets/152421676/cca71de0-6311-470b-b149-3ad74b07684d)

How many events have been played

![eventsplayed](https://github.com/rcs1978/hrdb/assets/152421676/51c6f99c-b8de-44a2-9830-e8a506c55a32)

List all the hosts and how many series and events it has hosted

![hosts](https://github.com/rcs1978/hrdb/assets/152421676/4623d16b-6949-419d-bec8-f346013642c3)

A list of games and how many times they've been played

![games](https://github.com/rcs1978/hrdb/assets/152421676/72396276-835c-4b6b-8d72-9052a86acae9)

How many events at the 8k-13k buy in level and how many average entries

![10kentries](https://github.com/rcs1978/hrdb/assets/152421676/f3298a30-6a25-444e-b91d-2af0568b0be0)

How many events at the 23k-27k buy in level and how many average entries

![25kentries](https://github.com/rcs1978/hrdb/assets/152421676/17115c54-94ec-46c5-b597-b2c8c0ff82a4)

--Avg Entries and the amount of PLO events played at the 8k-13 buy in

![10kentries](https://github.com/rcs1978/hrdb/assets/152421676/59711923-e778-491f-8d98-6a00e7efa92c)

--Avg Entries and the amount of PLO events played at the 23k-27k buy in

![25kploentries](https://github.com/rcs1978/hrdb/assets/152421676/a19167a3-7ec9-4c4e-9429-dd1c27a77f42)

How many mixed game events and average entries into those events

![mixedgameentries](https://github.com/rcs1978/hrdb/assets/152421676/3aebd939-adbf-49f8-8320-50d5a1589b2a)

Estimated ROI for those who have played at least 10 events or more

![estROI](https://github.com/rcs1978/hrdb/assets/152421676/8cde5a8b-150f-4b0a-bf20-d576b8541dc7)
![estROI_1](https://github.com/rcs1978/hrdb/assets/152421676/266ca037-184e-42b1-a1b0-b0b3ab67ae67)
![estROI_2](https://github.com/rcs1978/hrdb/assets/152421676/ab5e1c06-0c42-4fda-ac20-089c40cfc477)

average amount of events played by PlayerID and Average Buy In for those who played 7 Events

![averageeventsbuyins](https://github.com/rcs1978/hrdb/assets/152421676/52db3236-524a-4075-9847-b4d6d4dc586f)

--Avg Estimate ROI for those who played 7 events

![avg_est_roi](https://github.com/rcs1978/hrdb/assets/152421676/9b1b1170-5231-468b-9705-b5a9d8c5f119)

## Graphs

Percent of those who are profitable

![percentprofitable](https://github.com/rcs1978/hrdb/assets/152421676/0c4b3b64-b006-4bb2-8dec-2e174e2f830b)

Estimate Average ROI of players who played 7 events or more

![estroigraph](https://github.com/rcs1978/hrdb/assets/152421676/3c2ead80-3f1b-4cc3-b64b-1c00c91e5737)

Estimate Average ROI plot of those who played 7 events or more

![roiplot](https://github.com/rcs1978/hrdb/assets/152421676/75139704-1854-41ec-8c60-6894573f5c16)













































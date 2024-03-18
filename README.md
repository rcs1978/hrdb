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










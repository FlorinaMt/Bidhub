## Requirements

&emsp;Given the longstanding challenges in the auctioneering field, the stakeholders, such as the auction house and the auction participants have diverse needs and expectations, but all their requirements are fairness-oriented and together, they build a better understanding of the system. Six types of actors can be identified in the project and they have specific goals: 

Moderator 
- manages the auction system;
- is responsible for ensuring that the platform operates smoothly and fairly by overseeing auctions and Participants;
- has privileges in terms of accessibility

Seller
- the auction Participant who assumes the role of Seller by starting an auction after providing information on items;

Bidder 
- the auction Participant who assumes the role of Bidder by participating in auctions (placing bids, buying items, browsing ongoing auctions);

Participant
- general actor, can be seller, bidder or both;

Timer
- is responsible for starting, updating and ending auction’s countdown and for notifying its end;

Guest
- someone who visits the auction system and has the option to create an account, transforming them into a Participant;

### Functional Requirements
&emsp;The functional requirements outlined in this section detail the specific behaviors and capabilities that the auction system must exhibit to meet the needs and expectations of its users. These requirements ensure that the system provides a comprehensive experience, supporting various roles. Each requirement is designed to facilitate seamless interactions within the auction platform, enhance security, and ensure regulatory compliance. The requirements are articulated to be Specific, Measurable, Achievable, Relevant, and Time-bound (SMART), serving as the foundational elements for the system’s design and implementation. By adhering to these requirements, the auction system is well-equipped to handle the core functionalities necessary for efficient auction management and user satisfaction.
Functional requirements: 

1. As a Seller, I want to start an auction deal that has an auto generated ID, upload a picture, fill out the information about my item (title, description), apply price constraints (reserve price - the minimum price I am willing to accept, buyout price - the price I am willing to sell the item right away for, minimum bid increment) and set the auction duration in hours (time left for participating from the moment I started the auction), so I will be able to list my items and sell them within the specified auction duration. 

2. As a Bidder, I want to access the list of all ongoing auctions, showing the ID, title, current highest bid, picture and end time for each auction, so I can easily identify and participate in the auctions that interest me.

3. As a Bidder and Moderator, I want to open an auction and have access to all the necessary information about the item, including the title, description, reserve price, buyout price, minimum bid increment, auction time, picture, current highest bid and current highest bidder, so I can make informed decisions and effectively participate in the auction.

4. As a Bidder, I want to participate in an ongoing auction by offering at least the reserve price, if no other bids exist or increasing the highest bid (if I am not the current highest bidder) by at least the minimum bid increment, so I can compete for an item I am interested in, without outbidding myself.

5. As a Bidder, I want to receive a real-time notification with the auction ID when my bid is beaten for a specific item, so I can promptly increase my price in response and have a better chance of winning the auction

6. As a Participant, I want to access the chronological list of notifications, starting with the most recent ones, which includes timestamps and notification contents, allowing me to stay informed about relevant updates and actions, such as won items, deleted auctions or beaten bids.

7. As a Guest, I want to create an account by providing my first name, last name, date of birth, contact information (email address, phone number) and password so I can start to securely sell my items and participate in auctions. 

8. As a Participant, I want to log in to my account using my email address and password, so that I can securely access my notifications, sell items, and participate in auctions at any time.

9. As a Bidder, I want to buy an auction item for the specified buyout price if no bids have been placed on it within a specified time period, so that I can secure the item and skip the bidding process.

10. As a Seller, I want to access all my ongoing and closed auctions, and see the ID, title, the highest bid, picture and the end time for each auction, so I will stay up to date with the status of my items.

11. As a Bidder and Seller, I want to be notified and receive the other party’s contact information (including first name, last name, email address and phone number) and the auction ID after the auction time is over, so that we can communicate and close the deal independently.

Bidder - the Bidder with the highest bid after the auction end

Seller - the creator of the auction

12. As a Bidder and Moderator, I want to search for ongoing auctions using the IDs or words present in the titles, so I can easily find and access the items I’m interested in.

13. As a Bidder, I want to access all the ongoing and closed auctions where I previously placed a bid or bought the item and see the ID, title, the highest bid, picture and the end time for each auction, so I will stay up to date with information on deals I’m taking or took part in.

14. As a Participant and Moderator, I want to log out from my account, in order to prevent unauthorized access such as someone else using my device.

15. As the Moderator, I want to prohibit sellers from placing bids on their own auctions, to prevent them from artificially increasing the prices for the items.

16. As a Participant and Moderator, I want to reset my password by entering the old password and the new password, if I suspect unauthorized access or I want to choose a stronger password, so my account will be secured.

17. As the Moderator, I want to log in to my account using a provided email address and password, so that I can inspect Participants’ activity and manage the auctions.

18. As the Moderator, I want to set and display my contact information (including first name, last name, email address and phone number), so the Participants can easily contact me for assistance with issues or navigating the platform.

19. As the Moderator, I want to access all the ongoing and closed auctions, including the ID, title, highest bid, picture and end time for each auction, in order to effectively evaluate whether they comply with the rules and standards, based on my determination.

20. As the Moderator, I want to search for a Participant by their email address, so I can see their first name, last name, phone number, ban or unban them.

21. As the Moderator, I want to ban a Participant, provide a reason for banning, and have the reason displayed to the Participant when they attempt to log in and get the system to automatically log them out, delete their auctions, regardless of status, and their bids, if I decide that the Participant does not respect the rules, based on my determination.

22. As the Moderator, I want to unban and allow a previously banned Participant to log back into their account if I determine that my initial reason for banning them was too weak. 

23. As the Moderator, I want to delete an item from auction, regardless of status, by notifying and providing the Seller with a reason, if I decide that according to my determination, the item violates platform’s standards.

24. As a Participant, I want to delete my account, and automatically delete my started auctions and my placed bids, regardless of status, if I decide I don’t want to use the platform anymore.

25. As the Moderator, I want to access the list of accounts, with their first name, last name, email address and phone number, so I can investigate their activity and decide if they respect the rules.

26. As the Moderator, I want each auction to be open for at most 24 hours, so they will not be open for too long. 

27. As a Participant, I want to edit the information in my account, including the first name, last name, email address, phone number and date of birth, to update it if the data is no longer actual or if I entered the information when I created my account.

### Non-Functional Requirements

The following non-functional  requirements (see Table 2.3.1) define the system's operation and ensure its usability, reliability, performance and supportability, providing the foundation for a robust and efficient auction platform.

| No. | Summary | Non-Functional requirement | FURPS+ classification |
| ---- |----------|---------------------------|-----------------------|
| 28. | Age Restriction | Participants must be at least 18 years old to create an account. | Usability - ensures the user base is age-appropriate for the legal constraints |
| 29. |Countdown Timer | A countdown timer must be used to specify the time left for each ongoing auction in the format HH:MI:SS and close the auction when the time is up. | Reliability - the system is required to perform correctly under specific conditions (ending the auction precisely when the time is up) |
| 30.|Database Storage|The system must use a database (PostgreSQL) as storage strategy.|Performance - the choice of database impacts system performance in terms of data retrieval and storage efficiency|
| 31.|Image Support|The system must support JPEG images when starting an auction.|Supportability - ensures that the system is compatible with widely used standards and formats|

## Use Cases

1.    Start auction (Actor - Seller)
- allows the Seller to:
initiate auctions by providing details such as title, description, reserve price, buyout price, minimum bid increment, auction duration and an image.
  
2.    Participate in auction (Actor - Bidder)
- the Bidder can:
browse ongoing auctions;
search for ongoing auctions by id or words present in the title; 
place bids in auctions;
buy items at the buyout price;
receive notifications when their previous bids have been beaten.
3.    Create account (Actor - Guest)
- allows the Guest to:
create an account by providing personal information: first name, last name, email address, phone number and date of birth as well as a password. 
4.    Manage participant account (Actor - Participant)
- the Participant can:
log in and log out of their account;
reset their password;
edit or delete their account;
access the auctions they started or the auctions they participated in.
5.    Manage participants (Actor - Moderator)
- the Moderator can:
ban a Participant after specifying the reason;
unban a banned participant;
view a list of all participants’ contact information;
search for participants by email;
6.    Manage auctions (Actor - Moderator)
- the Moderator can:
browse both ongoing and finished auctions;
search for any auction by id or words present in the title; 
delete auctions if they violate rules.
7. Manage moderator account (Actor - Moderator)
the Moderator is allowed to:
set and display their own contact information for all participants;
log in and out of their account;
reset their password.
 7.   Update auction (Actor - Timer):
- the Timer:
calculates the moment when a started auction should end;
displays and updates the time left for bidders to participate in a specific auction.
notifies the end of the auction, which triggers the information exchange between the Seller and the final Bidder, if they exist;


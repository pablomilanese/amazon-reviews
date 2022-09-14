## AMAZON VINE ANALYSIS

#### OVERVIEW
The purpose of 'Amazon Vine Analysis' was to examine Amazon reviews written by members of the paid Amazon Vine Program.<br>
The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

The dataset considered for this project was "Personal Care Appliances".
In order to carry on our analysis we loaded our Amazon Data into a Spark dataframe. We then created different tables and uploaded them to AWS, using PostgreSQL as our engine.

#### RESULTS
* How many Vine reviews and non-Vine reviews were there?<br>
There were 3 Vine reviews and 3094 non-Vine reviews.
<img width="363" alt="image" src="https://user-images.githubusercontent.com/105120795/190059073-bf69c0f4-3066-475f-b18d-d54bc9eca979.png">
<img width="388" alt="image" src="https://user-images.githubusercontent.com/105120795/190059110-40bc98f3-b194-4358-af49-c56600682d13.png">
* How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?<br>
There were two five-star Vine reviews and 1704 five-star non-Vine reviews.
<img width="719" alt="image" src="https://user-images.githubusercontent.com/105120795/190059194-a1268da4-b322-414f-8f96-6d474b9184a6.png">
<img width="754" alt="image" src="https://user-images.githubusercontent.com/105120795/190059219-4655a1be-620f-4310-9a9a-fb3b249cdb8b.png">
* What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?<br>
The percentage of five-star Vine reviews was 67% and the percentage of five-star non-Vine reviews was 55%
<img width="581" alt="image" src="https://user-images.githubusercontent.com/105120795/190059351-7e30bdcc-0c8b-4091-9996-19fa15f34f99.png">


#### SUMMARY
To determine if there was positivity bias we broke down the Personal Care Appliances dataframe (with 20 upvotes or more) into a dataframe with paid reviews and unpaid reviews. According to our findings almost 70% of paid reviews had five stars and 55% of unpaid reviews had five stars. Although the percentages show that there is positivity bias it is important to note that there were only three five-star paid reviews with 20 or more upvotes. Given the low amount of paid reviews, especially when compared to the 3094 unpaid reviews, it would be misleading to assure that there was positivity bias.

To get a better picture we should answer the following four questions:<br>
* How many paid reviews are there, independently of how many upvotes they had?<br>
* How many unpaid reviews are there, independently of how many upvotes they had?<br>
* How many upvotes does a review need to be considered more trustworthy?<br>
* Why only consider reviews with 20 upvotes or more and not 15 or 10?<br>

Filtering our dataframe for reviews with less upvotes may give us a better understanding of how a paid program may have positivity bias.

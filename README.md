
#  A/B Testing and Performance Analysis of Recommendation Algorithms 

In this notebook, two recommendation algortihms are being compared statistically to see which fares well at the end of the day. Lets' say the new recommendation algorithm is the algorithm from my CLoset Companion project. Once the new recommendation algorithm is good to go, randomly assign users to either the control or treatment group to ensure that both groups are statistically similar and that differences in outcomes can be attributed to the changes in the recommender system. Their behaviour is captured - this could be if they viewed products, added it to cart, or purchased it.
The duration of the test depends on how data you'd want to collect and how much variability you want to capture.

Before fully deploying a new recommendation algorithm, A/B testing helps ensure it performs as expected without negatively impacting user experience. It also provides empirical evidence to guide decisions on which recommendation approach to adopt.

Control group: The existing recommender system or baseline algorithm.
Treatment group: The new recommender system.

## Hypothesis formulation
The new recommendation algorithm will lead to higher number of users purchasing/adding to carts/spending more time on the website. And it is very different to the old recommendation algorithm.
 

## Analysis and Metrics
For teh analysis, we'll first look at the difference in the features using central tendencies, and EDA. Once we see a certain trend, we can use statistical methods to see if the difference/trend is due to random chance. 

Metrics chosen: 
- Number of purchases
- AddtoCart
- WebsiteClicks
- Reach
- Cost Per Acquisition (CPA)
- Return on Investment (ROI)
- Click-Through Rate (CTR)


## Observations

The old recommender system reaches a broader audience, but that does not result in more people adding to cart (maybe due to good ad-marketing strategy). The new recommender system seems to be more focused, resulting in a stronger correlation between Add to Cart and Purchase.

The new algorithm seems to be doing a very good job at showing what the customers are searching for (this is inferred from the strong correlation between views, website clicks, add to cart).

The old recommendation system definetly was cost-effective but not as effective in its working as the new one.

### Two-Sample T-Test
Purchase: The new and old system have no significant difference in Purchase rates.
WebsiteClicks: There is no significant difference in WebsiteClicks rates
Reach: The difference in Reach rates between the two systems is statistically significant.
AddtoCart: The difference in AddtoCart rates between the two systems is statistically significant.

Although the old recommender does well in ROI and conversion rate (but again conversion rate is defined by number of website/ad clicks), the CTR is much better with the new system - meaning the new system is showing what the customer wants really well.

My recommendation would be to devise a new marketing strategy or use the same one as with old system for the new recommender system. The new system is doing well in converting viewers to customers and it seems to engage the customers who clicked on the website or links.

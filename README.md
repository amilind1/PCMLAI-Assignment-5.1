# PCMLAI-Assignment-5.1

Findings from data analysis done in the accompanying Jupyter notebook as as follows:

** High Acceptance:
Drivers in these categories tended to accept the Coffee House coupon most of the time:
- Drivers who go to a coffee house more than once.
- age: below21 - 68% (all other ages accepted coupon between 40 to 52% of time. Even for age 21, it dropped to 51%.)
- Drivers not going to an urgent place.
- Drivers who go to medium cost restaurants (Restaurant20To50) more than 4 times.
- At times of 10 AM and 2 PM.
- Drivers travelling with friend(s) or partners. Not with kids or alone.
- Expiration is in 1 day, not in 2 hours.
- Occupations: Healthcare Practitioners & Technical, Healthcare Practitioners & Technical, Transportation & Material Moving, Healthcare Support, Student
Seeing above, a business can consider to send coupon to any combination of these as per the situation / location / target population.

** High rejections:
It is equally important for business to know the categories for which the coupon had low acceptance rate. 
Here are the categories of drivers I found that had higher than 60% rejection rates:
- Drivers who never went to coffee house in past rejected it 82% of times.
- Drivers going home
- Income range of 75000 - 87499 rejected it 70% of times. (I am not sure why that would be... all other income ranges below and above this range accepted their coupon between 45 and 55% of times so no real preference seen in those.)
- Driving time to coupon place is 25 minutes or more.

** Few more notes:

1) In addition to the obvious observation from above that 82% of drivers who never went to coffee house rejected the coupon,
it is also an interesting and useful finding that 18% of drivers who never went to coffee house before were willing to go there with the coupon.
In a way, it tells you size of potential NEW customer base that can be enticed with a coupon.
With this start, some of them could come in future without a coupon.
Also, even during a visit with coupon, they could buy something without a coupon (at regular price) that doesn't qualify for the coupon. LOL.

2) Another point is that there were only 11 drivers in 'Building & Grounds Cleaning & Maintenance' category.
So conclusion for that category from this data may deviate a lot from total real population of this category.
There are more such categories with quite small sample count, so I would rather say that I can not make conclusions about categories from this particular dataset at least.

3) The approach that I used in this notebook to find highest and least acceptance categories can be extended further for
combinations of 2, 3 or more pairs of "metric name"-"category" and see the acceptance rates.
For 2 pairs for example, can prepare a dataframe of all combinations of "metric1-categ1-metric2-categ2" pairs from "all_categ_df" dataframe above.
Then get total count and Y count for that combination "metric1-categ1-metric2-categ2" from the coffee coupon dataframe.
Then calculate the percentages for Y=1 and 0 and sort them to get the highest and least acceptance cases.


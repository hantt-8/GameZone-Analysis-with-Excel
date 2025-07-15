# We’ll use a sample Excel dataset from a company called GameZone.
# They were founded in 2018 and sell gaming products worldwide — both new and refurbished.
# Most of their sales happen through their website, but they also have a mobile app and use different marketing channels.

# This dataset has about 20,000 records.

#DATA CLEANING
*I. Conceptualize the data*
Now — in this step, identify 3 Key items:
	1.	Grain – What does each row represent?
→ one order (Order ID)
	2.	Key Metric – What number matters most?
→ Order price in USD
	3.	Key Dimensions – Descriptive details
→ Date, Product, Platform, Channel, Country

If I were to tell you a quick story from this dataset, it would go like this: 

User 175e placed an order on December 24th, 2020. It was shipped two days later.
They bought a Nintendo Switch for about $170, through the website, using an affiliate marketing link.
We don’t know how the account was created, but we do know they’re located in the United States.

This step Helps us priority know what to clean/check first

Understanding these elements helps us know what matters — and what to clean and check first.

And if we already know the business question, like “How are sales doing in each region?”
Then we focus on the price and geography dimensions to get the answer.

*II. Locate solvable data issues.*

Goal: Find problems we can fix on our own (no need for business input)

These issues usually fall into a few common types: (slides)


How I Look for Issues:
	•	Scan for obvious errors/blank cells
	•	Use filters → check unique values
	•	Track everything in an Issue Log
Solution (read slide)

And one quick note on magnitude:
Magnitude = Problem Size
	•	How many rows are affected?
→ e.g. 50 rows = small
→ 5,000 rows = major
	•	Helps prioritize what to fix first

*III. Evaluate unsolvable data issues.*
Goal: Spot problems we can’t fix alone and you may need help from business team or engineer team who know context and system better to investigate it further.

There are a few common types:

Missing data where we just can’t guess the right value.

Outliers or strange values that might be real, or might be errors — but we’re not sure.

Business logic errors, like a shipping date that’s after the purchase date, which doesn’t make sense.

How do we handle unsolvable issues? 
- document them
- note the magnitude
- ask for more business/data context

*IV. Augment Data. This means Creating new data from existing data.*

Goal: Make the dataset more flexible, useful, and insightful

For example, I can break down purchase dates into weeks, months, or years. I can also create new metrics, like “time to ship,” which measures the days between purchase and shipping.

Add new time grains for purchase date
Add region from region table 
Add new column [Time_to_ship]: operational metric that shows day between purchase date and shipment date

*V. Documenting*
The last step is to go back and finalize it. 

What to include:
	•	How each issue was resolved
	•	Final decisions for each column
	•	% of data affected by each issue

Good documentation isn’t just for others — it also helps future you remember what was done and why.



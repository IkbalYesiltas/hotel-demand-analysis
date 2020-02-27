# Hotel-Booking-Demand-Analysis (Hotel Revenue Management)
Data Analysis of a city hotel located in Lisbon, concluding with business recommendations. 
The data is extracted from: https://www.sciencedirect.com/science/article/pii/S2352340918315191
and includes information about a city and resort hotels bookings made from 2015 to 2017, e.g. time of booking, length of stay, number of adults or children, average daily expenditures, and many more. Analysis was done mainly in Python using the Pandas and Matplotlib Libraries. 

## Motivation
As an aspiring data scientist, I wanted to test my abililites by working on real business datasets and see how I approach real-world problem solving. In my research I found this particular dataset, which is about 2 real hotels based in Algavre and Lisbon, thus including real customer data to work with. To keep the analysis concise I focused mainly on the city hotel in Lisbon.

## Key Questions
The main problem to tackle is a way to `increase Revenues`. To give viable answers to that, we first have to identify particular important variables based on actual guests (those who did not cancel, apart from cancellation questions of course). For instance, 
* Customer/Market Segmentation &rarr; Tailoring the hospitality experience towards an "avg customer" for maximum satisfaction rate
* Distribution Channels &rarr; Identify most frequently used distribution channel and the specific agencies
* Cancellation Rates &rarr; Identify why to come up with countermeasures
* Average Daily Rates &rarr; Find correlations in customer expenditures for the whole stay and determine optimal staying length (promote   these time frames with special offers)

## Analysis
First to work properly we have to clean the data a bit, filling in missing values for e.g. non-agency booking, and eliminating meaningless rows like those that contain not a single guest. 

For starters, we take a look at the customer/market segmentation.<br>By analyzing the data following "stereotypical" guest has been identified:<br>`adult transient travelers, originating from the main european countries, on-the-move and looking for a quick stay-in.`


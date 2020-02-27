# Hotel-Booking-Demand-Analysis (Hotel Revenue Management)
Data Analysis of a city hotel located in Lisbon, concluding with business recommendations. 
The data is extracted from: https://www.sciencedirect.com/science/article/pii/S2352340918315191
and includes information about a city and resort hotels bookings made from 2015 to 2017, e.g. time of booking, length of stay, number of adults or children, average daily expenditures, and many more. Analysis was done mainly in Python using the Pandas and Matplotlib Libraries. 

## Motivation
As an aspiring data scientist, I wanted to test my abililites by working on real business datasets and see how I approach real-world problem solving. In my research I found this particular dataset, which is about 2 real hotels based in Algavre and Lisbon, thus including real customer data to work with. To keep the analysis concise I focused mainly on the city hotel in Lisbon.

## Key Questions
The main problem to tackle is a way to `increase Revenues`. To give viable answers to that, I first had to identify particular important variables based on actual guests (those who did not cancel, apart from cancellation questions of course). For instance, 
* Customer/Market Segmentation &rarr; Tailoring the hospitality experience towards an "avg customer" for maximum satisfaction rate
* Distribution Channels &rarr; Identify most frequently used distribution channel and the specific agencies
* Cancellation Rates &rarr; Identify why to come up with countermeasures
* Average Daily Rates &rarr; Find correlations in customer expenditures for the whole stay and determine optimal staying length (promote   these time frames with special offers)

## Analysis
First to work properly I have to clean the data a bit, filling in missing values for e.g. non-agency booking, and eliminating meaningless rows like those that contain not a single guest. 

### Stereotypical guest
For starters, I took a look at the segmentation and booking channels.<br>By analyzing the data following "stereotypical" guest has been identified:<br>`adult transient travelers, originating from the main european countries, on-the-move and looking for a quick stay-in, favorably booking through a travel agency.`

<img src="/plots/demographics.png" alt="demographics" width="400" height="275"/> <img src="/plots/booking_type.png" alt="booking_type" width="400" height="275"/>
<img src="/plots/countries.png" alt="countries" width="400" height="275"/> <img src="/plots/travel_agencies.png" alt="agencies" width="400" height="275"/>

### Cancellation Rate
Next on the line is identifying the cancellation rate and its potential reasons to come up with countermeasures.<br>
The current rate is at `41.79%` which is roughly <b>3% below</b> the average of 39%!<br>
Potential reasons that were further looked at:
* Too long waiting times until reservation confirmation
* Low number of reoccuring guests 
* Wrong room assignment rate too high
<br><br><br>
Longer waiting times and cancellations have a <b>clear positive correlation</b> as following plot suggests an increase of roughly <b>60%</b> of accumulated waiting time for cancelled bookings.<br>
<img src="/plots/waiting_days.png" alt="waiting_days" width="450" height="275"/>

The rate of reoccurring guest is about `2.5%` which is <b>5.5% below the average</b> of 8% (determined by deloitte study). But to be fair, this may also be due to the fact, that the main customers are transient travellers, so the actual industrial standard of that kind of hotel should be identified for further analysis.<br><br>
Finally, I looked at the room assignment accuracy. How many of the guest did not get the room that they initially booked?<br>
A whopping `8.94%` of the rooms were not delivered while checking in as promised when booking. 

### Average Daily Rate
This metric is defined as the `sum of all lodging transactions / number of stayed nights`, thus being a key performance indicator.
The aim is to maximize the rate of course. <br>
The question I asked myself was then: "<i>Which is the optimal staying length that yields the highest transaction returns?</i>
"<br>
To answer that I plotted 2 graphs indicating for each length of stay the share of guests that booked that time frame and the average ADR  they produced. The following results were returned. <br><br><br>
<img src="/plots/staying_time_and_adr.png" alt="staying_time_and_adr" width="900" height="650"/>

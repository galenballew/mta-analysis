# Deploying street teams
## Identifying target MTA stations by traffic, commuter ridership, and income

Contributors:
* Galen Ballew [LinkedIn](https://www.linkedin.com/in/galenballew) [GitHub](https://github.com/galenballew)
* Ana Gentle [LinkedIn](https://www.linkedin.com/in/ana-elisa-gentle-96262891/en) [GitHub](https://github.com/anaelisagentle)
* Eva Ward [LinkedIn](https://www.linkedin.com/in/eva-ward) [GitHub](https://github.com/emw1687)

**The Challenge:**  
WomenTechWomenYes (WTWY), a non-profit organization in New York City, is raising money for their inaugural girl’s summer coding bootcamp. In order to provide underprivileged girls with scholarships, they need to raise $50,000 at their annual fundraising gala. From their previous galas, WTWY knows women working in tech and attendees with incomes above $200,000 are most likely to donate. To promote the event, street teams are being placed outside subway stations to hand out free gala tickets. In order to optimize the locations of our street teams, we are using MTA turnstile data and census data to locate subway stops in neighborhoods with average incomes of at least $200,000, high commuter ridership, and stops near major tech companies.
  
 **The Toolkit:**
 * Pandas
 * Seaborn
 * Dateutil
 * [MTA Turnstile data](http://web.mta.info/developers/turnstile.html)
 * [American Community Survey Data](https://factfinder.census.gov/faces/nav/jsf/pages/searchresults.xhtml?refresh=t)
 
**The Approach:**
 1. Pass station names to the Google Maps API and return matching zip codes
 2. Parse ACS data for zip codes with commuting to work > 68% and household income > $200k
 3. Append Station <---> Zip code Series (*Step 1*) to MTA dataframe
 4. Filter by zip codes gathered in *Step 2*
 5. Create visualizations to compare stations by date and time
 
**The Results:**  
We arrived at a meaningful list of four top canidate stations and their best days and times to be stationed at. Out of the four, we recommended three to our client. The fourth station that was left out was actually the highest in daily/hourly traffic, but lacked the qualitative assets the other three stations shared in common. It was important to recognize the diminishing returns on foot traffic at the stations - our clients employees can only approach and engage with so many people at one time. At some point, having more people in the station will not increase customer engagement and may actually *reduce* it due to the busy environment. 

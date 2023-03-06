# Metro Bike in Austin,TX

## The Take Aways

<!-- wp:paragraph -->
<ul><li>Data showed that a pilot program offering a free annual student membership and infrastructure investments were catalysts for the ridership surge in 2018. </li><li>Geospatial analysis of total rides by kiosk location revealed both the impact of the university pilot program and the Covid-19 pandemic.</li><li>To increase MetroBike ridership, future infrastructure projects should consider zones near colleges and introduce seasonal promotions or special events for the off-months of November, December, and January.</li></ul>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2>Introduction</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Austin is an emerging IT center after San Francisco. I am planning a summer internship or a full time job in Austin after graduation. I was curious about Austin's transportation infrastructure, so I did a casual project.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Austin, TX, USA is a car-centric city. In 2019, the city estimated that 74% of Austin residents commuted to work alone by car [1]. To manage its ever-growing traffic congestion, the City of Austin has been investing in the expansion of its public transit, city bikeways, and urban trails. The intention is to increase transportation options, to ultimately broaden the transportation behavior of its residents, and increase commuters that use public transit, walk, scoot, or bike.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>In summer 2020, the City and the Capital Metropolitan Transportation Authority (CapMetro) entered into a partnership with the local nonprofit Bike Share of Austin [2]. This partnership rebranded the nonprofit's bike-share program, previously called Austin B-cycle, as MetroBike. The partnership’s goal was to broaden the bike-share system and integrate it into the larger CapMetro public transit ecosystem [2].</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2>Key Business Objective</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>The project objective was to identify actionable steps to increase MetroBike ridership. Ridership generally refers to the number of individuals using a given transit program and here is represented by annual total trips. As a result, the data analysis aimed to understand what underlying factors contributed to increases and decreases in annual total trips taken during the years 2014-2020.</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2>Datasets</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Two datasets were downloaded from [online] austintexas.gov. Available at: &lt;https://https://data.austintexas.gov/browse?q=&sortBy=relevance> on March 1, 2023, respectively:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><li>Austin MetroBike Trips</li><li>Austin MetroBike Kiosk Locations</li><li>Community Survey</li></ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>In the Austin MetroBike Trips dataset, each row is an individual trip taken. There were 1,424,786 trips between 2013 and 2021.</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2>Data Cleaning</h2>
<!-- /wp:heading -->

<!-- wp:list -->
<ul><li>For the trips dataset, trip duration was used as an inclusion criteria. Trip duration is the span of time elapsed between checking a bike out of a kiosk station and returning it to a kiosk station. Only trips with durations greater than zero minutes and less than 11,520 minutes (8 days) were included. The zero minute and greater than 8-day trips were deemed to be potentially erroneous. These criteria removed 21,770 trips from the dataset.</li><li>For the trips dataset, the Checkout Kiosk Identification (ID) numbers were examined for missing data. Checkout Kiosk IDs were missing for 22,773 trips. To address this, these trips were linked to their kiosk ID number using their associated kiosk name. This procedure added a Checkout Kiosk ID number for 20,996 trips. 

The remaining 1,777 trips with missing Checkout Kiosk ID numbers were mobile stations used for special events. These mobile kiosks do not have ID numbers.  

Lastly, several Checkout Kiosk ID numbers were modified to ensure agreement with the ID number listed in the MetroBike Kiosk location dataset.</li><li>Two kiosk stations were added to the Kiosk location dataset. These kiosks stations were found in the Trips dataset but were missing from the Kiosk location dataset. These kiosks were “4th/Sabine” and “22.5/Rio Grande”.</li></ul>
<!-- /wp:list -->


<!-- wp:heading -->
<h2>Data Analysis</h2>
<!-- /wp:heading -->

<!-- wp:heading -->
<h3>Annual Total Trips</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>The annual total trips demonstrated a large surge in 2018, followed by decreases in both 2019 and 2020 (Fig. 1). Considering these results, this project sought to understand what factors may have contributed to the increase in 2018 and the decreases in 2019 and 2020.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>More specifically, the project's analyses focused on factors related to MetroBike physical infrastructure and customer behavior. The metrics included: total number of bikes, total number of kiosk locations, most popular membership types, total trips by month, and the top four kiosk stations by rides for each year.</p>
<!-- /wp:paragraph -->


<!-- wp:heading -->
<h2>Results</h2>
<!-- /wp:heading -->

<!-- wp:heading -->
<h3>The Infrastructure</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>The number of unique bike IDs rented was used as an indicator of the size of the MetroBike fleet. In 2018, the number of bikes increased by 609 bikes or 142% compared to 2017. The following years, 2019 and 2020, the bike fleets were smaller by 489 and 335 bikes respectively, compared to 2018</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The number of kiosk station IDs used to rent a bike was used as an indicator of the number of kiosk stations available. In 2018, the number of kiosk stations increased by 20 locations compared to 2017</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Moreover, in 2018, nine of the new kiosk stations were added on the University of Texas at Austin campus (informally known as UT Austin) and in the adjacent neighborhood of West University (Fig. 4). In Figure 4, the black circles are kiosk stations that remained the same between 2017 and 2018. New kiosk stations are indicated by a green circle and a “+” symbol. Removed kiosk stations are indicated by a red circle and a “-” symbol.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>However, since 2019, the number of kiosk stations has remained constant at 76 locations</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h3>Customer Behavior</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Between 2017 to 2020, the most popular membership type used to purchase a MetroBike pass was the UT Student Membership, followed by the Walk Up, Local365, Local30, and Weekender memberships</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Examining these membership types by year revealed that the UT Student Membership dominated in 2018 but declined in 2019 and 2020</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Considering the fluctuations in annual total rides, monthly ridership was examined for the years 2018 and 2019. For both years, the most popular months for trips were March, April, and May. For 2018, the months with the fewest rides were November, December, and January. In 2019, the months with the fewest rides were November, December, and August</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h3>Top Kiosk Locations</h3>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>The most popular kiosk stations between 2017 and 2020 are listed.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>For Figures 8-11, the kiosk locations are overlaid on a neighborhood map of Austin. At each kiosk station, an individual black bubble is displayed. The relative size of each bubble represents the number of trips at that particular kiosk checkout station for the given year. Additionally, the bubbles with a green circle at their center are the most popular kiosk stations for that particular year.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>In 2017, the top four kiosk stations were located on the south-side of Downtown and near a popular trail loop that runs along the Colorado River. These particular locations are near entertainment or parks and recreation areas.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>In 2018, the top four kiosk stations were located on the UT Austin campus or in the West University neighborhood (Fig. 9), the latter is an area near the university that is commonly known for student housing and amenities.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>In 2019, the top three kiosk stations were again located on the UT Austin campus or in the West University neighborhood. However, the fourth location was in the Zilker neighborhood, near the trail loop, primarily an entertainment or parks and recreation location.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>In 2020, the top four kiosk locations were south of Downtown and near the trail loop. This indicates a shift from campus life to entertainment or parks and recreation areas.</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2>Discussion</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>In 2018, Bike Share of Austin added nine kiosk stations on or near the UT Austin campus [3]. This infrastructure expansion was part of a pilot program to provide more mobility options to students. The program also created the UT Student Membership type which offered a free annual membership. This program was hugely successful with 63% of the total rides in 2018 attributed to UT Student Membership. Moreover, that same year, the top four most popular kiosk stations were on the UT Austin campus or in the adjacent West University neighborhood.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The pilot program ended in 2019, and the UT Student membership was offered to students for $12 per year [4]. Although the drop in ridership cannot be directly attributed to the program’s discontinuation, annual total trips and UT Student membership trips decreased by 71% and 84% respectively. The approximate size of the bike fleet also decreased by 47%. To be fair, the latter could have been the result of decreased bike demand. That all said, in 2019, three of the top four kiosk stations were, nevertheless, in or near the UT Austin campus area. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>In 2020, annual MetroBike ridership continued to be low (Fig 1). In contrast to 2018 and 2019, the most popular kiosk stations were no longer on or near the UT Austin campus but instead were south of Downtown. This shift is logical because UT Austin’s courses went virtual in mid-March 2020 as a result of the Covid-19 pandemic. Virtual course work continued in the summer semester and was prevalent in the fall semester as well. It also makes sense that the most popular kiosk locations were in entertainment or parks and recreation areas as more activities moved outdoors during the pandemic.</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2>Recommendations to Increase Ridership</h2>
<!-- /wp:heading -->

<!-- wp:list -->
<ul><li>Perform an inquiry into the downturn in UT student memberships since 2019. Example questions: How many UT students and staff have applied for the $12 per year membership? What percentage of the applications have been approved? How is the membership advertised?</li><li>Introduce seasonal promotions to increase ridership during off-months (Fig. 7). The months November, December, and January are great candidates. During these months, there can be periods of mild weather in Austin when biking could be potentially comfortable.</li><li>Introduce kiosk stations in areas that are densely populated by university students or near campuses. Even in 2019, which had an 84% drop (Fig. 6) in student membership ridership compared to 2018, three of the most popular kiosk stations were around a university campus (Fig. 10). For UT Austin, example neighborhoods would be Hyde Park and Hancock which are north of campus.</li></ul>
<!-- /wp:list -->

<!-- wp:heading -->
<h2>References</h2>
<!-- /wp:heading -->

<!-- wp:list -->
<ul><li>The City of Austin. (2019, April 11). Austin Strategic Mobility Plan Executive Summary and Introduction. The City of Austin. [Link](https://www.austintexas.gov/sites/default/files/files/Transportation/ASMP/ASMP_Chapters/AdoptedASMP_Executive_Summary_and_Introduction.pdf)</li><li>Thornton, R. (2020, September 25). Austin B-cycle rebranded as MetroBike. Austin Monitor. [Link](https://www.austinmonitor.com/stories/2020/09/austin-b-cycle-rebranded-as-metrobike/)</li><li>Pritchard, C. (2018, February 16). B-cycle goes to school. Austin Monitor. [Link](https://www.austinmonitor.com/stories/whispers/b-cycle-goes-school/)</li><li>Barton, J. (2019, January 23). Austin B-Cycle ends free student membership after University refuses funding operating costs. The Daily Texan. [Link](https://thedailytexan.com/2019/01/23/austin-b-cycle-ends-free-student-membership-after-university-refuses-funding-operating/)</li></ul>
<!-- /wp:list -->

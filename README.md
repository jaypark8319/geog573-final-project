Researching Gerrymandering in the 2024 South Korean Legislative Election


Objective: 
We endeavor to analyze the impact of gerrymandering in South Korea’s legislative election in 2024. We will look at the district boundaries, demographics, and vote distribution. The end goal of our study is to determine how the voting districts were divided in favor of certain parties based on demographics and partisanships of regions. 
Background:
The legislative election of 2024 was essentially an election of 22nd Congress of South Korea. The Democratic Party, the opposition to the incumbent party, won with 171 seats. The incumbent party, People’s Power Party,  won 108 seats. There were several independent parties aligned with the two parties aforementioned that won seats that totaled to 300 seats. 
Methods:
●	Data - We sourced several CSVs with the election results for the nationwide results and then the results for the individual candidates. We also sourced a JSON file and various csv files representing the electoral districts across South Korea. 
●	Geospatial Analysis - Utilized the geopandas package to view districts and used esda.moran to cluster regions based on their own and neighbors’ values. 
●	Quantitative Analysis - Use efficiency gaps to view any partisan gaps and advantages. 
Expected Outcomes:
●	We are conducting a model that would detect the partisan gerrymandering of certain elections, based on U.S. standards and we will use the data we collected to prove the validity of our model. 
Data Sources:
●	22nd Congressional Election of South Korea precinct-level returns (raw_result.csv): 
https://nec.go.kr/site/nec/ex/bbs/View.do?cbIdx=1084&bcIdx=265654

●	22nd Congressional Election of South Korea returns by eupmyeondong (2024_22_Elec_simplify.json, 22_Elec_SGG.csv): 
https://github.com/OhmyNews/2024_22_elec_map

Results:  
We started with the vote and wasted vote analysis. Through our data, we collected the total votes for both major parties (DP and PPP) across every district. To start, we calculated wasted votes for each district. For the winning party this was defined as all votes beyond what was needed to win the First Past the Post format. For the losing party every vote was considered wasted. It was discovered that in several districts there were large discrepancies. Specifically in Seoul and Gwangju, there were 57,578 and 38,455 wasted votes in relation to the other party.
Next we looked at the efficiency gap to evaluate fairness. Note that positive values indicate DP bias and negative values for PPP. We found that DP had a large bias in Gwangju (.314), Busan (.364), and Ulsan (.275). The PPP had a large bias in Gyeonggi (-.293), Daejeon (-.382), and Incheon (-.262). This indicates that in the capital region, the PPP has an advantage as well as in the central part of the nation. The DP has an advantage in the north and south western parts of the nation. 
Finally we can look at the maps we have created. We can see that the large chunks of the nation are highly biased in voting discrepancy. This corroborates our quantitative findings above. 

	Our results signify a significant imbalance in electoral fairness throughout the nation. The nation’s mixed member electoral system is designed to balance representation, but the numerous measurable efficiency gaps show uneven vote weight. These results are not definitive proof of intentional gerrymandering, our analysis points to system bias in voting distribution

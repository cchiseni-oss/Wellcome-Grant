Journal of Economic Growth (2022) 27:149–192 https://doi.org/10.1007/s10887-022-09202-8 

# **The economics of missionary expansion: evidence from Africa and implications for development** 



### **Remi Jedwab**<sup>**1**</sup> **· Felix Meier zu Selhausen**<sup>**2**</sup> **· Alexander Moradi**<sup>**3**</sup> 

Accepted: 22 January 2022 / Published online: 7 April 2022 © The Author(s) 2022, corrected publication 2022 

### **Abstract** 

How did Christianity expand in Africa to become the continent’s dominant religion? Using annual panel census data on Christian missions from 1751 to 1932 in Ghana, and pre1924 data on missions for 43 sub-Saharan African countries, we estimate causal effects of malaria, railroads and cash crops on mission location. We find that missions were established in healthier, more accessible, and richer places before expanding to economically less developed places. We argue that the endogeneity of missionary expansion may have been underestimated, thus questioning the link between missions and economic development for Africa. We find the endogeneity problem exacerbated when mission data is sourced from Christian missionary atlases that disproportionately report a selection of prominent missions that were also established early. 

**Keywords** Economics of religion · Religious diffusion · Human capital · Economic persistence · Measurement · Historical data · Atlases · Missions · Christianity · Africa 

**Mathematics subject classification** O10 · O40 · Z12 · I20 · N30 

## **1 Introduction** 

One of the most powerful cultural transformations in modern history has been the rapid expansion of Christianity to regions outside Europe. Conversion has been markedly rapid in sub-Saharan Africa. While Christians made up about 5% of the population in 1900, their share has grown to 57% today (Johnson and Grim 2020), making Africa the continent with 

> * Alexander Moradi Alexander.Moradi@unibz.it 

Remi Jedwab jedwab@gwu.edu 

Felix Meier zu Selhausen felix.meierzuselhausen@wur.nl 

- 1 Department of Economics, George Washington University, Washington D.C., USA 

- 2 Rural and Environmental History, Wageningen University, Wageningen, The Netherlands 

- 3 Department of Economics, Free University of Bozen-Bolzano, Bolzano, Italy 

Vol.:(0123456789)1 3 

Journal of Economic Growth (2022) 27:149–192 

150 

the highest number of Christians (Todd et al. 2018). At current trends, Africans will comprise 42% of the global Christian population by 2060. According to the World Values Survey, sub-Saharan Africa is also home to the world’s most observant Christians in terms of church attendance, making it “the future of the world’s most popular religion” (Economist 2015). 

The process of African mass-conversion was facilitated by vast Christian missionary efforts. Throughout the colonial era missions provided the bulk of formal education (Frankema 2012; Cogneau and Moradi 2014) and health care (Doyle et al. 2020). A recent and rapidly growing literature explores the long-term effects of missions in colonial Africa, as well as in India and Latin America. Web Appx. Table A1 summarizes 50 studies that 2015; Castelló-Climent find strong effects on local economic development (Bai and Kung et al. 2018; Valencia Caicedo 2019a), education (Gallego and Woodberry 2010; Acemoglu et al. 2014; Waldinger 2017; Baten et al. 2021; Calvi et al. 2021), health (Calvi and Mantovanelli 2018; Cagé and Rueda 2020; Menon and McQueeney 2020), fertility (Guirkinger and Villar 2022), social mobility (Wantchekon et al. 2015; Alesina et al. 2021), culture (Nunn 2010, 2014; Fenske 2015; Calvi et al. 2022), and political participation (Cagé and Rueda 2016).<sup>1</sup> 

While a large literature has studied the economic consequences of evangelization, the economics behind the expansion of Christianity remains poorly understood. One narrative describes missionaries as adventurers, with little to no information on local circumstances, crossing political boundaries and whose objective was to save souls no matter the cost (Oliver 1952; Cleall 2009). Their locational choices were highly erratic, but once settled, missions persisted. For example, Wantchekon et al. (2015, p. 714) describe how a series of historical accidents led missionaries to settle left rather than right of a river. An alternative view is that missionaries were following clear expansion strategies laid out by their own mission society (Johnson 1967; Terry 2015). For example, missionary Thauren (1931, pp. 19-20) described the strategy in Togo as follows: 

“The mission leadership knew that choosing suitable places would be crucial for missionizing the interior. Therefore, no effort was spared to get to know the interior better [...]. The mission society aimed to establish new stations in larger cities, so that few missionaries could spread the gospel to many. In particular, they preferred cities with regular markets. Moreover, the places needed to be centrally located [...].” 

Missions also aimed for financial independence, which would make them target wealthy locations. To our knowledge, the causal determinants of mission expansion have not been studied.<sup>2</sup> 

In this paper, we study the determinants and effects of missionary expansion in Ghana and sub-Saharan Africa as a whole. For various reasons, Ghana is an ideal testing ground. First, Ghana is one of the most devout Christian African countries today.<sup>3</sup> Second, Ghana received missionaries since the early 19th century, which allows us to investigate the role of quinine as a groundbreaking treatment for malaria ca. 1850. Missionary expansion in 

> 1 See Valencia Caicedo (2019b) and Meier zu Selhausen (2019) for surveys of the literature on missionary legacies. 

> 2 Nunn (2010) and Cagé and Rueda (2016) examine the effects of factors such as population density, urbanization, railroads, explorer routes, malaria and slavery. However, their quantitative analyses are not dynamic, nor causal. 

> 3 The Economist. _True Believers: Christians in Ghana and Nigeria_ . September 5th 2012. 

1 3 

Journal of Economic Growth (2022) 27:149–192 

151 

East Africa began later in the 1890s. Third, in Ghana missionaries operated in a comparatively free religious market with little interference by the colonial state (Gallego and Woodberry 2010).<sup>4</sup> Finally, Ghana holds rich historical data. Altogether, this enables us to shed light on a wide range of determinants of mission expansion. 

For Ghana, we create a novel annual panel dataset on the locations of missions at a precise spatial level over two centuries: 2091 grid cells of 0.1 × 0.1 degrees (12 × 12 km) in 1751–1932, when the number of missions increased from one to 1,832. Creating new data on the determinants of mission locations, descriptive results suggest that missionaries might have gone to healthier, more accessible, and richer areas, privileging these “better” locations first. They might also have invested more into these missions/locations (with administrative functions, European missionaries and schools). These results are confirmed using identification strategies for malaria, railroads, and cash crops, in Ghana, but also in sub-Saharan Africa. 

Once missionary expansion is better understood, we can study the long-term effects of missions. With a few exceptions, existing studies do not analyze the effects of missions on economic development _per se_ , focus on one mechanism at a time, and, more importantly, use data from mission atlases that are marred by omissions (see Web Appx. Table A1). Figure 1a plots the mission locations obtained from the two most commonly used sources: (i) the _Atlas of Protestant Missions_ (Beach 1903), first used by Cagé and Rueda (2016), and (ii) the _Ethnographic Survey of Africa_ (Roome 1925), digitized by Nunn (2010, 2014).<sup>5</sup> Using ecclesiastical census returns and other primary sources instead, we uncover vast discrepancies. Figure 1b shows that atlases omit more than  90% of missions in most African countries.<sup>6</sup> Beach (1903) and Roome (1925) imply congregation sizes of more than 3,000 and 15,000 per mission station respectively.<sup>7</sup> For Ghana, the two atlases miss 91–98% of missions, most of them in the hinterland (see Fig. 2a–b). Our census data suggest an average congregation size of 198 in 1925, which appears far more plausible.<sup>8</sup> 

We discuss the implications of the observed patterns of missionary expansion and the over-reliance on mission atlases for the study of the long-term effects of missions. We highlight three sources of endogeneity: (i) attenuation bias, (ii) selection bias, and (iii) omitted variable bias. 

First, we scrutinize the standard source of mission data. Atlases do not show the distribution of the universe of missions. Classical measurement error would lead to attenuation bias. However, measurement error may be non-classical, e.g. if omissions are not random. 

> 4 In contrast, Belgian, Portuguese and Spanish colonies granted Catholic missions a quasi-monopoly (Meier zu Selhausen 2019). French colonies followed from the 1890s on a more neutral treatment of missionaries in that they restricted most of the activities of both Catholics and Protestants (Sundkler and Steed 2000, p. 430). 

> 5 30 studies use Roome (1925), 6 studies use Beach (1903), 5 use Bartholomew et al. (1911), and 6 use Streit (1913). 

6 Weighting the country-specific omission rates in Beach (1903) and Roome (1925) by the countries’ population ca. 1920 (Frankema and Jerven 2014), we find for the whole of sub-Saharan Africa that 76% of Protestant missions are missing from Beach (vs. 91% for Ghana) and 91% of them are missing from Roome (vs. 98% for Ghana). 

7 Beach (1903) and Roome (1925) report 677 Protestant and 1,212 Christian mission stations respectively. According to the World Christian Database (Johnson et al. 2021), Protestants in 1900 numbered 2.2 million. For the year 1925, there were an estimated 20.2 million Christians in sub-Saharan Africa (excluding Ethiopia). 

8 Bartholomew et al. (1911) and Streit (1913) then miss circa 85–95% of missions in China, India, Korea, and Japan. 

1 3 

Journal of Economic Growth (2022) 27:149–192 

152 

We use our _census_ -based data on Ghana to show that atlases _positively_ select missions, in particular early, main or European residence missions located in more developed areas. This would bias estimates upward. 

Next, we examine whether the source of mission data affects the estimated long-term impact of missions in Ghana. Employing the control variables commonly used in the literature on missions in Africa (e.g., Nunn 2010, 2014; Cagé and Rueda 2016), we find strong effects that are twice as large for atlas missions than for census missions. If we use a rich and historically relevant set of control variables, estimated effects are considerably weaker. This also applies to Africa as a whole. 

Our interpretation is that mission atlases, because they report “better” missions endogenously located in “better” places, may capture effects that are not due to the missions themselves. Moreover, relying on atlases raises concerns of external validity. Estimated effects are measured for a selected subset of missions that are not representative of the _average_ mission. To measure causal long-term effects of missions, one must properly control for the spatio-historical determinants of missions, or use an identification strategy that can be implemented even with imperfect historical controls. While a handful of studies have relied on innovative identification strategies (e.g., Wantchekon et al. 2015; Cagé and Rueda 2016; Waldinger 2017; Valencia Caicedo 2019a)<sup>9</sup> , many studies use some controls and sometimes add spatial fixed effects. 

Our contribution is threefold. First, our paper relates to the literature on the determinants of the adoption and diffusion of religion (Bisin and Verdier 2000; Barro and McCleary 2005; McCleary and Barro 2006; Becker and Woessmann 2013; Becker et al. 2017). There are few quantitative works on religious diffusion, and none for sub-Saharan Africa. Michalopoulos et al. (2018) pointed to the role of geography and trade in the diffusion of Islam. Cantoni (2012) linked the spread of Protestantism in 16th century Germany to strategic choices of territorial lords, while Rubin (2014) shows that Protestantism followed cities’ adoption of the printing press. We show that in Africa Christianity spread along railroads, with the cultivation of cash crops, and with economic development more generally, before it diffused more broadly. 

Second, our contribution is methodological. Non-classical measurement error in historical data and their consequences for the analysis of path dependence are under-investigated. Measurement error in survey data, in contrast, has received a lot of attention (e.g. Bollinger 1996; Mahajan 2006). We emphasize the importance of: (i) reliable mission data, especially given external validity issues; (ii) relevant controls capturing the dynamics and factors behind missionary expansion; and, when needed, (iii) identification strategies that bypass issues related to these measurement issues. 

Finally, we add to the literature on the long-term impact of missions.<sup>10</sup> A large body of literature has found positive effects on various proximate determinants of economic growth (Web Appx. Table A1). Missions were the most important human capital promoting institutions to have emerged in developing countries during the colonial era. By shaping 

> 9 Wantchekon et al. (2015) rely on control villages that were as “as likely to be selected” as the villages with a mission. Cagé and Rueda (2016) compare different types of investments between missions. Valencia Caicedo (2019a) and Bergeron (2020) compare mission locations to places that missions abandoned for exogenous reasons. Valencia Caicedo (2019a) and Jedwab et al. (2021) compare locations exogenously evangelized by different denominations. Finally, Waldinger (2017) and Jedwab et al. (2021) exploit the initial directions of missionary expansion paths. 10 For seminal studies on the impact of the Reformation, see Becker and Woessmann (2009); Becker et al. (2016). 

1 3 



<!-- Start of picture text -->
(a) Missions Reported in Mission Atlases (b) Share of Omitted Missions in Mission Atlases<br>es<br>rs<br>8<br>f . A Zo<br>%, 2 oo<br>Beach in 1900 A pe TOS Bie « &<br>(Protestants) sete She gS Dy gue OS<br>* Roome in 1924 3a2 Pebtcate) ue oatsate? °g<br>(Protestants& Catholics) +"3 wa 3 4 YF ra<br>car poo i © < ZzaZ2R 929<br>eee aeons E x : 939 Z5Q<br>Syst Beach in 1900 (Protestants) JJ Roome in 1924 (Protestants & Catholics)<br><!-- End of picture text -->



<!-- Start of picture text -->
(a) Comparison in 1900 (b) Comparison in 1924<br>+<br>+ poms<br>+ + e + ee<br>+ + +<br>+ + r o<br>toe+ + 4 ¢<br>¢ +<br>+ ewe? ary Gee ” “<br>Ou oore )<br>¢@ Beach in 1900 (Protestants) @ Roome in 1924 (Protestants & Catholics)<br>Our Data in 1900 (Protestants) Our Data in 1924 (Protestants & Catholics)<br><!-- End of picture text -->

Journal of Economic Growth (2022) 27:149–192 

154 

Becker et al. 2017 ). With our improved data we find comparably weaker long-term effects of missions in Ghana and Africa.<sup>11</sup> 

## **2  New data on Ghana and Africa** 

To examine the determinants of missionary expansion, and draw implications for the analysis of long-term development, we require data on the location of missions over time, the locational factors potentially driving missions’ spatial expansion, and local economic development today. The Web Appendix provides more details on sources. Appx. Table A2 shows summary statistics. 

**Missions in Ghana.** We partition Ghana into 2091 grid cells of 0.1 x 0.1 degrees (12 x 12 km) and construct an annual panel data set from 1751 to 1932 (181 years). Merriam-Webster (2020) defines a mission station as “a place of missionary residence in or from which missionary activity in a given area is carried on.” We recreate the history of every mission station (N = 2144) for all mission societies (classified as Presbyterian, Methodist, Catholic and other) and geocode their locations. Our main sources are the _ecclesiastical census_ returns published in the _Blue Books of the Gold Coast_ , 1844–1932 (see Web Appx. Fig. A1 for an example). Each mission society was required to submit annual reports on its activities to the colonial administration, thereby listing all of their stations. Churches received annual grants from the colonial government for their pastoral services, which provided a strong incentive to report. Our data thus represents an _exhaustive census_ of missions. The early origins of mission societies are then well documented by society-specific anniversary reports, and we have no difficulties reconstructing missions before 1844. 

Using the same sources, we identify if a mission was a _main station_ or an _out-station_ . Main stations are the principal centers of a “circuit” - a society’s administrative unit. Main stations are larger and centrally located (Thauren 1931); they are headed by an ordained missionary. The congregations of out-stations are smaller but still of significant size and taken together have more members than main stations. All mission posts, not just main stations, built churches.<sup>12</sup> 

We also identify if a mission had a _school_ . We focus on “assisted schools”, which followed the government school curriculum and certified quality standards (Williamson 1952). As they received grants-in-aid, they were reported accurately. The existing mission 

11 Within the Unified Growth Theory (UGT) literature (see Galor 2005, 2011 for surveys), various studies examine how the emergence of human capital promoting institutions has affected the pace of the transition from stagnation to growth (Galor 2011). These studies have focused on the expansion of public schooling, such as the creation of a publicly supported secondary school system in the U.K. in 1902 (Galor and Moav 2006) and the U.S. High School Movement in the first half of the 20th century (Moav and Vollrath 2009). The weak long-term economic effects of colonial missions in Africa could be due to African countries having not yet fully entered the process of human capital demanding “industrialization” (see, for example, Gollin et al. 2016) that the UGT has shown to be the main driver behind human capital formation and the demographic transition, and thus the transition to modern economic growth. 

12 Typically, the first investment of every mission post was to build a church. For some years in the 1860s and 1870s, the ecclesiastical returns report the type of building, attendance and seat capacity of the mission post, the latter being a measure of how large the church building was. In 1867, 5% and 8% of Wesleyan and Presbyterian mission stations only had a “house” or a “room” respectively. Not only is this a small percentage, it is also of transitory nature. Within 10 years, all those stations had a church building. Seat capacity and attendance are strongly correlated. 

1 3 

Journal of Economic Growth (2022) 27:149–192 

155 

literature has not distinguished between main, out-stations and schools. We follow this decision in our main analysis. However, we will also study heterogeneous effects with respect to the type of mission. 

**Missionaries in Ghana.** We create a data set of all 338 male European missionaries stationed in Ghana during 1751–1890 from a variety of sources (data not available post1890). For the mortality analysis in Sect. 3, we reconstructed dates of service and death in Ghana. African missionary careers are less well-documented. From the Blue Books 1846–90, we retrieved the localities where European missionaries were permanently based and which missions they served occasionally.<sup>13</sup> 

**Locational Factors for Ghana.** We construct a GIS data set at the same grid resolution: (i) _Geography:_ Historical malaria intensity (based on genetic data) comes from DepetrisChauvin and Weil (2018). We compute the distance to the coast and obtain ports c. 1850 from Dickson (1969); (ii) _Political conditions:_ Data on large pre-colonial cities before 1800 are from Chandler (1987) and headchief towns in 1901 are from Guggisberg (1908). From Dickson (1969), we derive the boundary of the Gold Coast Colony established by the British c. 1850; (iii) _Transportation:_ We obtain from Dickson (1969) navigable rivers in 1850–1930 and trade routes circa 1850. Railroads (1897–1932) and roads (1932) come from Jedwab and Moradi (2016); (iv) _Population:_ From census gazetteers, we compile a GIS database of towns above 1000 inhabitants in 1891, 1901 and 1931. We also collect rural population data for 1901 and 1931. Because all cells have the same area, population levels are equivalent to densities;<sup>14</sup> (v) _Economic activities:_ Slave export and slave market data come from Nunn (2008) and Osei (2014) respectively. We obtain cash crop production areas from Dickson (1969) and total export value of cash crops from Frankema et al. (2018).<sup>15</sup> Mines are from Dickson (1969); and (vi) _Other:_ We obtain area, mean annual rainfall (mm) in 1900–1960, mean altitude (m), ruggedness (standard deviation of altitude), and soil fertility. 

**Contemporary Data for Ghana.** We use satellite data on night lights in 2010 as a proxy for local economic development (NGDC 2015). We use the radiance calibrated version of this data, to avoid issues related to top-coding.<sup>16</sup> Census data on religion, education, fertility, mortality, employment and urbanization in 2000 are from Ghana (2000). To study child mortality, we use seven _Demographic and Health Surveys_ (DHS) between 1993 and 2017 (USAID 2020).<sup>17</sup> 

**Data for Africa.** We compile data for 203,574 grid cells of 0.1 x 0.1 degrees (12 x 12 km) for 43 sub-Saharan African countries. The Blue Books of the Gold Coast (Ghana) are exceptionally rich in detail. Blue Books of other British colonies do not list 

> 13 This data captures Protestant missions only because Catholic expansion came after 1890. Missionary wives resided with their husbands. Unmarried female missionaries were comparably few during the 19th century (Schott 1879). 

> 14 While we have exhaustive urban data for all census years, we only have georeferenced rural population data for Southern Ghana in 1901. We thus include a dummy if any locality in the cell was surveyed by the 1901 census. 

> 15 We obtain soil suitability for the same cash crops from the _1958 Survey of Ghana Classification Map of Cocoa Soils for Southern Ghana_ , Survey of Ghana, Accra, as well as Gyasi (1992) and Globcover (2009). 16 This data records levels of luminosity beyond the normal digital number upper bound of 63. 

17 Since we only have data for 10% of the population census, the most rural cells of our sample do not have enough observations to correctly estimate these shares. We keep 1895 cells with at least 10 observations. When using the DHS, we keep cells with at least 5 children. Due to the smaller sample size, we must indeed adopt a smaller threshold. 

1 3 

Journal of Economic Growth (2022) 27:149–192 

156 

each station systematically over such a long period. Yearbooks of other colonies are completely silent. We thus use mission location data widely used in the literature. These stem from mission atlases. (Fahs 1925, p. 271) writes that these atlases are based on “hundreds of documents” and “society field reports” and admits “problems of what to include in or to exclude (...).” Keeping this caveat in mind, we use Beach (1903), compiled by Cagé and Rueda (2016), which reports the locations of 677 Protestant missions in 1900, and added the year of foundation ourselves. We then use Roome (1925), digitized by Nunn (2010), which shows the respective locations of Catholic and Protestant missions in 1924 (N = 1212). 

The set of locational factors for Africa follows the one for Ghana: (i) _Geography:_ Historical malaria intensity is from Depetris-Chauvin and Weil (2018) and tsetse fly ecology from Alsan (2015). We compute distance to the coast, and 19th century slave ports are from Nunn and Wantchekon (2011); (ii) _Political conditions:_ Data on large pre-colonial cities before 1800 are from Chandler (1987). Data on the capital, largest and 2nd largest cities come from Jedwab and Moradi (2016). The year of colonization for each ethnic group is from Henderson and Whatley (2014). Using the Murdock (1967) map of ethnic boundaries (Nunn 2008), we then assign a year of colonization to each cell. From the same sources, we know if the cell was in an ethnic area with a centralized state before colonization. We compute the distance to historical Muslim centers based on Ajayi and Ade and Michael Crowder, (1974) and Sluglett (2014); (iii) _Transportation_ : We obtain navigable rivers and lakes from Johnston (1915), pre-colonial explorer routes from Nunn and Wantchekon (2011) and railroads from Jedwab and Moradi (2016); (iv) _Population:_ We control for population density c. 1800 and log urban and rural population c. 1900 from HYDE (Goldewijk et al. 2010), and log city population c. 1900 for towns above 10,000 from colonial administrative sources;<sup>18</sup> (v) _Economic activities:_ We know if slavery and polygamy was historically practiced (Murdock 1967). The log number of slaves exported per land area is from Nunn and Wantchekon (2011). Land suitability measures for various cash crops are from FAO (2012). We obtain cash crops’ national export value in 1850–1924 (Frankema et al. 2018). Mines in 1900 and 1924 come from Mamo et al. (2019); (vi) _Other:_ We obtain area, mean annual rainfall (mm, 1900–60), mean altitude (m), ruggedness, and soil fertility.<sup>19</sup> Finally, we also use satellite data on night lights in 2010 (NGDC 2015). 

## **3  Background: missionary expansion in Ghana** 

**Colonization.** Since the 15th century European powers had established trading posts along the West African coast. By 1821, Britain had established an informal protectorate “ the Gold Coast ” in the coastal regions of Ghana. In 1874, the British defeated the inland Ashanti Kingdom centered around its capital Kumasi. The ensuing peace treaty of 1875 transformed the protectorate into a formal British colony with the same boundaries, the Gold Coast Colony. Between 1896 and 1900, two wars with Ashanti eventually forced the kingdom into a colony in 1902. British control was extended to the north at this occasion. 

> 18 Goldewijk et al. (2010) do not rely on census data for earlier centuries (there were no censuses then). These population estimates are unreliable. We nonetheless use them when replicating controls used in the literature. 

> 19 We also add a dummy if the main ethnic group in the cell has data in the Murdock (1967) Atlas and a dummy if the underlying anthropological survey used to create this data precedes 1900 or 1924. 

1 3 

Journal of Economic Growth (2022) 27:149–192 

157 

Rail construction began in 1897, which helped the British to consolidate their control over Ghana and lowered trade costs. This motivates the choice of five turning points for our descriptive analysis: 1751, 1850, 1875, 1897, and 1932. 

**Missionary Expansion.** The first mission station was established in 1751. Thereafter, various mission societies failed to maintain a permanent presence until Presbyterian and Methodist missionaries reached the Gold Coast in 1828 and 1835, respectively. Figure 3 shows the number of Christian missions, main stations, and mission schools from 1840 to 1932. By 1850, 904 Ghanaians had converted and 21 missions existed (Isichei 1995, p. 169; Miller 2003, p. 23). Mass-evangelization did not take off until the 1870s, when 67 Protestant missions served 6,000 Ghanaians. Catholic missions started their conversion efforts from 1880 onward. By 1932, the number of missions had expanded to 1832 with 340,000 followers (9% of the population; ≈ 186 followers per mission). The Christian share has since grown to 80% (USAID 2020). Missions viewed the provision of education as a way to attract new Christians. As such, they provided the bulk of schooling in colonial Ghana (Cogneau and Moradi 2014). As seen in Fig. 3, early missions differed from later missions in that many were main stations and had a school. 

**Constraints.** Missions initially settled along the coast (Fig. 4a–b). Missionaries shunned away from creating inland stations before they gathered essential intelligence traveling the country (Thauren 1931, pp. 19–21; Engel 1931, p. 14). The Ashanti Kingdom was hostile to Christian proselytizing, restricting missionary activities to the territory of the Gold Coast Colony (Fig. 4b–c). Access to the interior was facilitated by rail and road building since the early 20th century. By 1932, missions covered large parts of Southern Ghana (Fig. 4d). 

Malaria was the biggest killer, striking Europeans soon after arrival (Curtin 1961). This changed when quinine was introduced circa 1850 as cure and prophylaxis.<sup>20</sup> The significance was well understood. As Curtin (1973, p. 362) explains, quinine “helped to close an epoch. [It] ... was understood well enough in official and missionary circles to reduce sharply the most serious impediment to any African activity. ... [T]he price in human life was much lower.” Figure 5 confirms the high mortality among European missionaries in Ghana prior to the introduction of quinine.<sup>21</sup> Simultaneously with quinine, the presence of European missionary staff expanded considerably, from less than 20 pre-1850 to circa 60 post-1870 (Fig. 5a). However, their numbers always remained below 70 because employing African converts as missionaries was a cost-efficient strategy in both the pre- and postquinine eras. Firstly, Africans acquired immunity to malaria during childhood (Curtin 1973, p. 197).<sup>22</sup> Secondly, their salaries were lower and they spread the gospel in the local vernaculars (Schlatter 1916; Graham 1976; Agbeti 1986, p. 57).<sup>23</sup> 

20 In 1848, the Director-General of the Medical Department of the British Army sent a circular to all West African Governors, advising the general use of quinine prophylaxis (Curtin 1961, p. 108). Fischer (1991, p. 73; 99) explains that from 1845 on, Presbyterian missionaries received medical training before leaving for the Gold Coast and quinine was not missing in any of the missionaries’ pharmaceutical orders. However, the proper application of quinine was a gradual process. Missionaries did not apply the correct dose during fever until the late 1850s (Fischer 1991, pp. 74–75). 

21 Figure 5b shows that in Ghana the likelihood of European missionaries surviving more than three years during the pre-quinine era was about 30%, whereas in the post-quinine era it was about 80%. 

22 African missionary mortality was significantly lower than for Europeans in both eras (see Fig. 5b). 

23 By 1890, there were four African missionaries for every European. By 1918, Europeans constituted 2% and 8% of total Methodist and Presbyterian mission staff respectively (Parsons 1963, p. 4; Sundkler and Steed 2000, p. 717). Based on our data, the ratio of total mission stations to European missionaries increased substantially over time. 

1 3 



<!-- Start of picture text -->
Oo<br>So<br>Oo<br>N<br>So<br>lo}<br>2<br>ra<br>°<br>®<br>Qo<br>£8<br>aS 5<br>Zz<br>g<br>Fe° i=}lo}<br>wo<br>o ee<br>1840 1850 1860 1870 1880 1890 1900 1910 1920 1930<br>—— Missions ---~— Main Mission Stations Mission Schools<br><!-- End of picture text -->

Journal of Economic Growth (2022) 27:149–192 

159 



<!-- Start of picture text -->
(a) (b)<br>(c) (d)<br>Fig. 4   Location of Missions in Ghana for Selected Years.  Notes:  Subfigures 4( a - d ) show the location of<br>all census missions (Protestant and Catholic) in Ghana for selected turning points in the history of Ghana:<br>1850, 1875, 1897 and 1932. See Web Data Appendix for data sources.<br>(a) (b)<br>Pre-Quinine Post-Quinine<br>0 2 4 6 8 10<br>Analysis Time, Years of service in Ghana<br>1750 1770 1790 1810 1830 1850 1870 1890<br>Pre-quinine x European Pre-quinine x African<br>Lowess Mortality Rate N European Missionaries Post-quinine x European Post-quinine x African<br>80 1.00<br>.3 60 0.75<br>.25<br>Mortality Rate .2.15 40 Proportion surviving 0.50<br>.1 20 N European Missionaries<br>0.25<br>.05<br>0<br><!-- End of picture text -->

**Fig. 4** Location of Missions in Ghana for Selected Years. _Notes:_ Subfigures 4( **a** - **d** ) show the location of all census missions (Protestant and Catholic) in Ghana for selected turning points in the history of Ghana: 1850, 1875, 1897 and 1932. See Web Data Appendix for data sources. 

**Fig. 5** Mortality of European and Native Missionaries in Ghana, 1750–1890. _Notes:_ Subfigure 5( **a** ) shows mortality rates and the number of European male missionaries in 1751–1890. The post-quinine era is defined as post-1850. Subfigure 5( **b** ) shows Kaplan–Meier survival probabilities of European and African missionaries pre- and post-quinine (data for 1751–1890 period). See Web Appendix for data sources. 

very dependent on cocoa for their economic support” (Sundkler and Steed 2000, p. 216). This also applies to other parts of Africa. Various Protestant mission societies established 

1 3 

Journal of Economic Growth (2022) 27:149–192 

160 

trading companies that exported African cash crop produce and used their profits to sustain missionary activities (Johnson 1967; Gannon 1983). Catholic missions, in contrast, were less constrained as they relied on the financial backing of the Vatican and its missionary associations in Europe (Spitz 1924; Schmidlin 1933, pp. 560–564; Debrunner 1967). 

**Descriptive Analysis.** For 2091 cells _c_ and periods [ _t_ - _s_ ; _t_ ] 1751–1850, 1850–1875, 1875–1897, and 1897–1932, we run repeated regressions of the form _Mc_ , _t_ = _훼_ + _휌Mc_ , _t_ − _s_ + is the set of locational factors described before. As we control for missions in the first year _Xc훽t_ + _uc_ , _t_ where _Mc_ , _t_ is a dummy equal to one if there is a mission in cell _c_ in year _t_ and _Xc_ of the period _t_ - _s_ ( _Mt_ − _s_ ), the coefficients _훽t_ show the long-difference correlation between the factors and missionary expansion in each period. Standard errors account for spatial correlation within 100 km (Conley 1999).<sup>25</sup> 

Table 1 presents for each period the coefficients of selected variables among all the variables included: 1751–1850 (col. (1)), 1850–1875 (2), 1875–1896 (3) and 1897–1932 (4). In the earliest periods, missions appear to have avoided high-risk malaria areas and settled at their port of entry, in close proximity to the coast (col. (1)-(2)).<sup>26</sup> It was only after the British had defeated the Ashanti Kingdom in 1896 that missionaries expanded northwards beyond the borders of the Gold Coast Colony (col. (4)). Next, while earlier missions expanded along 19th century trade routes (col. (1)–(2)), later missions opened in proximity to railroads (col. (4)). The negative correlations for navigable rivers during the early period (col. (1)–(2)) mirror the correlations for malaria (river floodplains provide breeding grounds for mosquitoes). Missions then concentrated in dense urban areas (col. (1)–(4)). Mission expansion appears to have followed urban population patterns of 1891, 1901 and 1931. Once urban demand was partly satisfied, missions appear to have spread into densely populated rural areas (col. (3)–(4)). Expansion also took place in cash crop growing areas (col. (2)–(4)). Finally, these descriptive results hold if we include 35 ethnic group fixed effects or exclude controls defined ex-post (Jedwab et al. 2019). 

Overall, mission societies might have chosen, and might have been better received in, healthier, more accessible, and more developed areas ( _R_<sup>2</sup> = 0.50–0.61 in col. (2)–(4)). However, these results are not causal. Hence, our focus on malaria, railroads, and cash crops in the next section. 

## **4  Results: determinants of missionary expansion** 

### **4.1  Malaria and missionary expansion** 

Section 3 described the substantial costs of European **Difference-in-Difference (DiD).** missionary mortality and how quinine reduced malaria death rates in the 1850s, after which the number of missionaries gradually increased. We test this more formally in Table 2. For 2091 cells _c_ and 98 years _t_ from 1800 to 1897 (N = 204,918), we regress a dummy if there is a mission in cell _c_ and year _t_ on the historical malaria index of cell _c_ interacted with a post-quinine dummy (if year _t_ is after 1850) while simultaneously including cell and year fixed effects. We choose the end of our third period – 1897 – as the final year of the 

> 25 Following Kelly (2019), Web Appx. Fig. A2 shows that the spatial correlation of residuals is insignificant after circa 50 km. Using 100 km should thus give conservative estimates of standard errors. 

> 26 Summary statistics are reported in Web Appendix Table A2. Malaria and the tsetse index from Alsan (2015) are strongly correlated (0.86). We thus do not test for tsetse. 

1 3 

Journal of Economic Growth (2022) 27:149–192 

161 

post-treatment window (1850–1897). To ensure a pre-treatment window of similar length we choose 1800 as our starting year.<sup>27</sup> 

Table 2 shows that missions expanded into higher-risk malaria areas after 1850 (col. (1)). The effect of quinine is strong: A one standard deviation in malaria is associated with a 0.18 standard deviation increase in the mission dummy in 1850–1897 (relative to 1800–1849). In col. (2), we interact malaria with a dummy if year _t_ is between 1800 and 1824. This separates the pre-treatment window into two sub-periods. We find no differential effect for malaria before 1850, implying parallel trends. The effects hold but are smaller when adding district (as of 1931; N = 38)-year fixed effects to compare neighboring cells within the same district over time (col. (3)).<sup>28</sup> 

Using the baseline DiD specification, we study the intensive margin. Web Appx. Table A3 shows that, conditional on having a mission (i.e. the extensive margin), higher-risk malaria areas had more missions, more main stations and more mission schools per cell by 1897. Moreover, denominational differences confirm that economic considerations mattered for missionary expansion. Mainline Protestants depended more on local contributions and valued entrepreneurship and education (Barro and McCleary 2017). As such, their missionaries had to be better trained, which made the issue of their low tropical life expectancy particularly acute. Consistent with these facts, Web Appx. Table A3 show stronger post-1850 effects for Mainline Protestants than for non-Mainline Protestants. Catholic missions started their conversion efforts only postquinine from 1880 onward. We therefore exclude them from this analysis. 

**Fuzzy Panel Event Study.** Next, we show the effects of the introduction of quinine in a panel event study design. We restrict the analysis to the period 1800–1897, include cell fixed effects and district (1931)-year fixed effects, and aim to capture year-specific effects of historical malaria intensity _before_ and _after_ 1850 (1849 is the omitted year). Subfigure 6 (a) shows the coefficients for each of the 15 years before and after 1850 as well as for the years “1835-” (we use a single dummy for all the years before 1835) and “1865+” (we use a single dummy for all the years after 1865).<sup>29</sup> 

European missionaries entered higher-risk malaria areas after 1855 and further expansion took place in 1857, 1860 and 1865+. There is no trend before 1850. As explained in Sect. 3, quinine had been available in Ghana as early as the late 1840s, but mission societies learned about the proper medication of quinine much later. The panel-event study is thus not sharp but “fuzzy”. It also took mission societies time to respond and train and send enough European missionaries to Ghana. Spatial expansion was necessarily gradual. The sudden expansion in missions observed in 1855, the gradual expansion observed in 1855–1865, and the twice higher effects in 1865–1897 when the treatment is not “partial” anymore appear consistent with that. 

Of course, as we include more post-treatment years, the panel-event study is less sharp, and the treatment variables may pick up developments other than the diffusion of quinine. There is a trade-off between only considering the partial treatment window and considering a longer window. In our case, we focus on the pre-1897 period, so before the rail, road, and cash crop eras. 

Colonization may be a potential confounder. However, district-year fixed effects should take care of any spatial expansion of colonial rule. Furthermore, the boundaries of the Gold 

> 27 For cells _c_ and year _t_ , the specification is as follows (using Conley standard errors): Mission Dummy28 Results also hold when adding ethnic group-year fixed effects or cell-specific linear trends (Jedwab et al. _c_ , _t_ = _훼_ + _훽_ 1 Historical Malaria Index _c_ *Dummy1850−1897 + _휔c_ + _휆t_ + _vc_ , _t_ . 2018). 

> 29 For cells _c_ , districts _d_ , and year _t_ , the specification is as follows (using Conley standard errors): Mission Dummy _c_ , _t_ = _훼_ + Σ<sup>1865</sup> 1835<sup>+</sup> −<sup>_훽t_Historical Malaria Index</sup><sup>_c_*Dummy (Year = t) +</sup><sup>_휔c_+</sup><sup>_휅d_,</sup><sup>_t_+</sup><sup>_vc_,</sup><sup>_t_.</sup> 

1 3 

Journal of Economic Growth (2022) 27:149–192 

162 

Coast Colony and Ashanti barely changed between 1821 and 1902 (Sect. 3). Relatedly, the baseline results (col. 4) and the results with district-year fixed effects (col. 5) hold if we include dummies for the Gold Coast Colony and Ashanti interacted with year fixed effects. Finally, we decompose the 1850–1897 period into two subperiods. The British-Ashanti war started in 1872 after the British bought several Dutch coastal towns in 1871 and the Ashanti felt threatened by the British consolidating their control of the Gold Coast ports. We thus use 1850–1870 and 1871–1897. As seen in col. 6, the baseline effect is larger post1871, consistent with Fig. 6a. If we only focus on the 1850–1870 period, a one standard deviation in malaria is associated with a 0.08 standard deviation increase in the mission dummy. The results with district-year fixed effects are weaker (col. 7) but the specification may ask too much of the data, removing much of the spatial variation in malaria. 

More generally, given the fuzziness of the event study, we cannot be sure that the estimated effects are fully causal, especially in the late 19th century. These results should thus be taken with caution. 

**Missionary Data.** We estimate the same DiD model as before but we replace the dependent variable with a dummy indicating whether, for the years 1846–1890, mission stations were permanently inhabited or only monitored by European missionaries. Column (6) of Table 2 confirms a general increase in the number of missionaries in higherrisk malaria regions, which was partly driven by Europeans (col. (7)). Column (8) shows that quinine had a positive effect on the expansion of European permanent residences. Column (9) then shows that quinine had a stronger effect on African missionaries. Once standardized, the effect is about twice larger than for Europeans. 

This suggests that the expansion into malaria areas was driven by African missionaries. This result may seem counter-intuitive since African missionaries had acquired natural immunity in some form. However, one needs to take into account _specialization_ within mission societies. European missionaries were engaged in training and supervision activities. They mostly lived in coastal towns from where they would train African staff in church seminaries and routinely visit and supervise African missionaries in the hinterland. Second, in that period ordained priests were overwhelmingly European. Priests performed Christian rites that catechists were not allowed to do. These rites were important services provided at the stations.<sup>30</sup> Third, African catechists were cheaper to train and had a comparative advantage, for example due to their knowledge of local languages. 

As such, European missionaries had to routinely visit African-run stations, often traveling to/through high-risk malarial areas. Before quinine, European missionaries would not have been able to expand their hinterland activities (via African personnel). With quinine, more Europeans lived on the coast from where they trained and supervised African catechists, hence leading to a spatial expansion of missionary activities, especially in malarial areas.<sup>31</sup> Finally, quinine likely also helped expansion in less-malarial areas. Thus, our effects may be downward-biased and we may under-estimate the contribution of quinine to missionary expansion. 

> 30 Spitz (1924, p. 372) writes: “The shortage of missionary priests makes a well-trained body of native catechists of paramount importance. [They are later] frequently visited by [European] missionaries who superintend their work.” Debrunner (1967, p. 231) cites a letter from missionary Dennis Kemp who wrote: “The object of my visit was to strengthen the hands of the catechists; to endeavor to utter words of counsel, of encouragement and reproof, as circumstances required, to our congregations; to administer the sacraments, and to investigate cases of discipline.” 

> 31 Smith (1966, p. 51) writes: “After 1853 the first stream of trained catechists and teachers began to flow from the Seminary, a fact which enabled the Church to spread to practically every part of Akwapim.” 

1 3 



<!-- Start of picture text -->
(a) Effect of the Introduction of Quinine (1850) (b) Effect of Railroad Construction<br>| 1. Western (1901-11) 2. Eastern (1909-23) 3. Central (1926-27)<br>©-: aa i!f== \i<br>g . ! i ov<br>g= 8 ae an ——_— 2a ;i! avif<br>= o <4 ‘ f ! 1 A '<br>5 3 3 i Al.<br>i}5soS8 11! swio | } i .\_! c \e f ii!™“ I le} \l‘<br>c ° i Soft n—+ t ml xt<br>Soa yonnns o \ .! ,<br>a 3 | w / Ve i i dat ne<br>2 s — 3 a a. I 1 \|Aw<br>§ 843l\ \_-. ii‘ \| Bot8 | oles sv] \e aw) \<br>= te een eeeJ © V/V ! ~ )I i\i<br>1835- 1840 1845 1850 1855 1860 1865+ ft<br>-15- 10 -5 ° 5 10 15--15- -10 -5 O 5 10 15+-15- -10 -5 oO 5 10 15+<br><!-- End of picture text -->

Journal of Economic Growth (2022) 27:149–192 

164 

located within 30 km of a line as of 1932.<sup>33</sup> Column (3) of Web Appx. Table A4 motivates the 0–30 km distance. When including dummies for whether the cell is within 0–10, 10–20, 20–30, 30–40 and 40–50 km from a railroad, we find an effect until 30 km only. The table shows that railroads built after 1897 had no significant positive effect on mission settlement before 1897, thus confirming parallel trends. 

Panel A of Table 3 , row 1 shows a baseline 0–30 km railroad effect of 0.162***. There is no effect of the 0–30 km rail dummy in the periods before 1897–1932 (rows 2–4). The main result is robust to: (i) Adding 34 ethnic group or 38 district (1931) fixed effects (rows 5–6); (ii) Confining the rail dummy to the more exogenous western line (row 7). Its goal was to connect a port, two mines, and the Ashanti capital Kumasi, without consideration for locations in between. Because we include dummies for whether there is a port, mine and large city as controls, we capture their effects, and identification relies on cells connected by the railroad by chance; (iii) Using cells within 0–30 km of a placebo line, for which no spurious effect is found (row 8); and (iv) Instrumenting the 0–30 km rail dummy by a dummy equal to 1 if the cell is within 30 km from the Euclidean minimum spanning tree between the nodes of the triangular rail network: Sekondi, Kumasi and Accra (see Web Appx. Fig. A3). We drop the nodes, which means that we rely on cells connected by chance (row 9; IV-F. = 39). Overall, the effect is strong: A one standard deviation in the rail dummy is associated with a 0.14–0.15 standard deviation in the mission dummy. 

**Timing of Rail Building.** In Panel B of Table 3, for 2091 cells _c_ in years 1897–1932, we study the effect of the 0–30 km rail dummy for cell _c_ in year _t_ on whether the same cell _c_ has a mission in year _t_ , while adding cell and year fixed effects.<sup>34</sup> Row 10 shows a strong effect (0.179***). Row 11 shows there is no effect when adding one lead of the rail _t_ on missions in _t_ is dummy. Row 12 shows that the contemporaneous effect of railroads in captured by the lag of the rail dummy, suggesting that missions followed railroads. Rows 13–14 show that results hold when adding ethnic group-year or district-year fixed effects, to compare connected and unconnected neighboring cells over time. Row 15 indicates that the baseline effect is unchanged if we include 2091 cell-specific linear trends. Overall, panel estimates are similar to cross-sectional estimates. 

Results at the intensive margin point to the same direction (Web Appx. Table A5). When focusing on denomination-specific effects the various specifications show consistently stronger effects for Mainline Protestants than for non-Mainline Protestants and Catholics (see Web Appx. Table A6). This is in line with the fact that economic considerations mattered more for Mainline Protestants. 

**Panel Event Study.** We show the effects of the 30 km rail dummy (based on the year of completion) on mission expansion in a panel event study framework. The first year of completion is 1901. Our last year of data is 1932. We thus restrict the analysis to 1870–1932 so that we observe about 30 years before and after the event. We focus on the 301 cells that were within 30 km from a railroad before 1932. Because dynamic effects cannot be identified without never-treated cells in the sample (Borusyak and Jaravel 2018), we add 69 

> 33 For cells _c_ , the specification is (Conley SEs): Mission Dummy _c_ ,1932 = _훼_ + _훽_ 0-30 km Rail Dummy _c_ ,1932 + _XcB_ + _vc_ . For the cross-sectional analyses on the effects of railroads we omit the controls capturing economic development (e.g., population and cash crops) circa 1932. Existing roads at that time were then purposely built as feeder roads for the railroads (Dickson 1969). To avoid over-controlling, we thus also omit the “roads circa 1930” control. 

> 34 For cells _c_ and year _t_ , the model is (Conley SEs): Mission Dummy _c_ , _t_ = _훼_ + _훽_ 30 km Rail Dummy _c_ , _t_ + _휔c_ + _휆t_ + _vc_ , _t_ . 

1 3 

Journal of Economic Growth (2022) 27:149–192 

165 

placebo cells that were proposed to be connected (= be within 30 km from a railroad) but never were. Our sample includes 370 cells  x  63 years = 23,370 cell-years. We include cell and district-year fixed effects. We then show the effects for the 14 years _before_ and _after_ (− 1 is the omitted year). We also include a dummy that captures all the years before year − 15 (incl.; “15-”) and a dummy that captures all the years after year 15 (incl.; “15+”). Lastly, in settings with staggered adoption, the estimated effect is a weighted average of the effect of each subtreatment (Athey and Imbens 2022). Therefore, we investigate each line separately interacting each pre- and post-treatment dummy with a dummy for each line (Western, Eastern, Central).<sup>35</sup> 

Subfig. 6(b) shows the estimated coefficients. Both the Western and Eastern lines had strong effects on mission placement, especially after five years. The Central line does not show any positive effects (there is also a pre-trend), which is plausible. The Central line was built well after the other two lines (1925–1927 vs. 1901–1911 and 1909–1923). By then, mission societies had already established many missions along the Western and Eastern lines. In addition, the Central Line reached locations that were already quite connected. This line was built parallel to the coast, between the other two lines (Web Appx. A3), in areas that already had a few motor roads by the mid-1920s (Luntinen 1996). As such, the line barely reduced trade costs and the line was an economic failure.<sup>36</sup> To some extent, it is reassuring that we do not find an impact for this line. 

### **4.3  Cash crops and missionary expansion** 

Export commodities were an important source of African income during the colonial era (Austin 2003). Ghana experienced various commodity export booms and busts as a result of new crop diffusion and changing world demand (Dickson 1969, pp. 143–178): palm oil (1860–1910s), rubber (1890–1910s), kola (1900–1920s), and cocoa (1900–1930s).<sup>37</sup> We explore the relationship between cash crop cultivation, as a proxy for African incomes, and the expansion of missions. The fact that each export boom took place at different times and in different areas facilitates identification.<sup>38</sup> 

**Panel-Bartik.** In the absence of data on annual crop production at the cell level, we study the reduced-form effects of a Bartik-type shift-share instrument predicting labor demand for each crop sector _s_ in cell _c_ and year _t_ . Bartik IVs are used to generate exogenous labor demand shocks by averaging national employment growth across sectors using local sectoral employment shares as weights (Bartik 1991). We use a modified version of these: (i) We know the national export value of crop _s_ (palm, rubber, kola and cocoa) in year _t_ for the 1846–1932 period; (ii) We know in which cells _c_ crop _s_ was produced at 

35 For lines _r_ , cells _c_ , districts _d_ and year _t_ , we use (Conley SEs): Mission Dummy _c_ , _t_ = _훼_ + Σ<sup>_s_</sup> _s_<sup>=</sup> =<sup>15</sup> 15<sup>+</sup> −<sup>_훽s_,</sup><sup>_r_+</sup><sup>_휔c_+</sup><sup>_휅d_,</sup><sup>_t_+</sup><sup>_vc_,</sup><sup>_t_.</sup> 36 For example, Luntinen (1996, p. 120) writes: “From the Central Province cocoa was carried on road to the small beach ports, at the distance of fifty or sixty miles, whereas the railway to Takoradi via Huni Valley was more than one hundred miles long. In order to meet this competition the rates for cocoa were again drastically reduced in January 1930, but ‘the results were most disappointing’. The railway management tried to explain their plight.” 37 Export statistics for the period 1846–1932 (no data available before) confirm this (see Web Appx. Fig. A4). 38 We implement identification strategies due to the concern that missionaries locally promoted the cultivation of cash crops. However, in Ghana cash crop cultivation was essentially an African enterprise (Hill 1963; Austin 2014). 

1 3 

Journal of Economic Growth (2022) 27:149–192 

166 

any point during 1846–1932; (iii) We know the number of producing cells for crop _s_ ; (iv) Assuming that each producing cell was producing an equal amount, we predict the export value of crops _s_ in cell _c_ in year _t_ ; (v) Our exogenous measure of crop income in cell _s_ and year _t_ is then log export value of _all_ crops _s_ in cell _c_ and year _t_ ; and (vi) When studying its effects on missions, we add cell fixed effects, which capture the time-invariant production dummies, and year fixed effects, which capture changing national export values.<sup>39</sup> 

Row 1 of Table 4 shows a large positive effect (0.028***) of log predicted cash crop export value at the cell level. In terms of magnitude, the effect is strong as a one standard deviation in the value of cash crops is associated with a 0.20–0.23 standard deviation in the mission dummy. 

As explained by Goldsmith et al. (2020), shift-share instruments are not valid if the initial shares used are not exogenous. Row 2 shows that results hold if we construct the Bartik for the most important crops, palm oil and cocoa, using soil suitability dummies instead of production dummies (Globcover 2009).<sup>40</sup> Next, to ensure results are not biased by soil suitability having changed over time as a result of economic development, row 3 shows results hold when we use historical measures of soil suitability for palm oil, rubber and cocoa.<sup>41</sup> Goldsmith et al. (2020) also demonstrate that the Bartik estimator can be decomposed into a weighted combination of the estimates of all sectors, with the weights depending on how much each sector contributes to the identifying variation. Thus, Bartik estimators may hide the fact that they are driven by a few sectors only, and the specific exogeneity of their shares must be discussed. In our case, we rely on four crops – rather than say hundreds of industries – and rows 4–7 show results hold for each crop one by one. Furthermore, we build another Bartik for cocoa for which we have detailed geospatialized data on soil suitability. For each cell, we know the respective shares of moderately, highly and very highly suitable soils, as well as the relative average yields of these different types of soils. As seen in row 8 the estimated effect is similar to the baseline.<sup>42</sup> 

Moreover, no spurious effects are found when adding one lead of the Bartik (row 9). Instead, the effect of cash crops in _t_ on missions in _t_ is captured by a lag of the Bartik (row 10). This suggests missions followed cash crop incomes. Rows 11–13 show that results hold when adding ethnic group or district fixed effects interacted with year fixed effects or cell-specific linear trends. 

Finally, the same Bartik analysis shows additional effects on the number of missions or the opening of main stations once we control for whether the cell had a mission (see Web Appx. Table A7). The same Web Appendix table also confirms that cash crop incomes have stronger effects on Mainline Protestant missions than on Catholic missions or other Protestant missions. This is another piece of evidence that economic considerations strongly mattered for missionary expansion. 

**Summary.** A one standard deviation in malaria, railroads and cash crops is associated with a 0.08–0.18, 0.14–0.15 and 0.20–0.23 standard deviation increase in the mission 

> 39 For cells _c_ and year _t_ , the model is (Conley SE): Mission Dummy _c_ , _t_ = _훼_ + _훽̂_ Cash Crop Export _c_ , _t_ + _휔c_ + _휆t_ + _vc_ , _t_ . 

> 40 No soil suitability maps could be found for kola and rubber. 

> 41 No maps could be found for kola. 

> 42 Very highly suitable soils include class 1 and class 2 ochrosols and produce about 2000 pounds of dry cocoa per acre. Highly suitable soils include class 3 ochrosols and produce 1338 pounds per acre. Suitable soils include other types of cocoa soils and produce 223 pounds per acre. See Web Data Appx. for details on the sources used. 

1 3 

Journal of Economic Growth (2022) 27:149–192 

167 

dummy, respectively. However, there is a possibility that our estimates for malaria are not causal. Nonetheless, crudely adding these numbers, we obtain 0.42–0.56 (0.34–0.38 excl. malaria). Overall, the variables possibly explain a significant share of missionary expansion over time. The analysis also does not account for the effects of other locational factors or the general equilibrium effects of the three variables. 

### **4.4  Dynamics of missionary expansion** 

This section highlights the dynamics of missionary expansion by documenting the changing locational characteristics in the stock of missions over time. We construct a measure that summarizes how “attractive” a location was to missionaries. More precisely, we regress the mission dummy in 1932, _Mc_ ,1932 , on _all_ the possible determinants of mission placement _Xc_ of Table 1. We then obtain the predicted probability _Mc_ ,1932 = _XcB_ , or _locational score_ . We distinguish between four groups of cells in 1840–1932:<sup>43</sup> (i) cells with a mission in both _t_ − 1 and _t_ (“remains 1”); (ii) cells with no missions in _t_ − 1 but a mission opening in _t_ (“becomes 1”); (iii) cells with a mission in _t_ − 1 that exits in _t_ (“becomes 0”); and (iv) cells with no missions in both _t_ − 1 and _t_ (“remains 0”). Figure 7a plots a quadratic fit of the average score for those four groups. 

The pattern suggests that the best locations received missions first, and that marginally less good locations were increasingly added to the existing stock of mission locations. Indeed, cells with surviving missions (“remains 1”) rank consistently higher than cells that gain or lose missions (“becomes 1” or “becomes 0”) and their scores significantly exceed those of the “remains 0” group. Scores of all the four groups decrease over time. Scores of the “becomes 1” group decrease, because less and less attractive mission locations are added over time. Scores of the “remains 0” group decrease, because switchers are among the best locations of the cells with no missions.<sup>44</sup> 

Results hold if (not shown): (i) We use the period 1751–1840 to estimate the coefficient of each factor and study predicted scores post 1840; (ii) The urban share in 1931 is the predicted variable. 

### **4.5  Replication of the results for sub‑Saharan Africa** 

We replicate the analysis of the determinants of missionary expansion for sub-Saharan Africa. Obviously, unlike for Ghana, we have to rely on limited and possibly mismeasured data. 

**Descriptive Analysis.** In Table 6, for 203,574 cells in 43 countries, we regress a dummy if there is a mission according to the maps of Beach (1903), supposedly representing the year 1900 (col. (1)), or Roome (1925), supposedly representing the year 1924 (col. (2)), on various locational factors and country fixed effects. The regression is the same as for Ghana. Calculating Conley standard errors is too computationally intensive for that many cells. We therefore cluster standard errors at the district level (as of 2000). With 3284 

> 43 We use 1840 because it is the first year with 10 missions. 

> 44 When regressing the scores of the “remains 1”, “becomes 1”, “becomes 0”, and “remains 0” groups on the year, we find a significant negative effect: -0.003*** ( _R_<sup>2</sup> = 0.90), -0.005*** (0.46), -0.006*** (0.44), and -0.001*** (0.89), respectively. The high _R_<sup>2</sup> values imply that the best-ness of a location is predicted by the year it gained or lost a mission. 

1 3 

Journal of Economic Growth (2022) 27:149–192 

168 

districts, we get about 62 cells per district.<sup>45</sup> From the year of foundation reported for 83% of Protestant missions in Beach (1903), we construct a quasi-panel.<sup>46</sup> We then study in col. (3)–(5) how the correlations vary across three periods defined around four turning points: 1792 (first year with a mission), 1850 (date when anti-slavery efforts intensified), 1881 (start of the Scramble for Africa), and 1900 (last year of mission data in Beach 1903). 

Missionaries appear to have chosen locations with healthier environments (malaria, tsetse). Especially before 1850, missionaries seem to have avoided large pre-colonial cities, ethnic homelands colonized later, and Muslim centers, three measures of potential local resistance.<sup>47</sup> Transportation possibly played an important role: ports and coastal proximity may have facilitated initial access, while rivers, explorer routes, and railroads possibly enabled internal diffusion. Missionaries seem to have preferred large colonial cities and dense urban areas. We find positive correlations for slavery and cash crops. Finally, these correlations hold if we include 1158 country-ethnic group fixed effects or exclude controls defined ex-post (Jedwab et al. 2019). 

Overall, missions were established in better areas. However, the adjusted _R_<sup>2</sup> are low, at 0.03–0.04 in columns (1)–(2) vs. 0.35–0.61 for Ghana (Table 1). This is due to two reasons. First, the locations of the missions mapped in Beach (1903) and Roome (1925) are mismeasured due to inaccuracies in the georefencing of missions by Cagé and Rueda (2016) and Nunn (2010), respectively.<sup>48</sup> When combining the cells into 3x3 cells, the adjusted _R_<sup>2</sup> increases to 0.15 (not shown). Second, for Ghana, we compiled a rich data set of controls, but such data do not exist for the whole of Africa. 

Regarding causal effects, we do not know when quinine became the regular treatment in each country. However, we implement various identification strategies for railroads and cash crops. 

**Railroads.** Row 1 of Panel A in Table 5 shows the baseline effects of the 0–30 km rail dummy when including our control variables of Table 6. To avoid any over-controlling problem, we exclude controls that measure local economic development (population, crops, mining) c. 1900 (col. (1)) or 1924 (col. (2)).<sup>49</sup> Results hold if we apply the same cross-sectional identification strategies as for Ghana, whether: (i) adding ethnic (N = 1158) or district (as of 2000; 3284) fixed effects to compare neighboring cells (rows 2–3); (ii) using military or mining lines only (row 4), since their goal was to connect large pre-colonial cities or mines to a port without consideration for locations in between. Given the controls (we re-add mining), we capture the independent effects of locations that mattered 

> 45 The main results (Table 5, Table 6 and panel B of Table 8) hold when using larger grid cells to cluster standard errors, for example 10x10 mega-cells (N = 94 cells per mega-cell) or even 15x15 mega-cells (N = 199 cells) (not shown). 

> 46 To our knowledge, no one has ever used the panel aspect of this data. Panel data does not exist for Roome (1925). 

> 47 Distance to Muslim centers has a negative and almost significant correlation in col. (5) (which captures missionary expansion between 1881 and 1900), suggesting a more nuanced picture for Islam. Large cities in 1400 were mostly located in Muslim areas and their negative coefficients could reflect the fact that they were major Muslim centers. 

> 48 For example, for 109 missions reported in both Beach and Roome and digitized by Cagé and Rueda (2016) and Nunn (2010) respectively, we found an average distance of 2 cells between their georeferenced locations. 

49 For cells _c_ and countries _n_ and each separate year _t_ = {1900; 1924} , the specification is as folDummylows (standard errors clustered at the district level): Mission Dummy _c_ , _n_ , _t_ + _Xc_ , _n_ , _tBt_ + _휆n_ + _vc_ , _n_ , _t_ . _c_ , _n_ , _t_ = _훼_ + _훽t_ 0–30 km Rail 

1 3 



<!-- Start of picture text -->
(a) Locational Factors & Prob. of Missions (b) Correlation btw Atlas and Census Missions<br>5 - I I<br>— 2 | |<br>=o>=---- <2 | |<br>ge S55 22 olin\ || ||<br>25 © S 5= @ \Wey | |<br>8 ~ ° = ann | H<br>Ss rn NaN \ | |<br>at 5 * v ‘\ | |<br>8g 2o o Veyve | |<br>en 2 ssn. |! |<br>q waren g Maa |<br>oe Se ts-5-._|<br>< | —<br>° Zo<br>1840 1850 1860 1870 1880 1890 1900 1910 1920 1930 25 1840 1850 1860 1870 1880 1890 1900 1910 1920 1930<br><!-- End of picture text -->

Journal of Economic Growth (2022) 27:149–192 

170 

**Table 1** Correlates of missionary expansion, long-diff., selected factors 

|Dependent Variable|Dummy if C|ensus Mission i|n the Cell in S|elected Year:|
|---|---|---|---|---|
||1850|1875|1897|1932|
|Variables of Interest|(1)|(2)|(3)|(4)|
|Dummy Any Census Mission ... 1850/1875/1897||0.602***|0.392***|0.232***|
|||[0.082]|[0.028]|[0.058]|
|Historical Malaria Index|− 0.004*|− 0.005*|0.008|− 0.010|
||[0.002]|[0.003]|[0.006]|[0.007]|
|Log Distance to Coast|− 0.017*|− 0.027**|− 0.035|− 0.102***|
||[0.009]|[0.012]|[0.021]|[0.002]|
|Dummy if Port in the Cell 1850|0.166**|0.212***|0.129|− 0.159|
||[0.080]|[0.066]|[0.093]|[0.108]|
|Dummy if Outside Gold Coast Colony 1850|0.004|0.009|0.040|0.135**|
||[0.010]|[0.011]|[0.045]|[0.060]|
|Dummy if Navigable River 10 km|− 0.024**|− 0.023*|0.037*|0.022|
||[0.012]|[0.012]|[0.022]|[0.029]|
|Dummy if Ashanti Trade Route 1850 10 km|0.011|0.014**|− 0.004|0.006|
||[0.008]|[0.007]|[0.009]|[0.024]|
|Dummy if Non-Ashanti Trade Route 1850 10 km|0.012**|0.012**|0.002|0.026|
||[0.005]|[0.005]|[0.010]|[0.018]|
|Dummy if Railroad 1932 10 km|− 0.018**|− 0.017|0.067|0.079***|
||[0.008]|[0.010]|[0.066]|[0.018]|
|Log Urban Population 1891|0.015***|0.026***|0.008*|0.001|
||[0.005]|[0.007]|[0.005]|[0.002]|
|Log Urban Population 1901|− 0.000|0.007**|0.024***|− 0.011***|
||[0.005]|[0.003]|[0.008]|[0.003]|
|Log Urban Population 1931|0.001***|0.000|0.017***|0.032***|
||[0.000]|[0.002]|[0.007]|[0.011]|
|Log Rural Population 1901|0.001|0.001|0.007*|0.033***|
||[0.001]|[0.002]|[0.004]|[0.005]|
|Log Rural Population 1931|− 0.001|− 0.002|− 0.002|0.016**|
||[0.001]|[0.001]|[0.002]|[0.007]|
|Dummy if Palm Oil Plantation 1900–1936 50 km|0.018|0.029***|0.089***|0.082***|
||[0.013]|[0.011]|[0.019]|[0.016]|
|Dummy if Kola-Producing Cell 1932|− 0.025*|-0.017|0.042|0.073***|
||[0.015]|[0.016]|[0.042]|[0.019]|
|Dummy if Cocoa-Producing Cell 1927|0.006|0.008|0.073***|0.096**|
||[0.010]|[0.009]|[0.025]|[0.041]|
|R-squared|0.35|0.61|0.50|0.61|



For 2091 cells and each period [ _t_ - _s_ ; _t_ ], we regress a dummy if there is a census mission in year _t_ on a dummy if there is a census mission in year _t_ - _s_ and various locational factors. We do not report the coefficients of land area, rainfall, altitude, ruggedness, soil fertility, four dummies if the cell contained a large pre-colonial city circa 1800, the largest or 2nd largest city in 1901, a headchief town in 1901, or the central location of a mine in 1932, four dummies if the cell was within 10 km from a road in 1930, within 50 km from a slave market c. 1800, within 50 km from a rubber plantation in 1900–1936, or was surveyed by the 1901 Population Census, and the log of normalized slave exports in the 15th–19th centuries. 100 km Conley SE’s: * p<0.10, ** p<0.05, *** p<0.01. See Web Appendix for data sources. 

1 3 

Journal of Economic Growth (2022) 27:149–192 

171 

||Afri.|(11)|0.007***|[0.001]||||Y|Y|N|N|
|---|---|---|---|---|---|---|---|---|---|---|---|
||Euro.<br>Resid.|(10)|0.001***|[0.000]||||Y|Y|N|N|
|(1846–1890)|Euro.<br>Any|(9)|0.002***|[0.001]||||Y|Y|N|N|
|Missionary|Any|(8)|0.008***|[0.001]||||Y|Y|N|N|
|||(7)|||0.002***<br>[0.001]|0.011***|[0.002]|Y|N|Y|N|
|||(6)|||0.009***<br>[0.001]|0.028***|[0.002]|Y|Y|N|N|
|–1897)||(5)|0.005***|[0.001]||||Y|N|Y|Y|
|year_t_ **:**(1800||(4)|0.013***|[0.001]||||Y|Y|N|Y|
|n in cell_c_in||(3)|0.007***|[0.001]||||Y|N|Y|N|
|Census Missio||(2)|0.019***|[0.001]|− 0.002<br>[0.001]|||Y|Y|N|N|
|Dummy if||(1)|0.020***|[0.001]||||Y|Y|N|N|
|.:||nterest:|1850–97||1800–24<br>1850–70|1871–97||||Year FE|Ashanti Ctrls|
|Var||of I|ria*||ria*<br>ria*|ria*||FE|FE|ict-|&|
|Dep.||Vars|Mala||Mala<br>Mala|Mala||Cell|Year|Distr|GCC|



|(1)–(5): For 2091 cells_c_and 98 years_t_(N = 204,918), we regress a dummy if there is a census mission in cell_c_in_t_on malaria interacted with a dummy if_t_is between 1850<br>and 1897. (8)–(11): For 2,091 cells_c_and 40 years_t_(N = 93,253), we regress a dummy if there is a missionary / Euro. missionary (“Resid.” indicates that the missionary lives<br>there permanently instead of frequently visiting) / African missionary in cell_c_in_t_on malaria interacted with a post-1850 dummy. 100 km Conley SE’s: * p<0.10, ** p<0.05,|
|---|



1 3 

Journal of Economic Growth (2022) 27:149–192 

172 

**Table 3** Railroads and missionary expansion, long-differences and panel 

Panel A: Dependent Variable: Dummy if Census Mission in 1932 (incl. controls and a Dummy if Census Mission in 1897) 

|Efect of Dummy Railroad 0− 30 km in 1932:|Coef.|SE|Obs.|Controls|
|---|---|---|---|---|
|1. Baseline|0.162***|[0.033]|2091|Y|
|2. Dep.Var.: Dummy Mission 1850, Ctrl Dummy Mission 1751|− 0.015|[0.014]|2091|Y|
|3. Dep.Var.: Dummy Mission 1875, Ctrl Dummy Mission 1850|0.008|[0.020]|2091|Y|
|4. Dep.Var.: Dummy Mission 1897, Ctrl Dummy Mission 1875|0.031|[0.033]|2091|Y|
|5. Including Ethnic Group Fixed Efects (N = 34)|0.180***|[0.022]|2091|Y|
|<br>6. Including District in 1931 Fixed Efects (N = 38)|0.175***|[0.045]|2091|Y|
|<br>7. Railroad 0–30 km Dummy Defned Using Western Line Only|0.140**|[0.059]|2091|Y|
|<br>Railroad 0–30 km Dummy Defned Using Other Lines Only|0.174***|[0.025]|||
|<br>8. Railroad 0–30 km Dummy Defned Using existing Lines Only|0.176***|[0.041]|2091|Y|
|<br>Railroad 0–30 km Dummy Defned Using Placebo Lines Only|0.066|[0.055]|||
|<br>9. IV: 30 km from Straight Lines (Drop Nodes; IV F=39)|0.230**|[0.113]|2088|Y|



|Panel B: Dependent Variable: Dummy if Census Mission in year<br>Fixed Efects)<br>|_t_(Including C<br>|ell Fixed<br>|Efects a<br>|nd Year<br>|
|---|---|---|---|---|
|Efect of Dummy Railroad 0–30 km in Year_t_:|Coef.|SE|Obs.|Controls|
|10. Baseline Efect in Year_t_<br>|0.179***|[0.019]|75,276|N|
|11. Efect of the Lead when added<br>|0.011|[0.035]|73,185|N|
|12. Baseline Efect in Year_t_if adding 1 Lag<br>|0.010|[0.036]|73,185|N|
|<br>Efect of the Lag|0.171***|[0.036]|||
|13. Including Ethnic Group FE (N = 34) x Year FE (T = 36)|0.143***|[0.017]|75,276|N|
|14. Including District in 1931 FE (N = 38) x Year FE (T = 36)<br>|0.122***|[0.013]|75,276|N|
|15. Including 2,091 Cell-specifc linear trends|0.173***|[0.036]|75,276|N|



Panel A: For 2091 cells, we regress a dummy if there is a mission in 1932 on a dummy if there is a mission in 1897 and various controls (see text for details). Row 9: The IV is a dummy if the cell is within 30 km from the straight lines Sekondi-Kumasi and Accra-Kumasi (three nodes dropped). Panel B: For 2,091 cells _c_ and 36 years _t_ (1897–1932), we regress a dummy if there is a mission in cell _c_ in _t_ on a dummy if cell _c_ is within 30 km of a railroad in _t_ (cell FE & year FE incl.). 100 km Conley SE’s (SE’s clust. at district (1931) level in rows 9 and 15 where Conley SEs are too computationally intensive): * p<0.10, ** p<0.05, *** p<0.01. See Web Appx. for data sources. 

Overall, cross-sectional and panel estimates are similar, and a one standard deviation in the rail dummy is associated with a 0.01–0.09 standard deviation in the mission dummy. The magnitude of the effects is smaller than for Ghana (0.14–0.15). However, mission and railroad openings are mismeasured for the whole of Africa making the comparison with the Ghana results less relevant. 

Lastly, using the same cross-sectional or panel identification strategies, we find stronger effects for Mainline Protestants than for Catholics or other Protestants (Web Appx. Tables A8–A9). Thus, economic considerations also mattered more for Protestants when studying the determinants of mission expansion for the whole continent. 

1 3 

Journal of Economic Growth (2022) 27:149–192 

173 

**Table 4** Cash crops and missionary expansion, panel 

|Dependent Variable: Dummy if Census Mission in Year_t_(Including Cel<br>Efects)<br>|l Fixed Efec<br>|ts and Year|Fixed<br>|
|---|---|---|---|
|Efect of Log Predicted Cash Crop Export Value in Year_t_:|Coef.|SE|Obs.|
|1. Based on Palm Oil, Rubber, Kola & Cocoa Production|0.028***|[0.001]|181,917|
|2. Based on Contemporary Palm Oil & Cocoa Suitability|0.031***|[0.002]|181,917|
|3. Based on Historical Palm Oil, Rubber & Cocoa Suitability|0.023***|[0.001]|181,917|
|4. Based on Palm Oil Production Only|0.031***|[0.005]|181,917|
|5. Based on Rubber Production Only|0.020***|[0.001]|181,917|
|6. Based on Kola Production Only|0.043***|[0.002]|181,917|
|7. Based on Cocoa Production Only|0.042***|[0.001]|181,917|
|8. Based on Historical Moderate, High & Very High Cocoa Suitability<br>|0.029***|[0.001]|181,917|
|9. Overall Efect of Leads when Leads Added: 1 Lead<br>|− 0.003|[0.005]|179,826|
|<br>10. Baseline Efect in Year_t_when Lags Added: 1 Lag<br>|− 0.001|[0.005]|179,826|
|<br>Overall Efect of Lags when Lags Added: 1 Lag|0.029***|[0.001]||
|<br>11. Including Ethnic Group FE (N = 34) x Year FE (T = 87)|0.024***|[0.002]|181,917|
|12. Including District in 1931 FE (N = 38) x Year FE (T = 87)<br>|0.027***|[0.001]|181,917|
|13. Including 2,091 Cell-Specifc Linear Trends|0.024***|[0.006]|181,917|



For 2091 cells _c_ and 87 years _t_ (1846–1932), we regress a dummy if there is a mission in cell _c_ in _t_ on log predicted cash crop export value in cell _c_ in _t_ (cell FE and year FE included). Rows 2–8: Using alternative ways to construct the predicted value of cash crop exports. 100 km Conley SE’s (clust. at district (1931) level in row 13): * p<0.10, ** p<0.05, *** p<0.01. See Web Appendix for data sources. 

**Cash Crops.** We implement the same panel-Bartik strategy as for Ghana.<sup>54</sup> However, we only have panel data on missions before 1900. In addition, for the seven crops studied for Africa (cocoa, coffee, cotton, groundnut, palm oil, tea and tobacco), we could only find pre-1900 export values for 20 countries (N = 70,546 cells) c. 1850, 1860, 1870, 1875, 1880, 1890 and 1900 (N = 493,822). Using this data, we use the same method as for Ghana to construct the log export value of _all_ seven crops _s_ in cell _c_ and year _t_ . We then regress a dummy if there is a mission in cell _c_ in _t_ on log predicted cash crop export value in cell _c_ in _t_ , while adding cell and year fixed effects as well as country-year fixed effects.<sup>55</sup> 

Row 1 of col. (2) in Panel B of Table 5 shows a strong positive effect (0.001***) of log predicted cash crop export value. This effect is driven by one crop, palm oil, as other crops were not important at that time, with the exception of groundnuts that overlap with core Muslim areas. Next, no spurious effects are found when adding one lead of the Bartik (row 8), but the effect of cash crops in _t_ on missions in _t_ is mostly captured by a lag of the Bartik (row 9). Rows 10–11 show results hold when we add ethnic or district fixed effects interacted with year fixed effects. 

In terms of magnitude, however, the effect is not that strong: A one standard deviation in cash crop value is associated with a 0.02 standard deviation in the mission dummy 

> 54 There is a concern that missionaries locally promoted crop cultivation in other countries than Ghana. However, in most of colonial Africa, cash crop cultivation was driven by African initiative (Austin 2014) - not mission societies. 

> 55 For cells _c_ , countries _n_ , and years _t_ , the specification is (standard errors clustered at the district level): Mission Dummy _c_ , _n_ , _t_ = _훼_ + _훽̂_ Cash Crop Export Value _c_ , _n_ , _t_ + _휔c_ + _휆t_ + _휅n_ , _t_ + _vc_ , _n_ , _t_ . 

1 3 

Journal of Economic Growth (2022) 27:149–192 

174 

**Table 5** Railroads, cash crops and missions, long-diff. and panel, Africa 

|Panel A: Dependent Variable: Dummy if Atlas Mission|...|(1) Defne|d in 1900|(2) Defne|d in 1924|
|---|---|---|---|---|---|
|Efect of Dummy Rail 0–30 km ...||Defned in|1900|Defned in|1924|
|||Coef.|SE|Coef.|SE|
|1. Rail 0–30 km||0.007***|[0.002]|0.010***|[0.001]|
|2. Including Country-Ethnic Group Fixed Efects (N =|1,158)|0.008***|[0.002]|0.010***|[0.001]|
|<br>3. Including District ca. 2000 Fixed Efects (N = 3,284|<br>)|0.007***|[0.003]|0.007***|[0.001]|
|<br>4. Rail 0–30 km Dummy Using Military-Mining Lines|<br>Only|0.007***|[0.003]|0.006***|[0.002]|
|5. IV: 30 km from EMST Network (Drop Nodes; IV F|= 49/82)|0.025**|[0.011]|0.021***|[0.006]|
|6. Rail 0–30 km Dummy Using 1916 & 1922 Placebo Li|nes Only|0.001|[0.001]|0.001|[0.001]|
|Country FE, Controls of Table6except Pop, Crops, Roads<br>(see notes)|_t_|Y|Y|Y|Y|
|Panel B: Dependent Variable: Dummy if Atlas Mission ..|.<br>(1) in Y|ear_t_||(2) in Year|_t_|
|Efect of ...|~~Rail 0–~~|~~30 km Dum~~|~~my~~_~~t~~_|LogCash|Crop _t_|
||Coef.|SE||Coef.|SE|
|7. Baseline Efect in Year_t_|0.0027*|*<br>[0.|0011]|0.0011***|[0.0002]|
|<br>8. Efect of the Lead when Added|0.0004|[0.|0006]|0.0001|[0.0001]|
|<br>9. Baseline Efect in Year_t_if Lag Added|0.0028*|**<br>[0.|0011]|0.0004***|[0.0001]|
|<br>Efect of the Lag when Added|–0.0007|[0.|0013]|0.0009***|[0.0002]|
|<br>10. Including Ethnic-Year FE|0.0019*|[0.|0011]|0.0006**|[0.0003]|
|11. Including District-Year FE|0.0016|[0.|0013]|0.0008**|[0.0004]|
|Cell FE, Year FE, Country-Year FE|Y|Y||Y|Y|



Panel A: For 203,574 cells, we regress a dummy if there is an Atlas mission in 1900 (col. (1)) or 1924 (col. (2)) on the 0–30 km rail dummy and the controls of Table 6 except the population levels, cash crop and mining variables defined ca 1900 in col. (1) and ca 1924 in col. (2) (see footnote 33 for details). Panel B Col. (1): For 103,866 cells _c_ in 15 countries with railroads at one point in 1885–1990 and the years 1885, 1890, 1895 and 1900 (N = 415,464), we regress a dummy if there is a mission in cell _c_ in _t_ on a dummy if cell _c_ is within 30 km of a railroad in _t_ (cell FE, year FE, and country-year FE included). Panel B Col. (2): For 70,546 cells _c_ in 20 countries with cash crop export data and the years 1850, 1860, 1870, 1875, 1880, 1890 and 1900 (N = 493,822), we regress a dummy if there is a mission in cell _c_ in _t_ on log predicted cash crop export value in cell _c_ in _t_ (cell FE, year FE, and country-year FE included). See text for details on each regression. Robust SE’s clustered at the district (2000) level: * p<0.10, **p<0.05, *** p<0.01. See Web A ppx. for data sources. 

(vs. 0.20–0.23 for Ghana). However, both mission and cash crop values are mismeasured for Africa. 

Finally, the Bartik analysis shows an additional effect on the number of missions once we control for whether the cell had a mission (see Web Appx. Table A9). The table also confirms that cash crop incomes have stronger effects on Mainline Protestant missions than on other Protestant missions. 

### **4.6  Economic development and the adoption of a new religion** 

To summarize, missions were established in more developed areas. We now discuss why increased missionary supply was met by African demand for Christianity at these locations. 

1 3 

Journal of Economic Growth (2022) 27:149–192 

175 

**Table 6** Correlates of missions, long-diff., selected factors, Africa 

|Dependent Variable|Columns (1)–(|5) Dummy if A|tlas Mission in|the Cell in||
|---|---|---|---|---|---|
||Beach|Roome|Columns (3)|–(5) Beach in ...||
||in 1900|in 1924|1850|1881|1900|
||(1)|(2)|(3)|(4)|(5)|
|Dummy if Any Mission in ... 1850/1881||||0.9797***|0.9866***|
|||||[0.0037]|[0.0019]|
|Historical Malaria Index|− 0.0253***|− 0.0478***|− 0.0038|− 0.0147***|− 0.0065|
||[0.0094]|[0.0156]|[0.0029]|[0.0046]|[0.0063]|
|Tsetse Index|− 0.0033|− 0.0085***|− 0.0002|− 0.0017|− 0.0020|
||[0.0023]|[0.0028]|[0.0007]|[0.0012]|[0.0013]|
|Log Distance to Coast|− 0.0030***|− 0.0030***|− 0.0007***|− 0.0009***|− 0.0015***|
||[0.0005]|[0.0005]|[0.0002]|[0.0002]|[0.0003]|
|Dummy if Large Pre-colonial city 1400|− 0.0312***|0.0502|− 0.0082**|− 0.0134***|− 0.0100***|
||[0.0088]|[0.0398]|[0.0036]|[0.0046]|[0.0037]|
|Dummy if Largest or 2nd Largest City 1901|0.0579***|0.1734***|0.0264***|0.0207|0.0297**|
||[0.0196]|[0.0265]|[0.0095]|[0.0140]|[0.0145]|
|Year of Colonization|− 0.0000|− 0.0000***|− 0.0000**|− 0.0000|0.0000|
||[0.0000]|[0.0000]|[0.0000]|[0.0000]|[0.0000]|
|Dummy if Centralized State (Murdock)|0.0023***|− 0.0012*|0.0001|0.0012***|0.0011***|
||[0.0007]|[0.0007]|[0.0002]|[0.0004]|[0.0004]|
|Log Distance to Muslim Center|− 0.0006|0.0022***|0.0004**|− 0.0002|− 0.0005|
||[0.0005]|[0.0005]|[0.0001]|[0.0003]|[0.0003]|
|Dummy if Slave Port in the Cell 1800–1900|0.0458**|0.1306***|0.0121|0.0244|0.0071|
||[0.0222]|[0.0309]|[0.0118]|[0.0151]|[0.0132]|
|Dummy if Navigable River 10 km|0.0030**|0.0116***|− 0.0004|− 0.0004|0.0035***|
||[0.0014]|[0.0023]|[0.0003]|[0.0005]|[0.0012]|
|Dummy if Explorer Route 10 km|0.0006|0.0016*|0.0001|0.0002|0.0003|
||[0.0006]|[0.0008]|[0.0001]|[0.0004]|[0.0005]|
|Dummy if Railroad 1900/1924 10 km|0.0138***|0.0227***|0.0044**|0.0012|0.0046*|
||[0.0043]|[0.0027]|[0.0020]|[0.0023]|[0.0024]|
|Log city pop. ca 1900 (Loc.≥10,000)|0.0110***|0.0024|0.0034**|0.0026|0.0041*|
||[0.0029]|[0.0029]|[0.0017]|[0.0019]|[0.0021]|
|Log Urban Population 1900|0.0019***|0.0065***|0.0005***|0.0009***|0.0008***|
||[0.0004]|[0.0006]|[0.0002]|[0.0002]|[0.0002]|
|Log Rural Population 1900|0.0008***|0.0004**|0.0002**|0.0005***|0.0002*|
||[0.0002]|[0.0002]|[0.0001]|[0.0001]|[0.0001]|
|Dummy if Slavery (Murdock)|0.0011|0.0026***|0.0002|0.0002|0.0006|
||[0.0007]|[0.0009]|[0.0002]|[0.0004]|[0.0004]|
|Log Norm. Slave Exports 15th−19th C.|0.0009|0.0058***|− 0.0001|0.0006|0.0006|
||[0.0006]|[0.0011]|[0.0003]|[0.0004]|[0.0004]|
|Log Pred. Cash Crop Export val. 1900/1924|0.0005***|0.0005*|0.0002*|0.0003**|0.0001|
||[0.0002]|[0.0003]|[0.0001]|[0.0001]|[0.0001]|
|Dummy if Polygamy (Murdock)|− 0.0015**|0.0013*|− 0.0000|− 0.0010***|− 0.0006|
||[0.0006]|[0.0007]|[0.0001]|[0.0004]|[0.0004]|
|Fixed Efects|Country|Country|Country|Country|Country|
|<br>Adj. R-squared|0.03|0.04|0.02|0.25|0.52|



1 3 

Journal of Economic Growth (2022) 27:149–192 

176 

#### **Table 6** (continued) 

For 203,574 cells in 43 sub-Saharan African countries, we regress a dummy if there is an atlas mission in Beach in 1900 (col. (1)) or in Roome in 1924 (col. (2)) on various locational factors (country fixed effects always included). We do not report the coefficients of land area, rainfall, altitude, ruggedness, soil fertility, a dummy if there was a large pre-colonial city in the cell circa 1800, a dummy if the cell is within 10 km from a lake, a dummy if the cell is within 50 km from a mine in 1900 or 1924, a dummy if the main ethnic group in the cell before colonization according to Murdock (1959) does not have information on state centralization, slavery and polygamy, a dummy if we know the year of the anthropological study used by Murdock (1959) to create his data, and a dummy if that year precedes 1900/1924. Col. (3)–(5): For Beach and each period [ _t_ - _s_ ; _t_ ], we regress a dummy if there is a mission in _t_ on the locational factors and a dummy if there is a mission in _t_ - _s_ . Robust SE’s clustered at the district (2000 boundaries) level: * p<0.10, ** p<0.0 5, *** p<0.01. See Web Appx. for data sources. 

First, our results do not exclude the possibility that it was the poorest individuals in the richest places who converted to Christianity (Hastings 1994; Maxwell 2016). By the mid19th century, Christianity had broadened its appeal among the commercial elite, such as cash-crop farmers and merchants (Debrunner 1967). Indeed, missions required financially capable members to contribute to church activities (see Sect. 3). 

Second, Barro and McCleary (2003) argue that if participating in religious activities increases wages, for example because religion and human capital are complements, growth and religiosity go hand in hand. Missions supplied the bulk of formal education (Frankema 2012), which commanded a wage premium and facilitated occupational mobility (Ekechi 1971; Frankema and Van Waijenburg 2019; Meier zu Selhausen et al. 2018). However, the complementarity between Christianity and schooling weakened over time. In Ghana, since the 1870s missions increasingly opened without government approved schools. In 1932, only one out of six missions had a school (Fig. 3). After World War II states expanded the supply of state schools and missions lost their monopoly on schooling. Hence, schooling cannot fully account for the appeal of Christianity. 

Third, Christianity disrupted the monopoly, and spread at the expense of, African traditional religions. It has been argued that such religions constrained individual ownership and restricted the pursuit of self-interest (Pauw 1996; Alolo 2007). Christianity, in particular the Protestant denominations, are more capitalist in nature. There are also spiritual needs in a world where established systems of meaning became increasingly disrupted by changing social and economic circumstances, including new technologies (e.g., railroads and steamships). Africans sought a measure of conceptual control over these forces by turning to the new ideas offered by Christianity (Maxwell 2016). Thus, Christianity may have been for converts a more this-worldly religion. 

## **5  Implications for the study of long‑run economic development** 

Our results have several implications for the study of the long-run effects of colonial missions. Most studies retrieve mission location data from a source different from ours: Historical mission atlases. Using Ghana as an example, we first show that atlases select the most important missions (e.g. early, main or European residence stations). Second, we will examine the long-term economic and non-economic effects of missions when relying on atlas missions _or_ census missions and the standard controls used in the literature _or_ our controls, and compare different types of missions. 

1 3 

Journal of Economic Growth (2022) 27:149–192 

177 

### **5.1  Mission Atlases and non‑classical measurement error in missionary activity** 

In the literature, two mission atlases feature prominently: Beach (1903) and Roome (1925).<sup>56</sup> Yet, we find that atlases significantly underreport missions. For Ghana, atlases show far fewer missions than census returns: 26 vs. 304 (91% are missing) in 1900 (Beach 1903) and 23 vs. 1213 (98%) in 1924 (Roome 1925) (see Fig. 2a–b). For Africa, the extent of misreporting is of similar scale: Beach (1903) and Roome (1925) omitted 93% and 98% of missions (see Fig. 1b).<sup>57</sup> If measurement error is classical, estimates of the contemporary effect of missions will be downward biased. However, this is far from certain. Fahs (1925) pointed out that atlases overwhelmingly plot residence stations of European missionaries. In this case, measurement error is non-classical.<sup>58</sup> 

We can investigate the measurement error thanks to our unique data on _census_ missions and their characteristics. Examining the geographic distribution of missions in Ghana (see Fig. 2a and b) reveals two stylized facts. First, atlases miss most hinterland missions. Second, Roome (1925) does not capture the exponential growth of missions between 1900 and 1924. We study this further by calculating the coefficients of correlation between a dummy equal to one if there is an atlas mission (1900, 1924) and a dummy equal to one if there is a census mission in a cell for each year (1840–1932). Figure 7b shows high correlations for earlier years (0.8 for Beach (1903) and 0.4 for Roome (1925)).<sup>59</sup> Atlases thus best represent missions circa 1850 (that survived) instead of 1900, or 1924. 

Atlas missions also differ qualitatively. In Table 7 we regress a dummy equal to one if there is an atlas mission on cell-level mission characteristics derived from our data for the years 1900 and 1924. The correlations show that atlases capture not only early missions (col. (2) and (7)), but also main stations as well as missions with schools (col. (3) and (8)) and the residences of European missionaries (col. (4) and (9)). Some characteristics are then correlated with each other (col. (5) and (10)).<sup>60</sup> The  R<sup>2</sup> is then 0.64–0.45 (0.79–0.55 with 2x2 cells). Overall, atlases selected “better” missions. But, do atlases at least reliably select the “best” missions that received major investments? The answer is no. If we define the “best” missions as the ones that were main stations, where Europeans resided and which had a school, atlases still miss 68–83% of them. 

> 56 Based on Web Appx. Table A1, about 30 studies rely on either Beach (1903) or Roome (1925). 

> 57 The extent of omissions is relatively similar across movements and denominations: Beach (1903) misses 89% of Methodist missions and 92% of Presbyterian missions whereas Roome (1925) misses 97% of Protestant missions and 99% of Catholic missions. Other atlases compare as follows: 25 vs. 432 Protestant missions (i.e., 94% of missions are missing) in 1908 (Bartholomew et al. 1911) and 6 vs. 49 Catholic missions (88%) in 1913 (Streit 1913). 

> 58 Fahs (1925, p. 271) wrote that “[...] mapping the Christian advance which puts a red underline under some place-name to indicate the residence of a British or Continental or American missionary, but does not indicate where an Azariah or a Kagawa serves his people, fails to give needful perspective.” Mission atlases thus ignore the very significant contribution of African missionaries to Christian expansion (Meier zu Selhausen 2019). 

59 When combining cells into 2x2 cells to account for possible inaccuracies in the geocoding of atlas missions, the correlation of earlier years is 0.9 for Beach (1903) and 0.7 for Roome (1925) (not shown). 

60 The variables still describe different mission characteristics. Correlation coefficients between the eight variables average 0.45 (28 combinations), so much lower than 1. 

1 3 

Journal of Economic Growth (2022) 27:149–192 

178 

|||(10)|− 0.01|[0.03]<br>0.24*<br>[0.13]<br>0.12***<br>[0.02]<br>0.17***<br>[0.05]<br>− 0.01<br>[0.03]<br>0.09<br>[0.06]<br>− 0.09**<br>[0.04]<br>0.10***<br>[0.04]<br>2,069<br>0.45|he same year<br>* p<0.10, **|
|---|---|---|---|---|---|
|||(9)|0.02*|[0.01]<br>0.01<br>[0.03]<br>0.37***<br>[0.04]<br>2,069<br>0.29|the same cell t<br>m Conley SE’s:|
||1924|(8)|− 0.07**|[0.03]<br>0.22***<br>[0.05]<br>0.05*<br>[0.03]<br>0.10*<br>[0.06]<br>2,091<br>0.31|haracteristics in<br>r 22 obs. 100 k|
||10): Roome in|(7)|0.01***|[0.00]<br>0.46***<br>[0.14]<br>0.22***<br>[0.02]<br>2,091<br>0.28|the mission c<br>ry missing fo|
||Col. (6)–(|(6)|0.06***|[0.02]<br>2,091<br>0.05|oome (1924) on<br>of the missiona|
|||(5)|− 0.05|[0.05]<br>0.01<br>[0.12]<br>− 0.09**<br>[0.04]<br>0.06<br>[0.04]<br>0.59***<br>[0.11]<br>0.01<br>[0.01]<br>0.04**<br>[0.02]<br>0.10<br>[0.11]<br>2,069<br>0.64|h (1900) or R<br>–(10): Identity|
|.||(4)|0.03**|[0.01]<br>0.08*<br>[0.05]<br>0.40***<br>[0.07]<br>2,069<br>0.35|cell_c_in Beac<br>)–(5) and (9)|
|ssion in Cell_c_in..|900|(3)|− 0.04|[0.05]<br>0.06<br>[0.05]<br>0.61***<br>[0.11]<br>0.02<br>[0.03]<br>2,091<br>0.61|Atlas mission in<br>nsus data. Col. (4|
|f any Atlas Mi|5): Beach in 1|(2)|0.04***|[0.01]<br>0.53***<br>[0.05]<br>0.21***<br>[0.07]<br>2,091<br>0.37|if there is an<br>ated) in our ce|
|Dummy i|Col. (1)–(|(1)|0.16***|[0.03]<br>2,091<br>0.15|ss a dummy<br>erwise indic|
|Dependent Variable:|||Census Mission Year_t_|Created 1751–1850<br>Created 1851–1875<br>Log Num. Mission Year_t_<br>Main Station Year_t_<br>School Year_t_<br>Euro Residence 1846–90<br>Euro Visit 1846–90<br>Observations<br>R-squared|For 2091 cells_c_, we regre<br>(1900 or 1924, unless oth|



1 3 

Journal of Economic Growth (2022) 27:149–192 

179 

### **5.2  Non‑classical measurement error and long‑term economic effects** 

We now study the long-term economic effects of missions, depending on whether we rely on _census_ missions or _atlas_ missions. We run a regression correlating a dummy equal to one if the location had a mission ( _Mc_ , _g_ ) in 1900 or 1924 and economic development today ( _Dc_ , _g_ , _today_ ): 



Given the lack of data on incomes at the local level, we use log average night light intensity in 2010 – i.e., the total sum of night lights divided by area – as development indicator ( _Dc_ , _g_ , _today_ ). To avoid issues related to top-coding, we use the radiance calibrated version of this data (NOAA 2012), which records levels of luminosity beyond the normal digital number upper bound of 63.<sup>61</sup> 

For both Ghana and Africa, we examine how _휌_ varies if we include: (i) No controls _Xc_ , _g_ ; (ii) The “standard” controls commonly used in the literature on Africa ( _Std_ ). In particular, we merge the lists of controls from Nunn (2010, 2014) and Cagé and Rueda (2016). Small variations over this set of controls have been used, for example, by Fenske (2015), Okoye (2021), Henn et al. (2021) and Cagé and Rueda (2020);<sup>62</sup> (iii) Our full set of possible determinants from Table 1 (Ghana) or Table 6 (Africa) ( _Ours_ ); and (iv) Our full set of controls as well as controls for the _type_ of mission. The latter include (only available for Ghana; from Table 7) whether the mission was created in 1751–1850 or 1851–75, is a main station in _t_ , has a school in _t_ , a European missionary lived there in 1846–90, and a European missionary frequently visited the mission in 1846–90. When controlling for the type, the effect is estimated for _average_ missions, which minimizes external validity concerns. 

Table 8 presents the results. For Ghana, using the _census_ mission dummy (row 1 of Panel A), we find large unconditional effects of 1.05***–0.84*** (col. (1) and (6)). Adding the _standard_ controls reduces the estimated effect to 0.78***–0.73*** (col. (2) and (7)). An early colonial mission thus (relatively) increases night lights by 117–107%, or 0.35–0.49 if expressed in terms of standard deviations.<sup>63</sup> Next, with the imperfectly measured _Africa_ controls (from Table 6), the effect is further reduced by almost 50%, to 0.41***–0.38*** (col. (3) and (8)). If we use _our_ extended set of Ghana controls, the effect is further divided 

> 61 Nightlights have become a standard measure in the stream of literature that studies development at the local level in Africa (Michalopoulos et al. 2013, 2014; Alesina et al. 2016; Michalopoulos et al. 2018). 

> 62 Nunn (2010, 2014,Table 1) uses: (i) _European explorer routes before colonization_ ; (ii) _19th century railroads_ ; (iii) _soil quality_ ; (iv) _access to a water source_ ; and (v) _slave exports_ . For Ghana: (i) There were no explorers before official colonization (there is thus no variation across cells); (ii) There was no railroad before 1901 (ditto); (iii) We control for soil fertility; (iv) We add a dummy if the cell is within 10 km from a navigable river (there were no lakes then); and (v) We control for slave export intensity. (Cagé and Rueda 2016, 2020, Table 1) add: (vi) _rainfall_ ; (vii) _distance to the coast_ ; (viii) _malaria ecology_ ; (ix) _initial population density_ ; and (x) _dummies if large cities in 1400 or 1800_ . For Ghana: (vi) We control for rainfall; (vii) We control for distance to the coast; (viii) We control for malaria; (ix) We control for population density in 1800; and (x) We add a dummy if there was a large city in 1800 (none in 1400). 

> 63 117–107 comes from applying the formula 100 (exp(b - V(b)/2) - 1) (Halvorsen and Palmquist 1980; Kennedy 1981). 

1 3 

Journal of Economic Growth (2022) 27:149–192 

180 

||+Type|(10)|0.17***|[0.05]<br>0.33**|[0.16]|0.17***|[0.05]|0.16|[0.19]|_<br>_|the litera-<br>_is.Year_ _t_.<br>eb Appen-|
|---|---|---|---|---|---|---|---|---|---|---|---|
||Ours|(9)|0.19***|[0.05]<br>0.50***|[0.15]|0.19***|[0.05]|0.32*|[0.17]|_<br>_|larly used in<br>t_Log Num.M_<br>0.01. See W|
||Africa|(8)|0.38***|[0.09]<br>0.73***|[0.21]|0.38***|[0.09]|0.43*|[0.23]|0.37***<br>[0.03]|fed as regu<br>ble7excep<br>.05, *** p<|
||Std|(7)|): 1924 (Roome1925)<br>0.73***|[0.07]<br>1.43***|[0.10]|0.69***|[0.07]|1.08***|[0.12]<br>): 1924 (Roome1925)|0.59***<br>[0.04]|untries. “Standard”: Controls identi<br>1. “Type”: All Ghana controls of Ta<br>Africa (Panel B): * p<0.10, ** p<0|
|ell in 2010:|None|(6)|Col. (6)-(10<br>0.84***|[0.10]<br>1.60***|[0.22]|0.80***|[0.09]|1.40***|[0.23]<br>Col. (6)-(10|0.69***<br>[0.04]|ran African co<br>trols of Table<br>ries) level for|
|ity in the C|+Type|(5)|0.01|[0.03]<br>0.44**|[0.19]|0.01|[0.03]|0.43|[0.26]|_<br>_|3 sub-Saha<br>Ghana con<br>00 bounda|
|Light Intens|Ours|(4)|0.12|[0.08]<br>0.54***|[0.03]|0.09|[0.08]|0.48***|[0.10]|_<br>_|74 cells in 4<br>Ours”: All<br>district (20|
|Log Night|Africa|(3)|each1903)<br>0.41***|[0.08]<br>0.78***|[0.15]|0.37***|[0.10]|0.59***|[0.22]<br>each1903)|0.40***<br>[0.04]|ple: 203,5<br>f Table6. “<br>tered at the|
|nt Variable:|Std|(2)|5): 1900 (B<br>0.78***|[0.09]<br>1.39***|[0.09]|0.65***|[0.09]|1.22***|[0.09]<br>5): 1900 (B|0.60***<br>[0.05]|: Africa sam<br>ca controls o<br>nd SE’s clus|
|Depende|None|(1)|Col. (1)-(<br>1.05***|[0.13]<br>1.76***|[0.20]|0.89***|[0.10]|1.67***|[0.21]<br>Col. (1)-(|0.70***<br>[0.05]|ells. Panel B<br>a”: All Afri<br>(Panel A) a|
||Controls Included:|Efect of ... Mission Dummy:|**Panel A:** **_Ghana_**(N = 2,091)<br>1. Census Mission Dummy|2. Atlas Mission Dummy||Non-Atlas Mission Dummy|(= Census - Atlas Dummies)|3. Atlas Mission Dummy|**Panel B:** **_Africa_**(N = 203,574)|Atlas Mission Dummy|Panel A: Ghana sample: 2091 c<br>ture (see text for details). “Afric<br>100 Km Conley SE’s for Ghana<br>dix for data sources.|



1 3 

Journal of Economic Growth (2022) 27:149–192 

181 

by 2 or even 3, to 0.12–0.19*** (col. (4) and (9)).<sup>64</sup> Lastly, also controlling for the _type_ of missions, the effect decreases to 0.01–0.17*** (col. (5) and (9)). One standard deviation in the mission dummy is then associated with a 0.00–0.12 increase in the standard deviation in log night lights.<sup>65</sup> Therefore, we find that the average (census-based) missions had possibly no or weak effects on contemporary development in Ghana.<sup>66</sup> 

However, atlas missions, because they capture important missions, could still have strong long-term economic effects, especially if we do not control for their potentially endogenous placement and type. In row 2 of Panel A, we use the same model as in row 1 but, instead of the _census_ mission dummy, we include an _atlas_ mission dummy and a _nonatlas_ mission dummy (defined as census mission dummy - atlas mission dummy). Without controls, we obtain twice larger point estimates for atlas missions. The effect of atlas missions is still much larger, by 0.74*** (not shown), if we add the standard controls (col. (2) and (7)). Once we add our controls, including the type of missions (col. (5) and (10)), we again find nil or small effects for non-atlas mission (0.01–0.17***). Although atlas missions have a stronger effect, the difference with respect to non-atlas missions is barely significant (0.43*; col. (5)) or insignificant (0.15; col. (10)).<sup>67</sup> More generally, using our full controls rather than the standard controls decreases the effects of atlas missions for Ghana by (1–0.44/1.39)*100 = 68% for Beach and (1–0.33/1.43)*100 = 77% for Roome.<sup>68</sup> 

In row 3, Panel A of Table 8 , we study the effects for Ghana when we only include the _atlas_ mission dummy, in order to mimic the regressions we are running for Africa next. When doing so, the effect of atlas missions is slightly lower than when controlling for the non-atlas missions. However, the same patterns as before emerge. Using our full controls rather than the standard controls decreases the effects of atlas missions for Ghana by 65-85%. 

_atlas_ missions Finally, in Panel B, we examine for 43 African countries the effects of on contemporary night lights. The unconditional effect is 0.70*** (col. (1) and (6)). Adding the standard controls reduces the effect to 0.60–0.59*** (col. (2) and (7)). Thus, a colonial mission increases night lights by 82–80%, or 0.10–0.13 if expressed in terms of standard deviations. Adding our Africa controls then lowers the effect to 0.37–0.40*** (we found 0.43–0.59*** for Ghana, see row 3), or 0.07–0.08 if expressed in terms of standard 

64 One concern is that some of our controls are defined ex-post. If we exclude or adjust the timing of these controls, the estimated effects (c. 0.25***) are still two thirds lower than with the standard controls (not shown). We use roads c. 1900 and c. 1924 (instead of 1930). For 1924, we use railroads c. 1924 (instead of 1932). We exclude urban and rural populations in 1931 and the crop variables. However, our palm oil (measured in 1900–36), rubber (1900–36) and kola (1932) controls reflect conditions before 1924 (or even 1900) since these cash crops boomed early (Sect. 4.3). Cocoa is a perennial crop, and harvest begins after 5 years. Cocoa production c. 1927 reflects cocoa cultivation in 1922 or before. 65 We do not over-control for the number of missions here. If we do, we obtain –0.26*** and 0.05 (not shown). 

66 Note that we cannot distinguish whether the standard controls produce biased estimates because they do not capture selection on unobservables (missions were established in places likely to be developed even in the absence of a mission) or selection on beta (missions were established where the population was already receptive to missions ideas, and this pre-disposition could have contributed to long-run economic development). 

67 Without the ex-post controls, the atlas effect is three times lower than with the standard ones (not shown). 68 Ultimately, with our full controls, a census mission increases night lights by 1–18% whereas an atlas missions increases night lights by 37–52%. Jedwab and Moradi (2016) find that a railroad built in Ghana before 1918 increases night lights by 365% (the coefficient is 1.64 but we use the standard formula 100 (exp(b - V(b)/2) - 1)). 

1 3 

Journal of Economic Growth (2022) 27:149–192 

182 

deviations. If we also add two dummies for whether a Beach mission already existed pre1850 or in 1850–1881 – our only _type_ control for Africa –, the effect for the year 1900 decreases further to 0.28*** (not shown), which is about half the effect with the standard controls. However, the Africa controls are not as precisely measured as those for Ghana.<sup>69</sup> We also just showed how using better controls reduces the effects of atlas missions by 65–85% for Ghana. Were this the case for Africa, the standardized effect would only be 0.02. 

### **5.3  Extensions** 

**Measurement Error in the Controls.** If the best missions are selected, the long-term effects of missions will be over-estimated. The same is true if only mismeasured controls of mission placement are available. For example, for the Africa regressions, we have no choice but to use the Murdock (1967) map to obtain data on state centralization, slavery and polygamy. As such, the reported estimates when using our full controls likely remain upward-biased. As we just showed, the better measured Ghana controls, which do not rely on continental maps, reduce the effects twice as much as the Africa controls. Now, if we drop the Murdock controls and instead add ethnicity, country-ethnicity, province or district (as of 2000) fixed effects, the Africa effects slightly decrease to about 0.30***–0.35*** (see Panel A of Web Appx. Table A10). However, the mean province is large in Africa, with an area of 228,000 sq km vs. 197,000 on average for U.S. states. The mean ethnic territory (141,000) and the mean district (84,000) are then 1.4 and 2.3 times smaller than the average U.S. state, which is still large. For Ghana, when using the standard controls (see Panel B of Web Appx. Table A10), adding province, ethnicity or district fixed effects only reduces the 1900-based effect from 0.78*** to 0.74***, 0.58*** and 0.51***, respectively, vs. 0.01 with our full controls. The 1924-based effect only decreases from 0.73*** to 0.68***, 0.60*** and 0.50***, respectively, vs. 0.17*** with our full controls. Thus, the standard controls do not capture the fact that missionaries went to more developed areas _within_ these spatial units. 

**Spillovers.** Our main unit of analysis are grid cells of 0.1 x 0.1 degrees (12 x 12 km). The minimal distance from the centroid of the cell to its edge is 6 km, or a one-hour walking distance. Due to the lack of transportation technology, missions were likely to only influence local development during the colonial era. However, spillovers remain a possibility. We use the same model as before but also add the log of the minimal distance to a cell with a mission. When doing so, we find strong spillover effects with the standard controls but no effects when adding our controls (see Panel A of Web Appx. Table A11). Alternatively, if we use dummies if the cell is 0–10, 10–20 or 20–30 km from a cell with a mission, we find strong effects that are decreasing with distance with the standard controls, and no spillover effects for the year 1900 and a barely significant 10–20 km effect for the year 1924 when using our controls including for the type of missions (Panel B). 

> 69 For example, we use the pre-colonial explorer routes digitized by Nunn and Wantchekon (2011). This is an imperfect measure of pre-missionary era trade routes. For Ghana, this database returns 581 km of explorer routes (percentage of grids within 10 km of a route = 4.8%), whereas our sources indicate 6,526 km of trade routes (30.0%). For Madagascar, Nunn and Wantchekon (2011) do not record any explorer routes, whereas a different source suggests that all mission stations are clustered along explorer routes and the coast (see Web Appendix Figure A5). 

1 3 

Journal of Economic Growth (2022) 27:149–192 

183 

The fact that mission societies dispro- **Effects of Missions in More Developed Areas.** portionately established mission stations in more developed areas makes it even more surprising that we find nil or small long-term effects of colonial missions. For example, railroads and cash crops might have planted the seeds of future economic development, thus creating complementarities raising the long-term economic effects of missions. To examine how strong such complementarities could be, we use the model where we study the effects of the census mission dummy on log night light intensity in 2010. We then interact the census mission dummy with a dummy if the cell was ever within 30 km from a 1932 railroad as well as a dummy if the cell was potentially producing one of the four dominant cash crops during the colonial era (cocoa, kola, palm oil and rubber). As seen in Web Appx. Table A13, once we include our controls, we find no significant positive differential effects of missions in rail or cash crop areas vs. missions outside these areas. 

Our analysis suggests that the _aver-_ **Effects of Missions Depending on Their Type.** _age_ census mission might have had limited long-term economic effects. Yet, it could be that only census missions of a particular “importance” indeed mattered. We can examine this hypothesis for Ghana thanks to our unique data. We use the model where we study the effects of the census mission dummy on log night light intensity in 2010. However, we now also add variables capturing the _type_ of missions.<sup>70</sup> First, in columns (1) and (5), Table 9 we explore whether contemporary effects vary with the foundation year of the mission. With the standard controls (Panel A), we find strong positive effects for missions created early (in 1751–1850 or 1851–1875). With our controls (Panel B), the effects of early missions are about halved. It might be the case that early missions were able to accumulate growth effects over a longer period of time. Alternatively, early missions may have received more investments, i.e. they could have been main / school / European missions. In columns (2) and (6), we study the effects of the log number of missions – i.e., the intensive margin – and whether there was a main station or a school. With our controls (Panel B), we only find a significant effect of the log number of missions in 1900. In columns (3) and (7), we find strong effects of more European missions. The effects are about halved with our controls. Finally, if we add _all_ characteristics and our controls (Panel B), the only effects that remain significant are for missions ‘created 1851–1875’ and the log number of missions in 1900. Hence, controlling for early creation and density, we find no effects for main / school / European missions, which is surprising since these are characteristics that one might have expected to matter.<sup>71</sup> 

**Other Strategies.** We find similar non-results on long-term economic development if we employ other strategies. In Panel A of Web Appx. Table A16, we compare cells with Protestant missions, Catholic missions, and no missions (Nunn 2014; Cagé and Rueda 2020 ). With the standard controls, we find higher point estimates for Protestant missions. With our controls, point estimates are much lower, and their difference is reversed. We also compare cells where missions survived with cells where missions were abandoned as in Valencia Caicedo (2019a). For the year 1924, we find strong effects with the standard controls and no effects with our controls (Panel B). 

> 70 This mirrors the identification strategy of Cagé and Rueda (2016) who restrict their analysis to places near missions and compared missions with a printing press to missions without one. They assume that conditional on having a mission and the standard controls, having a certain type of mission is exogenous. 

> 71 The effects of early creation and density could be causal or reflect the fact that locations that received missions early, or had great demand for many missions, were special in ways not captured by our controls. 

1 3 

Journal of Economic Growth (2022) 27:149–192 

184 

**Example from the Literature.** Nunn (2014)’s seminal study uses the atlas missions from Roome (1925) and survey data from the 3rd round of the _Afrobarometer Surveys_ (2005–06) to study the effects of colonial-era missions on education for individuals aged 18 or older. Column (1) of Nunn’s Table 1 regresses the respondent’s educational attainment on the log number of atlas missions per 1,000 km among the respondent’s _ethnic group_ , adding country fixed effects, individual-level controls (age, gender, urban) and ethnicity-level controls (see footnote 57). Column (2) of Nunn’s Table 1 then uses the log number of atlas missions per 1000 km within 25 km from the respondents’ _village/residence_ as variable of interest (controls now defined at the cluster level). 

Column (1) of Panels A-B in our Web Appx. Table A12 reports Nunn’s main results for the first specification (0.10**) and second specification (0.14***), respectively. In column (2), we replicate these Africa results, also using the respondent as the main unit of observation (standard errors clustered at the ethnic group level). However, we use the 5th round of the _Afrobaromater Surveys_ (2011–13), which is closest to the year in which night lights are measured, includes 26 countries instead of 17, and has almost twice as many observations (N = 38,087 respondents belonging to 286 groups/5,776 clusters vs. 20,914 respondents belonging to 185 groups/2,693 clusters in Nunn (2014). We obtain similar results (0.13***–0.13***). However, once we include our Africa controls at the ethnicity or cluster level (col. (3)) and controls for whether the cell already had Beach (1903) missions in the early years 1850, 1881 or 1900, an imperfect proxy for the “type” of mission (col. (4)), the effects decrease by four times, and are not statistically significant for the first specification. The standardized effects are only 0.02–0.03. If we then use Nunn’s cluster level specification for Ghana (Panel C), we find no significant effects with our controls (col. (4)).<sup>72</sup> If we use our complete set of _census_ missions in Ghana, we still find no effects (Panel D). 

**Other Outcomes.** Since the literature has focused on the effects of colonial missions on proximate determinants of economic growth, we now use the same framework to study the long-term effects of the census missions on factors such as employment, education, health, and net fertility. The data added in this analysis is retrieved from Ghana’s 2000 _Population and Housing Census_ . When studying child mortality, we rely on the geospatialized _Demographic and Health Surveys_ (DHS) (1993, 1998, 2003, 2008, 2014, 2016, and 2017). Details on the data can be found in Sect. 2. 

Our analysis of night-lights in Ghana revealed that our controls (including the type of missions) make the effect of missions disappear or reduce it by 4–6 times compared to when only the standard controls are included. If we use instead the log of the cell’s urban population or the urban share of the cell, our controls reduce the long-term effect of missions by 6–12 times relative to the standard controls (rows 1–2 of Web Appx. Table A14).<sup>73</sup> If we use log total population, our controls make any effect of missions statistically insignificant (row 3).<sup>74</sup> 

If we use the employment shares of industry and services (row 4), manufacturing and financial, real estate and business services (FIRE) – arguably the “best” industrial and 

> 72 The effect in column (1) is only significant at the 10% level due to the low number of observations. We do not use the first specification for Ghana because only 17 Murdock ethnicities are present in the Afrobaromater data. 

> 73 Consistent with the 2000 census, we define as urban any locality above 5,000. 

> 74 The effects on log night light intensity are then mostly unchanged when controlling for log urban population (not shown but available upon request), implying that log night light intensity mostly captures per capita incomes. 

1 3 

Journal of Economic Growth (2022) 27:149–192 

185 

**Table 9** Long-term effects of missions depending on their type, Ghana 

|Dependent Variable:|Log Night|Light Intens|ity in the C|ell in 2010:|||||
|---|---|---|---|---|---|---|---|---|
|Dummies Defned in:|Year 1900|(same as Be|ach)||Year 1924|(same as R|oome)||
||(1)|(2)|(3)|(4)|(5)|(6)|(7)|(8)|
|**Panel A:**Standard Control|s Included||||||||
|Census Mission Year_t_|0.59***|0.32**|0.56***|0.26**|0.65***|0.14|0.63***|0.19|
||[0.05]|[0.16]|[0.07]|[0.11]|[0.07]|[0.12]|[0.08]|[0.12]|
|Created 1751–1850|0.65***|||0.27|0.77***|||0.10|
||[0.08]|||[0.27]|[0.06]|||[0.20]|
|Created 1851–1875|0.52***|||0.33*|0.60***|||0.25|
||[0.11]|||[0.17]|[0.06]|||[0.17]|
|Log Num.||0.44***||0.36***||0.42***||0.35***|
|Mission Year_t_|||||||||
|||[0.09]||[0.14]||[0.07]||[0.10]|
|Main Station Year_t_||0.23**||− 0.05||0.13||0.00|
|||[0.12]||[0.14]||[0.10]||[0.13]|
|School Year_t_||− 0.08||− 0.25**||0.18||0.17|
|||[0.12]||[0.11]||[0.12]||[0.14]|
|Euro Residence<br>1846–1890|||0.34**|0.24*|||0.38***|0.21***|
||||[0.15]|[0.14]|||[0.09]|[0.06]|
|Euro Visit 1846–1890|||0.65***|0.44**|||0.74***|0.30*|
||||[0.07]|[0.21]|||[0.08]|[0.17]|
|Panel B: Our Controls Incl|uded||||||||
|Census Mission Year_t_|0.07|− 0.15|0.01|− 0.24***|0.18***|0.05|0.19***|0.05|
||[0.08]|[0.12]|[0.05]|[0.09]|[0.05]|[0.10]|[0.05]|[0.08]|
|Created 1751–1850|0.35*|||0.28|0.36*|||0.25|
||[0.20]|||[0.27]|[0.20]|||[0.22]|
|Created 1851–1875|0.33***|||0.31**|0.34***|||0.31**|
||[0.10]|||[0.15]|[0.07]|||[0.15]|
|Log Num. Mission Year_t_||0.36***||0.33***||0.13||0.13|
|||[0.10]||[0.12]||[0.10]||[0.09]|
|Main Station Year_t_||0.09||− 0.08||0.03||− 0.01|
|||[0.10]||[0.07]||[0.09]||[0.09]|
|School Year_t_||− 0.23**||− 0.24***||0.06||0.11|
|||[0.14]||[0.08]||[0.06]||[0.08]|
|Euro Residence 1846–1890|||0.23***|0.15|||0.19***|0.09|
||||[0.08]|[0.12]|||[0.07]|[0.11]|
|Euro Visit 1846–1890|||0.31***|0.18|||0.29***|0.09|
||||[0.06]|[0.17]|||[0.07]|[0.16]|
|Observations|2,091|2,091|2,069|2,069|2,091|2,091|2,069|2,069|



For 2069–2091 cells in Ghana (note that the identity of the missionary is missing for 2091 – 2069 = 22 obs.), we regress our main measure of local economic development, log mean night light intensity in the cell in 2010, on the census mission dummy and mission characteristics in the cell, all defined in the same year (1900 / 1924). Panel A: _Standard Controls_ : Controls identified as regularly used in the literature (see text for details). Panel B: _Our controls_ : All controls of Table 1. “Euro Residence 1846–1890”: Mission stations where European missionaries permanently resided at one point in 1846–1890 (data not available for other years). “Euro Visit 1846–1890”: Mission stations where European missionaries did not permanently reside but frequently visited at one point in 1846–1890. Robust 100 km Conley SE’s: * p<0.10, ** p<0.05, *** p<0.01. See Web Appendix for data sources. 

1 3 

Journal of Economic Growth (2022) 27:149–192 

186 

service sectors (Gollin et al. 2016) – (row 5), or skilled occupations<sup>75</sup> (row 6), we find that our controls reduce the long-term effects of missions on these by 5–9, 5–8 and 4 times, respectively. In terms of standardized effects, we find 0.00–0.12 for night lights, 0.02–0.03 for urbanization and 0.05–0.09 for employment. Row 7 of Web Appx. Table A14 uses as the dependent variable the population share of Protestants and Catholics in 2000. Our controls barely change the long-run effect of missions on Christianity. The standardized effects are 0.08–0.15, higher than for economic outcomes. 

If we use the number of years of education (row 8) or the primary completion rate (row 9) for individuals aged 18 or more in 2000, our controls reduce the effects by about 3 times relative to the standard controls. If we use height- or weight-for-age z-scores for children below 5 in 1993–2017 (source: DHS), our controls reduce the effects by 1.3–2.0 times rela- _more_ tive to the standard controls (rows 10–11). Thus, our controls reduce the effects by than they do for Christianity, and _less_ than they do for economic outcomes. Also, the standardized effects are 0.10–0.17 for education and 0.04–0.09 for health, similar or higher than for economic outcomes.<sup>76</sup> 

Our controls reduce the effects of missions on completed fertility (row 12) and net completed fertility (row 13) – for 35–49 aged women in 2000 – by 2–4 times and 2.5–5 times relative to the standard controls, respectively. Completed (child) mortality then does not vary with missions (row 14). In terms of standardized effects, with our full controls, we find − 0.03/− 0.08 for net fertility, which is similar in size to economic outcomes. 

Overall, we find stronger, but still weak, effects on education, health, and fertility, implying that missions might have affected development outcomes without spurring economic development.<sup>77</sup> 

**Way Forward and External Validity.** Our paper proposes a number of potentially important predictors for colonial missions. In principle, those predictors can be used in matching procedures or as instrumental variables for the placement of missions. However, our set of determinants is not exhaustive. Hence, the exogeneity assumption may be violated. In addition, our results are specific to the African context. In other contexts such as in Latin America, missionaries activities and colonial infrastructure and economic investments were often jointly determined by colonial governments and the Catholic Church (Valencia Caicedo 2019a, 2019b). Christian missions were then more likely “proxies” for colonization in general, making it more difficult to isolate the effects of missions themselves.<sup>78</sup> 

> 75 These include managers, professionals, technicians, and clerks. 

> 76 In Ghana, missions did not invest into health care. Elsewhere, missions were often the only health care providers during the colonial era (Cagé and Rueda 2020). Still, few missions offered health services. Of all missions only 2% and 4% of Catholic (in 1910) and Protestant (in 1923) missions respectively operated a hospital (Streit 1913; Beach and Fahs 1925). Such investments were costly to missions because they were free of charge for most patients (Doyle et al. 2020). 

77 As shown in Web Appx. Table A15, we do not find any significant positive effects of main / school / European missions on educational outcomes today. We also find nil or contradictory effects for health outcomes. Finally, whether main stations or mission schools significantly reduce net fertility depends on whether we consider 1900 or 1924. 

78 In Ghana and other British colonies in Africa, the activities of the various mission societies and colonial infrastructure and economic investments were not coordinated. In Belgian, French, Portuguese and Spanish colonies, coordination was also minimal, thus more similar to the Anglo-Saxon model of privatized missionary markets than to the Spanish/Portuguese model of “bundled” colonization/missionization historically observed in Latin America. 

1 3 

Journal of Economic Growth (2022) 27:149–192 

187 

## **6  Conclusion** 

In this paper, we studied Christian missions, a major human capital promoting institution that emerged during colonial times. We argued that in order to estimate colonial missions’ long-term economic impact, one needs a better understanding of the dynamics and economics of missionary expansion. Focusing on Ghana and Africa, we described how missionaries privileged healthier, more accessible, and richer places first. In particular, we showed how - with quinine - malaria became less of an impediment, and how transport infrastructure and agricultural export commodities attracted missions. The diffusion of Christianity, education and culture depends on spatial patterns of economic development, even at low income levels. We then showed how non-classical measurement error in mission atlases and omitted variable bias are concerns that could lead to an overly optimistic account of the importance of missions for contemporary development. 

**Supplementary Information** The online version contains supplementary material available at https:// doi. org/ 10. 1007/ s10887- 022- 09202-8. 

**Acknowledgments** We gratefully thank Oded Galor, three anonymous referees, Robert Barro, Sascha Becker, James Fenske, Ewout Frankema, Laurence Iannaccone, Timur Kuran, Stelios Michalopoulos, Dozie Okoye, Elias Papaioannou, Jared Rubin, Felipe Valencia Caicedo, Jan Luiten van Zanden, and Leonard Wantchekon for their helpful comments. We are grateful to seminar audiences at AEHN (Wageningen, Sussex), ASREC (Bologna, Luxembourg), Belfast, Bocconi, Bolzano, CEPR Economics of Religion (Venice), CSAE (Oxford), Dalhousie, EHES (Tübingen), EHS (Keele), GDE (Zurich), George Mason, George Washington, Frankfurt, Göttingen, Ingolstadt, Munich, Namur, Passau, Stellenbosch, Sussex, Tübingen, Utrecht, Warwick and WEHC (Boston). We thank Nathan Nunn, Julia Cagé and Valeria Rueda, Morgan Henderson and Warren Whatley, for sharing their datasets. We thank Madeline De Quillacq for excellent research assistance. Meier zu Selhausen gratefully acknowledges financial support of the British Academy (Postdoctoral Fellowship no. pf160051 - _Conversion out of Poverty? Exploring the Origins and Long-Term Consequences of Christian Missionary Activities in Africa_ ) 

**Funding** Open access funding provided by Libera Università di Bolzano within the CRUI-CARE Agreement. 

**Open Access** This article is licensed under a Creative Commons Attribution 4.0 International License, which permits use, sharing, adaptation, distribution and reproduction in any medium or format, as long as you give appropriate credit to the original author(s) and the source, provide a link to the Creative Commons licence, and indicate if changes were made. The images or other third party material in this article are included in the article’s Creative Commons licence, unless indicated otherwise in a credit line to the material. If material is not included in the article’s Creative Commons licence and your intended use is not permitted by statutory regulation or exceeds the permitted use, you will need to obtain permission directly from the copyright holder. To view a copy of this licence, visit http:// creat iveco mmons. org/ licen ses/ by/4. 0/. 

## **References** 

Acemoglu, D., Gallego, F. A., & Robinson, J. A. (2014). Institutions, Human Capital, and Development. _Annual Review of Economics, 6_ (1), 875–912. 

Agbeti, J. K. (1986). _West African Church History_ . Leiden: E.J. Brill. Ajayi, J. F. A., & Crowder, M. (1974). _History of West Africa_ . London: Longman. 

Alesina, A., Hohmann, S., Michalopoulos, S., & Papaioannou, E. (2021). Intergenerational Mobility in Africa. _Econometrica, 89_ (1), 1–35. 

Alesina, A., Michalopoulos, S., & Papaioannou, E. (2016). Ethnic Inequality. _Journal of Political Economy, 124_ (2), 428–488. 

Alolo, N. (2007). African Traditional Religion and Concepts of Development: A Background Paper. RAD Working Papers Series 17, University of Birmingham. 

1 3 

Journal of Economic Growth (2022) 27:149–192 

188 

Alsan, M. (2015). The Effect of the TseTse Fly on African Development. _American Economic Review, 105_ (1), 382–410. Athey, S., & Imbens, G. W. (2022). Design-based analysis in Difference-In-Differences settings with staggered adoption. _Journal of Econometrics, 226_ (1), 62–79. 

Austin, G. (2003). African Rural Capitalism, Cocoa Farming and Economic Growth in Colonial Ghana. In T. Falola (Ed.), _Ghana in Africa and the world: essays in honor of Adu Boahen_ (pp. 437-453). Trenton, NJ: Africa World Press. 

- Austin, G. (2014). Explaining and evaluating the cash crop revolution in the "peasant" colonies of tropical Africa, ca. 1890-ca. 1930: Beyond "vent for surplus". In E. Akyeampong, R. H. Bates, N. Nunn, & J. Robinson (Eds.), _Africa’s Development in Historical Perspective_ (pp. 295–320). New York: Cambridge University Press. 

- Bai, Y., & Kung, J. (2015). Diffusing knowledge while spreading God’s message: Protestantism and economic prosperity in China, 1840–1920. _Journal of the European Economic Association, 13_ (4), 669–698. 

- Barro, R. J., & McCleary, R. M. (2003). Religion and Economic Growth across Countries. _American Sociological Review, 68_ (5), 760–781. 

- Barro, R. J., & McCleary, R. M. (2005). Which countries have state religions? _The Quarterly Journal of Economics, 120_ (4), 1331–1370. 

- Barro, R. J., & McCleary, R M. (2017). Protestants and Catholics and educational investment in Guatemala. AEI Economics Working Paper 9, American Enterprise Institute. 

- Bartholomew, J. G., Dennis, J. S., Beach, H. P., & Fahs, C. H. (1911). _World Atlas of Christian Missions: containing a directory of missionary societies, a classified summary of statistics, an index of mission stations, and maps showing the location of mission stations throughout the world_ . New York: Student Volunteer Movement for Foreign Missions. 

- Bartik, T. (1991). Who Benefits from State and Local Economic Development Policies?, Kalamazoo, MI: W.E. Upjohn Institute for Employment Research. 

- Baten, J., de Haas, M., Kempter, E., & Meier zu Selhausen, F. (2021). Educational gender inequality in Sub-Saharan African: a long-term perspective. _Population and Development Review, 47_ (3), 813–849. 

- Basel Mission. (1900). _Report of the Basel Evangelical Mission on the Gold Coast, West-Africa, 1900_ . Basel: Evangelische Missionsgesellschaft Basel. 

- Beach, H. P. (1903). _A Geography and Atlas of Protestant Missions: their environment, forces, distribution, methods, problems, results and prospects at the opening of the twentieth century_ (Vol. 2). New York: Student Volunteer Movement for Foreign Missions. 

- Beach, H. P., & Fahs, C. H. (1925). _World Missionary Atlas_ . New York: Institute of Social and Religious Research. 

- Becker, S. O., & Woessmann, L. (2009). Was Weber Wrong? A Human Capital Theory of Protestant Economic History. _The Quarterly Journal of Economics, 124_ (2), 531–596. 

- Becker, S. O., & Woessmann, L. (2013). Not the opium of the people: Income and secularization in a panel of Prussian counties. _American Economic Review: Papers and Proceedings, 103_ (3), 539–544. 

- Becker, S. O., Nagler, M., & Woessmann, L. (2017). Education and religious participation: city-level evidence from Germany’s secularization period 1890–1930. _Journal of Economic Growth, 22_ (3), 273–311. 

- Becker, S. O., Woessmann, L., Pfaff, S., & Rubin, J. (2016). Causes and consequences of the Protestant Reformation. _Explorations in Economic History, 62_ , 1–25. 

- Bergeron, A. (2020). Religion and the Scope of Morality: Evidence from Exposure to Missions in the D.R. Congo. Unpublished manuscript, Harvard University. 

- Bisin, A., & Verdier, T. (2000). Beyond the melting pot: Cultural transmission, marriage, and the evolution of ethnic and religious traits. _The Quarterly Journal of Economics, 115_ (3), 955–988. 

- Bollinger, C. R. (1996). Bounding mean regressions when a binary regressor is mismeasured. _Journal of Econometrics, 73_ (2), 387–399. 

- Borusyak, K., & Jaravel, X. (2018). Revisiting event study designs, with an application to the estimation of the marginal propensity to consume. Unpublished manuscript, Harvard University. 

- Cagé, J., & Rueda, V. (2016). The long-term effects of the printing press in sub-Saharan Africa. _American Economic Journal: Applied Economics, 8_ (3), 69–99. 

- Cagé, J., & Rueda, V. (2020). Sex and the Mission: The conflicting effects of early Christian missions on HIV in sub-Saharan Africa. _Journal of Demographic Economics, 86_ (3), 213–257. 

- Calvi, R., & Mantovanelli, F. G. (2018). Long-term effects of access to health care: Medical missions in colonial India. _Journal of Development Economics, 135_ , 285–303. 

- Calvi, R., Mantovanelli, F. G., & Hoehn Velasco, L. (2022). The Protestant Legacy: Missions, Gender, and Human Capital in India. _Journal of Human Resources_ , forthcoming. 

1 3 

Journal of Economic Growth (2022) 27:149–192 

189 

Cantoni, D. (2012). Adopting a New Religion: The case of Protestantism in 16th century Germany. _The Economic Journal, 122_ (560), 502–531. 

Castelló-Climent, A., Chaudhary, L., & Mukhopadhyay, A. (2018). Higher Education and Prosperity: From Catholic Missionaries to Luminosity in India. _The Economic Journal, 128_ (616), 3039–3075. Chandler, T. (1987). _Four Thousand Years of Urban Growth: An Historical Census, Lewiston_ . NY: St. David’s University Press. 

Cleall, E. (2009). Missionaries, Masculinities and War: The London Missionary Society in Southern Africa, c.1860-1899. _South African Historical Journal, 61_ (2), 232–253. 

Cogneau, D., & Moradi, A. (2014). Borders that divide: Education and religion in Ghana and Togo since colonial times. _Journal of Economic History, 74_ (3), 694–729. 

Conley, T. G. (1999). GMM estimation with cross sectional dependence. _Journal of Econometrics, 92_ (1), 1–45. 

Curtin, P. D. (1961). “The White Man’s Grave:” Image and Reality, 1780-1850. _Journal of British Studies, 1_ (1), 94–110. 

Curtin, P. D. (1973). _The Image of Africa: British Ideas and Action, 1780–1850,_ (Vol. 2). Madison: University of Wisconsin Press. 

Debrunner, H. W. (1967). _A History of Christianity in Ghana_ . Accra: Waterville Publishing House. 

Depetris-Chauvin, E., & Weil, D. (2018). Malaria and early African development: Evidence from the sickle cell trait. _The Economic Journal 128_ (610), 1207–1234. 

Dickson, K. B. (1969). _A historical geography of Ghana_ . London: Cambridge University Press. 

Doyle, S., Meier zu Selhausen, F., & Weisdorf, J. (2020). The Blessings of Medicine? Patient characteristics and health outcomes in a Ugandan Mission Hospital, 1908–1970. _Social History of Medicine, 33_ (3), 946–980. 

Ekechi, F. K. (1971). Colonialism and Christianity in West Africa: The Igbo Case, 1900–1915. _Journal of African History, 12_ (1), 103–115. 

Engel, P. A. (1931). _Die Missionsmethode der Missionare vom Hl. Geist auf dem afrikanischen Festland_ , Neuss: Missionshaus Knechtsteden. 

Fahs, C. H. (1925). On Making a Missionary Atlas. _International Review of Mission, 14_ (2), 260–273. FAO. (2012). GAEZ Global Agro-Ecological Zones (GAEZ v3.0). Fenske, J. (2015). African polygamy: Past and present. _Journal of Development Economics, 117,_ 58–73. Fischer, F. H. (1991). _Der Missionsarzt Rudolf Fisch und die Anfänge medizinischer Arbeit der Basler Mission an der Goldküste_ . Herzogenrath: Verlag Murken-Altrogge. 

Foster, P. (1965). _Education and Social Change in Ghana_ . Chicago: University of Chicago Press. Frankema, E. (2012). The origins of formal education in sub-Saharan Africa: Was British rule more Benign? _European Review of Economic History, 16_ (4), 335–355. 

Frankema, E., & Van Waijenburg, M. (2019). The great convergence. Skill accumulation and mass education in Africa and Asia. _CEPR Discussion Paper, 14150_ . 

Frankema, E., & Jerven, M. (2014). Writing history backwards or sideways: towards a consensus on African population, 1850–2010. _Economic History Review, 67_ (4), 907–931. 

Frankema, E., Williamson, J. G., & Woltjer, P. (2018). An economic rationale for the West African scramble? The commercial transition and the commodity price boom of 1835–1885. _Journal of Economic History, 78_ (2), 231–267. 

Gallego, F. A., & Woodberry, R. D. (2010). Christian missionaries and education in former African colonies: How competition mattered. _Journal of African Economies, 19_ (3), 294–329. Galor, O. (2005). From Stagnation to Growth: Unified Growth Theory. In P. Aghion, & S. Durlauf (Eds.), _Handbook of Economic Growth_ (pp. 441–494). Amsterdam: Elsevier. 

Galor, O. (2011). Inequality, Human Capital Formation, and the Process of Development. In E. Hanushek, 

S. Machin, & L. Woessmann (Eds.), _Handbook of the Economics of Education_ (Vol. 4; pp. 441–493). Amsterdam: Elsevier. 

Galor, O. (2011). _Unified Growth Theory, Princeton_ . New Jersey: Princeton University Press. 

Galor, O., & Moav, O. (2006). Das Human-Kapital: A Theory of the Demise of the Class Structure. _Review of Economic Studies, 73_ (1), 85–117. 

Gannon, M. (1983). The Basle Mission Trading Company and British colonial policy in the Gold Coast, 1918–1928. _Journal of African History, 24_ (4), 503–515. Ghana Statistical Service. (2000). _Population & Housing Census 2000_ . Accra: Government Printer. Globcover, Globcover Regional. (2009). _Africa_ 

Goldewijk, K. K., Beusen, A., & Janssen, P. (2010). Long-term dynamic modeling of global population and built-up area in a spatially explicit way: HYDE 3.1. _The Holocene, 20_ (4), 565–573. 

Goldsmith-Pinkham, P., Sorkin, I., & Swift, H. (2020). Bartik Instruments: What, When, Why, and How. _American Economic Review 110_ (8), 2586–2624. 

1 3 

Journal of Economic Growth (2022) 27:149–192 

190 

Gollin, D., Jedwab, R., & Vollrath, D. (2016). Urbanization with and without industrialization. _Journal of Economic Growth, 21_ (1), 35–70. 

Gould, P. R. (1960). _The Development of the Transportation Pattern in Ghana_ . Department of Geography, Northwestern University. 

Graham, C. K. (1976). _The History of Education in Ghana_ . Tema: Ghana Publishing Corporation. 

Guggisberg, F. G. (1908). _Index to the 1:125,000 Map of the Gold Coast Colony and Ashanti_ . London: W. & A.K. Johnston Limited. 

Guirkinger, C., & Villar, P. (2022). Pro-birth policies, missions and fertility: historical evidence from Congo. DeFiPP Working Paper 4, Université de Namur. 

Gyasi, E. A. (1992). Emergence of a new oil palm belt in Ghana. _Tijdschrift voor Economische en Sociale Geografie, 83_ (1), 39–49. 

Halvorsen, R., & Palmquist, R. (1980). The interpretation of dummy variables in semilogarithmic equations. _American Economic Review, 70_ (3), 474–475. 

Hastings, A. (1994). _The Church in Africa, 1450–1950_ . Oxford: Clarendon Press. Henderson, M., & Whatley, W. (2014). Pacification and Gender in Colonial Africa: Evidence from the Ethnographic Atlas. _MPRA Paper 61203_ . 

Henn, S., Larreguy, H., & Schmidt-Padilla, C. (2021). Missionary Activity, Education, and Long-run Political Development: Evidence from Africa. Unpublished manuscript, Harvard University. 

Hill, P. (1963). _The migrant cocoa-farmers of southern Ghana: a study in rural capitalism_ . Cambridge: Cambridge University Press. 

Isichei, E. A. (1995). _A History of Christianity in Africa: From Antiquity to the Present_ . London: SPCK. Jedwab, R., & Moradi, A. (2016). The permanent effects of transportation revolutions in poor countries: Evidence from Africa. _Review of Economics and Statistics, 98_ (2), 268–284. 

Jedwab, R., Meier zu Selhausen, F., & Moradi, A. (2018). The Economics of Missionary Expansion: Evidence from Africa and Implications for Development. CSAE Working Paper Series 7, Centre for the Study of African Economies, University of Oxford. 

Jedwab, R., Meier zu Selhausen, F., & Moradi A. (2019). The Economics of Missionary Expansion: Evidence from Africa and Implications for Development. Working Paper 10, George Washington University, Institute for International Economic Policy. 

Jedwab, R., Meier zu Selhausen, F., & Moradi, A. (2021). Christianization without economic development: Evidence from Ghana. _Journal of Economic Behavior & Organization, 190_ , 573–596. 

Johnson, H. B. (1967). The location of Christian missions in Africa. _Geographical Review, 57_ (2), 168–202. Johnson, T. M., & Grim, B. J. (2020). _World Religion Database_ . Leiden/Boston: Brill. 

Johnson, T. M., & Zurlo, G. A. (2021). _World Christian Database_ . Leiden/Boston: Brill 

- Johnston, H. H. (1915). The political geography of Africa before and after the war. _Geographical Journal, 45_ (4), 273–294. 

Kelly, M. (2019). The Standard Errors of Persistence. _CEPR Discussion Paper 13783_ . 

Kennedy, P. E. (1981). Estimation with correctly interpreted dummy variables in semilogarithmic equations [The Interpretation of Dummy Variables in Semilogarithmic Equations]. _American Economic Review, 71_ (4), 801–801. 

- Luntinen, P. (1996). _Railway on the Gold Coast: A Meeting of Two Cultures: A Colonial History_ . Helsinki: Suomalainen Tiedeakatemia. 

- Mahajan, A. (2006). Identification and estimation of regression models with misclassification. _Econometrica, 74_ (3), 631–665. 

- Mamo, N., Bhattacharyya, S., & Moradi, A. (2019). Intensive and extensive margins of mining and development: Evidence from Sub-Saharan Africa. _Journal of Development Economics, 139,_ 28–49. 

- Maxwell, D. (2015). The missionary movement in African and World History: Mission sources and religious encounter. _Historical Journal, 58_ (4), 901–930. 

- Maxwell, D. (2016). Christianity. In John Parker & Richard Reid (Eds.), _The Oxford Handbook of Modern African History_ (pp. 263–280). Oxford: Oxford University Press. 

- McCleary, R. M., & Barro, R. J. (2006). Religion and political economy in an international panel. _Journal for the Scientific Study of Religion, 45_ (2), 149–175. 

- Meier zu Selhausen, F., van Leeuwen, M. H. D., and Weisdorf, J. (2018). Social mobility among Christian Africans: Evidence from Ugandan marriage registers, 1895–2011’. _Economic History Review, 71_ (4), 1291–1321. 

- Meier zu Selhausen, F. (2019). Missions, Education and Conversion in Colonial Africa. In D. Mitch, & G. Cappelli (Eds.), _Globalization and the Rise of Mass Education_ (pp. 25–59). London: Palgrave Macmillan. 

1 3 

Journal of Economic Growth (2022) 27:149–192 

191 

Menon, N., & McQueeney, K. (2020). Christianity and girl child health in India. _World Development, 136_ , 105109. 

Merriam-Webster. (2020). _Mission station_ . https:// www. merri am- webst er. com/ dicti onary/ missi on stati on Meyer, B. (1999). _Translating the Devil: Religion and Modernity among the Ewe in Ghana_ . Edinburgh: Edinburgh University Press. 

Michalopoulos, S., Naghavi, A., & Prarolo, G. (2018). Trade and geography in the spread of Islam. _The Economic Journal, 128_ (616), 3210–3241. 

Michalopoulos, S., & Papaioannou, E. (2013). Pre-colonial ethnic institutions and contemporary African development. _Econometrica, 81_ (1), 113–152. 

Michalopoulos, S., & Papaioannou, E. (2014). National institutions and subnational development in Africa. _The Quarterly Journal of Economics, 129_ (1), 151–213. Michalopoulos, S., & Papaioannou, E. (2018). Spatial patterns of development: A meso approach. _Annual Review of Economics, 10_ (1), 383–410. 

Miller, J. (2003). _Missionary zeal and institutional control: organizational contradictions in the Basel Mission on the Gold Coast, 1828–1917_ . Cambridge. U.K.: William B. Eerdmans. 

Moav, O., & Vollrath, D. (2009). Inequality in landownership, the emergence of human-capital promoting institutions, and the Great Divergence. _Review of Economic Studies, 76_ (1), 143–179. Murdock, G. P. (1967). Ethnographic Atlas: A summary. _Ethnology, 6_ (2), 109–236. 

NGDC, _Global Radiance Calibrated Nighttime Lights_ 2015. 

NOAA. (2012). Average visible, stable lights, cloud free coverages. Nunn, N. (2008). The long-term effects of Africa’s slave trades. _The Quarterly Journal of Economics, 123_ (1), 139–176. 

Nunn, N. (2010). Religious conversion in colonial Africa. _American Economic Review: Papers and Proceedings, 100_ (2), 147-152. 

Nunn, N. (2014). Gender and Missionary Influence in Colonial Africa. In E. Akyeampong, R. H. Bates, N. Nunn, & J. Robinson (Eds.), _Africa’s Development in Historical Perspective_ (pp. 489–512). New York: Cambridge University Press. 

Nunn, N., & Wantchekon, L. (2011). The slave trade and the origins of mistrust in Africa. _American Economic Review, 101_ (7), 3221–3252. 

Okoye, D. (2021). Things fall apart? Missions, institutions, and interpersonal trust. _Journal of Development Economics,148_ , 102568. 

Oliver, R. A. (1952). _The Missionary Factor in East Africa_ . London: Longmans. 

Osei, S. K. (2014). Combining geo-historical information with GIS techniques: An example of the historical slave route heritage in Ghana. In J. Anquandah, B. Kankpeyeng, & W. Apoh (Eds.), _Current Perspectives in the Archeology of Ghana_ . Legon: University of Ghana Readers. 

Parsons, R. T. (1963). _The Churches and Ghana Society 1918–1955_ . Leiden: E. J. Brill. 

Pauw, C. M. (1996). Traditional African economies in conflict with Western Capitalism. _Mission Studies, 14_ (1), 203–222. 

Pietz, W. (1999). The fetish of civilization. In P. Pels, & O. Salemink (Eds.), _Colonial Subjects: Essays on the Practical History of Anthropology_ (pp. 53–81). Ann Arbor: University of Michigan Press. Quartey, S. (2007). _Missionary practices on the Gold Coast, 1832–1895: Discourse, gaze, and gender in the Basel Mission in pre-colonial West Africa, Youngstown_ . N.Y.: Cambria Press. 

Roome, W. R. M. (1925). _Ethnographic Survey of Africa: Showing the Tribes and Languages; also the Stations of Missionary Societies_ . London: Edward Stanford Ltd. 

Rubin, J. (2014). Printing and Protestants: An empirical test of the role of printing in the Reformation. _The Review of Economics and Statistics, 96_ (2), 270–286. 

Schlatter, W. (1916). _Geschichte der Basler Mission, 1815–1915_ . Basel: Missionsbuchhandlung. 

Schmidlin, D. (1933). _Jospeh, Catholic Mission History_ . Techny (ILL): Mission Press S.V.D. 

Schott, O. (1879). _The Basel Mission on the Gold-Coast, Western Africa on the 1st January 1879: A Retrospect on Fifty Years of Mission Work_ . Basel: Felix Schneider. 

Schreiber, D. A. W. (1936). _Bausteine zur Geschichte der Norddeutschen Missions-Gesellschaft_ . Bremen: Verlag der Norddeutschen Missions-Gesellschaft. 

Sluglett, P. (2014). _Atlas of Islamic History_ . New York: Routledge. 

Smith, N. T. (1966). _The Presbyterian Church of Ghana, 1835–1960: a younger Church in a changing society_ . Accra: Ghana Universities Press. 

Spitz, M. (1924). The growth of Roman Catholic missions in Africa. _International Review of Mission, 13_ (3), 360–372. 

Streit, K. (1913). _Atlas Hierarchicus: descriptio geographica et statistica Sanctae Romanae Ecclesiae tum occidentis tum orientis juxta statum praesentum accedunt nonnullae notae historicae necnon ethnographicae_ . Paderborn: Typographiae Bonifacianae. 

1 3 

Journal of Economic Growth (2022) 27:149–192 

192 

Summers, C. (2016). Education and Literacy. In J. Parker, & R. Reid (Eds.), _The Oxford Handbook of Modern African History_ (pp. 319–337). Oxford: Oxford University Press. 

Sundkler, B., & Steed, C. (2000). _A History of the Church in Africa, Cambridge_ . UK: Cambridge University Press. 

Terry, J. M. (2015). Missiology: An Introduction to the Foundations, History, and Strategies of World Missions. Nashville, Tennessee: B&H Publishing Group. 

Thauren, P. J. (1931) _Die Missionen der Gesellschaft des Göttlichen Wortes in den Heidenländern_ (Vol. 1). Die Mission in der ehemaligen deutschen Kolonie Togo, Post Kaldenkirchen: Missionsdruckerei Steyl. 

The Economist. (2015). The future of the world’s most popular religion is African. 25 December 2015. 

- Todd, J., Zurlo, G., Hickman, A., & Crossing, P. (2018). Christianity 2018: More African Christians and counting martyrs. _International Bulletin of Mission Research, 42_ (1), 20–28. 

USAID. (2020). _Demographic and Health Surveys_ . 

Valencia Caicedo, F. (2019a). The Mission: Human capital transmission, economic persistence and culture in South America. _The Quarterly Journal of Economics, 134_ (1), 507–556. 

Valencia Caicedo, F. (2019b). Missionaries in Latin America and Asia: A First Global Mass Education Wave, In D. Mitch, & G. Cappelli (Eds.), _Globalization and the Rise of Mass Education_ (pp. 61–98). London: Palgrave Macmillan. 

Waldinger, M. (2017). The long-run effects of missionary orders in Mexico. _Journal of Development Economics, 127,_ 355–378. 

- Wantchekon, L., Novta, N., & Klašnja, M. (2015). Education and human capital externalities: Evidence from colonial Benin. _The Quarterly Journal of Economics, 130_ (2), 703–757. 

- Welbourn, F. B. (1971). Missionary stimulus and African responses. In L. H. Gann, & P. Duignan (Eds.), _Colonialism in Africa: 1870–1960_ (Vol. 3; pp. 310–345). Cambridge: Cambridge University Press. 

- Williamson, S. G. (1952). Missions and education in the gold coast. _International Review of Missions, 41_ (3), 364–373. 

**Publisher’s Note** Springer Nature remains neutral with regard to jurisdictional claims in published maps and institutional affiliations. 

1 3 


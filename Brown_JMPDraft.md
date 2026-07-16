## The Persistent Effects of Bible Translations in Africa 



November 18, 2025 [Most recent version here] 

This paper studies how individual missionaries, through translation of the Bible into vernacular African languages, catalyzed missionary endeavors and shaped development outcomes in the long-run. Translation of the Bible required codification of previously oral languages, thus making them accessible to outsiders while enabling them to be used as media of instruction in mission schools. To quantify its effects, I construct new data on mission stations and link to them Bible translation data using biographical information on translators. Exploiting the panel nature of the data, I show that foreign staff presence at mission stations increases by 72% following a Bible translation. At these stations, I find large increases in missionary infrastructure including schools, hospitals and printing presses, but only in countries where colonial policy is favorable towards Protestant missionary activity. In such countries, this translates to, in the long run, 0.2 more years of schooling and a 0.1 points higher body mass index. Where colonial policy is adversarial to Protestant missions, educational attainment actually deteriorates as a result of Bible translation. 

###### **JEL Codes: F54, I25, N37, O43, Z12, Z13** 

> * Stellenbosch University. Email: gabriel.j.m.brown@gmail.com. I would like to thank Siwan Anderson, Chris Brown, Jane Brown, Claudio Ferraz, Johan Fourie, Patrick Francois, Anthony Gill, Sam Gyetvay, Masahiro Kubo, Matt Lowe, Isaac Mbiti, Jamie McCasland, Felix Meier zu Selhausen, Nathan Nunn, Pedro Pessoa, Valeria Rueda, Munir Squires, Felipe Valencia Caicedo as well as conference and seminar participants at the WGAPE meeting, ASREC meetings, the EHA annual conference, LEAP workshops, the YSI seminar, the ACEI conference, the WEHC conference and the AEHN conference for helpful comments. I thank Arya Chokshi, Sarthak Kwatra, Megha Shanbhag, Tshandapiwa Tshuma and Binyan Zhao who provided excellent research assistance. This research benefited from funding from the Centre for Innovative Data in Economics Research (CIDER) under the Canada Excellence Chair held by Professor Erik Snowberg. 

1 

##### **1 Introduction** 

Foreign missionaries to Sub-Saharan Africa fundamentally reshaped the continent. They spread Christianity (Nunn 2010), shaped the education and health landscapes for generations (Nunn 2014; Cag´e & Rueda 2020) and are even argued to have solidified ethnic identities (Vail 1989). Their presence and impact, however, was highly uneven. In some areas they established bustling hubs of activity whose imprints are still observed today, while in others they struggled to maintain a foothold. This raises the question: How do we explain both the lasting influence of missionary activity and its uneven distribution? 

In this paper, I study how individual missionaries, through translation of the Bible into vernacular African languages, catalyzed missionary endeavors and shaped development outcomes in the long-run. In translating the Bible, missionaries codified into written scripts languages that had been hitherto purely oral (Guinter 1927; Posner 2003, Laitin & Ramachandran 2022). Other foreigners could then learn the language through written documents and join the missionary effort (Sherk n.d.;Dutch Reformed Church of South Africa 1924; Smalley 1991; Pawlikova-Vilhanova 2011), thus permitting further investments, especially in education and health, two areas of missionary focus. Codification also meant that the vernacular language could be used as a medium of instruction in mission schools, thus facilitating the education of local people (Dutch Reformed Church of South Africa 1929; Vail 1989; Nana 2016). 

In order to quantify the effects of Bible translations, I combine various novel datasets. First, I create a global, panel dataset of missionary activity through the digitization of four Protestant atlases (Beach 1903; Dennis et al. 1911; Beach & St. John 1916; Beach & Fahs 1925) and two Catholic ones (Streit 1913; Streit 1929). I then create a dataset on all original Bible translations into every world language from the _Book of a Thousand Tongues_ (United Bible Societies 1972), a compiled Bible translation list from all major Bible societies, and the _Ethnologue_ (2000; 2000; 2005; 2009), a compendium of world languages. I link African Bible translations from before 1930 to geo-referenced mission stations by 

2 

using biographical information of missionary translators. I supplement these datasets with geo-referenced modern socio-economic indicators from the Demographic and Health Surveys (DHS). 

I supplement these data further with a categorization of colonial policy towards missionary activity. In particular, I assign policy stances to each African country in my sample with regards to education and health using official government documents and secondary sources. In education, I examine two policies: (1) whether indigenous languages were permitted as media of instruction in schools, and (2) the subsidization of Protestant mission schools. In health, I examine whether medical missionaries can practice with foreign credentials, i.e. from a country that is not the colonial power. I find near perfect correlation in all three policies among African countries<sup>1</sup> . Thus, I group African countries into two categories: indigenous-language-permitted (ILP) and colonial-language-enforced (CLE). I seek to estimate the causal effects of Bible translations separately for these two samples. 

The principal endogeneity concern with estimation is that mission stations tend to be located in already more central and prosperous areas (Jedwab et al. 2022) while Bible translators aimed to maximize the number of potential readers (Vail 1989; Tembo 2020). To help address this endogeneity concern, I show that, conditional on mission presence and year of first establishment, locations with and without a linked Bible are similar along observable characteristics. With these conditions, Bible translation sites in ILP countries are actually in less central areas as measured by distance to colonial railway while in CLE countries they are still more central. In light or these differences and the possibility of dissimilarity along unobservable characteristics, simple ordinary least squares (OLS) estimates cannot yield causal interpretation. 

When estimating a Bible translation’s effect on missionary expansion, I make use of the 

> 1Only in the Democratic of Republic of Congo and Somalia did the colonial governments not provide subsidies to Protestant mission schools yet they permitted the use of indigenous languages and allowed foreign credentials for medical practice. In all other countries, colonial governments either permitted indigenous language in schools, provided subsidies to Protestant mission schools and allowed doctors with foreign credentials to practice medicine or they enforced the colonial language, did not provide subsidies, and disallowed doctors with foreign credentials to practice. See Appendix Section A.3 for details. 

3 

panel nature of the data to conduct a matched difference-in-difference analysis. I begin by matching mission stations with and without a linked Bible translation on colonial policy, year of establishment and a set of LASSO-selected variables that may influence missionary location and expansion. I then assign treatment year based on the year of publication of the first published Bible book. I find that, with translation, there is an increase of nearly 3 more foreign missionaries and 0.34 mission stations in the area, representing 72% and 36% increases relative to the mean. A translation also decreases the likelihood of exiting the area by 13 percentage points. These effects are actually larger in CLE countries. Expansion takes places at both the site of translation itself and neighboring mission stations, but exclusively at those within the same linguistic homeland. 

I then turn to an analysis of the effects on missionary infrastructure. Only one edition of the Protestant atlases (Beach 1903) contains such information, meaning I can only conduct naive difference-in-difference analysis comparing Bible translations published before and after this edition. Still, I find a Bible translation increases the number of printing presses, primary schools, high schools, hospitals and dispensaries but only in ILP countries, where the colonial government was more permissive of missionary activity. Using geo-referenced building data from OpenStreetMap for the year 2024, I provide some suggestive evidence of the persistence of such infrastructure, especially hospitals and higher education institutions. 

I also look at the effect of Bible translations on the use of indigenous languages in schools. For this, I hand-code the number of grades each African language is used as medium of instruction in schools from 1960 until 2011. I find that all languages being used in schools in 1960 at post-independence are necessarily translated into the Bible, but that there is only an effect in ILP countries. 

Having established the effects of Bible translations on missionary staff and infrastructure, as well as education policy, I turn to an analysis of its effects on long-run development. I focus specifically on education and health outcomes as these were areas of focus for missionaries. To assess these effects, I measure treatment in two different ways: a person’s geographic 

4 

proximity to a historical Bible translation site and whether their ancestral language was translated. 

With regards to geographic proximity, I control for mission presence, year of establishment and a host of geographic and historical determinants of both mission activity and Bible translations. To strengthen causal interpretation, I use an instrumental variable (IV) strategy based on the proclivity of the first-established missionary society in translating the Bible. Intuitively, demand-side factors such as population density are endogenous to development but supply-side ones such as missionary society tendencies are more plausibly exogenous. I construct this measure by taking the total number of Bible verses translated by each missionary society throughout the world and dividing it by its total number of missions. I then take the log of this measure as my instrument. I find that this instrument is highly predictive of Bible translations. 

OLS estimates show that a Bible translation is associated with a 0.205 increase in years of schooling in ILP countries, but a 0.458 decrease in CLE ones. Interpreted differently, a Bible translation increases the effect of being proximate to a mission station on schooling by 65% in ILP countries, while more than annulling it in CLE ones. When using the IV specification, a Bible translation leads to a 1.765 increase in years of schooling in ILP countries but a 0.093 decrease in CLE ones. The latter coefficient, however, is not significant. I argue that, among all considered colonial policies towards missionaries, the restriction of indigenous languages in schools can best explain the negative result. That is, a Bible translation will facilitate use of the vernacular in churches and elsewhere in CLE countries, thus reducing use and familiarity with the colonial language. With regards to health, a Bible translation is associated with a 0.112-point increase in body mass index (BMI) in ILP countries and a 0.098 decrease in CLE ones, although the latter coefficient is not significant. The IV estimate is larger in magnitude than the OLS one and significant in the ILP sample but not statistically significant in the CLE one. 

I turn to a language-based treatment assignment in order to provide additional evidence 

5 

along a different source of variation. In particular, I conduct a difference-in-difference analysis comparing language groups for whom there is a Bible translation by 2007 to never-treated ones. I then make use of the fact that use of indigenous languages as media of instruction in schools is almost always limited to grades 1 to 3 to assign cohort-based exposure. Given that new languages are translated into the Bible every year, I adopt the estimator from Sun & Abraham (2021) to account for staggered treatment adoption. Using this source of variation, I find that a Bible translation increases schooling by approximately 0.4 years in ILP countries but decreases schooling by approximately the same amount in CLE ones. These estimates align closely with the OLS ones using geographic treatment assignment. 

My analysis on Bible translations in Sub-Saharan Africa contributes to an ever-growing literature on the long-run effects of missionaries. They have already been linked to improvements in education, not only in Africa (Fourie et al. 2014; Nunn 2014; Becker & Meier zu Selhausen 2023; Becker & Schmitt 2023; Okada da Silva et al. 2023), but throughout the world (Waldinger 2017; Valencia Caicedo 2019; Calvi et al. 2022). They have also been linked to religious conversion (Nunn 2010), improvements in health (Calvi & Mantovanelli 2018; Cag´e & Rueda 2020), increased political participation (Cag´e & Rueda 2016), liberal democracies (Woodberry 2012) and social views (Ananyev & Poyker 2021; Sol´a 2023;Bergeron 2025). These papers largely focus on the long-run effects of missionaries at the extensive margin. Jedwab et al. (2022) examine the role of quinine and colonial railways in the expansion of missionary activity at the extensive margin while Becker (2022) investigates the role of the expansion of colonial territory. By contrast, my paper focuses on the intensive margin. I show that language mastery underpins the lasting influence of large missionary hubs. I also contribute new data to this literature and emphasize the joint role of individual, pioneering missionaries and colonial policy in shaping missionary influence. 

My paper relates to a second literature linking the use of vernacular language to human capital accumulation. One major feature of the Protestant Reformation itself was a shift towards greater use of vernacular languages (Binzel et al. 2025), which allowed for human 

6 

capital accumulation through, among other things, the reading of the Bible (Becker & Woessmann 2009). My evidence, however, suggests that Bible translations in Africa were important not because Africans themselves read the Bible _en masse_ but rather, through codification, they enabled missionaries to learn African languages and thus work effectively. Codification also meant the use of indigenous languages in schools. Even early missionaries working in Africa believed that beginning one’s education in the vernacular language was beneficial (Buell 1928)<sup>2</sup> . Recent causal evidence has confirmed this belief (Seid 2016; Ramachandran 2017; Seid 2019; Kerwin & Thornton 2020 _a_ ), even for second language acquisition (Taylor & von Fintel 2016). My paper demonstrates that codification through Bible translation and legacies of colonial rule are strong determinants as to which languages are used in schools. 

Finally, my paper contributes to a literature showing how the arrival of foreign ideas or individuals can catalyze change. Accessibility of foreign books or information in a local language can precipitate knowledge gain and productivity boosts (Abramitzky & Sin 2014; Gupta et al. 2024; Juh´asz et al. 2024). Meanwhile the arrival of foreigners with new skills can galvanize social change (Dippel & Heblich 2021), boost scientific research (Moser et al. 2014) and enhance productivity (Hornung 2014). My paper aligns with these findings but demonstrates that foreign influence can only bring positive change in enabling policy environments. 

In the next section, I provide some historical background on Bible translations in Africa. Section 3 details the data that I use for analysis. In Section 4, I estimate the effects of Bible translations on missionary activity and language of instruction. Section 5 does the same for long-run development outcomes. Section 6 concludes. 

> 2One mission school teacher is quoted as saying “Of all the courses in the native school, French demands the most time and trouble and yields the least results.” (Buell 1928, p.58) 

7 

##### **2 Historical Background** 

###### **2.1 Language in Africa before Missionaries** 

Prior to missionary arrival, the vast majority of languages in Africa were purely oral<sup>3</sup> (Guinter 1927; Posner 2003, Laitin & Ramachandran 2022). There did not exist a written script. Moreover, the dialectical differences within languages was much greater than what is seen in modern times. That is, in many places, language could be best understood as a spectrum rather than a uniform entity within discrete boundaries. In his description of the Shona, Ranger (1989) describes how, from one village to the next, language remained the same but traveling from one end to the other of Shonaland, one would encounter major linguistic differences to the point of being mutually unintelligible. Thus, in translating the Bible, missionaries codified the language and standardized it across time and space<sup>4</sup> . This standardized version was often referred to as the ‘Bible dialect’ given how strong a role the Bible played in this process. 

###### **2.2 Missionary Activity in Africa** 

Christian missionary activity in Sub-Saharan Africa dates back to the fifteenth century among the Catholics who arrived in the Senegambia region and to the eighteenth century among the Protestants in the Cape Colony of South Africa. Early mission activity was restricted largely to coastal areas given security risks and the danger of contracting malaria. Thus, the establishment of European colonies subsequent to the Scramble for Africa and the introduction of quinine in the mid-nineteenth century allowed for an expansion of missionary activity throughout the continent (Becker 2022). Bible translation is also theorized to have 

> 3Exceptions mainly include languages of Ethiopia, Amharic and Ethiopic, which have long histories of writing. Ethiopia was also a Christian country long before the rest of Africa. For these reasons, I exclude it from my analysis. 

> 4This was especially true of those individuals who attended missionary schools. Law (1996) provides a quote from a Yoruba intellectual: “Civilization has toned up our language, and there is a tendency to speak one dialect and that is the written Yoruba of our Bible” 

8 

played an important role in the expansion of missionary activity (Smalley 1991), a theory which I test in this paper. 

The missionary enterprise benefited greatly from the colonial presence for protection, transportation technology and financial support, especially for educational activities. In many ways, this relationship was symbiotic in that the missionary enterprise also legitimized the colonial presence, provided educated locals for the colonial workforce and provided reports of activity within the colony (Becker 2022). This is not to say that the relationship between the colonial government and missionary societies was without its tensions and conflicts. Colonial governments often had a preference for missionary societies originating from their home country. Moreover, missionary societies would often actively or covertly oppose the abusive labour practices adopted by colonial governments (Soremekun 1971). In the subsection below, I consider three further policy areas in which colonial governments and missionary societies did not always see eye-to-eye, including the use of indigenous languages in education. I will show moreover that some colonial powers, such as the British, were more permissive with regards to missionary, especially Protestant, activity than others, such as the French. 

It should also be noted that missionary societies, even within denominations, did not all approach their work in the same way. In 1900, there were 62 distinct missionary societies working in Sub-Saharan Africa (Beach 1903) and by 1922, there were 111 (Beach & Fahs 1925)<sup>5</sup> . Among these, some tended to be more focused on Bible translation, such as the Baptist Missionary Society<sup>6</sup> , while others could be more focused on education or health. For example, the Church of Scotland Mission insisted that every mission station have a resident doctor (Iliffe 1998). 

> 5These numbers exclude societies working only in Ethiopia as it is considered part of Sub-Saharan Africa but is not part of my study given its long history with Christianity and written scripts 

> 6The Baptist Missionary Society traces its beginnings to William Carey’s work based out of Serampore in India. Together with his fellow missionaries they translated countless Bibles into Indian languages long before the Baptist Missionary Society ever set foot in Africa (United Bible Societies 1972). 

9 

###### **2.3 Bible Translations in Africa** 

Since the original Greek edition of the Bible<sup>7</sup> , it has been translated into an ever increasing number of languages. Having a Bible available in the vernacular gained special importance with the Protestant Reformation. A central tenet of Protestantism, called _Sola Scriptura_ , holds that ultimate religious authority can only come from the Bible itself, not the church. Thus, when missionaries started spreading throughout the world, it was Protestant missionaries who translated the Bible. In fact, it was not until 1965, as a result of the Second Vatican Council, that Catholics were even allowed to play a role in translation. For these reasons, the history of Bible translation in Africa before 1965 aligns only with Protestant, not Catholic, missionary activity. 

The first scripture translated in Africa was completed by Robert Moffat in 1830 when he translated the book of Luke into Setswana from his mission station at Kuruman in what is now northern South Africa (United Bible Societies 1972). In doing so, Moffat not only made scripture available in Setswana, but he also reduced the language into writing. Much like in other parts of the world, Bible translations standardized language and the ”bible dialect” gained prominence over other dialects (Vail 1989; Law 1996; Andersson & Janson 1997, van den Bersselaar 1997; Tembo 2020). In the years that followed, hundreds of his missionary colleagues did the same for languages across Africa. Missionaries began translating the Bible into languages with greater numbers of speakers (see Figure I). More recent Bible translations reach fewer and fewer people. 

Bible translators themselves are generally regarded to have been a special kind of missionary. They are often described as being excellent linguists (e.g. Seton 1962, p.84). Smalley (1991) describes them as having to combine “translation, general missionary work and a creative, sometimes distinguished scholarship”. Moreover, Bible translators would have been strongly encouraged to translate from the original tongues, such as Greek, though this would 

> 7The Old Testament was initially written in Hebrew (with some Aramaic) but the New Testament, and therefore the first _full_ Bible was written in Greek. 

10 

not have always been the case. For these reasons, the vast majority of Bible translators during the missionary era were foreign missionaries, not locals<sup>8</sup> . That is not to say that native people were not involved in the Bible translation project, only that they were not the impetus for it. 

Bible translations proved extremely useful to the missionary enterprise in two important ways. The first way was through the development of language learning tools for foreign missionaries. There is evidence that both the production of materials and the mastery of the indigenous language by a foreign missionary were invaluable in assisting other missionaries to learn the language. For example, A. S. Judd, a missionary with the Sudan United Mission, was the first to translate the Bible into Tiv (United Bible Societies 1972), a language of northern Nigeria. He then established the syllabus for learning Tiv for other missionaries to follow, a syllabus which included as its major reading the Gospels he translated (Dutch Reformed Church of South Africa 1924). These documents were often copied and provided to missionaries for language learning even before publication<sup>9</sup> . Even Catholic missionaries would be known to read translated scripture for the purpose of language learning (PawlikovaVilhanova 2011). Bible translators themselves became relative experts in the native language and would often assist others to learn it<sup>10</sup> . 

Through this channel, Bible translations could have long-term consequences for development. The following example illuminates this more clearly. Johannes Gottlieb Christaller of the Basel missionary society translated the Bible into Twi Akuapem, a Ghanaian language, starting in 1859 (United Bible Societies 1972) out of the Akropong missionary station (Anderson 1999, p.133). Later, Rudolf Fisch, of the same missionary society, learned and 

> 8There are of course exceptions to this rule such as Samuel Crowther, who translated the first Yoruba and Igbo Bibles. 

> 9For example, the book of Matthew was translated in 1917 and provided to other missionaries that year (Dutch Reformed Church of South Africa 1917), three years before the book was published in 1920 (United Bible Societies 1972) at which point a further 250 copies were printed. 

> 10For example, Florence Lang Sherk described how, upon arriving in northern Nigeria with the United Missionary Society, she spent the first years of her stay at Shonga, a Bible translation site. There, A. W. Banfield a fellow missionary who had translated the New Testament into the Nupe language, provided her with support and materials to learn Nupe. She left after five years to work with her husband at another station where Nupe was still spoken (Sherk n.d.). 

11 

mastered Twi then established a mission hospital at Aburi (Nasim 2023) only 18 kilometers from Akropong. That hospital still exists to this day even though it was transferred to Presbyterian missionaries in 1917. Thus, the initial investment into the Twi language catalyzed a long-series of events that led to better health care infrastructure in the long run. 

The second way Bible translations aided the missionary enterprise was in developing literacy among students at mission schools. Whenever possible, missionaries would use the native language as the medium of instruction in schools (Dutch Reformed Church of South Africa 1929; Vail 1989; Nana 2016). Using the native language rather than the colonial language was far more effective for learning, a fact that was already known at the time (Buell 1928)<sup>11</sup> and has been further shown in modern economic studies (e.g. Taylor & von Fintel 2016). The recently translated scripture would also form an important part of the school reading syllabus. However, the legal ability for missionary societies to instruct in the local language and use scripture as part of the syllabus depended entirely on colonial policy towards language. I explore differences in this regard among the various colonial powers in the next subsection. 

###### **2.4 Colonial Policy towards Missionary Activity** 

As previously mentioned, some colonial powers were more restrictive with regards to missionary activity than others. In this subsection, I look at three major policies affecting how missionary societies could operate in the areas of education and health. In particular, I look at (1) whether indigenous languages could be used as media of instruction in schools, (2) the subsidization of Protestant mission schools, and (3) the acceptance of foreign licensing for medical missionaries. I provide the stance on each of these policies in each African country in Table A2 and supporting evidence in appendix section A.3. Here, I provide some general comments. 

First, colonial governments were generally fully enabling or fully restrictive of missionary 

> 11Buell (1928) notes how French instructors would bemoan the fact that nothing would be learned while teaching in French 

12 

activity. That is, there is a high degree of correlation in the three policies mentioned above. A colonial government that allowed indigenous languages to be used in schools would also provide subsidies to Protestant mission schools, and allow medical missionaries with foreign licenses (i.e. not of the colonial country) to practice. The British colonies could be typified in this way, as could Liberia, South Africa, and Namibia. While the British initially intended to force their language onto indigenous people (Lewis 1962), they changed approach in the 19th century; from that point onward they allowed, even encouraged, the use of indigenous languages by their officials, the missionaries and in schools. They also provided substantial subsidies to mission schools in the form of grants-in-aid. These subsidies were provided on the basis of enrollment numbers and performance on standardized tests (Cogneau & Moradi 2014). Such policies meant that the vast majority of education in British colonies was provided by missionary societies (Nunn 2014) and that instruction was given largely in indigenous languages. 

Conversely, colonial governments that strictly enforced the use of the colonial language in schools did not provide subsidies to Protestant mission schools, and disallowed medical missionaries with foreign credentials to practice. Such was the case for most French colonies as well as the Portuguese colonies<sup>12</sup> . The French stance was largely a reflection of the 1905 French law mandating the separation of church and state; as a result of this law, education in their colonies became largely secular (Buell 1928). Moreover, a major goal of the French colonial powers was to have French spoken by each and every individual throughout their empire. These differences in policies towards missionaries align with the pre-existing understanding that the British preferred indirect rule, allowing local entities to have some agency, while the French preferred direct rule, thus limiting the agency of missionaries among others. 

> Policy towards missionaries, however, did not align perfectly with colonizer identity. The 

> 12Not only did the French colonial administration impose French as the language of learning but they forbade the use of indigenous languages in the classroom. Pupils would learn French through the direct method instead of using an intermediary language (Buell 1928). 

13 

former German colonies that became League of Nations Mandates after World War I<sup>13</sup> are the exceptions to this rule. In Togoland and the French Cameroons, following the transfer to French authority, the government demanded that all mission schools teach exclusively in French among other conditions. The American Presbyterian missions were ill-equipped to meet these demands and were at risk of closing down. Instead, they brought the issue forth to the American State Department. Closing mission schools would have violated the rights of foreign nationals in a Mandate country and thus French efforts were stopped. In these two countries, therefore, instruction in indigenous languages continued and subsidies were even provided to Protestant mission schools (Buell 1928, p.370-372). Indeed, colonial governments in League of Nations mandate territories became generally permissive of missionary activity. 

Given the above, I classify all sub-Saharan countries according to the policy of the colonial power. Specifically, I focus on the policy surrounding language use in schools, though as argued above this is highly correlated with the other two policy areas. I classify all British colonies, the Belgian colonies, the French Mandates (Cameroon and Togo), Liberia, South Africa and Namibia as being indigenous-language-permitted (ILP) countries. I classify the remaining French colonies and the Portuguese colonies as being colonial-language-enforced countries (CLE). 

##### **3 Data** 

In this section, I detail the different sources and methods used to construct the data on missionary activity, Bible translations, language of education, contemporary socio-economic outcomes, and geographical and historical controls. 

> 13Of the former German colonies, Togo was given to France, Tanganyika was given to Great Britain, Rwanda and Burundi were given to Belgium and Namibia became a territory of South Africa. Cameroon was shared between France and Great Britain. 

14 

###### **3.1 Missionary Data** 

###### **3.1.1 Protestant Missions** 

I construct a global dataset of Protestant missionary activity from four atlas editions (Beach 1903; Dennis et al. 1911; Beach & St. John 1916; Beach & Fahs 1925). These four editions represent snapshots of missionary activity in four years: 1900, 1908, 1915, and 1922 respectively. They include only mission stations at which a foreign missionary is located<sup>14</sup> . This omits all stations whereby only local workers are present, often considered outstations. Nonetheless, mission stations where foreign missionaries are located tend to be larger, better equipped, and with more work being done. Outstations, where they exist, tend to surround the main station (Jedwab et al. 2022). Thus, although information on all stations is not systematically available, main stations can act as good proxies for broader missionary activity. 

For each mission station in each edition throughout the world, I gather information on its geo-coordinates, the operating missionary society, the number of staff of each gender, the number of doctors<sup>15</sup> , and the year of establishment when available. Beach (1903) also includes additional information at the mission station level, including missionary infrastructure such as primary schools, secondary schools, printing presses, hospitals and more. Information on infrastructure does not appear complete, however, as a number of missionary societies report no additional infrastructure at any of their mission stations throughout the world<sup>16</sup> . I then link these mission stations across editions using the name, operating society and geo-coordinates of each mission station. Additional details on the process of digitization and linking can be found in appendix section A.1.1. 

> 14In this instance, “foreign” means most precisely someone who is working in a field among the unevangelized that is not their home. For example, it will still list missionaries who are working within the same country, such as in North America or South Africa, where there were large numbers of missionaries working within their own country, but among the unevangelized. By contrast, they will not keep close records of the countless local staff working in a field that is their home. 

> 15Beach & St. John (1916) is the only edition which does not include information on doctors. 

> 16The fact that this information is no longer reported in later editions also seems to suggest that infrastructure data may be incomplete. 

15 

With this digitized data, I construct a global and panel dataset of Protestant missionary activity from 1900 until 1922. Table A1 compares this dataset against existing ones from the literature. 

###### **3.1.2 Catholic Missions** 

I also construct a dataset of Catholic mission stations from two editions of the _Atlas Hierarchicus_ (Streit 1913; 1929). It is a panel dataset, global in nature, and includes information on missionary society and various infrastructure such as schools and hospitals<sup>17</sup> . Since Catholic missionaries were, with very few exceptions, uninvolved in the process of Bible translation, I mainly use the presence of Catholic missionaries as a control in this paper. 

###### **3.2 Bible Translations** 

I construct Bible translation information for each language from _The Book of a Thousand Tongues_ (United Bible Societies 1972) and four editions of the _Ethnologue_ (1996; 2000; 2005; 2009). From the former, I collect information on the year of publication, translating authors, and the missionary societies they belong to for the original publication of each Bible book in every non-European language until 1968<sup>18</sup> . I extend this information until 2007 using the latter but it only includes the year of first Bible portions, first New Testament and first Bible. 

For Bible translations started before 1930 in Africa, I construct the site of translation link using biographical information on the translators at the time of translation<sup>19</sup> . I use over 500 sources for roughly 300 translators including missionary society reports and secondary sources. Appendix section A.2 provides further detail on the process of linking Bible trans- 

> 17The later Catholic edition has already been digitized by Cag´e & Rueda (2020) but without missionary society 

> 18It also includes some information on revisions, though by its own admission, this list is not exhaustive. 

> 19In principle, this method can be extended to the rest of the world, but due to time constraints and the fact that site of translation information is not useful for analysis in this paper, I limit this to Africa. I choose 1930 as a cutoff year given that the vast majority of translations are conducted at mission stations and the latest missionary atlas represents missionary activity as of 1922. 

16 

lations to mission stations. Given that the vast majority of translations are completed by Protestant missionaries, translation sites are most often linked to Protestant mission stations<sup>20</sup> . For each Bible translation site, I also assign a number of Bible verses translated. When only one missionary society is involved in the translation of a given Bible book, I assign all of its verses to that station. However, if multiple societies formed a committee for the translation of a given Bible book, then I divide the number of translated verses equally among all participating societies. Data on number of Bible verses translated permits the estimation of the intensive margin of Bible translation. 

Figure II maps the Protestant and Catholic mission stations as well as the Bible translation sites throughout Africa. Figure A2 zooms in on Nigeria and differentiates between various missionary societies. It shows that mission stations of the same society tend to be geographically concentrated. Moreover, different societies translate the Bible to different degrees with some translating everywhere they go while others translate not at all. 

###### **3.3 Language in Education Data** 

In order to assess the effects of language development on language promotion, I have handcoded a dataset on the use of each African language in public schools from 1960 until 2011. Specifically, for every primary grade, I know whether each language is used as a medium of instruction or taught as a subject. This dataset is an expansion of Albaugh (2014), who completed a similar task but only gave a general country-level score on the use of African languages in schools. In constructing this dataset, I used many sources but one in particular that I used frequently is Leclerc (1999), who manages a website on the languages used in administration, schooling, etc. for most countries in the world. 

> 20Only 4 of 282 translation sites are not affiliated with missionary societies. Afrikaans, an Indo-European language, is translated at Paarl. Gaa has some translation done by an unaffiliated Ghanaian clergyman on his own in Accra. Hausa was initially translated by a resident of Freetown in Sierra Leone, even though the language originates from Northern Nigeria. The Tsimihety version of Malagsy also has some translation done by an unaffiliated Malagasy clergyman. 

17 

###### **3.4 Demographic and Health Surveys** 

To evaluate the effects of Bible translations on education and health outcomes, I use the Demographic and Health Surveys (DHS). The DHS are nationally representative and span a large number of African countries. For the analysis, I use all available data from rounds 2 through 7 from 33 sub-Saharan African countries<sup>21</sup> for which geo-coordinates are available, making for a total of 99 geo-coded rounds<sup>22</sup> . 

My principal outcomes of interest are years of schooling and body mass index (BMI). BMI is calculated as weight in kilograms divided by squared height in meters. For health effects, I limit the sample to those whose BMI falls within the segment where general health increases linearly with BMI following Calvi & Mantovanelli (2018)<sup>23</sup> . I make no sample restrictions with regards to years of schooling. I also use alternative educational outcomes for robustness tests, including literacy, primary school completion and secondary school completion. With regards to health outcomes, I also look at height and hemoglobin levels for robustness. In terms of individual-level controls, I include age, gender, and urban status. 

In some specifications, I consider Bible translation into a person’s ancestral language rather than their proximity to a Bible translation site. I proxy ancestral language using reported ethnicity<sup>24</sup> . In these specifications, I am limited to 88 rounds from 22 countries given ethnicity is not reported in some country surveys<sup>25</sup> . 

In Table I, I provide summary statistics of a person’s exposure, both linguistic and ge- 

> 21When looking at missionary expansion in Sub-Saharan Africa, I have a sample of 39 countries. 

> 22On average each country has three geo-coded rounds of data available but some have as few as one round of data (e.g. the Central African Republic) while others have all 6 rounds of data available (e.g., Ghana). I omit all data from Ethiopia as explained above. 

> 23That is, I omit individuals for whom BMI falls below 15 and above 30. As BMI increases past 30, health complications due to obesity start to arise. 

> 24While the relationship between ethnicity and language is not one-to-one in Africa, a link can most often be easily made between the two. For example, in many Southern and East African countries, the language will simply be a prefix followed by the ethnicity name. For example, the Tswana are an ethnic group in Botswana and South Africa and the language they speak is Setswana, which literally means language of the Tswana. Where the link is more tenuous or the DHS information is simply not rich enough to capture this relationship, I omit them from analysis on ancestral languages. For example, in the South African and Zimbabwean DHS surveys, they report race (White, Black, Asian, etc.) instead of ethnicity. 

> 25In these specifications, I do not use geographical controls thus allowing me to use rounds of DHS for which there is no geo-location. 

18 

ographic, to Bible translations from the sample of DHS respondents. Panel A reports the statistics for DHS respondents in ILP countries while Panel B does the same for CLE countries. With regards to linguistic exposure, by 2007, a person is equally likely to have some scripture translation in their language in ILP (88%) and CLE (86%) countries. However, in ILP countries, translations begin much earlier and there is much more of the Bible translated as compared to CLE countries. With regards to geographic exposure, 23% of DHS respondents in ILP countries are within 25 kilometers of an historical translation site while only 16 % in CLE countries are. In sum, there is greater exposure to Bible translations in ILP than CLE countries, especially in the earlier periods. This reflects the colonial-era policies towards language use and missionaries outlined in the previous section. 

###### **3.5 Historical and Geographical Data** 

As per Jedwab et al. (2022), missionary societies tended to settle in more prosperous, central areas. Moreover, Bible translation sites may be even more selective given translators wanted to maximize the number of readers and thus began with larger languages (Vail 1989; Tembo 2020). Thus, to account for this selection, I control for a wide array of characteristics, both geographical and historical. Appendix A.5 provides further information on how each of these variables are sourced and constructed. 

###### **3.5.1 Historical Data** 

To account for the fact that mission stations and Bible translation sites are often located in more densely populated areas, I use population density information as of the year 1850 from the History Database of the Global Environment (HYDE) (Klein Goldewijk et al. 2011). I choose the year 1850 as it precedes the large expansion of missionary activity in Africa around that time due to the introduction of quinine. Missionary expansion has also been shown to occur along railways (Jedwab et al. 2022). I use data on colonial-era railways from 

19 

Jedwab & Moradi (2016) and supplement it with data from Nunn & Wantchekon (2011)<sup>26</sup> . I also use data on explorer routes from Nunn & Wantchekon (2011). Mission expansion was often restricted in areas of heavy Muslim influence by colonial governments to avoid conflicts (e.g., Bingham 1919; Cogneau & Moradi 2014). On the other hand, in Muslimmajority areas, Bible translation into the local language was a less obtrusive missionary task than opening Christian mission schools or even baptism of locals (Rosen 2020). Location of historical Muslim centers comes from Jedwab et al. (2022). 

###### **3.5.2 Geographical Data** 

Missionaries would also choose locations that would promote a greater chance of success. For these reasons, mission stations could be located in proximity to the coast, to the capital city, and to freshwater. I collect these data from Natural Earth (2024). Missionaries could also only station themselves in a location if the risk of dying from malaria was not so great. For this reason, I use data on malaria ecology from Kiszewski et al. (2004) and McCord & Anttila-Hughes (2017). In order to sustain themselves, missionaries would often have to rely on their own agricultural production. For this reason, I include data on average precipitation, number of growing days and the suitability of rainfed crops from the Global Agro-Ecological Zones (GAEZ). Rugged terrain may be less accessible to outsiders and would have thus historically provided better protection from slave raiders, which missionaries would have actively opposed. Ruggedness data comes from Nunn & Puga (2012). Finally, I also include information on the presence of various natural resources including petroleum (Lujala et al. 2007), diamonds (Gilmore et al. 2005), gold (Balestri 2012), and gems (Lujala 2009). 

> 26The Jedwab & Moradi (2016) data includes colonial railways built until 1960 and maps all railways with greater precision than Nunn & Wantchekon (2011). However, they do not include South African colonial railways which Nunn & Wantchekon (2011) does include. 

20 

###### **3.5.3 Determinants of Missions and Bible Translations** 

In Table II, I use the above historical and geographical characteristics to compare DHS clusters with (i) no Protestant mission station, (ii) a Protestant mission station but no translation site and (iii) a Protestant mission station and a translation site. Distance measures are taken from the cluster itself while other measures use the average amount within a 25-kilometer radius. From the table, it is clear that Protestant missions are established in more central prosperous areas (Jedwab et al. 2022). When comparing Protestant mission stations with and without Bible translations, they are more similar but still present some significant differences. For example, mission stations with a Bible translation tend to be located in areas with significantly greater pre-existing population density than mission stations without one. It is also noteworthy that mission stations with Bible translations are established on average 13 years earlier than those without. 

In Table III, I estimate the effect of a translation site on these same historical and geographic characteristics, conditional on mission presence within a 25-kilometer radius as well as the year of establishment of the first mission. I also separate out the sample into indigenous-language-permitted (ILP) countries and colonial-language-enforced (CLE) ones. I find that among mission stations established around the same time, those with a Bible translation are not located in more central or prosperous areas. For example, the difference in population density is small and insignificant. In CLE countries, however, I find that even conditional on year of establishment, places with a Bible translation site tend to be located in more prosperous and central areas. That is, they are located in places with higher population density and lower malaria risk while being closer to the capital and colonial railways. 

##### **4 Bible Translations and Missionary Activity** 

In this section, I present the empirical strategy and results relating to the expansion of missionary activity as a result of Bible translations. 

21 

###### **4.1 Foreign Missionaries** 

To test the effects of Bible translations on missionary activity, I exploit the panel nature of the mission data and the timing of publication to conduct a matched event study. I match mission stations with a linked Bible translation to never-treated stations. Before matching, I apply a set of sampling restrictions. First, I consider all sub-Saharan African missions, not only the ones in countries with DHS surveys. Second, I restrict to Bible translations starting between 1882 and 1929. Given that I have snapshots of missionary activity in 1900, 1908, 1915 and 1922, it means that some translations only have data for periods pre-translation and some only have data for post-translation periods. Third, I restrict to missions that include information on the year of establishment. Fourth, given that there can be multiple missions per town, I restrict the control sample to the first established mission in the town. Finally, I restrict all missions so that there are no other earlier Bible translations within a 50-kilometer radius to rule out confounding effects of other translations. For never-treated missions this implies that there are no translation sites within a 50-kilometer radius. 

To match stations with a translation to those without, I use propensity-score matching with exact constraints. Specifically, paired stations must (i) be located in the same policy space (ILP or CLE country) (ii) be established within the same 5-year window (e.g. 18801884) and (iii) either both be established first within a 25-kilometer radius or both not. I then use all historical and geographic variables listed in Table II to predict translating, selecting among them with a Lasso logit regression to eliminate sensitivity to variable choice. Table A5 shows the resulting pairs are generally well balanced across covariates, whether Lassoselected or not. 

Once matching is complete, I run the following event-study specification: 

22 



_Yit_ represents outcomes for mission station i, belonging to matched pair p, in year t. The set of outcomes reflect various measures of missionary activity within a 25-kilometer radius of the mission station i. There are four years of data reflecting the four digitized Protestant missionary atlases: 1900, 1908, 1915 and 1922. _αt_ and _αp_ are year and pair fixed effects respectively. _TRi_ is an indicator variable for whether the mission station is linked to a Bible translation. Due to small sample size, I group years into relative periods rather than estimating year-specific coefficients. Relative periods _RPk_ ( _p_ ) are determined jointly for the matched pair by the year of publication of first Bible portions at the treated mission. In addition, I allow for a three-year publication delay<sup>27</sup> . Publication years are grouped into the following 7 periods: 1882-1888, 1889-1895, 1896-1902, 1903-1910, 1911-1917, 1918-1924, 1925-1929. I then assign relative periods based on the period of publication and the year of data. So, for example, a publication year of 1885 falls within the first period and thus has data for the relative periods +2, +3, +4, and +5 from the 1900, 1908, 1915, and 1922 atlases respectively<sup>28</sup> . I use the relative period -1 as reference. The coefficients of interest, _δk_ , capture average differences in outcome between treated and untreated mission stations relative to the reference period. Standard errors, _ϵipt_ , are clustered at the mission station level. 

> 27This delay reflects the fact that copies of the translated scripture would be available to missionaries years prior to its actual publication. As previously mentioned, the book of Matthew was translated into Tiv in 1917 and provided to other missionaries that year (Dutch Reformed Church of South Africa 1917), three years before the book was published in 1920 (United Bible Societies 1972). This publication delay reflects the fact that most initial publications were done in Europe as European Bible societies would print scripture at a highly subsidized price. 

> 28 Conversely, a publication year of 1913 falls within the 5th period and thus has data for the relative periods -2,-1,0 and 1 from the 1900, 1908, 1915 and 1922 atlases respectively. 

23 

Figure III plots the estimated coefficients _δk_ from the above event study on the number of foreign missionaries within a 25-kilometer radius in the full sample as well as separately for CLE and ILP countries. Before translation, treated and control stations follow parallel trends, supporting the identifying assumption. Immediately following translation, treated stations host on average 1.12 more foreign missionaries than control ones. The impact grows over time with there being an additional 5.69 missionaries five periods (26-33 years) later. These results are consistent with Bible translations acting as drivers, not merely byproducts, of missionary activity, as hypothesized by Smalley (1991). Figures A5 and A6 show that the results are robust to the removal of the publication delay and to including country as a matching constraint respectively. Figure A7 finds that there are as many as 14 more foreign missionaries after 5 periods within a larger 50 kilometer radius<sup>29</sup> . 

To estimate the total effect of translations on missionary activity rather than for each relative period individually, I run the following specification: 



As above, _Yipt_ are outcomes for mission station i, within matched pair p, at year t. _αp_ are pair fixed effects. _TRi_ is an indicator for whether mission i is linked to a translation. _POSTpt_ is an indicator for whether year t is later than the translation year assigned to pair p, accounting for the three-year publication delay. _β_ 3 is the coefficient of interest that captures the differential effect of being a translation mission in a year after translation is completed. Standard errors, _ϵipt_ , are clustered at the mission station level. 

Table IV displays results from the above equation. Column (1) reports for the number of foreign staff in total within a 25-kilometer radius. In the full sample, there are 2.97 more foreign missionary working after translation, representing an 86% increase compared 

> 29I limit the sample to those mission stations, treatment and control, that have no earlier translations within a 100 kilometer radius to avoid violations of the stable unit treatment value assumption (SUTVA). 

24 

to the mean. The coefficient is even larger in CLE countries, though there are also fewer observations. The vast majority of this increase comes from missionaries belonging to the same missionary society that translated (column 2) rather than other missionary societies (column 3). Roughly half the increase comes from missionaries working at the translation site itself (column 4), with the rest working at other missions within the 25-kilometer radius (column 5). Even when missionaries expand to other mission stations, they work almost exclusively within the same language polygon (columns 6 and 7). These results confirm the role of Bible translations in making the language accessible both at the translation site and in nearby areas that use the same language. Column 8 shows that there is also a small but significant increase in the number of mission stations. Relatedly, there is an 11 percentage point decrease in the likelihood of exit (column 9). Meanwhile, column 10 shows there is an increase in the number of missionary doctors, but this result is only significant in ILP countries. 

Figures A8, A9, A10, A12, A13, and A14 provide the event-study equivalents to columns 2 through 9. Figure A11 repeats the event study by examining expansion within the same language polygon versus outside it, except estimating the effect on the number of foreign missionaries working within a 50 kilometer radius instead. It shows that the expansion within the language polygon is strategic and not a mechanical artifact of there being no area within the radius that falls outside the language polygon. Together these results show that Bible translations greatly increased the number of foreign missionaries working in the area and that their expansion entailed both a greater concentration of missionaries at the translation site itself as well as an expansion into nearby areas that spoke the same language. There is no evidence of spillover effects to other missionary societies. 

###### **4.2 Missionary Infrastructure** 

In this subsection, I estimate the effects of Bible translations on missionary infrastructure. The empirical strategy largely follows that of the previous subsection on foreign mission- 

25 

aries. However, unlike for the number of foreign missionaries, information for missionary infrastructure is available only for the year 1900 (Beach 1903). Thus, I can only conduct a naive difference-in-difference estimation without verifying that trends prior to translation are parallel. I also restrict the sample further to only include mission stations belonging to missionary societies for which at least 10% of their global mission stations have at least some infrastructure reported. I implement this restriction to avoid treating lack of reporting as lack of infrastructure. Once this restriction is applied, I use the same matching algorithm described in the previous section and run the following specification: 



_Yip_ represent outcomes on missionary infrastructure within a 25-kilometer radius of mission station i belonging to matched pair p. _αp_ are pair fixed effects. _TRi_ is an indicator for whether mission i is linked to a translation. _POSTp_ is an indicator variable equal to 1 if the data available for pair p comes after the year of first Bible translation publication. I do still allow for a three-year publication delay. In other words, _POSTp_ is equal to 1 if a mission is linked to a translation started in 1902 or earlier. _β_ 3 is the parameter of interest as it captures the change in infrastructure due to the presence of a Bible translation. 

Table V reports the results from equation 1 on a set of religious, education-related and health-related infrastructure. Panel A shows results for the entire sample while panels B and C show results for ILP and CLE countries respectively. Following translation, there are significant increases in church membership (column 3), printing presses (column 4), primary schools (column 5), high schools (column 6), hospitals (column 8) and dispensaries (column 9). These results are large in magnitude as, for example, there are 0.34 more high schools, a roughly 189% increase relative to the mean. Moreover, these results are driven almost entirely by effect sizes in ILP countries. Coefficients in CLE countries are insignificant and 

26 

smaller in magnitude. These results show that the growth of missionary presence does not lend itself simply to more translation work but rather to investment in printing, education and health. The difference between ILP and CLE countries does show, however, that an enabling policy environment is crucial for this investment. 

###### **4.3 Infrastructure Persistence** 

In this subsection, I provide some suggestive evidence of the persistence of the infrastructure built during missionary times until modern times. To do this, I use building data from OpenStreetMap, selecting from it geo-coordinates for all schools, universities and hospitals. I detail how I collect this data further in appendix section A.6. Because this data exists only for a post-period, I can no longer conduct difference-in-difference estimation. Instead, I run a simple OLS regression among mission stations with and without Bible translations, while controlling for a host of geographical and historical factors as well as year of establishment. While this method is more likely to suffer from omitted variable bias than difference-indifference, Table III showed that, conditional on year of establishment, missions with and without Bible translations were broadly similar, at least in ILP countries. I still restrict the sample so that there are no earlier translations within a 50-kilometer radius to avoid having both treated and control missions within the same area. Thus, I run the following specification: 



_Yic_ are modern infrastructure outcomes within a 25-kilometer radius of mission i in country c. Specifically, I use indicator variables for the presence of any schools, universities and hospitals in the year 2024. _αc_ are a set of country fixed effects. _Xi_ is a host of geographic, historical and mission controls at the mission station level. Geographic and historical con- 

27 

trols are the same as those shown in Table II. I control for year of establishment flexibly by creating a set of indicator variables for whether the mission is established in 25-year blocks starting in 1805 and ending in 1930. _TRi_ is an indicator for whether mission i is linked to a translation. Standard errors, _ϵic_ , are two-way clustered at the second administrative regional level and cell of a 0.5 degree grid of the world. In appendix section B, I show that clustering in this way approximates Conley standard errors using a 50-kilometer cutoff. 

Table VI shows that there is an increase in the presence of universities everywhere but that this increase is only significant in the case of ILP countries. There is no significant increase in the presence of schools due to historical Bible translation sites, likely due to the present ubiquity of primary schools. There is an increase in the presence of hospitals, but only in ILP countries. These results provide some evidence of persistence of missionary infrastructure constructed immediately following Bible translation. 

###### **4.4 Language of Instruction** 

In this subsection, I estimate the effects of Bible translation on the language of instruction in schools. Data on the language of instruction used by missionary societies in the preindependence period is not widely available and therefore I make use of data I constructed for the post-independence period, building on Albaugh (2014)’s work. Post-independence data is still highly informative of missionary practices given that many governments throughout Africa continued with the education policy that had been developed prior to independence (Albaugh 2014). Thus, I estimate the effects of Bible scripture being available in a language on the use of that language as a medium of instruction in schools immediately post-independence. Specifically, I run the following specification: 



28 

_Ylc_ is an outcome variable for language l in country c. The outcomes of interest are whether language l is used as medium of instruction in country c immediately post-independence. The sample of languages comes from the Ethnologue, which means that all languages spoken in that country will be included in the regression. I also look at the number of grades in which that language is used as a medium of instruction. _αc_ are country fixed effects. _TRl_ is an indicator variable for whether there exists published Bible scripture in that language prior to 1960, roughly the date of independence for most African countries. _Xl_ is a set of control variables at the language level consisting of indicator variables for the number of countries in which that language is spoken. _ϵlc_ are standard errors two-way clustered at the country and language level. 

Table VII shows the results of equation 2. It shows that languages for which there is a Bible translation are far more likely to be used in schools as a medium of instruction, but only in ILP countries. In CLE countries, there is little to no use of indigenous languages with or without a Bible translation. In ILP countries, the Table shows that a Bible translation is a necessary condition for use as a medium of instruction, given the large coefficient estimates and the fact that almost no languages without a translation are used in schools. For example, in column (1), in ILP countries, only 0.8% of languages without any Bible translation are used in schools but, with a translation, that likelihood increases to 11.9 %. These results suggest that colonial policy towards language use in mission schools was effective. 

##### **5 Bible Translations and Modern Development** 

In this section, I estimate the effects of Bible translations on modern development. For this, I make use of two different sources of variation. First, I use geographic variation in exposure to a historical translation site. That is, a DHS cluster that is within 25 kilometers of a translation site will be considered treated. Second, I use linguistic variation in exposure through the Bible being translated into one’s ancestral language. 

29 

###### **5.1 Empirical Strategy** 

To test the effects of being proximate to a historical Bible translation, I implement the following specification: 



_Yigct_ are developmental outcomes for individual i at geo-referenced DHS cluster g within country c interviewed in round t. I use years of schooling to measure human capital and body mass index as a measure of general health. I also show robustness to alternative measures. _αct_ are country-by-round fixed effects to account for any country characteristics that determine simultaneously Bible translation and development. These fixed effects also account for country-specific trends in educational or health-related outcomes. _TRg_ is a binary variable for whether a translation site is found within a 25-kilometer radius of the DHS cluster. _Xi_ is a set of individual level controls including gender, age, age squared and a binary variable indicating whether the individual lives in an urban setting. _GEOHISTg_ corresponds to a vector of geographical and historical controls as shown in Table II. 

_MISSIONg_ is a set of variables controlling for exposure to mission stations within a 25-kilometer radius. Specifically, I control for the presence of a Protestant mission station, the presence of a Catholic mission, and the year of the first established Protestant mission in 25-year blocks starting in 1805 and ending in 1930. Thus, the coefficient of interest, _β_ , can be interpreted as the additional effect of a translation site, conditional on the presence and timing of missionary activity in the area. It is worth noting that I do not control for the number of mission stations but merely their presence. As seen in the previous section, Bible translations increase the number of missions in an area and thus controlling for total number of missions would also control for the effect. 

_ϵigct_ are standard errors that are two-way clustered at the second administrative level 

30 

(often districts) and the cell level of a 0.5 by 0.5 decimal degree grid of the world. The combination of these clusters is designed to imitate Conley standard errors without the computing problems that come with allowing for geographical serial correlation on a very large dataset. Intuitively, by clustering using multiple unrelated geographical shapes, there are fewer neighboring points that do not have at least one shape in common. Appendix section B demonstrates that clustering standard errors in this way approximates Conley standard errors with a cutoff distance of 50 kilometers. 

###### **5.2 OLS Results** 

###### **5.2.1 Education Outcomes** 

Table VIII reports the coefficients of the long-run effects of Bible translations on years of schooling separately for ILP countries (Panel A) and CLE countries (Panel B). Column (1) includes only country by round fixed effects individual controls. Coefficients are similarly large in ILP and CLE countries, testament to the selection of mission stations and Bible translation sites into more central, prosperous areas. Column (2) adds historical and geographic controls. The coefficient for ILP countries remains positive and significant, but the coefficient for CLE countries becomes negative, albeit insignificant. This confirms results from Table III that Bible translation sites are more selectively located in CLE countries than in ILP ones. 

Column (3) includes the presence of mission stations, both Catholic and Protestant, as controls. In ILP countries, being proximate to a Bible translation site increases years of schooling by 0.283 years, or by 62% of the effect of Protestant missions alone. In these countries, Catholic missions contribute little to long-run human capital accumulation, even though their schools were provided with subsidies. In CLE countries, being proximate to a Bible translation site reduces years of schooling by 0.386 years, thus annulling the positive effect of a Protestant mission station<sup>30</sup> . By contrast, being proximate to a Catholic mission 

> 30Though I cannot rule out that the positive coefficient on a Protestant mission station is still due to 

31 

increases schooling by 0.521 years. This is testament to the fact that, in CLE countries, Catholic missionaries were often compatriots of the colonial government and that Catholic mission schools were provided with subsidies, unlike Protestant ones. These results help resolve a debate within the mission literature surrounding the relative benefits of Protestant versus Catholic missions. Nunn (2014) initially found that Protestant missions improved education outcomes more in the long run than Catholic ones. However, using missionary data from (Beach & Fahs 1925) rather than Roome (1925), Becker & Meier zu Selhausen (2023) find similarly large effects for both denominations. These results point to the fact that success of a mission station, either Protestant or Catholic, depends heavily on the policy environment in which it is situated. 

Column (4) includes further a series of controls for the year of establishment of the first Protestant mission station in the area. Table III showed that, conditional on year of establishment of the first Protestant mission, locations with and without Bible translations were largely similar in ILP countries. For this reason, it is my preferred specification. Being proximate to a Bible translation increases years of schooling by 0.205 years in the long run. Meanwhile, in CLE countries, there is a decrease of 0.433 years. In both samples, these results may be underestimates given Bible translations can produce missionary investment outside of the 25-kilometer radius. On the other hand, Bible translation sites in CLE countries are established in already more central and prosperous areas, even conditional on year of establishment. 

Table A8 reports the robustness of the coefficients from my preferred specification to alternative clustering of standard errors. The choice of clusters is made to resemble Conley standard errors with 50-, 75- and 100-kilometer cutoffs while being computationally feasible (see Appendix Section B). 

Table A14 reports the long-run effects of Bible translation sites on alternate measures of human capital using my preferred specification. Primary school completion significantly selection, even with a set of historical and geographical controls 

32 

increases by 2.3 percentage points, secondary completion by 0.9 percentage points, though not significant, and literacy significantly increases by 1.6 percentage points. 

The results in ILP countries align broadly with long-run effects of mission stations on human capital. For example, Nunn (2014) finds that each mission within a 25-kilometer radius of a person’s residence increases schooling by 0.143 years. Becker & Meier zu Selhausen (2023) find that being within 25 kilometers of any Protestant mission increases schooling by 14.5 percent<sup>31</sup> . It also aligns with findings that specific missionary investments lead to differential improvements as Cag´e & Rueda (2016) find that a 1 percent increase in proximity to a printing press is associated with an increase of 6.3 percent of a standard deviation. 

By contrast, to my knowledge, no prior studies have found that mission presence or specific missionary investments have led to worse educational outcomes, as is the case for Bible translations in CLE countries. In Appendix C, I develop a model that can help explain this negative effect. In essence, a Bible translation facilitates non-school spheres of society, especially church, to operate in the indigenous language rather than the colonial one. This then robs children of familiarity with the colonial language, thus weakening their educational performance in school. Moreover, it is only the policy around language use in schools which can explain this. By contrast, not subsidizing Protestant mission schools cannot explain why mission stations with a Bible translation would produce worse educational outcomes than those with one. 

###### **5.2.2 Health Outcomes** 

Table IX reports the long-run effects of being proximate to a Bible translation site on body mass index (BMI) separately for ILP (Panel A) and CLE (Panel B) countries. Following Calvi & Mantovanelli (2018), the sample is restricted to the portion of BMI that is increasing with general health. Similar to education outcomes, results are largest in columns 1 and 2, 

> 31In Latin America, Valencia Caicedo (2019) finds illiteracy decreases by 10% moving 100 kilometers closer to a Catholic mission. In Mexico, Waldinger (2017) finds that being within 5 kilometers of a Catholic mission increases schooling by 0.66 years. In India, Calvi et al. (2022) find that residences within 25 kilometers of a Protestant mission have 2 percentage points higher literacy rates. 

33 

before controlling fully for selection into central and prosperous areas. Column 3 shows that, in ILP countries, being proximate to a Bible translation increases BMI by 0.1 or 0.03% of a standard deviation. This represents an effect size 109% of that of a Protestant mission on its own. When controlling for the year of first Protestant establishment, the coefficient is largely unchanged. These results are consistent with the increases in doctors and medical infrastructure surrounding Bible translation sites. Meanwhile, in CLE countries, being proximate to a Bible translation site leads to a decrease in BMI between 0.161 (column 3) and 0.102. However, these coefficients are not statistically significant. There had been no increase in doctors or medical infrastructure following translation in CLE countries. 

Table A18 reports the robustness of the coefficients from my preferred specification to alternative clustering of standard errors. 

Table A19 reports coefficients for a set of alternative health measures. In ILP countries, being proximate to a Bible translation site also lends itself to a significant 0.9 percentage point decreased likelihood of being underweight (BMI less than 18.5). It also lends itself to being taller with lower likelihood of anemia, but these coefficients are not significant. In CLE countries, however, I find that being proximate actually lends itself to a significant increase in height but also significantly lower hemoglobin levels. These opposing effects on health outcomes suggest caution when interpreting these effects. 

The evidence from ILP countries aligns with evidence from colonial India (Calvi & Mantovanelli 2018) where reducing distance to a Protestant medical mission by 50% increases BMI by 0.09 standard deviations. These results also align with Cag´e & Rueda (2020) who study Africa and find that positive health outcomes are associated with medical missions in particular and not just any mission station. 

###### **5.3 IV Estimation** 

Table III had shown that, conditional on year of establishment, missions with and without Bible translations were well balanced along observable characteristics in the ILP sample, 

34 

but not in the CLE sample. Moreover, there may be unobserved characteristics such as openness to outsiders or interest in Western education (Vail 1989) that may have influenced the location of Bible translation sites. To address this possible endogeneity, I use the log proclivity of the first established missionary society in the area as an instrument. Intuitively, the demand-side factors for Bible translation such as population density, openness to outsiders, etc. are endogenous to long-run development while the supply-side factors such as missionary society priorities are plausibly exogenous. That is, some missionary societies were renowned for Bible translation and would adopt this practice in every location they went regardless of demand. For instance, the Baptist Missionary Society translated the Bible into numerous South Asian languages before ever setting foot in Africa. I construct the instrumental variable in the following way: 



I create a society specific measure of proclivity taking the total number of verses they translate at all their missions throughout the world and divide that by the number of global missions. Then to account for the fact of diminishing returns to language development with each Bible verse, I take the log of the society’s proclivity<sup>32</sup> . Calvi & Mantovanelli (2018) construct a similar instrument using medical missions belonging to a society divided by total missions as measure of missionary-society-level focus on health. However, I only consider the proclivity of the first established missionary society. Information about demand for Bible translations is more plausibly unknown to the first society rather than subsequently established societies. 

> 32Heaps’ Law in linguistics states that the number of unique words in a document follows roughly a square-root relationship. Language development also has diminishing growth with regards to the number of unique words. Thus, taking the log of verses is a good proxy for language development. 

35 

There are two important caveats in using this instrument. First, A10 shows that even after controlling for mission presence and year of establishment, differences in location preference persist. In ILP countries, locations established first by a high proclivity society tend to be further from colonial railways and closer to historical Muslim centers. In CLE countries, high proclivity societies tend to settle in places with easier access to freshwater sources and more growing days per year<sup>33</sup> . Second, A13 shows that missionary societies with higher proclivities to translate the Bible also tend to invest more in education. This, however, is unsurprising given the effect of Bible translations themselves on education investment. 

Notwithstanding the above caveats, I run the following first-stage regression: 

_TRgc_ = _β_ 0 + _θc_ + _γ_ 1 _LogProclivityFirstg_ + _γ_ 2 _GEOHISTg_ + _γ_ 3 _MISSIONg_ + _µgc_ 

_TRgc_ is an indicator variable equal to 1 if DHS cluster g in country c is within 25 kilometers of a Bible translation site. _θc_ are country fixed effect. _LogProclivityFirstg_ is the instrumental variable as described in the previous paragraph. _GEOHISTg_ and _MISSIONg_ are the same vectors of control variables as described in equation 3. Standard errors, _µgct_ , are clustered in the same way as in equation 3. 

Column 5 of Table VIII provides the estimated coefficient of _γ_ 1, the parameter of interest while the first-stage F-statistic is shown in column 6. In ILP countries (Panel A), doubling the proclivity of the first society increases the likelihood of there being a linked Bible translation by 4.8 percentage points or 27% relative to the mean. The associated F-statistic is roughly 45, well clear of common thresholds for instruments (Staiger & Stock 1997; Stock & Yogo 2005). The effect is even larger in CLE countries but with an F-statistic of roughly 30 due to larger standard errors. 

Column 6 of Table VIII reports the coefficients from the second stage regression. In ILP countries, being proximate to a Bible translation site leads to a 1.765 increase in years of 

> 33These two measures are obviously correlated with one another. 

36 

schooling. This coefficient is much larger than what has been found previously in the literature, suggesting the two-stage-least-square estimation may suffer from a weak instrument. In CLE countries, the coefficient is -0.093. These results provide support for the positive effect in ILP countries but shed some doubt on the result in CLE countries. Additionally, by using variation in society proclivity, they highlight the stark differences in development outcomes from the work of various missionary societies. 

###### **5.4 Treatment Intensity** 

In this subsection, I provide some evidence that greater treatment intensity corresponds to larger effect sizes. In particular, I measure treatment intensity by number of verses translated, geographical proximity to translation site, and temporal proximity to the time of translation. 

###### **5.4.1 Education Outcomes** 

Table A15 examines the heterogeneity by amount of translation according to discrete categories (columns 1 and 4), log number of verses (columns 2 and 5) and a second order polynomial of verses (columns 3 and 6). In ILP countries, there is not a linear relationship between amount of translation and educational attainment. Missions with both very little (less than the Gospels) or very much (at least one full Bible translated) translation have no significant effect on educational attainment. Meanwhile, mission stations with an intermediate amount of translation show large effects. These results are consistent with Bible translations being positively associated with language development but potentially being time costly and crowding out other more productive investments. There is a less of a clear pattern in CLE countries with all translation amounts being deleterious on development. 

Table A16 Panel A shows that, in ILP countries, effect sizes on education are larger for individuals closer in proximity to the site of translation. Panel B shows that, in CLE countries, the largest negative effects are again closer in proximity to the site of translation. 

37 

However, columns (4) and (5) of Panel B are less supportive of this view as distance to translation site is negatively correlated with educational attainment. 

Table A17 examines the heterogeneity by year of birth for ILP countries (columns 1-2) and CLE countries (columns 3-4). In ILP countries, educational gains are largest among earlier cohorts, suggesting a large immediate effect followed by a gradual decline. This is consistent with the fact that, in colonial times few other, non-missionary, educational opportunities were available but that over time education, especially primary schooling, became widespread. In CLE countries, however, the negative effect size is smaller in absolute magnitude to begin but is more persistent over time. 

###### **5.4.2 Health Outcomes** 

Table A20 finds that mission stations in ILP countries with generally greater amounts of translation have larger effects on BMI but the results are not statistically significant. In CLE countries, there is no clear pattern of an association between amount of translation and health outcomes. Table A21 finds that, in ILP countries, closer proximity to the site of translation leads to greater improvements in health while, in CLE countries, the opposite is true. 

Table A22 finds health improvement due to Bible translation may actually be larger for later generations. In CLE countries, the worst health effects from translation actually occur for later generations. These results are in contrast to those for education outcomes whereby the greatest effects were felt among earlier generations. These results can be explained in part by the fact that translation sites maintain their infrastructural advantage in health into modern times, unlike in education (see Table VI). Moreover, it is possible that as quality of medical assistance improves over time the treatment effects of being more proximate to a hospital also increase. 

38 

###### **5.5 Linguistic Variation of Bible Translations** 

Thus far, I have considered treated individuals to be those who live in close proximity to historical Bible translation sites. In this subsection, I instead consider treated individuals to be those whose ancestral languages, which I proxy with their ethnicity, have a Bible translation. In the previous analysis, I was restricted to translations which I could link to historical mission stations. With this analysis, however, I can extend my attention to all original Bible translations until the year 2007. In so doing, I am extending the empirical strategy adopted by Okada da Silva et al. (2023), who consider a smaller set of Bible translations completed in the 1980s. 

###### **5.5.1 Empirical Strategy** 

Simply comparing members of different language groups with and without a Bible translation would yield biased results due to the fact that missionaries chose languages for translation based on the potential number of readers. Moreover, it is possible that individuals endogenously select into ethnic groups with a codified language if they show a preference for education. Thus, to address these concerns I adopt a difference-in-difference framework. The first “difference” comes from comparing individuals with a Bible translation in their language to others who have still never had a Bible translated into their language. As previously mentioned, individuals are assigned to their ancestral language through their ethnicity. The second “difference” comes from the fact that Bible translations, and language codification generally, were essential for the use of indigenous languages in schools. Moreover, with very few exceptions, indigenous languages have only been used as medium of instruction for the first three grades (see Figure A18). Thus, I can consider cohorts aged 9 and younger at the time of the publication of some biblical scripture to be exposed to treatment while cohorts aged 10 and older to be unexposed. For this reason, I can causally estimate the effects on education but not health outcomes. In health, there is no clear distinction in effect sizes among different cohorts. 

39 

Given that the Bible is translated into new languages each and every year, it means there is staggered adoption of treatment. Furthermore, given a high likelihood that earlier translations target larger languages with potentially heterogeneous treatment effects, a twoway fixed effect estimator will be biased (Sun & Abraham 2021). For this reason, I implement the estimator from Sun & Abraham (2021) that accounts for these particularities. Due to sample size restrictions, I group cohorts together into three years bins relative to the year of publication of first Bible scripture. 

In particular, I run the following specification: 



In this specification, I estimate effects on outcomes _yiecb_ for individual i of ethnicity e surveyed in country c born in year of birth bin b. _αct_ are country by year of birth fixed effects to account for country-specific trends that may influence both translation and education. That is, trends of treated language groups against those of untreated groups in the same country. _αe_ are ethnicity fixed effects. _Xi_ is a vector of individual level controls including gender, age and age squared at time of interview as well as urban status. Only individuals aged between 24 and -8 (i.e. born 8 years after publication) at the time of publication are included in the sample. Ages are grouped into 3 year bins. I use the age bin between 12 and 10 as the excluded reference group given they are the first to be untreated and ethnicity fixed effects. Thus, the coefficients _β_ [24 _,_ 22] up to _β_ [15 _,_ 13] estimate trends prior to translation while the rest measure the treatment effect of Bible translations. Finally, _ϵiecb_ are standard errors clustered at the ethnicity level, i.e. the level of treatment. 

40 

###### **5.5.2 Results** 

Figure IV plots the coefficients _βb_ from equation 4 on years of schooling. In the same graph, it shows the estimates for the full sample, ILP countries and CLE ones. Among cohorts too old to benefit from a Bible translation, there is no evidence of differential trends among treated and untreated language groups in any of the samples. Among younger cohorts, however, there is an immediate significant effect for the cohort aged 7 to 9. In ILP countries, this effect is positive while in CLE ones, it is negative, echoing the results found using geographic variation in Table VIII. In ILP countries, this effect grows to roughly 0.4 more years of schooling and remains persistent over time. While the magnitude is somewhat larger than that found using geographical variation, it is within the range of effects found in Table A17 among different generations. With regards to CLE countries, this negative effect grows over time reaching a magnitude of -0.6 years of schooling for the youngest considered cohort. 

Figures A19 and A20 repeat this exercise for literacy and primary school completion respectively. For example, there is as much as a 6-percentage point increase in literacy among ILP countries and 2-percentage point decrease among CLE ones. Together, these results further confirm the effects found in the previous subsections using geographic variation in treatment. They show that investment in language in environments that are permissive of those languages’ use in schools can have positive consequences for education. However, in environments which repress the use of those languages, investment may simply make individuals less in tune with the language of formal systems. 

##### **6 Conclusion** 

In this paper, I investigate how Bible translations in Africa shaped missionary presence and long-run development outcomes. Missionaries made key investments in education and health throughout the continent but their presence was unevenly felt across regions, even within the same country. Bible translations, through the codification of language, made it possible 

41 

for foreign missionaries to learn the local language and work effectively. Exploiting the panel nature of the data, I find that, following a Bible translation, there is a large increase in the number of foreign missionaries. However, only where colonial policy was favorable to missionary investment, i.e. ILP countries, do we see increases in infrastructure such as schools, hospitals and printing presses. 

Using a variety of specifications that make use of either geographic or linguistic exposure to Bible translations, I find that Bible translations only increased educational attainment and improved health outcomes in the ILP countries. In CLE countries, where colonial policy was adversarial towards missionary activity, we actually see a deterioration of education outcomes. 

My paper suggests that language development and education policy interact in meaningful ways to influence human capital accumulation. One the one hand, it suggests there may be large educational gains to using indigenous languages as media of instruction in countries that have thus far restricted them. Many such languages may already be codified and widely used. On the other hand, it suggests that the revitalization of dying languages may only worsen educational attainment if it deprives children of time spent with the language taught in schools. 

42 

##### **References** 

- Abadie, A., Athey, S., Imbens, G. W. & Wooldridge, J. M. (2023), ‘When Should You Adjust Standard Errors for Clustering?’, _Quarterly Journal of Economics_ **138** (1), 1–35. 

- Abramitzky, R. & Sin, I. (2014), ‘Book Translations as Idea Flows: The Effects of the Collapse of Communism on the Diffusion of Knowledge’, _Journal of the European Economic Association_ **12** (6), 1453–1520. 

- Albaugh, E. A. (2014), _State-Building and Multilingual Education in Africa_ , Cambridge University Press. 

- Ananyev, M. & Poyker, M. (2021), ‘Christian missions and anti-gay attitudes in Africa’, _Journal of Economic Behavior and Organization_ **184** , 359–374. **URL:** _https://doi.org/10.1016/j.jebo.2021.02.003_ 

- Anderson, G. H. (1999), _Biographical Dictionary of Christian Missions_ , William B. Eerdmans Publishing Company, Grand Rapids, Michigan. 

- Andersson, L.-G. & Janson, T. (1997), _Languages in Botswana: Language Ecology in Southern Africa_ . 

- Aram, B. I. (2022), ‘Marwaale, Tabitha Maria Madgadelena’. **URL:** _https://dacb.org/stories/somalia/marwaale-tabitha/_ 

- Asewie, B. A. (2013), Towards a Model for Contextualising Christianity in the, PhD thesis, South African Theology Seminary. 

- Balestri, S. (2012), ‘Gold and civil conflict intensity: Evidence from a spatially disaggregated analysis’, _Peace Economics, Peace Science and Public Policy_ **18** (3), 1–17. 

- Beach, H. P. (1903), _A Geography and Atlas of Protestant Missions: their environment, forces, distribution, methods, problems, results and prospects at the opening of the twentieth century_ , Student Volunteer Movement for Foreign Missions, New York. 

- Beach, H. P. & Fahs, C. H. (1925), _World Missionary Atlas_ , Institute of Social and Religious Research, New York. 

- Beach, H. P. & St. John, B. (1916), _World Statistics of Christian Missions: Containing a Directory of Missionary Societies, a Classified Summary of Statistics, and an Index of Mission Stations Throughout the World_ , The Committee of Reference and Counsel of the Foreign Missions Conference of North America. 

- Becker, B. (2022), ‘The Empire Within: Longitudinal Evidence on the Expansion of Christian Missions in Colonial Africa’, _Journal of Historical Political Economy_ **2** (2), 333–362. 

- Becker, B. & Meier zu Selhausen, F. (2023), Women on a Mission: Protestant Legacies of Gender Equality in Africa? 

43 

- Becker, B. & Schmitt, C. (2023), ‘License to educate: The role of national networks in colonial empires’, _World Development_ **169** , 106286. 

- Becker, S. O. & Woessmann, L. (2009), ‘Was Weber Wrong? A Human Capital Theory of Protestant Economic History’, _Quarterly Journal of Economics_ **124** (2), 531–596. 

- Bergeron, A. (2025), From Kin to Creed: Missions and the Reconfiguration of Social and Moral Order in Colonial Congo. 

- Bingham, R. V. (1919), ‘Britain’s Crisis in Missionary Policy’, _The Evangelical Christian_ (June), 165–167. 

- Binzel, C., Link, A. & Ramachandran, R. (2025), The Protestant Reformation and Its Transformation of Society : The Rise of the Vernacular. 

- Buell, R. L. (1927), ‘The Struggle in Africa’, _Foreign Affairs_ **6** (1), 22–40. 

- Buell, R. L. (1928), _The Native Problem in Africa, vol.2_ , The MacMillan Company, New York. 

- Bunche, R. J. (1934), ‘French Educational Policy in Togo and Dahomey’, _The Journal of Negro Education_ **3** (1), 69–97. 

- Cag´e, J. & Rueda, V. (2016), ‘The Long-Term Effects of the Printing Press in sub-Saharan Africa’, _American Economic Journal: Applied Economics_ **8** (3), 69–99. 

- Cag´e, J. & Rueda, V. (2020), ‘Sex and the mission: The conflicting effects of early Christian missions on HIV in sub-Saharan Africa’, _Journal of Demographic Economics_ **86** (3), 213– 257. 

- Calvi, R., Hoehn-Velasco, L. & Mantovanelli, F. G. (2022), ‘The Protestant Legacy Missions, Gender, and Human Capital in India’, _Journal of Human Resources_ **57** (6), 1946–1980. 

- Calvi, R. & Mantovanelli, F. G. (2018), ‘Long-term effects of access to health care: Medical missions in colonial India’, _Journal of Development Economics_ **135** (July), 285–303. 

- Cameron, D. (1924), ‘An Ordinance to Enable Trustees of Corporate Bodies to Title Be Appointed and to Have Perpetual Succession and to Hold Land’. 

- Changuion, L. & Steenkamp, B. (2012), _Disputed land: the historical development of the South African land issue, 1652-2011_ , Protea Books, Pretoria. 

- Cogneau, D. & Moradi, A. (2014), ‘Borders that divide: Education and religion in Ghana and Togo since colonial times’, _Journal of Economic History_ **74** (3), 694–729. 

- Conley, T. G. (1999), ‘GMM estimation with cross sectional dependence’, _Journal of Econometrics_ **92** (1), 1–45. 

- Council, T. C. M. & Board, T. C. P. (1895), The Medical and Pharmacy Register for the Colony of the Cape of Good Hope, Technical report, Johannesburg. 

44 

- Dahl, Ø. (2011), Linguistic policy challenges in Madagascar, _in_ C. Thornell & K. Leg`ere, eds, ‘North-South contributions to African languages’, Cologne, pp. 51–79. 

- Dennis, J. S., Beach, H. P. & Fahs, C. H. (1911), _World Atlas of Christian Missions: Containing a Directory of Missionary Societies, a Classified Summary of Statistics, and Index of Mission Stations, and Maps Showing the Location of Mission Stations Throughout the World_ , Student Volunteer Movement for Foreign Missions, New York. 

- Dippel, C. & Heblich, S. (2021), ‘Leadership in Social Movements: Evidence from the “FortyEighters” in the Civil War’, _American Economic Review_ **111** (2), 472–505. 

- Dutch Reformed Church of South Africa (1917), ‘Minutes of the Meeting of the Council of Missionaries for the Dutch Reformed Church’s Missionary Work in Tiviland from 25 to 29 January, 1917’, _KS1182_ . 

- Dutch Reformed Church of South Africa (1924), ‘Minutes of the Council Meeting of the Sudan Mission of the Dutch Reformed Church of South Africa held at Sevav from 9 to 19 April, 1924’, _KS1182_ . 

- Dutch Reformed Church of South Africa (1929), ‘Minutes of the Council Meeting of the Sudan Mission of the Dutch Reformed Church of South Africa held at Mkar 15 April 1929’, _KS1182_ . 

- Eriksson, K. (2014), ‘Does the language of instruction in primary school affect later labour market outcomes? Evidence from South Africa’, _Economic History of Developing Regions_ **29** (2), 311–335. 

   - **URL:** _http://dx.doi.org/10.1080/20780389.2014.955272_ 

- Fast, A. (2018), ‘Sacred children and colonial subsidies: The missionary performance of racial separation in Belgian Congo, 1946–1959’, _Missiology: An International Review_ **46** (2), 124– 136. 

- Food and Agricultural Organization of the United Nations (2024), ‘Global Agro-Ecological Zones’. 

**URL:** _https://gaez.fao.org/_ 

- Fourie, J., Ross, R. & Viljoen, R. (2014), ‘Literacy at South African Mission Stations’, _Journal of Southern African Studies_ **40** (4), 781–800. 

- Gardinier, D. E. (1991), ‘The American Presbyterian Mission in Gabon: Male Mpongwe Converts and Agents, 1870-1883’, _American Presbyterians_ **69** (1), 61–70. 

- Gathogo, J. M. (2020), ‘Settler-Missionary Alliance in Colonial Kenya and the Land Question’, _Studia Historiae Ecclesiasticae_ **46** (2). 

- Gilmore, E., Gleditsch, N. P., Lujala, P. & Rød, J. K. (2005), ‘Conflict diamonds: A new dataset’, _Conflict Management and Peace Science_ **22** (3), 257–272. 

45 

- Gordon, R. G. J., ed. (2005), _Ethnologue: Languages of the World, Fifteenth edition_ , SIL International, Dallas, Texas. 

- Greenwood, A. (2015), Introduction: Looking beyond the state, _in_ ‘Beyond the state: The colonial medical service in British Africa’, pp. 1–18. 

- Grimes, B. F., ed. (1996), _Ethnologue: Languages of the World, Thirteenth edition_ , SIL International, Dallas, Texas. 

- Grimes, B. F., ed. (2000), _Ethnologue: Languages of the World, Fourteenth edition_ , SIL International, Dallas, Texas. 

- Guinter, C. W. (1927), ‘The Pioneer Missionary and the Unwritten Language’, _The Lightbearer_ **23** (1), 92–93. 

- Gupta, A., Ponticelli, J. & Tesei, A. (2024), Language Barriers, Technology Adoption and Productivity: Evidence from Agriculture in India. 

- Hornung, E. (2014), ‘Immigration and the diffusion of technology: The huguenot diaspora in Prussia’, _American Economic Review_ **104** (1), 84–122. 

- Iliffe, J. (1998), _East African Doctors: A History of the Modern Profession_ , University of Cambridge. 

- Jedwab, R., Meier zu Selhausen, F. & Moradi, A. (2022), ‘The economics of missionary expansion: evidence from Africa and implications for development’, _Journal of Economic Growth_ **27** (2), 149–192. 

- Jedwab, R. & Moradi, A. (2016), ‘The permanent effects of transportation revolutions in poor countries: Evidence from Africa’, _Review of Economics and Statistics_ **98** (2), 268–284. 

- Juh´asz, R., Sakabe, S. & Weinstein, D. E. (2024), ‘Codification, Technology Absorption, and the Globalization of the Industrial Revolution’, _SSRN Electronic Journal_ . 

- Kanagasabai, U. (2024), The Health Care System in Liberia, Technical report. 

- Kelly, M. (2019), The Standard Errors of Persistence. 

- Kerwin, J. T. & Thornton, R. L. (2020 _a_ ), ‘Making the Grade: The Sensitivity of Education Program Effectiveness to Input Choices and Outcome Measures’, _Review of Economics and Statistics_ . 

- Kerwin, J. T. & Thornton, R. L. (2020 _b_ ), Making the Grade: The Sensitivity of Education Program Effectiveness to Input Choices and Outcome Measures. 

- Kimani, G. P. (2020), Contribution of the German Neukirchen Mission in the Establishment of Western Education in the Tana River County, Kenya 1885-1986, PhD thesis, Kenyatta University. 

46 

- Kiszewski, A., Mellinger, A., Spielman, A., Malaney, P., Sachs, S. E. & Sachs, J. (2004), ‘A global index representing the stability of malaria transmission’, _American Journal of Tropical Medicine and Hygiene_ **70** (5), 486–498. 

- Klein Goldewijk, K., Beusen, A., Van Drecht, G. & De Vos, M. (2011), ‘The HYDE 3.1 spatially explicit database of human-induced global land-use change over the past 12,000 years’, _Global Ecology and Biogeography_ **20** (1), 73–86. 

- Kouega, J.-P. & Alo’o, M. R. (2022), ‘Language Use in the Catholic Church in Cameroon: The Case of the French Service and the Bulu Service in a Parish of Sangmelima’, _European Journal of Language and Culture Studies_ **2** (6), 38–47. 

- Laitin, D. D. & Ramachandran, R. (2022), ‘Linguistic diversity, official language choice and human capital’, _Journal of Development Economics_ **156** (September 2020), 102811. 

- Laury, P. A. (1905), _A History of Lutheran mission_ , 2 edn, Pilger Publishing House, Perkasie, Pennsylvannia. 

- Law, R. (1996), Local Amateur Scholarship in the Construction of Yoruba Ethnicity, _in_ L. de la Gorgendiere, K. King & S. Vaughan, eds, ‘Ethnicity in Africa: Roots, Meanings and Implications’, Centre of African Studies, University of Edinburgh, pp. 55–90. 

- Leclerc, J. (1999), ‘L’Am´enagement Linguistique dans le Monde’. **URL:** _https://www.axl.cefan.ulaval.ca/_ 

- Lewis, L. J. (1962), _Phelps-Stokes Reports on Education in Africa_ , Oxford University Press, London. 

- Lewis, M. P., ed. (2009), _Ethnologue: Languages of the World, Sixteenth edition_ , SIL International, Dallas, Texas. 

- Lujala, P. (2009), ‘Deadly Combat over Natural Resources’, _Journal of Conflict Resolution_ **53** (1), 50–71. 

- Lujala, P., R¨od, J. K. & Thieme, N. (2007), ‘Fighting over oil: Introducing a new dataset’, _Conflict Management and Peace Science_ **24** (3), 239–256. 

- McCord, G. C. & Anttila-Hughes, J. K. (2017), ‘A malaria ecology index predicted spatial and temporal variation of malaria burden and efficacy of antimalarial interventions based on African serological data’, _American Journal of Tropical Medicine and Hygiene_ **96** (3), 616–623. 

- Moon, D. (n.d.), ‘Church, John Edward (1899-1989): Prominent leader of the East African Revival’. **URL:** _https://www.bu.edu/missiology/missionary-biography/c-d/church-john-edward1899-1989/_ 

- Moser, P., Voena, A. & Waldinger, F. (2014), ‘German Jewish ´emigr´es and US invention’, _American Economic Review_ **104** (10), 3222–3255. 

47 

- Nana, G. (2016), ‘Language Ideology and the Colonial Legacy in Cameroon Schools: A Historical Perspective’, _Journal of Education and Training Studies_ **4** (4), 168–196. 

- Nasim, L. M. R. (2023), _Medical Missionaries and Colonial Knowledge in West Africa and Europe, 1885-1914_ , Palgrave Macmillan, Basel, Switzerland. 

- Natural Earth (2024), ‘Free Vector and Raster Map Data’. **URL:** _https://www.naturalearthdata.com/_ 

- Nunn, N. (2010), ‘Religious conversion in Colonial Africa’, _American Economic Review: Papers and Proceedings_ **100** (2), 147–152. 

- Nunn, N. (2014), ‘Gender and missionary influence in Colonial Africa’, _Africa’s Development in Historical Perspective_ (February), 489–512. 

- Nunn, N. & Puga, D. (2012), ‘Ruggedness: The blessing of bad geography in Africa’, _Review of Economics and Statistics_ **94** (1), 20–36. 

- Nunn, N. & Wantchekon, L. (2011), ‘The slave trade and the origins of Mistrust in Africa’, _American Economic Review_ **101** (7), 3221–3252. 

- Okada da Silva, V., Romero, M. N., Stocker, A. & Thornton, R. (2023), Long-Lasting Effects of Exposure to Bible Translations : Evidence from Sub-Saharan Africa. 

- Pawlikova-Vilhanova, V. (2011), ‘The Role of Early ”Missionaries of Africa’ or ”White Fathers” in the Study and Development of African Languages’, _Asian and African Studies_ **20** (2), 267–288. 

- Posner, D. N. (2003), ‘The colonial origins of ethnic cleavages: The case of linguistic divisions in Zambia’, _Comparative Politics_ **35** (2), 127–146. 

- Ramachandran, R. (2017), ‘Language use in education and human capital formation: Evidence from the Ethiopian educational reform’, _World Development_ **98** , 195–213. 

- Ranger, T. (1989), Missionaries, Migrants and the Manyika: The Invention of Ethnicity in Zimbabwe, _in_ L. Vail, ed., ‘The Creation of Tribalism in Southern Africa’, University of California Press, pp. 118–146. 

- R´epublique Fran¸caise (1925), Rapport Annuel du Gouvernment Francais sur l’administration sous mandat des territoires du Cameroon pour l’annee 1924, Technical report, Paris. 

- R´epublique Fran¸caise (1927), Rapport Annuel du Gouvernment Francais sur l’administration sous mandat des territoires du Cameroon pour l’annee 1926, Technical report, Paris. 

- Roome, W. R. M. (1925), _Ethnographic Survey of Africa: Showing the Tribes and Languages; also the Stations of Missionary Societies_ , Edward Stanford Ltd., London. 

- Rosen, L. (2020), ‘Missionary Encounters: Moroccan Engagement with the Western Other’, _Hesperis-Tamuda_ **55** (2), 157–171. 

48 

- Rubin, J. (2014), ‘Printing and Protestants: An Empirical Test of the Role of Printing in the Reformation’, _The Review of Economics and Statistics_ **96** (2), 270–286. 

- Scalvedi, C. (2020), Cruce et Aratro: Fascism, Missionary Schools, and Labor in 1920s Italian Somalia, _in_ D. Matasci, M. B. Jeronimo & H. G. Dores, eds, ‘Education and Development in Colonial and Postcolonial Africa’, Springer Nature, pp. 143–171. 

- Seid, Y. (2016), ‘Does learning in mother tongue matter? Evidence from a natural experiment in Ethiopia’, _Economics of Education Review_ **55** , 21–38. 

- Seid, Y. (2019), ‘The impact of learning first in mother tongue: evidence from a natural experiment in Ethiopia’, _Applied Economics_ **51** (6), 577–593. 

- Seton, B. E. (1962), The Founding of Methodist Missions in South Africa, PhD thesis, University of Cape Town. 

- Sherk, F. L. (n.d.), ‘My Nigeria Experiences, 1906-1919’. 

- Smalley, W. A. (1991), _Translation as Mission: Bible Translation in the Modern Missionary Movement_ , Mercer University Press, Macon. 

- Sol´a, D. (2023), Brother votes for brother: The effects of Pentecostal political influence in Brazil. 

- Soremekun, F. (1971), ‘Religion and Politics in Angola: the American Board Missions and the Portuguese Government, 1880-1922.’, _Cahiers d’´etudes africaines_ **11** (43), 341–377. 

- Staiger, D. & Stock, J. H. (1997), ‘Instrumental Variables Regression with Weak Instruments’, _Econometrica_ **65** (3), 557. 

- Stock, J. H. & Yogo, M. (2005), Testing for Weak Instruments in Linear IV Regression. 

- Streit, K. (1906), _Katholischer Missionsatlas: Enthaltend die gesamten Missionsgebiete des Erdkreises_ . 

- Streit, K. (1913), _Atlas Hierarchicus: Descriptio geographica et statistica S. Romanae Ecclesiae tum Occidentis tum Orientis juxta statum praesentem_ . 

- Streit, K. (1929), _Atlas Hierarchicus: Descriptio geographica et statistica Sanctae Romanae Ecclesiae tum occidentis tum orientis juxta statum praesentum accedunt nonnullae notae historicae necnon ethnographicae, Paderbornae: sumptibus typographiae Bonifacianae_ . 

- Sun, L. & Abraham, S. (2021), ‘Estimating dynamic treatment effects in event studies with heterogeneous treatment effects’, _Journal of Econometrics_ **225** (2), 175–199. 

- Taylor, S. & von Fintel, M. (2016), ‘Estimating the impact of language of instruction in South African primary schools: A fixed effects approach’, _Economics of Education Review_ **50** , 75–89. 

49 

- Tembo, D. (2020), ‘Missionaries and the Standardisation of Vernacular Languages in Colonial Malawi, 1875-1935’, _The Society of Malawi Journal_ **73** (2), 1–17. 

- Tyrberg, A. (2014), Kyrka i Jubaland ?, PhD thesis, Uppsala University. 

- United Bible Societies (1972), _The Book of a Thousand Tongues_ , United Bible Societies. 

- Vail, L. (1989), _The Creation of Tribalism in Southern Africa_ , University of California Press. 

- Valencia Caicedo, F. (2019), ‘The Mission: Human Capital Transmission, Economic Persistence, and Culture in South America’, _Quarterly Journal of Economics_ pp. 507–556. 

- van den Bersselaar, D. (1997), ‘Creating ’ Union Ibo ’: Missionaries and the Igbo Language’, _Africa: Journal of the International African Institute_ **67** (2), 273–295. 

- Waldinger, M. (2017), ‘The long-run effects of missionary orders in Mexico’, _Journal of Development Economics_ **127** (December 2015), 355–378. 

- Woodberry, R. D. (2012), ‘The missionary roots of liberal democracy’, _American Political Science Review_ **106** (2), 244–274. 

- Wright, H. O. S. (1925), Colonial Reports Annual. No 1245. Nigeria, Technical Report 1245, London. 

   - **URL:** _ibsysdigi.library.illinois.edu/ilharvest/Africana/Books201105/3064634/3064634_ _~~1~~ 924/3064634_ _~~1~~ 924_ _~~o~~ pt.pdf_ 

50 

##### **Main Tables** 

51 

Table I: Exposure to Bible Translations 

|**Obs**|**Mean**|**SD.**|**Min.**|**p75**|**p90**|**p95**|**Max.**|
|---|---|---|---|---|---|---|---|
|_Panel A: Indigenous Language Permi_<br>**Linguistic Exposure Measures**<br>|_tted_|||||||
|Any Translation<br>652131|0.88|0.33|0|1|1|1|1|
|Year of First Translation<br>571960|1894.81|36.60|1530|1919|1947|1960|2006|
|Translated Verses<br>650501<br>|19874.98|13191.04|0|31102|31102|31102|31102|
|**Geographic Exposure Measures**||||||||
|Translation Sites<br>1171188|0.23|0.56|0|0|1|1|5|
|Translated Verses<br>1171188|1940.64|6675.42|0|0|4133|11813|65593|
|Languages Translated<br>1171188|0.21|0.50|0|0|1|1|5|
|_Panel B: Colonial Language Enforced_||||||||
|**Linguistic Exposure Measures**||||||||
|Any Translation<br>452664|0.86|0.35|0|1|1|1|1|
|Year of First Translation<br>387129|1929.51|54.28|1505|1967|1982|1997|2006|
|Translated Verses<br>452456|8100.84|10718.61|0|7957|31102|31102|31102|
|**Geographic Exposure Measures**||||||||
|Translation Sites<br>629609|0.15|0.48|0|0|1|1|4|
|Translated Verses<br>629609|1769.04|6542.82|0|0|1071|10418|39144|
|Languages Translated<br>629609|0.12|0.37|0|0|1|1|2|



Notes: This table reports summary statistics for linguistic and geographic exposure to Bible translation among DHS respondents. A person is linguistically exposed if there is a Bible translation in the language linked to their reported ethnicity. All Bible translations until 2006 are considered under this definition. Any translation refers to any translation started in a respondent’s ancestral language before 2007. Translated verses refers to the number of verses translated in a person’s ancestral language prior to 1969 using information from the _Book of a Thousand Tongues_ (United Bible Societies 1972). A person is geographically exposed if they are living within 25 kilometers of a Bible translation site. Only historical Bible translations started before 1930 are considered under this definition. Translation sites refers to the number of translation sites that can be found within 25 kilometers. Translated Verses under geographic exposure refers to the number of verses translated at those translation sites. Languages translated refers to the number of different languages translated at those translation sites. 

Table II: Determinants of Missions and Translation Sites 

||(1)|(2)|(3)|T-|test|
|---|---|---|---|---|---|
||No Mission|Mission, no Translation|Translation|Dife|rence|
|Variable|Mean/SE|Mean/SE|Mean/SE|(2)-(1)|(3)-(2)|
|_Geographical Characteristics_||||||
|Log Distance to Coast|5.607|4.921|4.765|-0.686***|-0.156**|
||(0.056)|(0.114)|(0.204)|||
|Log Distance to Capital|5.273|4.612|4.019|-0.661***|-0.593***|
||(0.036)|(0.091)|(0.171)|||
|Log Distance to Fresh Water|3.652|3.784|3.239|0.133*|-0.546***|
||(0.034)|(0.044)|(0.106)|||
|Suitability for Rainfed Crops|7.746|7.441|7.317|-0.306***|-0.124***|
||(0.025)|(0.045)|(0.082)|||
|Average Precipitation per Day|2.843|3.411|3.608|0.568***|0.197|
||(0.045)|(0.119)|(0.150)|||
|Growing Days per Year|209.920|236.711|264.566|26.792***|27.854|
||(2.751)|(3.789)|(6.763)|||
|Natural Resource|0.165|0.344|0.231|0.178***|-0.112***|
||(0.011)|(0.023)|(0.026)|||
|Malaria Ecology|15.151|10.701|11.813|-4.450|1.112|
||(0.287)|(0.519)|(0.896)|||
|Ruggedness|0.602|0.810|0.907|0.209**|0.097***|
||(0.021)|(0.037)|(0.075)|||
|_Historical Characteristics_||||||
|Log Population Density 1850|1.901<br>(0.037)|2.407<br>(0.063)|3.036<br>(0.091)|0.506***|0.628***|
|Log Distance to Colonial Railway|4.388|3.258|3.117|-1.130***|-0.141|
||(0.050)|(0.105)|(0.175)|||
|Log Distance to Explorer Route|4.547<br>(0.037)|4.715<br>(0.075)|4.628<br>(0.112)|0.168***|-0.087|
|Within 200KM of Muslim Center|0.165|0.088|0.142|-0.078|0.055*|
||(0.010)|(0.012)|(0.033)|||
|_Mission Characteristics_||||||
|Year of First Protestant Mission|N/A|1897.282<br>(0.965)|1883.725<br>(3.030)|N/A|-13.558***|
|N|28291|12471|7246|||
|Clusters|2753|1428|693|||



Notes: The table compares geographical, historical and missionary characteristics in 25 kilometer buffers around DHS clusters for which there are (1) no Protestant missions, (2) a Protestant mission but no Bible translations and (3) both a Protestant mission and a Bible translation. In the last two columns, I report t-test differences with country fixed effects and standard errors clustered at the second administrative level of region (often districts). All missing values in balance variables are assigned the group mean. 

53 

###### Table III: Conditional Balance of Translation Sites 

||Indigenou|s Language|Permitted|Colonial|Language E|nforced|
|---|---|---|---|---|---|---|
||Variable<br>Mean<br>(1)|Translation<br>Coefcient<br>(2)|p-value<br>(3)|Variable<br>Mean<br>(4)|Translation<br>Coefcient<br>(5)|p-value<br>(6)|
|_Geographic Characteristics_|||||||
|Log Distance to Coast|5.53|0.18|(0.15)|4.84|-0.50|(0.25)|
|Log Distance to Capital|4.90|0.14|(0.43)|4.93|-1.14|(0.02)**|
|Log Distance to Fresh Water|3.62|-0.21|(0.04)**|3.62|-0.50|(0.20)|
|Suitability for Rainfed Crops|7.61|-0.01|(0.92)|7.59|-0.62|(0.28)|
|Average Precipitation per Day|3.28|0.08|(0.36)|2.75|-0.36|(0.28)|
|Growing Days per Year|242.62|5.42|(0.25)|189.08|1.69|(0.87)|
|Natural Resource|0.23|-0.05|(0.23)|0.20|0.12|(0.46)|
|Malaria Ecology|10.95|-0.54|(0.34)|18.72|-3.39|(0.01)**|
|Ruggedness|0.84|0.16|(0.03)**|0.42|0.14|(0.31)|
|_Historical Characteristics_|||||||
|Log Population Density 1850|2.35|0.02|(0.81)|1.91|1.07|(0.08)*|
|Log Distance to Colonial Railway|3.75|0.34|(0.01)**|4.21|-0.87|(0.02)**|
|Log Distance to Explorer Route|4.52|0.03|(0.72)|4.78|0.24|(0.34)|
|Within 200KM of Muslim Center|0.12|0.01|(0.83)|0.19|0.11|(0.12)|



Notes: Each coefficient in columns (2), and (5) come from separate regressions that include country fixed effects, controls for presence of a Catholic or a Protestant mission within 25 kilometer radius and a set of indicator variables for the year of first established Protestant mission in 25 year blocks starting in 1805 and ending in 1930. The unit of observation is the DHS cluster. Columns (3), and (6) report the p-values for the regressions shown in columns (2), and (5) respectively. Standard * ** errors are two-way clustered at the second administrative regional level and 0.5 by 0.5 degree cell. _p <_ 0 _._ 10, _p <_ 0 _._ 05, *** _p <_ 0 _._ 01 

Table IV: Bible Translations and Missionary Growth 

||All<br>(1)|Translating<br>Society<br>(2)|Other<br>Societies<br>(3)|Translation<br>Site<br>(4)|Other<br>Stations<br>(5)|Same<br>Language<br>Polygon<br>(6)|Other<br>Language<br>Polygons<br>(7)|Mission<br>Stations<br>(8)|Exit<br>(9)|Doctors<br>(10)|
|---|---|---|---|---|---|---|---|---|---|---|
|**Panel A: Full Sa**|**mple**||||||||||
|Translation * Post|2.97***|2.72***|0.25|1.59***|1.39***|2.93***|0.04|0.34***|-0.13***|0.19***|
||(0.64)|(0.52)|(0.40)|(0.38)|(0.50)|(0.62)|(0.07)|(0.12)|(0.04)|(0.07)|
|Observations|1,072|1,072|1,072|1,072|1,072|1,072|1,072|1,072|1,072|804|
|Mean Dep. Var.|4.14|3.35|0.78|2.69|1.45|4.04|0.10|0.95|0.39|0.18|
|**Panel B: Indigen**|**ous Lang**|**uage Permit**|**ted**||||||||
|Translation * Post|2.63***|2.53***|0.10|1.51***|1.12**|2.58***|0.05|0.28**|-0.11**|0.20***|
||(0.70)|(0.57)|(0.45)|(0.43)|(0.53)|(0.68)|(0.08)|(0.12)|(0.05)|(0.08)|
|Observations|920|920|920|920|920|920|920|920|920|690|
|Mean Dep. Var.|4.26|3.43|0.82|2.76|1.50|4.14|0.11|0.96|0.38|0.19|
|**Panel C: Colonia**|**l Langua**|**ge Enforced**|||||||||
|Translation * Post|5.09***|3.92***|1.18|2.09**|3.00*|5.09***|0.00|0.73**|-0.22*|0.16|
||(1.58)|(1.32)|(0.81)|(0.86)|(1.51)|(1.58)|(.)|(0.35)|(0.12)|(0.12)|
|Observations|152|152|152|152|152|152|152|152|152|114|
|Mean Dep. Var.|3.41|2.85|0.56|2.26|1.15|3.41|0.00|0.86|0.39|0.13|



Notes: This table displays results for the effects of Bible translation on number of foreign missionaries within a 25 kilometer radius. Only missions for which there are no earlier Bible translations within 50 kilometers, information on year of establishment is available, and that are located in Sub-Saharan Africa are sampled. Missions with translation (treatment) are matched one-to-one with stations without translation (control) using propensity score matching. Control missions must further be the first established station in a given town. Mission stations must first both be the first station established in a 25 kilometer radius or not. They must also belong to the same 5-year block for year of establishment and finally they must both be in an indigenous-language-permitted (ILP) or colonial-language-enforced (CLE) country. Propensity score is then computed on a set of LASSO-selected variable among the following set: log distances to the capital, to the coast, to a fresh water source, to explorer routes, to colonial railways as well as average malaria ecology, daily precipitation, average crop suitability, ruggedness, log of population density in 1850, presence of natural resources (gold, diamond, gems, or oil) and finally being within 200 kilometers of a Muslim center. In assigning treatment dates, I allow for a 3 year publication delay. No controls are used. Standard errors are clustered at the mission station level and shown in parentheses. * _p <_ 0 _._ 10, ** _p <_ 0 _._ 05, *** _p <_ 0 _._ 01 

Table V: Bible Translations and Missionary Infrastructure in 1900 

|||**Religiou**|**s**||**E**|**ducation**|**al**|**H**|**ealth**|
|---|---|---|---|---|---|---|---|---|---|
||Bible<br>Rooms<br>(1)|Log of<br>Chapels<br>(2)|Log of<br>Church<br>Members<br>(3)|Printing<br>Presses<br>(4)|Log of<br>Primary<br>Schools<br>(5)|High<br>Schools<br>(6)|Colleges<br>(7)|Hospitals<br>(8)|Dispensaries<br>(9)|
|**Panel A: All Cou**|**ntries**|||||||||
|Translation * Post|0.07|0.03|0.84**|0.15**|0.43*|0.34**|0.03|0.18**|0.40**|
||(0.07)|(0.17)|(0.42)|(0.07)|(0.22)|(0.15)|(0.04)|(0.09)|(0.15)|
|Observations|302|302|302|302|302|302|302|302|302|
|Mean Dep. Var.|0.05|0.41|1.96|0.07|0.64|0.18|0.02|0.07|0.19|
|**Panel B: Indigeno**|**us Lan**|**guage Per**|**mitted**|||||||
|Translation * Post|0.09|0.15|1.21***|0.18**|0.58***|0.33**|0.04|0.23**|0.51***|
||(0.07)|(0.17)|(0.44)|(0.08)|(0.21)|(0.17)|(0.04)|(0.10)|(0.17)|
|Observations|266|266|266|266|266|266|266|266|266|
|Mean Dep. Var.|0.04|0.39|1.93|0.07|0.64|0.18|0.02|0.08|0.19|
|**Panel C: Colonial**|**Langua**|**ge Enfor**|**ced**|||||||
|Translation * Post|0.00|-0.73|-1.54|0.00|-0.56|0.42|0.00|-0.12|-0.35*|
||(0.32)|(0.59)|(0.92)|(0.00)|(0.99)|(0.38)|(.)|(0.12)|(0.19)|
|Observations|36|36|36|36|36|36|36|36|36|
|Mean Dep. Var.|0.11|0.52|2.25|0.06|0.64|0.17|0.00|0.03|0.19|



Notes: This table displays results for the effects of Bible translation on missionary infrastructure within a 25 kilometer radius. Only missions for which there are no earlier Bible translations within 50 kilometers, information on year of establishment is available, and that are located in Sub-Saharan Africa are sampled. Missions with translation (treatment) are matched one-to-one with stations without translation (control) using propensity score matching. Control missions must further be the first established station in a given town. Mission stations must first both be the first station established in a 25 kilometer radius or not. They must also belong to the same 5-year block for year of establishment and finally they must both be in an indigenous-language-permitted (ILP) or colonial-language-enforced (CLE) country. Propensity score is then computed on a set of LASSO-selected variable among the following set: log distances to the capital, to the coast, to a fresh water source, to explorer routes, to colonial railways as well as average malaria ecology, daily precipitation, average crop suitability, ruggedness, log of population density in 1850, presence of natural resources (gold, diamond, gems, or oil) and finally being within 200 kilometers of a Muslim center. In assigning treatment dates, I allow for a 3 year publication delay. No controls are used. Standard errors are clustered at the mission station level and shown in parentheses. * _p <_ 0 _._ 10, ** _p <_ 0 _._ 05, *** _p <_ 0 _._ 01 

Table VI: Bible Translations and Infrastructure in 2024 

|Any University<br>(1)|Any School<br>(2)|Any Hospital<br>(3)|
|---|---|---|
|**Panel A: Full Sample**|||
|Translation Site<br>0.0849**<br>(0.0346)|0.0139<br>(0.0394)|0.1047**<br>(0.0416)|
|Observations<br>1,563|1,563|1,563|
|Mean Dep. Var.<br>0.1779|0.5099|0.3615|
|**Panel B: Indigenous Language **|**Permitted**||
|Translation Site<br>0.0734*<br>(0.0380)|0.0119<br>(0.0430)|0.1039**<br>(0.0457)|
|Observations<br>1,385|1,385|1,385|
|Mean Dep. Var<br>0.1718|0.5220|0.3567|
|**Panel C: Colonial Language E**|**nforced**||
|Translation Site<br>0.1000<br>(0.0826)|-0.0292<br>(0.1152)|-0.0418<br>(0.0987)|
|Observations<br>178|178|178|
|Mean Dep. Var.<br>0.2247|0.4157|0.3989|



Notes: This table displays results for the effects of Bible translation on the presence of various infrastructure in the year 2024. The unit of observation is the Protestant mission station. Data on 2024 infrastructure comes from Open Street Map which provides the geographic location of buildings of various types including universities, schools, and hospitals. Outcome variables are indicator variables for whether any of that type of building is found within 25 kilometers of the mission station. All regressions include a set of geographical and historical controls as shown in Table II. They also include controls for the year the mission was established in 25 year blocks starting in 1805. Standard errors are two-way clustered at the second administrative regional level and * ** *** 0.5 by 0.5 decimal degree cell. _p <_ 0 _._ 10, _p <_ 0 _._ 05, _p <_ 0 _._ 01 

57 

Table VII: Bible Translation and Use of Vernacular as Medium of Instruction in 1960 

||Medium of<br>Instruction (0/1)<br>(1)|Medium of<br>Instruction (Grades)<br>(2)|
|---|---|---|
|**Panel A: All Countries**|||
|Any Translated Verses 1960|0.072***<br>(0.021)|0.213***<br>(0.064)|
|Observations|2,671|2,671|
|Mean without Translation|0.006|0.016|
|**Panel B: Indigenous Lang**<br>Any Translated Verses 1960|**uage Permitted**<br>0.111***<br>(0.027)|0.329***<br>(0.082)|
|Observations|1,728|1,728|
|Mean without Translation|0.008|0.023|
|**Panel C: Colonial Langua**|**ge Enforced**||
|Any Translated Verses 1960|0.001<br>(0.001)|0.002<br>(0.002)|
|Observations|942|942|
|Mean without Translation|0.001|0.003|



Notes: This table displays the effects of a vernacular African language being translated into the Bible on its use as a medium of instruction in schools. The unit of observation is the language-country pair. All specifications include country fixed effects as well as a series of dummy variables for the number of countries in which the language is spoken. Standard errors are two-way clustered at the language and coun* ** *** try level. _p <_ 0 _._ 10, _p <_ 0 _._ 05, _p <_ 0 _._ 01 

58 

###### Table VIII: Bible Translations and Years of Schooling 

|Dependent||Ye|ars||Translation|Years|
|---|---|---|---|---|---|---|
|Variable:||Scho|oling||Site|Schooling|
||OLS<br>(1)|OLS<br>(2)|OLS<br>(3)|OLS<br>(4)|OLS<br>(5)|2SLS<br>(6)|
|**Panel A: Indigenous Langua**|**ge Permit**|**ted**|||||
|Translation Site|1.035***<br>(0.115)|0.506***<br>(0.085)|0.291***<br>(0.093)|0.205**<br>(0.101)||1.765***<br>(0.469)|
|Protestant Mission|||0.448***<br>(0.071)||||
|Catholic Mission|||0.083<br>(0.078)||||
|Log Proclivity of First Society|||||0.048***<br>(0.007)||
|Observations<br>Mean Dep. Var.<br>First Stage F-stat|1,138,944<br>6.340|1,138,361<br>6.340|1,138,361<br>6.340|1,138,361<br>6.340|1,138,361<br>0.179|1,138,361<br>6.340<br>45.326|
|**Panel B: Colonial Language **<br>Translation Site|**Enforced**<br>1.105***<br>(0.210)|-0.115<br>(0.186)|-0.403**<br>(0.183)|-0.458***<br>(0.146)||-0.093<br>(0.385)|
|Protestant Mission|||0.272**<br>(0.113)||||
|Catholic Mission|||0.522***<br>(0.112)||||
|Log Proclivity of First Society|||||0.088***<br>(0.017)||
|Observations|620,426|620,426|620,426|620,426|620,426|620,426|
|Mean Dep. Var.|3.368|3.368|3.368|3.368|0.111|3.368|
|Country by Round FE|Yes|Yes|Yes|Yes|Yes|Yes|
|Individual Controls|Yes|Yes|Yes|Yes|Yes|Yes|
|Geographic Controls|No|Yes|Yes|Yes|Yes|Yes|
|Historical Controls|No|Yes|Yes|Yes|Yes|Yes|
|Mission by Year Controls|No|No|No|Yes|Yes|Yes|
|First Stage F-stat||||||25.924|



Notes: This table displays results of the effects of being proximate to a historical Bible translation on years of schooling. Individual controls include age, age squared, gender, and urban status. Geographical and historical controls are as shown in II. Mission by year controls consist of the presence of a Catholic mission within 25 kilometers and indicator variables for Protestant missions established in 25 year blocks beginning in 1805 and ending in 1930 for a total of 5 blocks. Standard errors are two-way clustered at the second administrative level and 0.5 decimal degree grid-cell. * _p <_ 0 _._ 10, ** _p <_ 0 _._ 05, *** _p <_ 0 _._ 01 

59 

###### Table IX: Bible Translations and Body Mass Index 

|Dependent||Body|Mass||Translation|Body Mass|
|---|---|---|---|---|---|---|
|Variable:||Ind|ex||Site|Index|
||OLS<br>(1)|OLS<br>(2)|OLS<br>(3)|OLS<br>(4)|OLS<br>(5)|2SLS<br>(6)|
|**Panel A: Indigenous Langua**|**ge Permit**|**ted**|||||
|Translation Site|0.336***|0.154***|0.103**|0.112***||0.358*|
||(0.048)|(0.038)|(0.041)|(0.041)||(0.191)|
|Protestant Mission|||0.089***<br>(0.031)||||
|Catholic Mission|||0.074**<br>(0.036)||||
|Log Proclivity of First Society|||||0.048***<br>(0.007)||
|Observations|447,080|446,893|446,893|446,893|446,893|446,893|
|Mean Dep. Var.|6.060|6.060|22.029|22.029|0.175|22.029|
|First Stage F-stat||||||45.633|
|**Panel B: Colonial Language **|**Enforced**||||||
|Translation Site|0.356***|0.028|-0.163|-0.098||0.082|
||(0.077)|(0.098)|(0.132)|(0.121)||(0.226)|
|Protestant Mission|||0.281**<br>(0.113)||||
|Catholic Mission|||-0.019<br>(0.059)||||
|Log Proclivity of First Society|||||0.102***<br>(0.018)||
|Observations|189,591|189,591|189,591|189,591|189,591|189,591|
|Mean Dep. Var.|2.697|2.697|21.652|21.652|0.109|21.652|
|Country by Round FE|Yes|Yes|Yes|Yes|Yes|Yes|
|Individual Controls|Yes|Yes|Yes|Yes|Yes|Yes|
|Geographic Controls|No|Yes|Yes|Yes|Yes|Yes|
|Historical Controls|No|Yes|Yes|Yes|Yes|Yes|
|Mission by Year Controls|No|No|No|Yes|Yes|Yes|
|First Stage F-stat||||||31.713|



Notes: This table displays results of the effects of being proximate to a historical Bible translation on body mass index. Individual controls include age, age squared, gender, and urban status. Geographical and historical controls are as shown in II. Mission by year controls consist of the presence of a Catholic mission within 25 kilometers and indicator variables for Protestant missions established in 25 year blocks beginning in 1805 and ending in 1930 for a total of 5 blocks. Standard errors are two-way clustered at the second administrative level and 0.5 decimal degree grid-cell. * _p <_ 0 _._ 10, ** _p <_ 0 _._ 05, *** _p <_ 0 _._ 01 

60 



<!-- Start of picture text -->
400 1<br>—— Languages<br>—— Cumulative Density<br>8<br>300<br>2<br>2<br>o3 6 la<br>2,c 200 2®o<br>S &<br>42<br>=]<br>oO<br>100<br>2<br>0 0<br>1800 1825 1850 1875 1900 1925 1950 1975 2000<br>Year<br><!-- End of picture text -->

- awa 

- ATES ae 

- _ rae wn rae wn wn so 

- _ Bee 



<!-- Start of picture text -->
ATES<br>ae<br>_ rae wn rae wn wn so<br>_ Bee<br><!-- End of picture text -->



<!-- Start of picture text -->
30<br>& 207. ae oe : ps me a : : ae ae oe oe<br>&<br>lo 1<br>N;<br>£<br>‘5 @ All<br>® 10 M CLE<br>2 A ILP<br>re i<br>ue ;<br>€ 0 -—— — — -@mA. + asain [aneeeieetianeieesienialiensleeeiesie t h elieeientientionta<br>Bol at om A td<br>-10 i<br>ass<br>-4 -3 -2 -1 0 1 2 3 4 5<br>Periods since Translation Publication<br><!-- End of picture text -->



<!-- Start of picture text -->
20 |<br>&<br>8<br>3 0 - —+H- -oma-+ | ——-4—-—-@. ——.g--—-|---+-- @mcLEAll<br>Z | A ILP<br>><br>ss<br>-4 a<br>[24,22] [21,19] [18,16] [15,13] [12,10] [9,7] [6,4] [3,1]  [0,-2] [-3,-5]  [-6,-8]<br>Age at Publication<br><!-- End of picture text -->

##### **A Data Appendix** 

###### **A.1 Missionary Atlases** 

In this paper, I digitize four Protestant missionary atlases (Beach 1903; Dennis et al. 1911; Beach & St. John 1916; Beach & Fahs 1925) and two Catholic missionary atlases (Streit 1913; Streit 1929). The Protestant missionary atlases were compiled by mission scholars from reports provided by missionary societies on their activities. They largely represent missionary activity for the years 1900 (Beach 1903), 1908 (Dennis et al. 1911), 1915 (Beach & St. John 1916), and 1922 (Beach & Fahs 1925)<sup>1</sup> . With the exception of Beach (1903), they only report on mission stations where a foreign missionary is stationed. Thus, if there are outstations where only national staff are stationed then they would not be included. For this paper, I digitize all information available at the mission station level. This includes information on the operating missionary society, the year of establishment and the number of foreign missionaries separately for men, married women, unmarried women as well as doctors. Beach (1903) also includes information on a whole set of missionary investments including schools, hospitals, printing presses, etc. However, I do not include information available at higher levels of aggregation. For example, in later atlases they might include the number of school pupils aggregated among all mission stations belonging to a certain society for each country. Some of these missionary atlases have been previously digitized by various authors as shown in A1. However, I re-digitize all of them for a few reasons. First, previous efforts focused on a specific area such as India or Africa. I re-digitize them for the entire world. Second, previous efforts missed some important information. For example, Cag´e & Rueda (2016)’s digitization of Beach (1903) omits all stations that are not mapped within the atlas. Instead, I can locate them by linking them to mapped entries in subsequent editions or through missionary reports and secondary sources. Moreover, in their publicly available version, they also aggregate all mission information at the town level when there are multiple missionary societies operating 

> 1For passages in evidence of these dates, for Beach (1903), see the preface. For Dennis et al. (1911), see page 13. For Beach & St. John (1916), see page 107. For Beach & Fahs (1925), see page 12. 

65 

in the same town. I list observations at the mission station level which is a town-missionary society pair. Third, by re-digitizing, I can more easily link mission stations across editions, which has not previously been done. As for Catholic missionary atlases, they represent the two editions of the _Atlas Hierchicus_ authored by Carolus Streit. He also authored the _Katholischer Missionsatlas_ (Streit 1906) which I do not digitize here. The two atlases that I do digitize are similarly compiled from missionary reports but for ”the present date”, meaning no exact year is given though the year is likely in close proximity to the year of publication. These atlases map out places of missionary residence but do not clarify whether that includes only foreign missionaries, though that is presumably the case. At the missionlevel, they do not include information on the number of missionaries working but they do provide information on characteristics of the mission, including the population of the town and the presence of various infrastructure such as hospitals, colleges, etc. They do provide information, however, on the numbers of missionaries at the missionary district level. For this paper, I did not digitize this information. The 1929 edition has already been digitized by Cag´e & Rueda (2020) but in their digitization they didn’t include the operating missionary society, which I include in my digitization. I also link the missions across editions and digitize for all of Africa, Asia and Oceania whereas Cag´e & Rueda (2020) focus solely on Africa. 

###### **A.1.1 Digitizing Protestant Missionary Atlases** 

In digitizing these documents, I strive to include as much information as possible from the atlas and maximize the precision of geocoordinates. I begin with Beach & Fahs (1925) as it includes the greatest number of missions and would have had the most precision mapping given its later date. 

**Optical Character Recognition:** To begin, I conduct optical character recognition (OCR) on indices of Protestant missions as well as lists of missionary societies. Once complete, I manually corrected any mistakes in the scanned text so that it would match the atlases. To do this, I created several flags that would indicate a typo or misprint. For 

66 

example, mission listings followed very precise punctuation which could be checked. From the cleaned text, I could separate out information on the town, the operating society, the number of staff, etc. 

**Geo-coordinates:** To provide geo-coordinates, I first measure the position of each mission station in a physical atlas up to the half millimeter. Comparing that with the measured length and width of the square, I calculate up to a high degree of precision the implied coordinates of the mission on the map. However, implied coordinates from maps dating back to the early 20th century could lack precision especially on a continent like Africa. To address this, I then search for towns of that name in OpenStreetMap in a 2 by 2 decimal degree (approximately 222 kilometers) centered on the implied coordinates. I then assign the actual coordinates of that mission station to the closest town to the implied map coordinates. Given the possibility of town names changing over time or being misspelled, it is possible the closest town of the same name may not actually be the intended mission station. To address this, I flag all produced geo-coordinates of towns that were more than 60 kilometers from the map coordinates<sup>2</sup> . I validate each one of these manually. 

I also manually enter coordinates for all mission stations for which no town is returned within the 2 by 2 degree box. Often this is due to changes in spelling. For example, there is a mission station listed as Nyangkundi in Beach & Fahs (1925) but the town is now spelled Niakunde. 

I also provide geo-coordinates for un-mapped missions. For earlier editions, this is often done through the linking process described in the next section. But I also do this manually for un-linked missions. For example, for Kambui mission station, Beach & Fahs (1925) provides the following: “Not on map; about 6 miles north-west of Kiambu (not underscored).” Then I find Kambui Girls High School on Google Maps in the approximate location indicated in the atlas and assign that as the geo-coordinates for the Kambui mission station. 

> 2There is no specific reason why 60 kilometers is the cutoff except that that’s where I stopped. I started with a cutoff of 100 kilometers and then gradually checked shortened the cutoff in order to validate a greater set of coordinates. 

67 

**Linking across editions:** Many missions operated over many years and are listed in multiple editions of the atlases. To link across editions, I first have to link missionary society abbreviations across editions. For example, in the 1903 and 1911 editions, there is the American Baptist Mission Union (ABMU). However, in the 1916 and 1925 editions, they become the American Baptist Foreign Missionary Society (ABF). In reporting missionary society names and abbreviations, I use the latest edition in which they are present. Then I link missions to other editions using the grid square, which provides the range of possible coordinates, and all mission stations from the other editions whose actual coordinates fall within that square. I create a link if there is geographical match in this way as well as a match on mission name and missionary society. I then manually search for links among unlinked stations to address for the use of alternate names or changes in spelling. For example, the 1903, 1911, and 1916 editions use Cantonese romanization of Chinese names (e.g. “chau”) whereas the 1925 edition uses the Wade-Giles system (“chow”). In order to create the links, I change the name of earlier editions to match the name provided in the later edition and then re-run the matching algorithm. 

Having extracted information on society, staff, etc., then geo-located and linked across editions, I have finished digitization of the Protestant missionary atlases. 

###### **A.1.2 Digitizing Catholic Missionary Atlases** 

As of the writing of this paper, I have only digitized these atlases for Africa, Oceania and Asia. North and South American missions remain to be digitized. 

**Extracting Information:** In the Streit Catholic missionary atlases, all mission-level information is included within the maps. That is, there is no additional index for each mission station as in the case of the Protestant missionary atlases. Thus, I extract all information on each mission station directly and manually from the maps. The information includes the population of the town, its position in the Catholic hierarchy, and the presence of seminaries, high schools, etc. Regions of each map were shaded in different colors to 

68 

represent the different missionary districts where a single missionary society would operate. 

**Geo-coordinates:** I establish geo-coordinates for Catholic mission stations in the same way as for Protestant mission stations described above. However, without separate indices for each mission station, there are no un-mapped mission stations in need of geo-location. 

**Linking across editions:** All linking is done manually but in general is much more straightforward given the territorial separation of Catholic missionary societies. By comparison, dozens of Protestant missionary societies could be operating in the same town. 

###### **A.2 Bible Translations** 

In accumulating information, I focus only on original translations into each language and leave out any information on revisions of those translations. The main reason for that is that my two main sources, United Bible Societies (1972) and the _Ethnologue_ , do so. They do so because keeping track of all the myriad Bible revisions in each language becomes an unachievable task. I do, however, include all original translations into dialects that were later considered to be the same language. For example, Fante is later considered to be a dialect of Akan but received its own Bible translation starting in 1877. 

###### **A.2.1 Compiling Information on Bible Translations** 

I compile information on Bible translations from two main sources: the _Book of a Thousand Tongues_ (United Bible Societies 1972) and editions 13 through 16 of the _Ethnologue_ ((Grimes 1996; Grimes 2000; Gordon 2005; Lewis 2009). The former provides detailed information on the original translation of each book of the Bible for each language until 1968. An excerpt of the book is shown in A1. For each translated book of the Bible, it includes information on the year of publication, the publishing institution, who the translators were, which missionary society they belonged to if any, the type of script used for writing and even the printing location in some cases. It also provides a small passage from the translation for each language, usually the Gospel of Mark, chapter 1, verses 1 through 4. From this I 

69 

extracted manually the year of publication for each book. For example, in my spreadsheet, the Bemba entry is coded as follows: 

”1904: John; 1906: Mark; 1910: Ephesians, 1John-3John; 1911: Gospels; 1913: Acts; 1914: Philemon, Jude; 1916: NT, Psalms; 1942: Genesis; 1943: Isaiah; 1956: Bible”. 

From this, and information on the number of verses in each book of the Bible (which remains constant across languages), I have the number of translated verses per year until 1968. 

In order to extend this data temporally, I make use of editions of the _Ethnologue_ . It is a compendium of world languages which contains information on the year of first publication of each of the following: Bible portions, full New Testament and full Bible. I gather data from four different editions, given that information may be lacking from any specific one. It does not provide information, however, on which books were translated at what times, meaning that I cannot know with precision how many verses are translated at any given time. Nevertheless, it extends the temporal data on the very first publication in a given language until 2007. 

###### **A.2.2 Constructing Site of Translation Data** 

In constructing the site of translation data, I rely heavily on the fact that the vast majority of early translators are missionaries stationed at specific stations. Thus, the site of translation is the mission where the translators were stationed at the time of translation. Multiple missionary translators from the same missionary society could be involved in the translation, while multiple missionary societies could also contribute. In order to make the data tractable, I allow for only one translation site per missionary society. This implies that even if translators from the same missionary society are stationed at different missions, I allocate the translation site to a single one. I do this for a few main reasons. First, the _Book of a Thousand Tongues_ lists entries by publisher, not by book or translator, making it infeasible to allocate specific books to specific translators. Second, even if multiple translators 

70 

are involved, there is often one who is considered to be the primary one due to being the first or taking on the bulk of the translation. Finally, from a data feasibility perspective, information on the location all missionaries at different times is difficult to obtain for many missionary societies. Primary translators tended to be more well known, making them easier to track over time. 

Thus, I start by making a list of missionary translators from the _Book of a Thousand Tongues_ , separated out by society. I then search for biographical information on each of the missionary translators. Some missionary societies keep detailed records of the location of all their staff for every year, while others provide very little information. For the latter, I supplement that information with secondary sources. Below is the excerpt from my spreadsheet on the location of translators of Bemba which corresponds to the excerpt shown in A1. 

-  “1000T, p.40: First book (John) translated by Daniel Crawford of the Garenganze mission; 2 books and parts of another translated by Henry Nutter, William Freshwater and Ernest Lewis of the London Missionary Society, the Gospels completed by Dugald Cambell of Garenganze, the NT finished by Nutter, Freshwater and Lewis of the LMS; in 1929 the White Fathers begin a translation afresh of Bemba with 3 books by 1934, 5 by 1948, and the rest of the New Testament by 1957 

-  Assessment: I’m putting LMS as primary society here given that they translated early on and did most of the translation for the New Testament; Daniel Crawford was also translating the Sango language among that group instead 

-  Musambachime, 1994, “The Ubutwa Society in Eastern Shaba and Northeast Zambia to 1920”, p.90, 97: William Freshwater provides annual reports of the Mbereshi Mission for 1914 and 1924 

-  Musambachime, 1987, ‘Northern Rhodesia Tax Stamps as an Aid to Chronology” in History in Africa, p.368: Freshwater reports from Mbereshi in 1904 

71 

-  https://library.soas.ac.uk/Record/CWM.LMS.12/HierarchyTree?recordID=CWM.LMS.12 : A report by Ernest Lewis from Mbereshi 

-  Musambachime, 1994, p.92: Dugald Campbell is placed at Mambilima 

-  Wiki (Mambilima Falls): Mambilima Falls were previously known as Johnstone Falls which is a mission run by the CMML in Beach 1925 

-  DACB (William Lammond): Another missionary of the CMML who did some translation of the Bible was stationed at Mambilima which the article makes clear was called Johnston Falls and was established in 1898” 

From this, I code there as being two translation sites: one at Mbereshi and another at Johnston Falls (Mambilima). Two of the three missionary translators from the London Missionary Society are stationed at Mbereshi while I could not find information on the location of the third. Both missionary translators from the Garenganze Mission (later part of the Christian Missions in Many Lands, or CMML) are stationed at Johnston Falls. Note that whenever possible I try finding information on location at the time of translation and not just at any time given that missionaries could move from station to station over the course of their career. So, while I first find information that William Freshwater is stationed at Mbereshi in 1914 and 1924, by searching further I learn that he is also stationed there in 1904. This is important considering his first publication of a Bible book is completed in 1906. One can also note that I put an emphasis on determining which missionary society could be considered the primary one among them. I did not follow a hard and fast rule for this but I weighed who translated first and how much they translated. In the end, however, I did not use this distinction in any of the analysis for the paper. 

I repeat this process for the 258 African languages with a translation started before 1930. I include translations which involved only very small amounts of translation, as well as translations into what later came to be considered dialects, in order to avoid selection bias into the data. One great aid in locating the site of translation for each language was the map 

72 

of missionary stations for each society that I had already created (described in the previous section). Instead of conducting broad searches for sources referring to each translator, I could search for them in combination with the mission stations of their missionary society located within or near the language polygon of the language they were translating. Thus, I could Google search: “‘William Freshwater’ ‘Mbereshi’” or “ ‘William Freshwater’ ‘Mporokoso’” (another nearby London Missionary Society station in the area) instead of just “William Freshwater”. Once I have linked Bible translations to mission stations, I assign verses to each site based on which books it translated. For example, at the Mbereshi mission, the London Missionary Society (LMS) were responsible for the original translation of all New Testament books except for the Gospels of Matthew, Luke, and John which were done by the Christian Missions in Many Lands (CMML). They also translated the book of Psalms from the Old Testament. Thus, I assign 7317 verses to the LMS at Mbereshi<sup>3</sup> and 3101 to the CMML at Johnston Falls. When it seems there are multiple societies involved in the translation of the same Bible books, I first looked for further information which could decipher which societies were responsible for which books. However, if they had formed committee or if I could not find any such information, I allocate the number of verses for each book translated in common equally across all participating societies. 

###### **A.3 Colonial Policy towards Missionaries** 

In this subsection, I provide the evidence that allows me to assign to each country a policy stance on four policies: (1) whether indigenous languaes were permitted as media of instruction in schools, (2) the subsidization of Protestant mission schools, (3) whether medical missionaries with foreign credentials (i.e. not from the same country as the colonizer) and (4) whether missionary societies have the legal right to hold land. I omit discussion of the fourth policy in the text as it is more tangential to education and health outcomes. Table 

3There are 7957 verses in the New Testament then subtract 1071, 1151, and 879 for the books of Matthew, Luke, and John respectively and finally adding 2461 for the book of Psalms. 

73 

A2 provides a breakdown of colonial policies across different colonial and legal arrangements. Before providing the evidence for each country, I make a couple of observations. 

Following the end of World War I, German colonies were distributed among Allied countries by the League of Nations. In sub-Saharan Africa, these are Tanganyika (present-day Tanzania), which was given to Great Britain; Cameroon and Togo, given to France; Rwanda and Burundi, which were given to Belgium; and finally South West Africa (present-day Namibia), given to South Africa. There was also a small part of Cameroon given to Great Britain. In these transferred colonies, officially called mandates, legal authority did not fall solely with the new colonial power. For example, the colonial government could only impose control over missionary societies that was ’necessary for the maintenance of public order and good government’. When the French government attempted to enforce the use of the French language in mission schools in Cameroon, one of its League of Nations mandates, the American missionary societies brought the issue to their United States State Department as there was a treaty signed between the two countries (Buell 1928, p.355). As a result, American missionary societies practicing in Cameroon were able to use the indigenous language in teaching. 

It is noteworthy in Table A2 that there is very strong correlation in colonial policies towards missionary activity. That is, colonial governments are either very restrictive of missionary activity, as in the case of French and Portuguese colonies, or they are very permissive, even enabling, as in the case of the rest. Only in the Democratic Republic of Congo is this correlation not perfect. There, while they allow the use of the indigenous languages in schools, they do not provide subsidies to Protestant missionary schools. In the following paragraphs, I provide passages in support of the assessments of colonial policy made in Table A2. In general, colonial powers were receptive of missionary activity and thus the instances in which they were not tend to be written about more explicitly. Still, I have tried to provide evidence for positive reception as well in each case. 

74 

###### **A.3.1 British Colonies** 

###### **Permission of Indigenous Languages in Schools:** 

-  The Belgian colonial government in the Congo ”allows and encourages, as does the British Government, missionaries to use the native language in their schools.” (Buell 1927, p.33) 

-  ”In the past practically all controlling nations forced their languages on the Native people and discouraged the use of their Native tongue. This was true centuries ago in Great Britain. Fortunately at time present only Powers that still maintain this attitude in some of their possessions are the French and the Portuguese.” (Lewis 1962, p.64) 

**Subsidization of Protestant Mission Schools:** ”The British colonies subsidize British and foreign and Catholic and Protestant missions alike” (Buell 1928, p.598) 

**Licensing of Foreign Medical Missionaries:** Medical missionaries work throughout British colonies. For example, in Tanzania they formed the Medical Missionary Committee which feature many missionary societies with aims of providing medical care (Greenwood 2015) 

###### **Missionary Societies Holding Land:** 

-  In general, missionary societies in British colonies had the right to hold land. For Nigeria, for example, ”The Land (Perpetual Succession) Ordinance (No. 32 of 1924) made provision enabling trustees of corporate bodies to be appointed and to have perpetual succession and to hold land.” (Wright 1925, p.19) Then from the ordinance itself, it reads ”any body or association of persons established for any religious, educational... may apply... to the Governor for a certificate of registration of the trustees or trustee of such a community, body or association of persons as a corporate body.” (Cameron 1924, p.2) Missionary societies could of course hold land prior to 1924 but as unincorporated bodies. 

75 

-  Gathogo (2020) describes how missionary societies in Kenya were able to acquire land thanks to the protectorate government. 

###### **A.3.2 French Colonies** 

###### **Permission of Indigenous Languages in Schools:** 

-  ”The government states: ’French should be imposed upon the greatest possible number of natives and serve as the lingua franca throughout the whole extent of French West Africa” (Buell 1928, p.51) 

-  ”French is not only taught as a subject, but is used as the medium of instruction from the very beginning; the native language of the people is not used at all. This emphasis upon French to the exclusion of the tongue used in the villages and homes of the students is a characteristic of French education in Africa which one does not find either in the British or Belgian colonies.” (Buell 1928, p.57) 

-  In 1922, the French Government enacted a decree carrying into effect this treaty, which provides that no private school could be opened without the authorization of the government ... ’Education must be given exclusively in French; the employment of native idioms is forbidden’... Thus all teachers in mission schools must know the French language, and teach only in French in the mission schools” (Buell 1928, p.71) 

-  “In Dahomey [modern Benin] a greater diversity of languages is found. In these territories as in all the French West African possessions, the missions have not done as much toward unification of the native languages as in the colonies of other nations. This is perhaps explained by the official attitude of the French government toward the mission schools, which have received little encouragement.” (Bunche 1934, p.81) 

-  In Madagascar, “French as a language of instruction and as a subject were introduced by the French colonists, holding the power from 1896 to 1960” (Dahl 2011, p.51). 

76 

“When the French authorities took over the leadership of the schools they first tried to reduce the number of ‘foreign’ teachers. French was introduced both as a subject and as language of instruction in the schools... This caused lots of troubles for the confessional schools where Malagasy had been the language of instruction.” (Dahl 2011, p.54-55) 

 

**Subsidization of Protestant Mission Schools:** ”In both the Togo and the Cameroons, the French Administration grants subsidies to mission schools- in contrast to the policy in French West Africa.” (Buell 1928, p.356) 

###### **Licensing of Foreign Medical Missionaries:** 

-  ”Likewise the government requires in theory foreign medical missionaries to obtain a Portuguese medical decree. It seems that only one such missionary has received this degree. At present, however, the government allows medical missionaries to practice among natives by sufferance. The same rule in regard to the licensing of missions and the necessity of educational and medical certificates is followed in French territories.” (Buell 1927, p.32) 

-  ”En ce qui concerne les m´edecins ´etrangers, leurs service ont ´et´e accept´es `a d´efaut des m´edecins fran¸cais pour permettre de faire la soudure en attendant l’accroissement du nombre des m´edecins coloniaux .” (Buell 1928, p.194) 

**Missionary Societies Holding Land:** ”Neither the French nor the Portuguese allow foreign missionary societies to become incorporated or to hold land.” (Buell 1927, p.32) 

###### **A.3.3 French Mandates** 

###### **Permission of Indigenous Languages in Schools:** 

-  “The Mandates administration tolerates the use of native language in private schools and it subsidizes mission schools, in contrast to an opposite policy in the French colonies proper.” (Buell 1928, p.372) 

77 

-  “In Africa the French have not hesitated to decree that French shall be the universal medium of expression, though this is not their decision in Madagascar.” (Bunche 1934, p.78) 

-  “It appears that the French language policy is subject to criticism on political grounds in its application to Togo, because of of the mandate status of this territory” (Bunche 1934, p.83) 

###### **Subsidization of Protestant Mission Schools:** 

-  ”The British colonies subsidize British and foreign and Catholic and Protestant missions alike; the French Government in Togo and the Cameroons follows the same policy” (Buell 1928, p.598) 

-  ”In both the Togo and the Cameroons, the French Administration grants subsidies to mission schools- in contrast to the policy in French West Africa. These grants are made according to results obtained from examinations given students in recognized mission schools by the government.” (Buell 1928, p.356) 

###### **Licensing of Foreign Medical Missionaries:** 

-  In Cameroon, ”The hospitals and doctors of the Presbyterian mission also treat more than fifty thousand natives annually.” (Buell 1928, p.348) It is worth noting that the Presbyterians in Cameroon were American and not French. 

-  Translated from French: “The American mission has five doctors at its service.” (R´epublique Fran¸caise 1927, p.29) 

**Missionary Societies Holding Land:** The following citation contains Article 7 of the February 13 1923 decree concerning Cameroon and the relationship between France and the United States found within the Annual Report of the Mandate Administration on Cameroon for the year 1924. Translated from French: ”The mandate power shall ensure throughout 

78 

the extent of the Territory, complete freedom of conscience and the free exercise of all forms of worship, which are not contrary to public order or to good morals; it shall give to all missionaries who are nationals of any State member of the League of Nations the faculty to enter, circulate and reside in the Territory, to acquire and possess properties therein, to erect buildings for religious purposes and to open Schools, it being understood, however, that the mandatory shall have the right to exercise such control as may be necessary for the maintenance of public order and good administration and to take for this purpose all useful measures.” (R´epublique Fran¸caise 1925, p.204) 

###### **A.3.4 Portuguese Colonies** 

###### **Permission of Indigenous Languages in Schools:** 

-  “In the past practically all controlling nations forced their languages on the Native people and discouraged the use of their Native tongue. This was true centuries ago in Great Britain. Fortunately at the time present only Powers that still maintain this attitude in some of their possessions are the French and the Portuguese.” (Lewis 1962, p.64) 

- “ 

-  The Portuguese government had, since 1914, offered missions five hundred hectares of land to any mission station on condition that the missionaries taught the Portuguese language on a full scale. The missions had politely refused the offer. If the missionaries thought they could get away with merely teaching as little Portuguese as possible they were mistaken.” 

-  “On December 9, 1921, Norton de Matos, the high commissioner of Angola, handed down a decree on education... [which] stated categorically that the missions were supposed ’to teach the Portuguese language... Not to teach any foreign language’ Article II stated, ’It is not permitted to teach native languages in schools’. Article III stated, ’The use of the native language is only allowed orally in religious instruction 

79 

and, as a help, during elementary period of teaching the Portuguese language.” No book or pamphlet could be published except in Portuguese... The Portuguese text, however, might be accompanied by a parallel version in the native language... The decree was very far-reaching. It was as if the mission could make no move in any way without feeling the weight of the Portuguese government.” 

-  Upon request from missionaries, “the high commissioner allowed the missions to publish hymn books, a few in Portuguese and a few in Umbindu. He turned down the mission’s request for the use of the vernacular as a medium for education in lower grades.” 

**Subsidization of Protestant Mission Schools:** “State elementary schools exist only for white students, Mesticos, and assimilated Africans. The African student is therefore obliged to go to a missionary school, either Catholic or Protestant,... Fees at state-subsidized Catholic elementary schools are somewhat lower.” 

**Licensing of Foreign Medical Missionaries:** “Likewise the government requires in theory foreign medical missionaries to obtain a Portuguese medical decree. It seems that only one such missionary has received this degree. At present, however, the government allows medical missionaries to practice among natives by sufferance.” (Buell 1927, p.32) 

**Missionary Societies Holding Land:** “Neither the French nor the Portuguese allow foreign missionary societies to become incorporated or to hold land.” (Buell 1927, p.32) 

###### **A.3.5 Belgian Democratic Republic of Congo** 

###### **Permission of Indigenous Languages in Schools:** 

-  The Belgian colonial government in the Congo “allows and encourages, as does the British Government, missionaries to use the native language in their schools.” (Buell 1927, p.33) 

-  “No mission in the Congo is obliged to conform to the government education program nor to submit to inspection unless it wishes to receive a subsidy. In this respect, 

80 

missionaries have more freedom in the Congo than in any French and most British territories.” (Buell 1928, p.597) 

-  “The Colony also undertakes to pay the mission the sum of three thousand francs for each new native dialect , the grammar and vocabulary of which the mission supplies to the government.” 

###### **Subsidization of Protestant Mission Schools:** 

-  “The new educational plan of the government means that no Protestant missions in the Congo proper will be eligible for a government subsidy” (Buell 1928, p.598) 

-  “In 1926 the Congo adopted a policy of granting educational subsidies of an additional three million francs to ’national’ missions. As there are no Belgian Protestant missions in the Congo proper, these sums go entirely to Roman Catholic missions.” 

-  “Protestant missionary societies... had been only too happy to accept the offer of funds in 1946” (Fast 2018, p.125) 

**Licensing of Foreign Medical Missionaries:** “Protestant missions have also done effective medical work... At present, Protestant missions maintain twenty-seven doctors, forty-eight European nurses... The government assists this work by admitting some medical supplies into the territory free of duty, and by granting small subsidies to mission doctors and hospitals.” (Buell 1928, p.588). Note as well from the previous paragraph that there are no Belgian Protestant missionaries making these mission doctors foreign. 

**Missionary Societies Holding Land:** “the Belgian Congo has been more liberal towards foreign missionaries. It grants missionary societies ’civil personality’ and authorizes them to hold land.” (Buell 1927, p.33) 

###### **A.3.6 Belgian Mandates** 

**Permission of Indigenous Languages in Schools:** 

81 

-  As per the above, the Belgian government was generally encouraging of the use of native languages and their management of Ruanda-Urundi fell under that policy as well. 

-  “Some Protestant missionaries would not care to accept the financial support of the Belgian Government on the ground that it would prejudice their independence.” (Buell 1928, p.597-8). This sentence shows that Protestant missions could have independence even if they weren’t always financially supported. 

**Subsidization of Protestant Mission Schools:** In “Ruanda-Urundi where Belgian Protestants have taken over former German work... The 1926 Ruanda budget appropriates twenty-five thousand francs for Protestant missions.” (Buell 1928, p.597) 

**Licensing of Foreign Medical Missionaries:** John Edward Church was an English medical missionary who worked in Rwanda from the late 1920s onward. The Church Missionary Society established multiple medical missions in Rwanda. (Moon n.d.) 

**Missionary Societies Holding Land:** “the Belgian Government grants ’civil personality to Protestant and Catholic missions alike. After thus being incorporated, a mission may acquire land from the government or presumably from the natives.” (Buell 1928, p.598) 

###### **A.3.7 South Africa and Namibia** 

**Permission of Indigenous Languages in Schools:** “In 1953, the apartheid government passed the Bantu Education Act... The Act also implemented the Eiselen Commission’s recommendation that all students be taught in their mother tongue for the first eight years of school... Language of instruction policy before the 1950s was largely a relic of the practice of mission schools, which were established in the nineteenth century. Natal schools taught in the student’s mother tongue for six years and in the three other provinces - the Transvaal, Cape, and Free State - instruction was in the student’s mother tongue for only four years.” (Eriksson 2014, p.316) 

82 

**Subsidization of Protestant Mission Schools:** “In the Union of South Africa the provincial governments are giving increasing financial assistance to the mission schools, and multiplying the government schools.” (Lewis 1962, p.186) 

**Licensing of Foreign Medical Missionaries:** There are many examples of medical missions in South Africa staffed by foreign doctors. The official ordinance of 1891 gives medical doctors with various foreign diplomas the right to practice within the Cape Colony, a colony forming part of the Union of South Africa in 1910. (Council & Board 1895, p.48) 

**Missionary Societies Holding Land:** Changuion & Steenkamp (2012) note how missionary societies owned land: ”In Natal alone, the missionary societies owned a total of 144 192 acres”. 

###### **A.3.8 Liberia, American Settlement** 

**Permission of Indigenous Languages in Schools:** “The Elementary School is to have a course of four years, in which the following subjects... are to be taught in the native language” (Buell 1928, p.762) 

**Subsidization of Protestant Mission Schools:** “Hitherto, the various American mission boards, aided to a certain extent by the various Colonization Funds, have annually poured into Liberia a sum of three hundred thousand dollars ... which has been expended largely on Liberian teachers and preachers.” (Buell 1928, p.759) 

**Licensing of Foreign Medical Missionaries:** Liberia relied heavily on Christian missionary organizations for the provision of health care. In 1947, they even set out to expand the use of foreign doctors in their medical system (Kanagasabai 2024) 

**Missionary Societies Holding Land:** Missionary societies were able to hold land in Liberia. The Lutherans owned ”nearly 500 acres of land” at Muhlenberg Mission (Laury 1905, p.210) 

83 

###### **A.3.9 Somalia, Italian Colony** 

###### **Permission of Indigenous Languages in Schools:** 

-  In Catholic missionary schools, they would ”follow the ”Italian national curriculum” (Scalvedi 2020, p.154) 

-  However, in the few Protestant mission schools, they would teach in Swahili (Aram 2022) 

-  Per Olsson, a Swedish evangelical missionary would teach in Somali (Tyrberg 2014, p.35) 

**Subsidization of Protestant Mission Schools:** Translated from Swedish: ”the Italian government did not approve the erection of school buildings” (Tyrberg 2014, p.29). Also mentioned that teacher salaries had to be paid from school fees. 

**Licensing of Foreign Medical Missionaries:** Multiple medical doctors of the Swedish Evangelical missionary society worked in Somalia and the Italian government had ”strongly supported” healthcare efforts (Tyrberg 2014, p.35). 

**Missionary Societies Holding Land:** ”The same year, 5 acres of land was also purchases in Mana Mofi for a future station there.” (Tyrberg 2014, p.11) 

###### **A.4 Language in Education (1960-2011)** 

Above I provide evidence as to which colonial powers permitted the use of indigenous languages in schools. Existing evidence suggests that, when possible, missionaries would in fact use the indigenous language (Dutch Reformed Church of South Africa 1929; Gardinier 1991; Tyrberg 2014; Kimani 2020) Unfortunately, systematic data on the language of instruction in mission schools for each of the 137 missionary societies working in sub-Saharan Africa does not exist. I did, however, construct a dataset on the extent each African language was used as language of instruction in the post-independence period. Given the strong correlation between language of instruction policy before and after independence (Albaugh 2014), 

84 

this data can provide some validation of the colonial policies discussed in the previous section. In constructing the dataset, I benefited greatly from the work of (Albaugh 2014) who accomplished a similar task except at the country-level. Thus, her work provides scores for each country in terms of how much they use indigenous languages in education. From there, I consulted various sources to determine which languages, if any, were used in education. Most notable and frequent among these resources is Leclerc (1999). 

For example, for Zambia, Albaugh (2014) provides a score of 6 (out of 10) at independence, 0 in 1990 and 4 in 2004. She also makes various notes justifying her scores for each year. Building off her notes and a number of additional sources, most notably Leclerc (1999), I note the most crucial information and assign extent of use for each language in each country from 1960 to 2011. Below are my notes for Zambia<sup>4</sup> : 

-  Zambia (ZMB): Albaugh p.70 

-  “British colonization. Local langauages used as a medium of instruction to 4th grade. Four local languages selected in 1928: Cibemba, Cinyanja, Citonga, Silozi. English thereafter. 

-  Leclerc: “en 1950 ... les langues locales ne furent enseign´ees que durant les deux premi`eres ann´ees du primaire, pour ˆetre remplac´ees par une langue v´ehiculaire dominante jusqu’en cinqui`eme ann´ee. Ensuite, l’anglais rempla¸cait d´efinitivement les langues locales 

-  Leclerc: There’s mention of English, Swahili, Bemba and Nyanja as being “langues v´ehiculaires” 

-  Leclerc: “ces langues peuvent ´egalement servir de langue d’enseignement dans les ´ecoles primaires ... : le bemba, le nyanja, le lozi, le tonga, le kaond´e, le luval´e et le lunda. Ces sept langues sont utilis´ees ainsi que l’anglais, dans les premi`eres ann´ees de scolarit´e primaire” 

> 4 Bullet points without explicit reference are referencing Albaugh (2014). 

85 

-  “In 1966, the Ministry of Education ruled that English would be the medium of instruction from Grade 1 onward” 

-  Leclerc: “Sept langues nationales furent reconnues comme mati`eres d’enseignement sur une base r´egionale: le bemba, le kaond´e, le lozi, le lunda, le luval´e, le nyanja et le tonga. ... les sept langues locales ont ´et´e choisies par le governement de Kaunda de mani`ere arbitraire” 

-  “Between 1975 and 1977 ... proposed a return to the earlier practice of using local languages in first four years, but the proposal was rejected” 

-  “In 1993 and 1995 ... showed that Zambian students’ reading levels were abysmal ... One of the contributing factors was determined to be the use of English as the initial language of literacy 

-  “in 1996 the government implemented a pilot reading program in Cibemba” I’m not including this program because it seems like an improvement on existing language studies not an increase in existing ones. It’s a daily literacy hour in English and Zambian languages not the inclusion of Zambian languages 

-  Evidence that Zambian languages are still taught as subjects: Leclerc: L’enseignement primaire: “l’enseignement des langues zambiennes doit ˆetre de 6 1/2 heures/semaine. Au second cucle du primaire, l’enseignement en langue zambienne baisse `a 4h/semaine” 

-  2000: “English will continue to be used as the official medium of instruction, but teachers are encouraged when necessary and relevant to use the familiar language for explanations” 

-  I don’t include this informal practice either because there are no accompanying materials, testing, etc. and it seems common for teachers across Africa to not always follow the formal policy 

86 

From the above notes, I can assign the extent of use for each Zambian language as either a medium of instruction or subject in schools from pre-independence to 2011, the final date of consideration in Albaugh (2014). An important underlying assumption is that if there is never any mention of a specific language being used in schools then I treat that language as not being used even if other indigenous languages are being used. I also tend to focus on official policy on language which comes with it the language of tests and textbooks. It is possible and even likely when the medium of instruction is a colonial language that teachers sometimes rely on the indigenous language in class to teach certain things. These things, however, are practically immeasurable and thus I focus only on official policy. 

###### **A.5 Geographic and Historical Variables** 

In this section, I describe how I construct each of the geographic and historical variables that I use as controls 

###### **A.5.1 Geographic Variables** 

**Log distance to the coast:** The coastline shapefile is sourced from Natural Earth (2024). Distance is then calculated using a Near function to the geo-located DHS cluster (not buffer). Distances are then converted to kilometers and logs are taken after adding 1. All log distances are calculated in this way. 

**Log distance to the capital:** Capitals are also taken from Natural Earth (2024) by first using the populated places shapefile and then selecting capitals among them. 

**Log distance to fresh water source:** I consider rivers and lakes to be fresh water sources. Data on lakes and rivers are also taken from Natural Earth (2024). I first take the distance to each of them and then take the minimum of these two distances in order to create the distance to a fresh water source. 

**Average suitability of rainfed crops:** Construction of suitability of rainfed crops follows the method used by Cag´e & Rueda (2016). Data on crop suitability comes from Food 

87 

and Agricultural Organization of the United Nations (2024). Rasters of rainfed suitability are taken for each crop of the major crop groups<sup>5</sup> . For each crop, I convert its raster to point data and then take the average of values within buffers (either around DHS clusters or Protestant missions). Then, the maximum suitability is taken from all the crops in the category for each buffer (either buffers around DHS clusters or Protestant mission stations). Finally, the average is taken among all these maxima to get a single measure of rainfed crop suitability in the area. 

**Average daily precipitation:** Precipitation data is also taken from Food and Agricultural Organization of the United Nations (2024). The raster is converted to point data and then I average among all points within the buffer to get average yearly precipitation at the buffer level. I then divide by 365 to get the average daily precipitation. 

**Growing days per year:** Growing days per year is also taken from Food and Agricultural Organization of the United Nations (2024). It is constructed in an analogous manner to precipitation above. 

**Presence of natural resources:** I combine four different datasets on natural resources into a single measure: gold (all of placer, surface, and vein), diamonds (both kimberlite and alluvial), gems, and petroleum (both on- and off-shore). Gold data is taken from Balestri (2012), diamond data comes from Gilmore et al. (2005), gems data comes from Lujala (2009), and petroleum data comes from Lujala et al. (2007). I create a variable that captures the presence of each one within buffers (either for DHS clusters or for Protestant missions). I then take the maximum of these variables to capture the presence of any natural resource. 

**Malaria ecology:** Rasters on malaria ecology are taken from Kiszewski et al. (2004) and converted to a point shapefile. Due to the lower resolution of this raster, value points 

> 5Among cereals, there is wheat, wet rice, dry rice, maize, barley, sorghum, rye, pearl millet, foxtail millet, oat, and buckwheat. Among tubers, there is white potato, sweet potato, cassava, and yam. Among sugar, there is sugar cane, and sugar beet. Among pulse, there is phaseolus bean, chickpea, cowpea, drypea, gram, and pigeonpea. Among oils, there is soybean, sunflower, rape, groundnut, oil palm, and olive. Among vegetables, there is cabbage, carrot, onion, and tomato. Among fruits, there is banana, citrus, and coconut. Among stimulants, there is cocoa, coffee, tea, and tobacco. Among fibres, there is cotton, and flax. Among feed stocks, there is jatropha, miscanthus, switch grass, and reed canary grass. 

88 

are given at further distances and some buffers do not contain any points. For this reason, I calculate the malaria ecology for each DHS cluster or Protestant mission by taking the malaria ecology of the closer point. 

**Ruggedness:** Data on ruggedness is taken from Nunn & Puga (2012). After converting their data to a raster, I lower the resolution 10 times (to 5 arc minutes or roughly 9.26 kilometers) before converting the raster to points. Otherwise, it would be too computationally intensive. I then link these points to buffers taking again the mean. Finally, I divide by 100000 to obtain ruggedness in terms of hundreds of meters as recommended. 

###### **A.5.2 Historical Variables** 

**Log population density in 1850:** Population density is taken from HYDE (Klein Goldewijk et al. 2011) for the year 1850. 1850 is chosen as the date since it precedes almost all missionary activity across Africa but is perhaps more accurate to circumstances when missionaries arrived then, say, the year 1800. 

**Log distance to colonial railway:** Data on colonial railways is combined from two sources: Nunn & Wantchekon (2011) and Jedwab & Moradi (2016). Jedwab & Moradi (2016) provide more precise mapping and include railway lines built until 1960. They omit, however, railways built in South Africa which Nunn & Wantchekon (2011) contain as well. 

**Log distance to explorer route:** Data on explorer routes is taken from Nunn & Wantchekon (2011) 

**Proximity to historical Muslim center (within 200 kilometers):** Location of historical Muslim centers comes from Jedwab et al. (2022). Very few countries in Africa, however, are home to such centers. Thus in order to avoid spurious relationships from a faraway location, I create an indicator variable for whether a location is within 200 kilometers of one such historical center. 

89 

###### **A.6 Other Variables** 

**Infrastructure 2024:** Infrastructure for the year 2024 is taken from OpenStreetMap. For some buildings it also provides the type. For others it will have the name. Thus, to construct the set of school buildings, I select from the type “school” or “ecole” as well as names that include the string “SCHOOL” that do not belong to the types “university” or “college”. I include its counterparts in French, Spanish and Portuguese and convert all strings to uppercase in order to avoid false negatives due to case sensitivity. For universities, I select all buildings belonging to the type “university” or “college”. I also include all buildings whose names include the strings “UNIVERSITY” or “COLLEGE” or “FACULTY” as well as their French, Spanish and Portuguese counterparts while not belonging to the types “school” or “ecole”. Finally to construct hospitals, I select all buildings of the types “hospital” or “clinic”. I also include building names that include any of the strings “HOSPITAL”, “CLINIC”, or “DISPENSARY” as well as their French, Spanish and Portuguese counterparts. 

90 

##### **B Spatial Correlation and Standard Errors** 

Kelly (2019) has shown that persistence studies tend to suffer from spatial autocorrelation and that without proper accounting, reported results may just be spurious. Moreover, in my main geographical specification, I assign translation sites to buffers within a 25 kilometer radius. That is, all DHS clusters within a 25 kilometer radius of a translation site are assigned the same treatment status. As per Abadie et al. (2023), standard errors should be clustered at the level of treatment. In my context, DHS clusters as far as 50 kilometers can be considered “treated” by the same translation site. Thus, a conservative approach but one that captures all instances of shared treatment assignment would be use Conley standard errors (Conley 1999) allowing for correlation within a 50 kilometer distance. However, Conley standard errors are often impracticable in contexts with large amounts of data due to computational requirements. Thus, in response many empirical papers in the persistence literature will cluster standard errors using administrative regions (e.g. districts) or grids of various size cells (e.g. 0.5 by 0.5 decimal degrees<sup>6</sup> ). One issue with such clusters, no matter the size, is that observations on either side of the borders for such clusters may share treatment assignment yet will be treated as unrelated. To address this, I adopt two-way clusters using both the second administrative regional level and a 0.5 by 0.5 decimal degree grid. The intuition behind this strategy is shown in Figure A16. By clustering along two geographic categories that have uncorrelated lines, observations that fall on either side of the border of a shape belonging to one category will often fall within the same shape in the other category. 

I compare these approaches more formally in table A6. It reports for each combination of clusters the share of DHS location pairs within a certain distance that belong to the same cluster. These can be compared to how Conley standard errors would behave. That is, if one uses Conley standard errors with a 50 kilometer cutoff, all DHS location pairs within 50 kilometers would be treated as being spatially correlated and no DHS location pairs outside of 50 kilometers would be treated as being spatially correlated. Using one-way clusters 

> 60.5 decimal degrees equates approximately to 55 kilometers. 

91 

performs consistently worse at grouping together nearby locations than two-way clusters. For example, 1 by 1 degree cells (approximately 111 kilometers by 111 kilometers) only groups together 94% of all location pairs within 10 kilometers of each other. By contrast, a two-way clustering using the second administrative regional level and 0.5 by 0.5 degree cells groups together 97% of all such location pairs. At the other extreme, 14% of all location pairs between 90 and 100 kilometers of each fall within the same 1 degree cell while only 1% fall within either the second administrative regional level or the same 0.5 degree cell. Put differently, in comparison to Conley standard errors, two-way clustering using smaller, but unrelated geographical levels has fewer false negative and fewer false positives than one-way clustering using a larger geographical level. In summary, an approach that adopts two-way clustering using smaller geographical levels resembles much more closely the behavior of Conley standard errors than one-way clustering at a larger geographical level. It should be finally noted that multi-way clustering does not suffer from the same computational difficulties that Conley standard errors do. 

Table A7 presents a series of regressions of the coefficient a Bible translation site on years of schooling following the main specification 3 but aggregating all individual responses to the DHS location level<sup>7</sup> . Each regression differs only in the standard errors it uses. In columns (1)-(4), I use Conley standard errors using 25, 50, 75, and 100 kilometer cutoffs respectively. In columns (5)-(10), I use various methods of two-way clustering. Columns (5)-(7) use clusters at the second administrative regional level while columns (8)-(10) use clusters at the first administrative regional level. Columns (5) and (8) also cluster using 0.5 degree cells, (6) and (9) using 0.75 degree cells, finally (7) and (10) using 1 degree cells. Standard errors shown in column (5) which clusters at the second-administrative level and 0.5 degree cell resembles most Conley standard errors with a 50 kilometer cutoff albeit being slightly larger. It is for this reason that I adopt these clusters for standard errors in my main 

> 7Note that the coefficients are different in Table A7 than column (4) of Table A14 given that by aggregating, DHS locations with fewer observations are now given more weight. The conleyreg package in R while being superior computationally than its Stata alternatives does not have any option for weighting. 

92 

specifications throughout the paper. 

In Tables A8 and A18, I report the robustness of results to using different combinations of two-way clustering. Specifically, I cluster at the second administrative regional level and 0.75 degree grid cell to imitate Conley standard errors with a 75 kilometer cutoff. I also cluster at the second administrative regional level and 1 degree grid cell to imitate the same but with a 100 kilometer cutoff. 

##### **C Conceptual Framework** 

In this section, I provide a simple conceptual framework that provides some intuition for the set of results presented in the empirical analysis. In particular, I model missionary decisions on allocation of staff and language of instruction conditional on Bible translation and colonial policy. I model also the repercussions of language of instruction on educational attainment and health. In this framework, I do not however model directly the decision to translate the Bible. I take it as exogenous. Certainly, missionary societies did strategically choose where to translate the Bible. However, there may be exogenous variation at missionary society level in terms of ideological priorities as well as idiosyncratic differences between missionaries. As previously mentioned, Bible translators were often great linguists and they, moreover, may have had to abandon translation projects due to personal reasons such as sickness in the family. 

###### **C.1 Setup** 

This model features three actors: a colonial government, a missionary society and a set of villagers. The colonial government sets policy towards missionary activity including whether indigenous languages can be used in schools, whether to subsidize Protestant mission schools and whether to allow foreign medical missionaries to practice without re-licensing. Theoretically, these governments could theoretically adopt any combination of strategies. However, 

93 

in practice, governments tended to be either restrictive of missionary activity across all policies or permissive on all of them. Thus, I continue with the above use of ILP and CLE countries. 

Missionary societies aim to evangelize villagers, and provide basic education and health services. They operate mission stations,s, throughout the world and allocate missionaries, m, to them. They have a total of S mission stations and M missionaries to allocate. Mission stations can either be the site of a Bible translation site, B, or not. That is _Bs ∈{_ 0 _,_ 1 _}_ . Evangelical success, _E_ ( _·_ ), at a given mission station, s, can be represented by the following: 



That is, a Bible translation site increases the effectiveness of missionary work by a factor of _γ >_ 0. Then, missionary societies seek to maximize evangelical success across all their stations throughout the world. Assuming they weight success at each station equally, they solve the following problem: 



Mission societies also choose in which language to teach subject to the availability of a written script and colonial policy towards language in education. In this model, there are only two languages: the colonial language and the indigenous language. The availability of a written script is determined perfectly by the presence of a Bible translation. In choosing, missionaries seek to maximize education attainment among villagers. Therefore, in ILP countries, they can choose between the indigenous language and the colonial language, provided a Bible translation exists in the indigenous language. However, in CLE countries, they must teach in the colonial language. 

94 

For villagers, there are three spheres of life: home, church, and school. Further, only one language can be used in each of these spheres among the two possible languages. I assume that, at home, the indigenous language is used exclusively. This aligns with observations at the time, that even in French colonies, where best efforts were made to encourage French at every turn, the indigenous language was always spoken in homes (Buell 1928, p.58)<sup>8</sup> . Clearly in other colonies more permissive of the use of indigenous languages, villagers would have been spoken their native tongue at home. 

At church, services can be carried out in either the colonial language or the indigenous language. This assumption again aligns with historical evidence that, while the French colonial administration enforced French in schools, it adopted a more lax policy towards church services and religious activity (Buell 1928, p.73)<sup>9</sup> . However, preachers will choose the language of service that maximizes church membership subject to the availability of religious text in that language. Indeed, in a study of church services, Kouega & Alo’o (2022) note that French is often used when religious text is not available in the indigenous language. However, once it does become available, the church will choose to use that language as the religious text becomes much more understandable to the congregation (Dutch Reformed Church of South Africa 1929; Asewie 2013). 

Finally, I assume that the likelihood of literacy increases with the familiarity a person has with the language of instruction. This assumption aligns with a host of literature on the matter (Taylor & von Fintel 2016; Seid 2016; Ramachandran 2017; Seid 2019; Kerwin & Thornton 2020 _b_ ). 

###### **C.2 Predictions** 

From this simple framework, I generate six predictions regarding the presence of a Bible translation as compared to a mission station without a Bible translation. 

> 8 Buell (1928, p.58): “French educators regretfully admit that in their homes the natives carry on conversation entirely in the native language.” 

> 9 Buell (1928, p.73): ”Services must be in public, and they must be given in a native or in the French language. No other education than that of religion can be given in such edifices.” 

95 

H1) There will be greater missionary activity in both ILP and CLE countries. 

- H2) In ILP countries but not CLE countries, missionaries choose the indigenous language as the language of instruction in schools. 

- H3) In ILP countries, educational attainment will be higher. 

- H4) In CLE countries, educational attainment will be lower. 

- H5) In ILP countries, health outcomes will be better. 

- H6) In CLE countries, health outcomes will be similar. 

The intuition behind predictions H3 and H4 is shown in Figure A17. A Bible translation in an ILP country enables educators to teach in the language best known to the local people. With a translation, the language of instruction, here the indigenous language, is used in all three spheres of society. Without a translation, the language of instruction, here the colonial language, is only used at school and at church, but not at home. However, in CLE countries, a Bible translation takes away one sphere of society, i.e. church, where the language of instruction, i.e. the colonial language, would have been used. Thus, children are even less familiar with the language of instruction than had there not been any translation. 

It is worth noting that only the policy towards language can generate these opposite effects. In a country without subsidies for Protestant mission schools, a Bible translation would still increase educational attainment although perhaps to a lesser extent. 

With regards to predictions H5 and H6, it simply becomes a matter of which missionaries can practice medicine and therefore establish clinics and hospitals in the area. In ILP countries, where they can practice, more missionaries means more health care provision. In CLE countries, more missionaries does not lead to more health care provision but also does not lead to less of it either. 

96 

##### **Appendix Tables** 

Table A1: A Comparison of Protestant Missionary Datasets from Atlases 

|Datasets|Atlas (Publication Year)<br>[Year of Activity]|Geographic Coverage|Pioneer Missions in Africa|Information|
|---|---|---|---|---|
|Brown (2025) [This paper]|Beach (1903) [1900]<br>Dennis et al. (1911) [1908]<br>Beach & St. John (1916) [1915]<br>Beach & Fahs (1925) [1922]|Global|1956 locations, 2519 missions|Panel across all editions,<br>location, staf, society, and<br>infrastructure from Beach (1903) only|
|Nunn (2010)|Roome (1925) [1924]|Africa|933 missions|Location|
|Cag´e & Rueda (2016)|Beach (1903) [1900]|Africa|723 locations<sup>10</sup>|Location, staf, society,<br>infrastructure|
|Calvi & Mantovanelli (2018)|Dennis et al. (1911) [1908]|India|N/A|Location, staf|
|Becker (2022)|Beach & Fahs (1925) [1922]|Africa|1529 locations, 1895 missions|Location, staf|



Notes: This table compares the Protestant missionary dataset I assembled against previously assembled datasets. 

> 10In their data, they aggregate missions of different missionary societies into a single row. 

97 

###### Table A2: Colonial Policies towards Missionaries 

|Country<br>Group|Countries<br>in Group|Indigenous<br>Language<br>Permitted<br>in Schools?|Protestant<br>Mission<br>Schools<br>Subsidized?|Foreign<br>Doctors Can<br>Practice with<br>Foreign Licensing|Missionary<br>Societies<br>Can Hold<br>Land?|
|---|---|---|---|---|---|
|British Colonies|Botswana, Gambia, Ghana, Kenya,<br>Lesotho, Malawi, Nigeria, Seychelles,<br>Sierra Leone, South Sudan, Sudan,<br>Swaziland, Tanzania, Uganda,<br>Zambia, Zimbabwe|Yes|Yes|Yes|Yes|
|French Colonies proper|Benin, Burkina Faso, Central African<br>Republic, Chad, Cote d’Ivoire,<br>Gabon, Guinea, Madagascar, Mali,<br>Republic of Congo, Senegal|No|No|No|No|
|French Mandates|Cameroon, Togo|Yes|Yes|Yes|Yes|
|Portuguese Colonies|Angola, Mozambique|No<sup>11</sup>|No|No|No|
|Belgian Colonies|Democratic Republic of the Congo|Yes|No|Yes|Yes|
|Belgian Mandates|Rwanda, Burundi|Yes|Yes|Yes|Yes|
|Liberia (Independent)|Liberia|Yes|Yes|Yes|Yes|
|South Africa plus|South Africa, Namibia|Yes|Yes|Yes|Yes|
|Italian Colonies|Somalia|Yes|No|Yes|Yes|



Table A3: Determinants of Missions and Translation Sites - Indigenous Language Permitted 

||(1)|(2)|(3)|T-|test|
|---|---|---|---|---|---|
||No Mission|Mission, no Translation|Translation|Dif|erence|
|Variable|Mean/SE|Mean/SE|Mean/SE|(2)-(1)|(3)-(2)|
|_Geographical Characteristics_||||||
|Log Distance to Coast|5.987|5.106|5.050|-0.881***|-0.056***|
||(0.041)|(0.107)|(0.199)|||
|Log Distance to Capital|5.325|4.613|4.282|-0.712***|-0.331**|
||(0.022)|(0.088)|(0.169)|||
|Log Distance to Fresh Water|3.601|3.768|3.422|0.167**|-0.346***|
||(0.030)|(0.042)|(0.082)|||
|Suitability for Rainfed Crops|7.775|7.510|7.340|-0.265***|-0.170***|
||(0.016)|(0.039)|(0.092)|||
|Average Precipitation per Day|3.063|3.363|3.705|0.300***|0.342|
||(0.044)|(0.106)|(0.143)|||
|Growing Days per Year|233.348|238.905|274.885|5.557***|35.980|
||(2.366)|(3.931)|(5.620)|||
|Natural Resource|0.170|0.325|0.221|0.155***|-0.103***|
||(0.011)|(0.024)|(0.025)|||
|Malaria Ecology|11.538|10.266|10.631|-1.273*|0.366|
||(0.280)|(0.455)|(0.671)|||
|Ruggedness|0.779|0.836|1.015|0.057|0.179***|
||(0.031)|(0.041)|(0.088)|||
|_Historical Characteristics_||||||
|Log Population Density 1850|1.989|2.443|3.141|0.454***|0.698***|
||(0.037)|(0.064)|(0.088)|||
|Log Distance to Colonial Railway|4.398|3.123|3.170|-1.275***|0.047|
||(0.037)|(0.087)|(0.154)|||
|Log Distance to Explorer Route|4.434<br>(0.037)|4.637<br>(0.069)|4.513<br>(0.088)|0.203***|-0.124*|
|Within 200KM of Muslim Center|0.137|0.094|0.110|-0.043|0.015|
||(0.009)|(0.013)|(0.017)|||
|_Mission Characteristics_||||||
|Year of First Protestant Mission|N/A|1896.941<br>(0.992)|1883.186<br>(2.808)|N/A|-13.755***|
|N|15796|10746|5779|||
|Clusters|2028|1319|629|||



Notes: The table compares geographical, historical and missionary characteristics in 25 kilometer buffers around DHS clusters for which there are (1) no Protestant missions, (2) a Protestant mission but no Bible translations and (3) both a Protestant mission and a Bible translation. In the last two columns, I report t-test differences with country fixed effects and standard errors clustered at the second administrative level. All missing values in balance variables are assigned the group mean. 

99 

Table A4: Determinants of Missions and Translation Sites - Colonial Language Enforced 

||(1)|(2)|(3)|T-|test|
|---|---|---|---|---|---|
||No Mission|Mission, no Translation|Translation|Dife|rence|
|Variable|Mean/SE|Mean/SE|Mean/SE|(2)-(1)|(3)-(2)|
|_Geographical Characteristics_||||||
|Log Distance to Coast|5.127|3.767|3.643|-1.360***|-0.124|
||(0.105)|(0.419)|(0.631)|||
|Log Distance to Capital|5.208|4.604|2.982|-0.604***|-1.621**|
||(0.077)|(0.371)|(0.351)|||
|Log Distance to Fresh Water|3.715|3.887|2.516|0.171|-1.370**|
||(0.066)|(0.172)|(0.355)|||
|Suitability for Rainfed Crops|7.711|7.010|7.227|-0.701***|0.217*|
||(0.052)|(0.188)|(0.187)|||
|Average Precipitation per Day|2.566|3.709|3.225|1.143|-0.485|
||(0.081)|(0.526)|(0.463)|||
|Growing Days per Year|180.302|223.045|223.915|42.743|0.870|
||(4.922)|(11.836)|(19.278)|||
|Natural Resource|0.160|0.461|0.270|0.302***|-0.192**|
||(0.020)|(0.069)|(0.088)|||
|Malaria Ecology|19.719|13.413|16.468|-6.306|3.056**|
||(0.459)|(2.228)|(3.223)|||
|Ruggedness|0.378|0.651|0.484|0.273*|-0.167|
||(0.019)|(0.093)|(0.118)|||
|_Historical Characteristics_||||||
|Log Population Density 1850|1.790|2.184|2.621|0.394***|0.437**|
||(0.070)|(0.236)|(0.255)|||
|Log Distance to Colonial Railway|4.376|4.101|2.909|-0.275***|-1.193|
||(0.104)|(0.546)|(0.623)|||
|Log Distance to Explorer Route|4.689|5.200|5.082|0.511|-0.118|
||(0.070)|(0.331)|(0.426)|||
|Within 200KM of Muslim Center|0.201|0.046|0.270|-0.155|0.224*|
||(0.020)|(0.023)|(0.136)|||
|_Mission Characteristics_||||||
|Year of First Protestant Mission|N/A|1899.409<br>(3.279)|1885.853<br>(10.090)|N/A|-13.556**|
|N|12495|1725|1467|||
|Clusters|743|116|68|||



Notes: The table compares geographical, historical and missionary characteristics in 25 kilometer buffers around DHS clusters for which there are (1) no Protestant missions, (2) a Protestant mission but no Bible translations and (3) both a Protestant mission and a Bible translation. In the last two columns, I report t-test differences with country fixed effects and standard errors clustered at the second administrative level. All missing values in balance variables are assigned the group mean. 

100 

Table A5: Balance in Matching Mission Stations 

|(1)|(2)|T-test|
|---|---|---|
|No Translation<br><br>Variable<br>Mean/SE|Translation<br>Mean/SE|Diference<br>(1)-(2)|
|_Exact Matched Variables_|||
|Indigenous Language Permitted<br>0.858<br>(0.030)|0.858<br>(0.030)|0.000|
|First Station within 25km<br>0.896<br>(0.027)|0.896<br>(0.027)|0.000|
|Year Established<br>1900.642<br>(1.530)<br>_LASSO-selected Variables_|1900.739<br>(1.548)<br>|-0.097|
|Log Distance to Coast<br>5.601|6.001|-0.400**|
|(0.122)|(0.134)||
|Log Distance to Fresh Water<br>3.227|2.961|0.265|
|(0.142)|(0.142)||
|Crop Suitability<br>7.686|7.748|-0.061|
|(0.038)|(0.036)||
|Average Daily Precipitation<br>3.242<br>(0.134)|3.225<br>(0.096)|0.017|
|Growing Days per year<br>233.800|244.899|-11.100|
|(7.807)|(6.580)||
|Malaria Ecology<br>11.000|11.925|-0.925|
|(0.774)|(0.754)||
|Mineral Presence<br>0.149|0.157|-0.007|
|(0.031)|(0.032)||
|Ruggedness<br>0.692<br>(0.065)|0.693<br>(0.072)|-0.001|
|Log Population Density 1850’<br>1.633<br>(0.100)|1.679<br>(0.101)|-0.046|
|Log Distance to Colonial Railway<br>4.210<br>(0.144)|4.245<br>(0.147)|-0.035|
|Log Distance to Explorer Route<br>4.409<br>(0.136)|4.241<br>(0.127)|0.168|
|Within 200KM of Muslim Center<br>0.104|0.157|-0.052|
|(0.027)<br>_Not Selected Variables_|(0.032)||
|Log Distance to Capital<br>5.323|5.354|-0.031|
|(0.078)|(0.103)||
|N<br>134|134||



Notes: This table compares mission stations with a Bible translation against their matched stations without a translation. These stations are compared along their characteristics that were used for exact matching, caliper matching, and unmatched variables. Robust standard errors are shown in parentheses. The final column reports the difference and the significance * ** *** of that difference. _p <_ 0 _._ 10, _p <_ 0 _._ 05, _p <_ 0 _._ 01. 

101 

###### Table A6: Shared Coverage of Pairs of DHS Clusters 

|Distance|Admin2|Admin1|0.5 degree|0.75 degree|1 degree|Admin2 or<br>0.5 degree|Admin2 or<br>0.75 degree|Admin2 or<br>1 degree|Admin1 or<br>0.5 degree|Admin1 or<br>0.75 degree|Admin1 or<br>1 degree|
|---|---|---|---|---|---|---|---|---|---|---|---|
|(in km)|Level|Level|cell|cell|cell|cell|cell|cell|cell|cell|cell|
|0-10|0.70|0.94|0.89|0.95|0.94|0.97|0.98|0.99|0.99|1.00|1.00|
|10-20|0.32|0.73|0.69|0.83|0.84|0.79|0.88|0.90|0.91|0.95|0.96|
|20-30|0.16|0.54|0.48|0.68|0.75|0.56|0.73|0.79|0.74|0.86|0.88|
|30-40|0.09|0.40|0.32|0.55|0.64|0.38|0.59|0.68|0.59|0.74|0.78|
|40-50|0.06|0.31|0.18|0.43|0.54|0.23|0.46|0.57|0.44|0.60|0.68|
|50-60|0.04|0.23|0.06|0.31|0.45|0.09|0.33|0.47|0.28|0.46|0.57|
|60-70|0.03|0.19|0.01|0.20|0.36|0.03|0.22|0.38|0.19|0.35|0.48|
|70-80|0.02|0.15|0.00|0.11|0.28|0.02|0.12|0.29|0.15|0.24|0.39|
|80-90|0.01|0.13|0.00|0.04|0.21|0.01|0.05|0.22|0.13|0.16|0.31|
|90-100|0.01|0.11|0.00|0.01|0.14|0.01|0.02|0.15|0.11|0.11|0.23|



Notes: This table provides the share of DHS cluster pairs within a certain distance that belong to the same cluster. For example, 70% of DHS cluster pairs within 10 kilometers of each other fall within the same second administrative regional level. 97% of DHS cluster pairs within 10 kilometers of each other fall within either the same second administrative regional level or the same 0.5 by 0.5 degree grid cell. 

Table A7: Translation Sites and Years of Schooling with various Standard Errors 

|Standard Error|Conley|Conley|Conley|Conley|Admin2 and|Admin2 and|Admin2 and|Admin1 and|Admin1 and|Admin1 and|
|---|---|---|---|---|---|---|---|---|---|---|
|Clusters|25km|50km|75km|100km|0.5 degree cell|0.75 degree cell|1 degree cell|0.5 degree cell|0.75 degree cell|1 degree cell|
||(1)|(2)|(3)|(4)|(5)|(6)|(7)|(8)|(9)|(10)|
|Translation Site|0_._170<sup>_∗∗_</sup>|0_._170<sup>_∗_</sup>|0_._170<sup>_∗_</sup>|0_._170<sup>_∗_</sup>|0_._170<sup>_∗_</sup>|0_._170<sup>_∗_</sup>|0_._170<sup>_∗_</sup>|0_._170<sup>_∗_</sup>|0_._170|0_._170|
||(0_._077)|(0_._092)|(0_._100)|(0_._103)|(0_._094)|(0_._100)|(0_._103)|(0_._106)|(0_._109)|(0_._112)|
|Observations|32321|32321|32321|32321|32321|32321|32321_._000|32321|32321|32321|



Notes: This table presents different standard errors from the same regression. The regression measures the effect of a translation site on years of schooling in indigenous-languagepermitted (ILP) countries. The unit of observation is the DHS location. Regressions include country by round fixed effects as well geographical and historical characteristics as controls as shown in Table II. They also include controls for the presence of Protestant and Catholic missions as well as a set of indicator variables indicating the year of first establishment of a Protestant mission in 25 year blocks starting in 1830. 

Table A8: Bible Translations and Years of Schooling - Robustness to Different Standard Errors 

|Panel A: Indigenous Language|Permitted|
|---|---|
|(1)<br>(2)|(3)|
|**Panel A: Indigenous Language Permitted**||
|Translation Site<br>0.205**<br>0.205*|0.205*|
|(0.101)<br>(0.109)|(0.111)|
|Observations<br>1,138,361<br>1,138,361|1,138,361|
|Mean Dep. Var.<br>6.340<br>6.340|6.340|
|**Panel B: Colonial Language Enforced**||
|Translation Site<br>-0.458***<br>-0.458***<br>(0.146)<br>(0.167)|-0.458***<br>(0.164)|
|Observations<br>620,426<br>620,426|620,426|
|Mean Dep. Var.<br>3.368<br>3.368|3.368|
|SE Clusters<br>Admin2 + 0.5 deg.<br>Admin2 + 0.75 deg.|Admin2 + 1 deg.|



Notes: This table displays results of the effects of being proximate to a historical Bible translation on years of schooling. Individual controls include age, age squared, gender, and urban status. Geographical and historical controls are as shown in II. Mission by year controls consist of the presence of a Catholic mission within 25 kilometers and indicator variables for Protestant missions established in 25 year blocks beginning in 1805 and ending in 1930 for a total of 5 blocks. Clusters for standard errors are indicated in the table. For example, Admin2 + 0.5 deg. indicates two-way * ** clustering at the second administrative regional level and a 0.5 by 0.5 degree grid. _p <_ 0 _._ 10, *** _p <_ 0 _._ 05, _p <_ 0 _._ 01 

104 

Table A9: Determinants of Mission Stations by Proclivity of First Established Society 

||(1)|(2)|(3)|T-|test|
|---|---|---|---|---|---|
||No Mission|No or Low Proclivity|High Proclivity|Dife|rence|
|Variable|Mean/SE|Mean/SE|Mean/SE|(2)-(1)|(3)-(2)|
|_Geographical Characteristics_||||||
|Log Distance to Coast|5.607|4.670|4.950|-0.937***|0.280**|
||(0.056)|(0.186)|(0.128)|||
|Log Distance to Capital|5.273|4.509|4.342|-0.764***|-0.167|
||(0.036)|(0.158)|(0.110)|||
|Log Distance to Fresh Water|3.652<br>(0.034)|3.759<br>(0.078)|3.505<br>(0.068)|0.107|-0.254|
|Suitability for Rainfed Crops|7.746|7.343|7.419|-0.404***|0.076*|
||(0.025)|(0.093)|(0.047)|||
|Average Precipitation per Day|2.843<br>(0.045)|3.716<br>(0.214)|3.379<br>(0.095)|0.872**|-0.337**|
|Growing Days per Year|209.920|230.453|254.369|20.533***|23.916|
||(2.751)|(6.428)|(4.159)|||
|Natural Resource|0.165|0.333|0.288|0.168***|-0.045*|
||(0.011)|(0.032)|(0.022)|||
|Malaria Ecology|15.151|10.882|11.212|-4.270**|0.330**|
||(0.287)|(0.930)|(0.541)|||
|Ruggedness|0.602|0.868|0.836|0.266|-0.032|
||(0.021)|(0.060)|(0.046)|||
|_Historical Characteristics_||||||
|Log Population Density 1850|1.901|2.114|2.874|0.213***|0.760***|
||(0.037)|(0.105)|(0.061)|||
|Log Distance to Colonial Railway|4.388|3.095|3.256|-1.293***|0.162**|
||(0.050)|(0.161)|(0.114)|||
|Log Distance to Explorer Route|4.547<br>(0.037)|4.798<br>(0.113)|4.631<br>(0.075)|0.251|-0.167|
|Within 200KM of Muslim Center|0.165|0.060|0.129|-0.105|0.069***|
||(0.010)|(0.015)|(0.020)|||
|_Mission Characteristics_||||||
|Year of First Protestant Mission|N/A|1897.544<br>(2.139)|1889.941<br>(1.728)|N/A|-7.603***|
|N|28291|6118|13599|||
|Clusters|2753|627|1437|||



Notes: The table compares geographical, historical and missionary characteristics in 25 kilometer buffers around DHS clusters for which there are (1) no Protestant missions, (2) a Protestant mission belonging to a no or low proclivity society is established first and (3) a mission belonging to a high proclivity society is established first. In the last two columns, I report t-test differences with country fixed effects and standard errors clustered at the second administrative level. All missing values in balance variables are assigned the group mean. 

105 

Table A10: Conditional Balance of High Proclivity Societies 

||Indigen|ous Language P|ermitted|Colon|ial Language E|nforced|
|---|---|---|---|---|---|---|
||Variable<br>Mean<br>(1)|Log Proclivity<br>Coefcient<br>(2)|p-value<br>(3)|Variable<br>Mean<br>(4)|Log Proclivity<br>Coefcient<br>(5)|p-value<br>(6)|
|_Geographic Characteristics_|||||||
|Log Distance to Coast|5.53|-0.03|(0.27)|4.84|-0.03|(0.70)|
|Log Distance to Capital|4.90|-0.01|(0.80)|4.93|-0.23|(0.01)***|
|Log Distance to Fresh Water|3.62|0.03|(0.16)|3.62|-0.13|(0.01)***|
|Suitability for Rainfed Crops|7.61|-0.02|(0.19)|7.59|0.05|(0.18)|
|Average Precipitation per Day|3.28|-0.01|(0.78)|2.75|0.11|(0.08)*|
|Growing Days per Year|242.62|0.71|(0.47)|189.08|1.94|(0.51)|
|Natural Resource|0.23|0.01|(0.61)|0.20|-0.04|(0.01)**|
|Malaria Ecology|10.95|-0.12|(0.34)|18.72|0.32|(0.18)|
|Ruggedness|0.84|0.00|(0.93)|0.42|0.04|(0.20)|
|_Historical Characteristics_|||||||
|Log Population Density 1850|2.35|0.04|(0.10)|1.91|0.05|(0.25)|
|Log Distance to Colonial Railway|3.75|0.07|(0.01)**|4.21|-0.15|(0.01)***|
|Log Distance to Explorer Route|4.52|0.01|(0.58)|4.78|0.01|(0.64)|
|Within 200KM of Muslim Center|0.12|0.01|(0.02)**|0.19|0.00|(0.92)|



Notes: Each coefficient in columns (2), and (5) come from separate regressions that include country fixed effects, controls for presence of a Catholic or a Protestant mission within 25 kilometer radius and a set of indicator variables for the year of first established Protestant mission in 25 year blocks starting in 1805 and ending in 1930. The unit of observation is the DHS cluster. Columns (3), and (6) report the p-values for the regressions shown in columns (2), and (5) respectively. Standard errors are two-way * ** *** clustered at the second administrative regional level and 0.5 by 0.5 degree cell. _p <_ 0 _._ 10, _p <_ 0 _._ 05, _p <_ 0 _._ 01 

Table A11: Determinants of Mission Stations by Society Proclivity - Indigenous Language Permitted 

||(1)|(2)|(3)|T-|test|
|---|---|---|---|---|---|
||No Mission|No or Low Proclivity|High Proclivity|Dife|rence|
|Variable|Mean/SE|Mean/SE|Mean/SE|(2)-(1)|(3)-(2)|
|_Geographical Characteristics_||||||
|Log Distance to Coast|5.987|4.957|5.137|-1.030***|0.180***|
||(0.041)|(0.178)|(0.123)|||
|Log Distance to Capital|5.325|4.511|4.492|-0.815***|-0.019|
||(0.022)|(0.160)|(0.101)|||
|Log Distance to Fresh Water|3.601|3.703|3.625|0.102|-0.078|
||(0.030)|(0.079)|(0.051)|||
|Suitability for Rainfed Crops|7.775|7.457|7.448|-0.317***|-0.010**|
||(0.016)|(0.096)|(0.049)|||
|Average Precipitation per Day|3.063|3.764|3.372|0.701***|-0.392*|
||(0.044)|(0.206)|(0.092)|||
|Growing Days per Year|233.348|236.798|257.242|3.449***|20.444|
||(2.366)|(7.271)|(3.868)|||
|Natural Resource|0.170|0.286|0.290|0.116***|0.004|
||(0.011)|(0.033)|(0.023)|||
|Malaria Ecology|11.538|9.893|10.590|-1.645***|0.696**|
||(0.280)|(0.876)|(0.416)|||
|Ruggedness|0.779|0.968|0.871|0.189**|-0.096*|
||(0.031)|(0.074)|(0.050)|||
|_Historical Characteristics_||||||
|Log Population Density 1850|1.989|2.037|2.942|0.048***|0.905***|
||(0.037)|(0.107)|(0.060)|||
|Log Distance to Colonial Railway|4.398|2.923|3.224|-1.475***|0.301***|
||(0.037)|(0.127)|(0.097)|||
|Log Distance to Explorer Route|4.434|4.820|4.505|0.386***|-0.315|
||(0.037)|(0.095)|(0.064)|||
|Within 200KM of Muslim Center|0.137|0.036|0.125|-0.102**|0.089***|
||(0.009)|(0.009)|(0.014)|||
|_Mission Characteristics_||||||
|Year of First Protestant Mission|N/A|1896.746|1890.319|N/A|-6.426***|
|||(2.563)|(1.527)|||
|N|15796|4651|11874|||
|Clusters|2028|547|1342|||



Notes: The table compares geographical, historical and missionary characteristics in 25 kilometer buffers around DHS clusters for which there are (1) no Protestant missions, (2) a Protestant mission belonging to a no or low proclivity society is established first and (3) a mission belonging to a high proclivity society is established first. Comparisons are made only within indigenous-language-permitted (ILP) countries. In the last two columns, I report t-test differences with country fixed effects and standard errors clustered at the second administrative level. All missing values in balance variables are assigned the group mean. 

107 

Table A12: Determinants of Mission Stations by Society Proclivity - Colonial Language Enforced 

||(1)|(2)|(3)|T-|test|
|---|---|---|---|---|---|
||No Mission|No or Low Proclivity|High Proclivity|Dife|rence|
|Variable|Mean/SE|Mean/SE|Mean/SE|(2)-(1)|(3)-(2)|
|_Geographical Characteristics_||||||
|Log Distance to Coast|5.127|3.762|3.666|-1.365***|-0.096|
||(0.105)|(0.485)|(0.540)|||
|Log Distance to Capital|5.208|4.503|3.311|-0.705***|-1.192**|
||(0.077)|(0.423)|(0.358)|||
|Log Distance to Fresh Water|3.715|3.935|2.680|0.220|-1.256**|
||(0.066)|(0.188)|(0.312)|||
|Suitability for Rainfed Crops|7.711|6.978|7.222|-0.732***|0.243**|
||(0.052)|(0.220)|(0.160)|||
|Average Precipitation per Day|2.566|3.562|3.422|0.996|-0.140**|
||(0.081)|(0.616)|(0.398)|||
|Growing Days per Year|180.302|210.337|234.591|30.036|24.254|
||(4.922)|(11.919)|(17.020)|||
|Natural Resource|0.160|0.483|0.281|0.323***|-0.202***|
||(0.020)|(0.084)|(0.073)|||
|Malaria Ecology|19.719|14.016|15.499|-5.703|1.483|
||(0.459)|(2.447)|(2.908)|||
|Ruggedness|0.378|0.552|0.593|0.175***|0.040|
||(0.019)|(0.079)|(0.109)|||
|_Historical Characteristics_||||||
|Log Population Density 1850|1.790|2.360|2.406|0.570***|0.047|
||(0.070)|(0.259)|(0.232)|||
|Log Distance to Colonial Railway|4.376|3.639|3.480|-0.737***|-0.159|
||(0.104)|(0.559)|(0.596)|||
|Log Distance to Explorer Route|4.689|4.728|5.500|0.039|0.772|
||(0.070)|(0.363)|(0.377)|||
|Within 200KM of Muslim Center|0.201|0.138|0.158|-0.062|0.019|
||(0.020)|(0.056)|(0.119)|||
|_Mission Characteristics_||||||
|Year of First Protestant Mission|N/A|1900.080|1887.334|N/A|-12.746|
|||(3.631)|(8.656)|||
|N|12495|1467|1725|||
|Clusters|743|85|101|||



Notes: The table compares geographical, historical and missionary characteristics in 25 kilometer buffers around DHS clusters for which there are (1) no Protestant missions, (2) a Protestant mission belonging to a no or low proclivity society is established first and (3) a mission belonging to a high proclivity society is established first. Comparisons are made only within colonial-language-enforced (CLE) countries. In the last two columns, I report t-test differences with country fixed effects and standard errors clustered at the second administrative level. All missing values in balance variables are assigned the group mean. 

108 

Table A13: Priorities of High Proclivity Societies 

|Dependent Variable:||Procliv|ity to Tr|anslate||
|---|---|---|---|---|---|
||(1)|(2)|(3)|(4)|(5)|
|Education Infrastructure (PCA)|0.83***<br>(0.24)||||1.17***<br>(0.27)|
|Health Infrastructure (PCA)||0.29<br>(0.34)|||-0.19<br>(0.25)|
|Religious Infrastructure (PCA)|||0.20<br>(0.23)||-0.41<br>(0.27)|
|Infrastructure for the Marginalized (PCA)||||-0.31<br>(0.19)|-0.24<br>(0.18)|
|Observations|221|221|221|221|221|
|Mean Dep. Var.|1.47|1.47|1.47|1.47|1.47|



Notes: This table reports regressions of a missionary society’s log proclivity to translate against other investment priorities. The unit of observation is the missionary society and regressions are weighted by the number of missions in the society. Log proclivity to translate is defined as the logarithm of the average number of Bible verses translated across all of its missions globally. Missionary infrastructure is grouped into four categories: education, health, religious and for marginalized. Education infrastructure includes primary schools, high schools, colleges, industrial schools and kindergartens. Health infrastructure includes hospitals, dispensaries, medical schools, and number of doctors. Religious infrastructure includes chapels, Sunday schools, theological schools, temperance societies and white cross societies. Infrastructure for the marginalized includes anti-foot-binding societies, anti-opium societies, schools for the blind, schools for the deaf, foundling asylums, insane asylums, leper asylums, orphanages and refuges for opium victims. Principal component scores are then taken at the mission station level for each of these categories. Finally, the average of principal component scores across all mission stations with a missionary society is calculated to create a score at the missionary society level. Robust standard errors are reported in parentheses. 

109 

Table A14: Alternative Education Measures 

||Years of<br>Schooling<br>(1)|Completed<br>Primary<br>(2)|Completed<br>Secondary<br>(3)|Literate<br>(4)|
|---|---|---|---|---|
|**Panel A: Indigenous L**|**anguage Pe**|**rmitted**|||
|Translation Site|0.205**|0.023**|0.009|0.016*|
||(0.101)|(0.009)|(0.008)|(0.009)|
|Observations|1,138,361|1,139,191|1,139,191|1,047,484|
|Mean Dep. Var.|6.340|0.554|0.146|0.584|
|**Panel B: Colonial Lang**|**uage Enfo**|**rced**|||
|Translation Site|-0.458***|-0.033**|-0.018***|-0.048**|
||(0.146)|(0.016)|(0.005)|(0.019)|
|Observations|620,426|620,904|620,904|590,554|
|Mean Dep. Var.|3.368|0.291|0.044|0.324|
|Country by Round FE|Yes|Yes|Yes|Yes|
|Individual Controls|Yes|Yes|Yes|Yes|
|Geographic Controls|Yes|Yes|Yes|Yes|
|Historical Controls|Yes|Yes|Yes|Yes|
|Mission by Year Controls|Yes|Yes|Yes|Yes|



Notes: Individual controls include age, age squared, gender, and urban status. Geographical and historical controls are as shown in II. Mission by year controls consist of the presence of a Catholic mission within 25 kilometers and indicator variables for Protestant missions established in 25 year blocks beginning in 1805 and ending in 1930 for a total of 5 blocks. Standard errors are two-way clustered at the second administrative level and 0.5 decimal * ** *** degree grid-cell. _p <_ 0 _._ 10, _p <_ 0 _._ 05, _p <_ 0 _._ 01 

110 

Table A15: Intensive Margin of Bible Translation on Years of Schooling 

||Indigenous|Language|Permitted|Colonial|Language|Enforced|
|---|---|---|---|---|---|---|
||(1)|(2)|(3)|(4)|(5)|(6)|
|Minimal Translation (verses _<_3779)|0.035|||-0.661**|||
||(0.110)|||(0.281)|||
|Gospels Translated (3779_≤_verses _<_7957)|0.398**|||-0.162|||
||(0.194)|||(0.222)|||
|New Testament Translated (7957_≤_verses _<_31102)|0.474***<br>(0.157)|||-0.488**<br>(0.221)|||
|Full Bible Translated (verses _≥_31102)|-0.206|||-0.539*|||
||(0.161)|||(0.290)|||
|Translation Site||0.344|0.259**||-0.784|-0.490*|
|||(0.424)|(0.122)||(0.898)|(0.277)|
|Log Translated Verses||-0.016|||0.037||
|||(0.050)|||(0.103)||
|Translated Verses (1000s)|||-0.001|||0.005|
||||(0.013)|||(0.053)|
|Verses Squared (1000s)|||-0.000|||-0.000|
||||(0.000)|||(0.001)|
|Observations|1,138,361|1,138,361|1,138,361|620,426|620,426|620,426|
|Mean Dep. Var.|6.340|6.340|6.340|3.368|3.368|3.368|
|Country by Round FE|Yes|Yes|Yes|Yes|Yes|Yes|
|Individual Controls|Yes|Yes|Yes|Yes|Yes|Yes|
|Geographic Controls|Yes|Yes|Yes|Yes|Yes|Yes|
|Historical Controls|Yes|Yes|Yes|Yes|Yes|Yes|
|Mission by Year Controls|Yes|Yes|Yes|Yes|Yes|Yes|



Notes: Individual controls include age, age squared, gender, and urban status. Geographical and historical controls are as shown in II. Mission by year controls consist of the presence of a Catholic mission within 25 kilometers and indicator variables for Protestant missions established in 25 year blocks beginning in 1805 and ending in 1930 for a total of 5 blocks. Standard errors are two-way clustered at the second administrative level and 0.5 decimal degree grid-cell. * _p <_ 0 _._ 10, ** _p <_ 0 _._ 05, *** _p <_ 0 _._ 01 

111 

Table A16: Proximity to Bible Translation on Years of Schooling 

|Bufer size|15km<br>(1)|25km<br>(2)|35km<br>(3)|25km<br>(4)|25km<br>(5)|
|---|---|---|---|---|---|
|**Panel A: Indigenous Language **|**Permitted**|||||
|Translation Site|0.283**<br>(0.126)|0.205**<br>(0.101)|0.107<br>(0.094)|||
|Log Distance to Translation Site||||-0.247***<br>(0.084)|-0.076<br>(0.065)|
|Log Distance to Protestant Mission||||-0.287***<br>(0.087)|-0.415***<br>(0.066)|
|Log Distance to Catholic Mission||||0.163*<br>(0.089)|0.012<br>(0.066)|
|Observations|1,137,569|1,138,361|1,138,601|119,918|242,290|
|Mean Dep. Var.|6.340|6.340|6.340|6.872|6.680|
|**Panel B: Colonial Language En**|**forced**|||||
|Translation Site|-0.696***<br>(0.163)|-0.458***<br>(0.146)|-0.357**<br>(0.142)|||
|Log Distance to Translation Site||||-0.587***<br>(0.101)|-0.376***<br>(0.136)|
|Log Distance to Protestant Mission||||0.185<br>(0.187)|0.266*<br>(0.144)|
|Log Distance to Catholic Mission||||-0.444<br>(0.287)|-0.171<br>(0.181)|
|Observations|620,380|620,426|620,426|17,360|35,339|
|Mean Dep. Var.|3.368|3.368|3.368|5.082|4.330|
|Country by Round FE|Yes|Yes|Yes|Yes|Yes|
|Individual Controls|Yes|Yes|Yes|Yes|Yes|
|Geographic Controls|Yes|Yes|Yes|Yes|Yes|
|Historical Controls|Yes|Yes|Yes|Yes|Yes|
|Mission by Year Controls|Yes|Yes|Yes|No|No|
|Sample Restriction||||_<_ 50km|_<_ 100km|



Notes: Individual controls include age, age squared, gender, and urban status. Geographical and historical controls are as shown in II. Mission by year controls consist of the presence of a Catholic mission within 25 kilometers and indicator variables for Protestant missions established in 25 year blocks beginning in 1805 and ending in 1930 for a total of 5 blocks. Sample restriction indicates the distance from a translation site in order to be included in the sample. In column (4), only respondents within 50 kilometers of a translation site are included while column (5) restricts to 100 kilometers. Standard errors are two-way clustered at the second administrative level and 0.5 decimal degree grid-cell. * _p <_ 0 _._ 10, ** _p <_ 0 _._ 05, *** _p <_ 0 _._ 01 

112 

Table A17: Effects by Year of Birth on Years of Schooling 

||**ILP Co**<br>(1)|**untries**<br>(2)|**CLE C**<br>(3)|**ountries**<br>(4)|
|---|---|---|---|---|
|Translation Site|0.626**<br>(0.311)||-0.395<br>(0.338)||
|Year of Birth - 1930|0.092***<br>(0.014)||0.132***<br>(0.011)||
|Translation * (Year of Birth - 1930)|-0.008<br>(0.005)||-0.001<br>(0.006)||
|P. Mission * (Year of Birth - 1930)|-0.003<br>(0.003)||-0.004<br>(0.004)||
|Translation * Born before 1950||1.104*<br>(0.593)||-0.492**<br>(0.215)|
|Translation * Born 1950-1960||0.459*<br>(0.235)||-0.413*<br>(0.247)|
|Translation * Born 1960-1970||0.281**<br>(0.137)||-0.425**<br>(0.193)|
|Translation * Born 1970-1980||0.272**<br>(0.129)||-0.380*<br>(0.205)|
|Translation * Born 1980-1990||0.220*<br>(0.121)||-0.533***<br>(0.204)|
|Translation * Born after 1990||0.092<br>(0.115)||-0.449***<br>(0.166)|
|Observations|1,138,361|1,138,361|620,426|620,426|
|Mean Dep. Var.|6.340|6.340|3.368|3.368|
|Country by Round FE|Yes|Yes|Yes|Yes|
|Individual Controls|Yes|Yes|Yes|Yes|
|Geographic Controls|Yes|Yes|Yes|Yes|
|Historical Controls|Yes|Yes|Yes|Yes|
|Mission by Year Controls|Yes|Yes|Yes|Yes|
|Year of Birth Controls|No|Yes|No|Yes|
|Mission by YOB Controls|No|Yes|No|Yes|



Notes: Individual controls include age, age squared, gender, and urban status. Geographical and historical controls are as shown in II. Mission by year controls consist of the presence of a Catholic mission within 25 kilometers and indicator variables for Protestant missions established in 25 year blocks beginning in 1805 and ending in 1930 for a total of 5 blocks. Year of birth controls consist of indicator variables for the same year of birth categories shown in the table: before 1950, 1950-1960, 1960-1970, 1970-1980, 1980-1990, after 1990. Mission by YOB controls consist of the Protestant mission indicator interacted with the year of birth categories. Standard errors are two-way clustered * ** *** at the second administrative level and 0.5 decimal degree grid-cell. _p <_ 0 _._ 10, _p <_ 0 _._ 05, _p <_ 0 _._ 01 

113 

Table A18: Bible Translations and Body Mass Index - Robustness to Different Standard Errors 

||Panel A: Indigenous Language|Permitted|
|---|---|---|
||(1)<br>(2)|(3)|
|**Panel A: Indigeno**|**us Language Permitted**||
|Translation Site|0.112***<br>0.112***|0.112**|
||(0.041)<br>(0.043)|(0.045)|
|Observations|446,893<br>446,893|446,893|
|Mean Dep. Var.|22.029<br>22.029|22.029|
|**Panel B: Colonial **|**Language Enforced**||
|Translation Site|-0.098<br>-0.098<br>(0.121)<br>(0.124)|-0.098<br>(0.123)|
|Observations|189,591<br>189,591|189,591|
|Mean Dep. Var.|21.652<br>21.652|21.652|
|SE Clusters<br>A|dmin2 + 0.5 deg.<br>Admin2 + 0.75 deg.|Admin2 + 1 deg.|



Notes: This table displays results of the effects of being proximate to a historical Bible translation on years of schooling. Individual controls include age, age squared, gender, and urban status. Geographical and historical controls are as shown in II. Mission by year controls consist of the presence of a Catholic mission within 25 kilometers and indicator variables for Protestant missions established in 25 year blocks beginning in 1805 and ending in 1930 for a total of 5 blocks. Clusters for standard errors are indicated in the table. For example, Admin2 + 0.5 deg. indicates two-way * ** clustering at the second administrative regional level and a 0.5 by 0.5 degree grid. _p <_ 0 _._ 10, *** _p <_ 0 _._ 05, _p <_ 0 _._ 01 

114 

Table A19: Alternative Health Measures 

||Body Mass<br>Index<br>(1)|Underweight<br>(2)|Height<br>(3)|Height<br>for Age (z)<br>(4)|Moderate to<br>Severe Anemia<br>(5)|Hemoglobin<br>Level (g/dL)<br>(6)|
|---|---|---|---|---|---|---|
|**Panel A: Indigenous La**|**nguage Per**|**mitted**|||||
|Translation Site|0.112***|-0.009***|0.146|0.024|-0.005|0.051|
||(0.041)|(0.003)|(0.128)|(0.022)|(0.004)|(0.038)|
|Observations|446,893|446,893|478,606|477,500|307,970|307,876|
|Mean Dep. Var.|22.029|0.107|159.381|-0.687|0.096|12.894|
|**Panel B: Colonial Lang**|**uage Enforc**|**ed**|||||
|Translation Site|-0.098|0.009|0.775***|0.130***|0.011|-0.141**|
||(0.121)|(0.011)|(0.215)|(0.037)|(0.011)|(0.066)|
|Observations|189,591|189,591|200,768|199,974|159,251|162,644|
|Mean Dep. Var.|21.652|0.134|160.188|-0.557|0.145|12.202|
|Country by Round FE|Yes|Yes|Yes|Yes|Yes|Yes|
|Individual Controls|Yes|Yes|Yes|Yes|Yes|Yes|
|Geographic Controls|Yes|Yes|Yes|Yes|Yes|Yes|
|Historical Controls|Yes|Yes|Yes|Yes|Yes|Yes|
|Mission by Year Controls|Yes|Yes|Yes|Yes|Yes|Yes|



Notes: Individual controls include age, age squared, gender, and urban status. Geographical and historical controls are as shown in II. Mission by year controls consist of the presence of a Catholic mission within 25 kilometers and indicator variables for Protestant missions established in 25 year blocks beginning in 1805 and ending in 1930 for a total of 5 blocks. Standard errors are two-way clustered at the second administrative level and 0.5 decimal degree grid-cell. Underweight is defined as having a body mass index of less than 18.5. * _p <_ 0 _._ 10, ** _p <_ 0 _._ 05, *** _p <_ 0 _._ 01 

115 

Table A20: Intensive Margin of Bible Translation on Body Mass Index 

||Indigenous|Language|Permitted|Colonial|Language|Enforced|
|---|---|---|---|---|---|---|
||(1)|(2)|(3)|(4)|(5)|(6)|
|Minimal Translation (verses _<_3779)|0.065|||-0.240|||
||(0.060)|||(0.170)|||
|Gospels Translated (3779_≤_verses _<_7957)|0.141**|||0.065|||
||(0.061)|||(0.180)|||
|New Testament Translated (7957_≤_verses _<_31102)|0.073<br>(0.078)|||-0.032<br>(0.172)|||
|Full Bible Translated (verses _≥_31102)|0.312***|||-0.179|||
||(0.088)|||(0.200)|||
|Translation Site||-0.188|0.099*||-0.166|-0.093|
|||(0.239)|(0.055)||(0.671)|(0.206)|
|Log Translated Verses||0.035|||0.008||
|||(0.028)|||(0.074)||
|Translated Verses (1000s)|||-0.004|||0.002|
||||(0.006)|||(0.034)|
|Verses Squared (1000s)|||0.000*|||-0.000|
||||(0.000)|||(0.001)|
|Observations|446,893|446,893|446,893|189,591|189,591|189,591|
|Mean Dep. Var.|22.029|22.029|22.029|21.652|21.652|21.652|
|Country by Round FE|Yes|Yes|Yes|Yes|Yes|Yes|
|Individual Controls|Yes|Yes|Yes|Yes|Yes|Yes|
|Geographic Controls|Yes|Yes|Yes|Yes|Yes|Yes|
|Historical Controls|Yes|Yes|Yes|Yes|Yes|Yes|
|Mission by Year Controls|Yes|Yes|Yes|Yes|Yes|Yes|



Notes: Individual controls include age, age squared, gender, and urban status. Geographical and historical controls are as shown in II. Mission by year controls consist of the presence of a Catholic mission within 25 kilometers and indicator variables for Protestant missions established in 25 year blocks beginning in 1805 and ending in 1930 for a total of 5 blocks. Standard errors are two-way clustered at the second administrative level and 0.5 decimal degree grid-cell. * _p <_ 0 _._ 10, ** _p <_ 0 _._ 05, *** _p <_ 0 _._ 01 

116 

Table A21: Proximity to Bible Translation on Body Mass Index 

|Bufer size|15km<br>(1)|25km<br>(2)|35km<br>(3)|25km<br>(4)|25km<br>(5)|
|---|---|---|---|---|---|
|**Panel A: Indigenous Language **<br>Translation Site|**Permitted**<br>0.131***<br>(0.044)|0.112***<br>(0.041)|0.083**<br>(0.038)|||
|Log Distance to Translation Site||||-0.018<br>(0.048)|-0.019<br>(0.035)|
|Log Distance to Protestant Mission||||-0.114**<br>(0.051)|-0.119***<br>(0.035)|
|Log Distance to Catholic Mission||||-0.009<br>(0.043)|-0.054<br>(0.033)|
|Observations|446,623|446,893|446,999|42,734|90,661|
|Mean Dep. Var.|22.029|22.029|22.029|22.200|22.177|
|**Panel B: Colonial Language En**|**forced**|||||
|Translation Site|-0.222*<br>(0.133)|-0.098<br>(0.121)|-0.044<br>(0.103)|||
|Log Distance to Translation Site||||0.048<br>(0.079)|0.083<br>(0.060)|
|Log Distance to Protestant Mission||||-0.170*<br>(0.097)|-0.250***<br>(0.092)|
|Log Distance to Catholic Mission||||0.013<br>(0.100)|0.047<br>(0.078)|
|Observations|189,591|189,591|189,591|6,020|12,548|
|Mean Dep. Var.|21.652|21.652|21.652|22.441|22.229|
|Country by Round FE|Yes|Yes|Yes|Yes|Yes|
|Individual Controls|Yes|Yes|Yes|Yes|Yes|
|Geographic Controls|Yes|Yes|Yes|Yes|Yes|
|Historical Controls|Yes|Yes|Yes|Yes|Yes|
|Mission by Year Controls|Yes|Yes|Yes|No|No|
|Sample Restriction||||_<_ 50km|_<_ 100km|



Notes: Individual controls include age, age squared, gender, and urban status. Geographical and historical controls are as shown in II. Mission by year controls consist of the presence of a Catholic mission within 25 kilometers and indicator variables for Protestant missions established in 25 year blocks beginning in 1805 and ending in 1930 for a total of 5 blocks. Sample restriction indicates the distance from a translation site in order to be included in the sample. In column (4), only respondents within 50 kilometers of a translation site are included while column (5) restricts to 100 kilometers. Standard errors are two-way clustered at the second * ** *** administrative level and 0.5 decimal degree grid-cell. _p <_ 0 _._ 10, _p <_ 0 _._ 05, _p <_ 0 _._ 01 

117 

Table A22: Effects by Year of Birth on Body Mass Index 

||**ILP Co**<br>(1)|**untries**<br>(2)|**CLE C**<br>(3)|**ountries**<br>(4)|
|---|---|---|---|---|
|Translation Site|0.082<br>(0.232)||2.134***<br>(0.501)||
|Year of Birth - 1930|0.038***<br>(0.010)||0.107*<br>(0.057)||
|Translation * (Year of Birth - 1930)|0.001<br>(0.004)||-0.044***<br>(0.009)||
|P. Mission * (Year of Birth - 1930)|-0.015***<br>(0.002)||0.006<br>(0.007)||
|Translation * Born before 1950||-0.773<br>(1.651)||-0.314<br>(2.590)|
|Translation * Born 1950-1960||0.032<br>(0.153)||0.705**<br>(0.340)|
|Translation * Born 1960-1970||0.087<br>(0.098)||0.565**<br>(0.222)|
|Translation * Born 1970-1980||0.110*<br>(0.066)||0.283**<br>(0.131)|
|Translation * Born 1980-1990||0.123***<br>(0.045)||-0.399***<br>(0.149)|
|Translation * Born after 1990||0.122*<br>(0.066)||-0.575***<br>(0.143)|
|Observations|446,893|446,893|189,591|189,591|
|Mean Dep. Var.|6.060|6.060|2.697|2.697|
|Country by Round FE|Yes|Yes|Yes|Yes|
|Individual Controls|Yes|Yes|Yes|Yes|
|Geographic Controls|Yes|Yes|Yes|Yes|
|Historical Controls|Yes|Yes|Yes|Yes|
|Mission by Year Controls|Yes|Yes|Yes|Yes|
|Year of Birth Controls|No|Yes|No|Yes|
|Mission by YOB Controls|No|Yes|No|Yes|



Notes: Individual controls include age, age squared, gender, and urban status. Geographical and historical controls are as shown in II. Mission by year controls consist of the presence of a Catholic mission within 25 kilometers and indicator variables for Protestant missions established in 25 year blocks beginning in 1805 and ending in 1930 for a total of 5 blocks. Year of birth controls consist of indicator variables for the same year of birth categories shown in the table: before 1950, 1950-1960, 1960-1970, 1970-1980, 1980-1990, after 1990. Mission by YOB controls consist of the Protestant mission indicator interacted with the year of birth categories. Standard errors are two-way clustered * ** *** at the second administrative level and 0.5 decimal degree grid-cell. _p <_ 0 _._ 10, _p <_ 0 _._ 05, _p <_ 0 _._ 01 

118 

##### **Appendix Figures** 

119 

### (CHI)BEMBA 

#### 130 

UBUTENDEKO bwe landwe lisuma lya kwa Yesu Klistu, Mwana Lesa. E fintu chyalembwa muli Esaya kasesema, achiti, Mona, ndetuma nkombe yandi ku ntanshi ya Uyo[shiwimensowalate **y** anyoobe, musebo obe; lya umo ulebilikishya mu chiswebebe, Teyanyeni musebo wa Mfumu, Lunyjikeni nshila shyakwe. Yoane aishile, uyo wabatishile mu chiswebebe, na uyo washimikile ububatiso bwa bulapilo pa kufulunganya kwa mpulumushi, Nga kwafumine Mk i.1-4 1965 

The Bemba language is spoken over a large part of Zambia (particularly in the Copper Belt, where it is the lingua franca) and by groups in adjacent areas of Katanga Province of CongoKinshasa. It is used officially throughout much of northern and north-central Zambia, where, under Government sponsorship, a vernacular literature is being developed. A Bantu tongue, ChiBemba is related to IchiWiza, IchiLala, and IchiLamba. 

1904 John National BS of<sup>Scotland</sup> 

Translated by Daniel Crawford, Garenganze Mission. 

1906Mark 1910 Ephesians 1-3John BFBS Translated by Henry C. Nutter, William Freshwater, and Ernest W’. Lewis, London MS. 

###### 1911 Gospels NBSS 

Translated by Dugald Campbell, Garenganze Mission. 

1913. Acts 1914Matthew Philemon Jude 1915 Luke 1916 New Testament Psalms BFBS Translated by H, C, Nutter, W’. Freshwater, andE. W’, Lewis. 



<!-- Start of picture text -->
-\ — T _ ~ )<br>iey a at,<br>SA \ , \<br>\ F SP — wt<br>J ! AOSokoto X Nee yw a ‘ =~ S y ee 7<br>JA A [a<br>( A N<br>wnarm '1 Gusau<br>‘ f ° Kano 5<br>Ln ¢ ey Maidug<br>I<br>y<br>\ faeia<br>\¢<br>)I<br>\}n Kaduna 1g<br>{~ a NIGERIA . 1923 }<br>1923 Bauchi Gombe @<br>IN \ 2 @ ° ° eo<br>a~ ,4 1904 @ 1919i906 1915@ 281920194 7 ©ees e ..°on 1924@1916 %4~<br>J Oo eu1909 gal915 1910 1923@ @1912 1907 s910 @1919 isi3 Zs:<br>‘ 1906 2) (3) s 3) @ A) Pie ou x} y, Garc<br>—_, f 1g99 @ 1911 1903 Abuja oe 1906 ey” 1923 f a<br>1919<br>ii 1902 )Oooe” —_© ©21S © YW @ A x x) x)1923 Bo|j<br>‘i @ 1917 ghtorin 1915 [o) @ —<br>g\.j S1892@r.e1856eo >yaoe1911© e reget13979 19085630@ is22e- .1919? envie :219071906eo” f }}f°:<br>[ S 185 on ee a” . 1922 1923 ry @is11 1<br>t eis @1895 — 1876 Oo1899e @ @ Oo %,,,5 1911e- “J oN<br>1 @ = - 7 1924 y Af or<br>otongul\2 4852ekaad =os A Benin:: a 913 “ite° J af 4 ‘-<? ?‘hsae, yé<br>184 01 @ 9 18575  "ap 19111904 Pia@1912isso fe rd pa  bamenda<br>Warri_ A 1890 8 600 4<br>Bightight of ow @i912ofl 91910 1920®%@ oe:111883od(,y CAMEROON<br>Benin a © Port‘Evo 2, 18461895 \7 ‘<br>1828 1911 1908 E<br>@ a<br>co 1887<br>H i @ cMML @ sBc py<br>Translation Sites Malas Yaoundé<br>Full . @ cms @ SDA ><br>Translation @ RCSA @ sm<br>a me @ GBB @ suM<br>wd @ msc @ urs<br>Mission Stations @ nsc @ uMsM<br>Society. Gul: hd PMMS @ WMMS oe ;<br>@ pFBs “'2@ QIM A Catholic Missions a 2aoa —<br>@ sA Esri, TomTom, Garmin, FAO, NOAA, USGS<br>\ 9<br>EQUATORIAL ! f<br><!-- End of picture text -->



<!-- Start of picture text -->
“7<br>ca ae<br>i ee =>er i¥ bs<br>oe ee Gera i 8<br>os ee<br><!-- End of picture text -->



<!-- Start of picture text -->
° 307 __ Translation Treatment ; . . .<br>© — Control '<br>oO 1<br>> 1<br>© 1<br>om 25 1<br>&>'I<br>Q i<br>=i<br>Q20<br>xEi1<br>Q;<br>é |<br>=<br>te 1<br>£i<br>”10 ey é<br>c ;<br>a1<br>o1<br>LLe) i1<br>> 8 3 |<br>ra)<br>ne}<br>5<br>2 S 1<br>0 ~~<br>ass<br>-30 -25 -20 -15- -10 -5 0 5 10 15 20 25 30 35 40<br>Years since Publication<br><!-- End of picture text -->



<!-- Start of picture text -->
20 oe nae<br>2 15<br>ao} ;<br>© 1<br>Ee 1<br>x 1<br>lo 1<br>Ni<br><10<br>5 ' @ All<br>2 MCLE<br>2 A ILP<br>6 5<br>Le 1<br>ie) '<br>a) '<br>no} 1<br>E<br>assrs |<br>-4 -3 -2 -1 0 1 2 3 4 5<br>Periods since Translation Publication<br><!-- End of picture text -->



<!-- Start of picture text -->
S 10<br>E<br>is 1<br>Ni<br>5 @ All<br>3 A ILP<br>ig<br>ie) '<br>--|-3-<br>E 0 ¢ = — — -OnA -- —— — Sep ee rH<br>Zz ;<br>assrs |<br>-4 -3 -2 -1 0 1 2 3 4 5<br>Periods since Translation Publication<br><!-- End of picture text -->



<!-- Start of picture text -->
30 ;<br>o i<br>=} '<br>S 20 '<br>fo)x=i!!<br>re) i<br>£<br>‘5 @ All<br>2 10 me re ‘ ppd : M@ CLE<br>o 1<br>LL ;<br>° : A ILP<br>3|<br>E ee ee<br>Zz 0 — 4 — om —: SS<br>-10 ;<br>assae<br>-4 -3 -2 -1 0 1 2 3 4 5<br>Periods since Translation Publication<br><!-- End of picture text -->



<!-- Start of picture text -->
o i<br>=}<br>Tw I!<br>£<br>E<br>5 5 |<br>N<br>£<br>‘5 @ All<br>2 MH SameSociety<br>2 A OtherSocieties<br>re !<br>LL<br>©<br>no} 1<br>Ee 1<br>5 !<br>Zz<br>5i<br>a<br>-4 -3 -2 -1 0 1 2 3 4 5<br>Periods since Translation Publication<br><!-- End of picture text -->



<!-- Start of picture text -->
10<br>o i<br>=) '<br>To 1<br>£<br>E<br>rn<br>NI<br>£<br>5 ' @ All<br>2 HH TranslationSite<br>2 A OtherStations<br>o I<br>LL i<br>o '<br>ne} 1<br>E '<br>5S I<br>Zz ;<br>5 '<br>rs<br>-4 -3 -2 -1 0 1 2 3 4 5<br>Periods since Translation Publication<br><!-- End of picture text -->



<!-- Start of picture text -->
10<br>oi<br>2<br>To 1'<br>g<br>E<br>rn<br>N I<br>[=<br>is @ All<br>2 HM SameLanguage<br>3 A OtherLanguage<br>ro) 1<br>Le i<br>o 0 a- Om -- —}& —— A — po<br>3<br>E 1<br>5S I<br>Zz<br>5 1<br>ressrs rs rs es |<br>-4 -3 -2 -1 0 1 2 3 4 5<br>Periods since Translation Publication<br><!-- End of picture text -->



<!-- Start of picture text -->
25<br>wn 20 i<br>me) '<br>© '<br>Ee '<br>3s 1<br>0 15 '<br>[=<br>‘S @ Al<br>2 HM SameLanguage<br>2 10 A OtherLanguage<br>o I<br>LL<br>‘S<br>g<br>9<br>e<br>Zz=) ' :<br>—<br>-4 -3 -2 -1 0 1 2 3 4 5<br>Periods since Translation Publication<br><!-- End of picture text -->



<!-- Start of picture text -->
3 3<br>—& 2<br>iSN;<br>@ All<br>5<br>5 | M@ CLE<br>5 A ILP<br>gz '<br>—E '<br>=} 1<br>=2 0 Heth 4 ome pS he ee pte —— _<br>-4<br>rT,<br>-4 -3 -2 -1 0 1 2 3 4 5<br>Periods since Translation Publication<br><!-- End of picture text -->

# i1 



<!-- Start of picture text -->
o '<br>5S 1<br>ie)©1<br>E ;<br>Te}xN11'<br>& 1<br>oi<br>8<br>jo} 1<br>Q '1<br>c '<br>aD 1<br>o 1<br>fo) '<br>We 1<br>ie)oO 0} — +h; Sate Sain Unies (ented Ge<br>®'<br>a 1<br>=<br>=) 1<br>4<br>—S——— sr rr er<br>-4 -3 -2 -1 0 1 2 3 4 5<br>Periods since Translation Publication<br><!-- End of picture text -->



<!-- Start of picture text -->
o i<br>=} i<br>Tw 1<br>S|<br>E<br>5<br>5 1<br>N'<br>=<br>‘5 @ All<br>2 MH Female<br>ro) t<br>LL '<br>rf u A Male<br>© '<br>no} 1<br>Ee51t<br>zi<br>5t<br>a|<br>-4 -3 -2 -1 0 1 2 3 4 5<br>Periods since Translation Publication<br><!-- End of picture text -->

- omOS eae \ Kee 

- Nes ea eerAIS aN ES aes 



<!-- Start of picture text -->
ILP Countries CLE Countries<br>With translation:<br>Indigenous Lol<br>< <<br>oO . . oO . :<br>€ | Without translation E Without translation<br>‘=! Colonial Lol = Colonial Lol<br>=z =z<br>ry ©<br>Cc Cc<br>2 ne)<br>i} ®<br>5 5 With translation:<br>2 2 i ranslation:<br>mw uw Colonial Lol<br>1 2 3 1 2 3<br>Lol Spheres of Use Lol Spheres of Use<br><!-- End of picture text -->



<!-- Start of picture text -->
.02<br>.015<br>2<br>cot<br>{0}<br>Q<br>.005<br>0<br>0 2 4 6 8<br>Grade<br><!-- End of picture text -->



<!-- Start of picture text -->
05<br>> | . @ All<br>5 0 —2H— e - oath Te —— @-|--l4--+-—41— mm cle<br>4 n A ILP<br>=.05 0 forrrrren ? Serciiniinnnaanniin<br>[24,22] [21,19] [18,16] [15,13] [12,10] [9,7] [6,4] [8,1] [0-2] [-3,-5] [-6,-8]<br>Age at Publication<br><!-- End of picture text -->



<!-- Start of picture text -->
05<br>><br>S '<br>E 3<br>es @ Al<br>3 0 —+H- oF — oma -F —— —i,——4—— MCLE<br>a. ° A ILP<br>[o) 1<br>v& n<br>[24,22] [21,19] [18,16] [15,13] [12,10] [9,7] [6.4] [3,1]  [0,-2] [-3,-5] [-6,-8]<br>Age at Publication<br><!-- End of picture text -->





## Data
## Codebook








Afrobarometer Round 10 Survey in
## 38 Countries  Merged Codebook

Prepared by Alfred Torsu, August, 2026


## User Guide

## About
Afrobarometer (AB) is a pan-African, non-partisan survey research network that conducts public attitude
surveys on democracy, governance, the economy, and society. We are the world’s leading source of high-
quality data on what Africans are thinking.

Our vision is “A world in which Africa’s development is anchored in the realities and aspirations of its
people”.

AB is a non-profit company limited by guarantee with headquarters in Accra, Ghana.

For more information about Afrobarometer, visit our  https://www.afrobarometer.org/about/

## Citation
Afrobarometer data are protected by copyright. Authors of any published work based on Afrobarometer
data or papers are required to acknowledge the source, including, where applicable, citations to data sets
posted on the website. Please acknowledge the copyright holders in all publications resulting from the use
of Afrobarometer data by means of bibliographic citation in this form:

Afrobarometer Data, [Country(ies)], [Round(s)], [Year(s)], available at http://www.afrobarometer.org.

We also ask users to send/email copies of any publications, papers, or reports that employ Afrobarometer
data to Brian Howard, Afrobarometer’s head of publications, at bhoward@afrobarometer.org

## Data Weights
Afrobarometer includes four weights in our datasets. Two weights are used in all country-level datasets,
and an additional two weights are used in our multi-country, merge datasets for each round. The
withinwt_ea and withinwt_hh weights correct for over-and under-sampling at the national level. Each
respondent is assigned a weight based on the inverse of their probability of selection, accounting for factors
like geographical region and urban-rural distribution. The difference between the two withinwt variables is
that while withinwt_ea accounts for enumeration population size, withinwt_hh factors in enumeration
population AND household size, and is not available for earlier rounds of the survey.

In each merge dataset, we have two additional weight variables, combinwt_ea and combinwt_hh. These
weight variables are based on the withinwt_ea and withinwt_hh variables, but they also standardise all
national samples in the merge dataset so that each country has equal weight in the continental average.

In general, a weighting variable should be used when reporting national (withinwt_ea or withinwt_hh) or
cross-national (combinwt_ea or combinwt_hh) results to ensure accuracy and reliability when making
generalisations or drawing conclusions at the national level or multi-country level.
For more information on Afrobarometer sampling protocols and weight construction, please visit our
webpage

NOCALL Variables (Unit non-response)


In Afrobarometer surveys, interviewers record unsuccessful household calls as a “NOCALL”. Reasons for
unsuccessful calls may include (but are not limited to) refusals to interview by the selected respondent or
household members, absence of the randomly selected respondent, or respondents not meeting the
selection criteria (citizens over the age of 18 who speak one of the survey languages). These NOCALLs are
recorded as variables embedded in each successful case. If interviewers have five unsuccessful calls before a
successful interview, users will find that NOCALL1 to NOCALL5 contain the reasons for the unsuccessful calls
before the successful interview.

Non-response coding
Afrobarometer utilises a standardised set of non-response codes across all questions and surveys. They are
as follows:
- Missing=-1 (no “system missing” data or empty cells)
- Don’t know= 9, 99, 999 or 9999
- Refused to answer=8, 98, 9998 or 9998
- Not Applicable=7, 97, 997 or 9997
- No Further Response/Answer=96, 996 or 9996
- Not asked in country=9994

Computed variables:
AB data sets include three computed variables that are Afrobarometer’s signature indicators
of Lived Poverty, Demand for Democracy, and Supply of Democracy, each of which is
described below.

Lived Poverty Index (LPI):

“As a contribution to the tracking of poverty in Africa, Afrobarometer offers
the Lived Poverty Index (LPI), an experiential measure that is based on a
series of survey questions about how frequently people actually go without
basic necessities during the course of a year. The LPI measures a portion of
the concept of poverty that is not captured well by other measures, and thus
offers an important complement to official statistics on poverty and
development (Mattes, 2008)”
## 1
## .

The LPI is computed both as a raw average of the frequency with which respondents go
without five basic necessities (Q7A-E), and as a categorial variable that groups respondents
as experiencing no, low, moderate or high lived poverty.

The following syntax is used to generate these two variables (in .sps format).

## RECODE

## 1
Mattes, R. “The Material and Political Bases of Lived Poverty in Africa: Insights from the Afrobarometer”,
afrobarometer.org, 2008, https://www.afrobarometer.org/wp-content/uploads/2022/02/AfropaperNo98.pdf.
See also Mattes, R and Patel, J. “Lived Poverty Resurgent: COVID-19 restrictions feed economic contraction to
drive down living standards in Africa”, Afrobarometer.org, 2022, https://www.afrobarometer.org/wp-
content/uploads/2022/12/PP84-PAP19-Lived-poverty-resurgent-Afrobarometer-Pan-Africa-Profile-
## 31dec22.pdf



## Q7A Q7B Q7C Q7D Q7E(0=0) (1=1) (2=2) (3=3) (4=4)  (ELSE=SYSMIS) INTO
q7a_r q7b_r q7c_r q7d_r q7e_r .
## VARIABLE LABELS
q7a_r 'Go W/O Food'
q7b_r 'Go W/O Water'
q7c_r 'Go W/O Medical Care'
q7d_r 'Go W/O Cooking Fuel'
q7e_r 'Go W/O Cash Income'.
## EXECUTE.

COMPUTE LivedPoverty = (q7a_r + q7b_r + q7c_r + q7d_r + q7e_r)  / 5.
VARIABLE LABELS LivedPoverty 'Lived Poverty Index (average index of 5 poverty items)'.
## EXECUTE.

- Recode LPI to the categorical variable.

## RECODE
LivedPoverty
(0=0) (0.2 thru 1.0 =1) (1.2 thru 2.0 = 2) (2.2 thru 4.0 =3) INTO
LivedPoverty_CAT.
VARIABLE LABELS LivedPoverty_CAT 'LPI_Categorical'.
VALUE LABELS LivedPoverty_CAT 0 "No Lived Poverty" 1 "Low Lived Poverty" 2 "Moderate Lived Poverty"
3 "High Lived Poverty".
## EXECUTE.

Format LivedPoverty_CAT(F3.0).
## EXECUTE.

Demand for Democracy (DemandDemo):
DemandDemoI’ is a long-standing Afrobarometer indicator that combines explicit support
for democracy (Q22) with rejection of all three non-democratic alternatives (Q21) – one-
party rule, military rule, and strongman/one-man rule – using the following syntax:

## RECODE
Q21A Q21B Q21C (5=0) (4=0) (3=0) (2=1) (1=1) (9=0) (ELSE = SYSMIS) INTO q21a_r1 q21b_r1 q21c_r1  .
## VARIABLE LABELS
q21a_r1 'reject 1 party rule, no-yes'  /
q21b_r1 'reject military rule, no-yes' /
q21c_r1 'reject pres dictatorship, no-yes'  .
## EXECUTE.

**** compute DEMAND FOR DEMOCRACY

COMPUTE DemandDemo = (q22_r1 +  q21a_r1 +  q21b_r1 + q21c_r1 ).
VARIABLE LABELS DemandDemo 'Demand for Democracy (additive index of 4 democratic commitments:
support (1,2=0)(3=1)(else=sysmis) + reject (5,4,3,9=0)(2,1=1)(else=sysmis)' .
VALUE LABELS  DemandDemo 0 "No demand for democracy" 1 "Agrees w/ 1 of 4 components" 2 "Agrees w/ 2
of 4 components"
3 "Agrees w/ 3 of 4 components" 4 "Full demand for democracy".
## EXECUTE .

Supply of Democracy (SupplyDemo):



SupplyDemo combines the indicators of perceived extent of democracy (Q32) and
satisfaction with the way democracy works (Q33) to provide a single indicator of the extent
to which governments are supplying democracy to their citizens. The syntax is as follows:

## RECODE
Q32 (1=0) (2=0) (9=0) (8=0) (3=1) (4=1) (ELSE=SYSMIS) INTO q32_r1.
VARIABLE LABELS q32_r1 'how democratic is govt recoded, 0-1, dk=0'.
## EXECUTE.


## RECODE
Q33 (0=0) (1=0) (2=0) (9=0) (3=1) (4=1) (ELSE=SYSMIS) INTO q33_r1.
VARIABLE LABELS q33_r1 'satisfaction with democracy recoded, 0-1)'.
## EXECUTE.


COMPUTE SupplyDemo = (q32_r1 + q33_r1).
VARIABLE LABELS SupplyDemo 'Supply of Democracy (additive index of 2 items: satisfaction
(0,1,2,9=0)(3,4=1)(else=sysmis) + extent (1,2,8,9=0)(3,4=1)(else=sysmis)'.
VALUE LABELS  SupplyDemo 0 "Perceives no supply" 1 "Perceives supply of one, not both" 2 "Perceives full
supply of democracy (Extent +Satisfaction)".
## EXECUTE.

Format  SupplyDemo  (F3.0).
## EXECUTE.

Limitations of Afrobarometer Data
Afrobarometer uses national probability sampling designed to generate a sample that is a representative
cross-section of all citizens aged 18 and above. Samples usually include either 1,200 or 2,400 cases. A
randomly selected sample of n=1,200 cases allows inferences to national adult populations with a margin
of sampling error of +/-2.8 percentage points with a confidence level of 95%. With a sample size of n=2,400,
the margin of error decreases to +/-2.0 percentage points at a 95% confidence level.  The margins of error
will increase for sub-national groups (regions, demographic groups, etc.). While efforts are made to
minimize nonresponse, some biases may exist if certain groups are underrepresented in the final sample.



## Codebook
## URBRUR
## Value Count
Label Urban or Rural Primary Sampling Unit
## Type Numeric
## Measurement Nominal
## 1 Urban 22486
## 2 Rural 22396
3 Peri-Urban 718

## COUNTRY
## Value Count
## Label Country
## Type Numeric
## Measurement Nominal
## 1 Algeria 0
## 2 Angola 1200
## 3 Benin 1200
## 4 Botswana 1200
## 5 Burkina Faso 0
## 6 Burundi 0
## 7 Cabo Verde 1200
## 8 Cameroon 1200
## 9 Central African Republic 0
## 10 Chad 1200
## 11 Comoros 1200
12 Democratic Republic of the Congo 0
13 Congo-Brazzaville 1200
14 Côte d'Ivoire 1200
## 15 Djibouti 0
## 16 Egypt 0
## 17 Equatorial Guinea 0
## 18 Eritrea 0
## 19 Eswatini 1200
## 20 Ethiopia 0
## 21 Gabon 1200
## 22 Gambia, The 1200
## 23 Ghana 1200
## 24 Guinea 1200
25 Guinea-Bissau 1200
## 26 Kenya 1200
## 27 Lesotho 1200


## 28 Liberia 1200
## 29 Libya 0
## 30 Madagascar 1200
## 31 Malawi 1200
## 32 Mali 1200
## 33 Mauritania 1200
## 34 Mauritius 1200
## 35 Morocco 1200
## 36 Mozambique 1200
## 37 Namibia 1200
## 38 Niger 0
## 39 Nigeria 1200
## 40 Rwanda 0
41 São Tomé and Príncipe 1200
## 42 Senegal 1200
## 43 Seychelles 1200
## 44 Sierra Leone 1200
## 45 Somalia 0
## 46 South Africa 1200
## 47 South Sudan 0
## 48 Sudan 0
## 49 Tanzania 1200
## 50 Togo 1200
## 51 Tunisia 1200
## 52 Uganda 1200
## 53 Zambia 1200
## 54 Zimbabwe 1200

## COUNTRY.BY.REGION
## Value Count
Label Country by Region
## Type Numeric
## Measurement Nominal
## 1 West Africa 16800
## 2 East Africa 8400
## 3 Southern Africa 12000
## 4 North Africa 3600
## 5 Central Africa 4800

## COUNTRY.BY.REGION.AU
## Value Count
Label Country by Region (AU Classification)
## Type Numeric


## Measurement Nominal
## 1 West Africa 16800
## 2 East Africa 9600
## 3 Southern Africa 10800
## 4 North Africa 3600
## 5 Central Africa 4800

## COUNTRY.BY.REGION.UN
## Value Count
Label Country by Region (UN Classification)
## Type Numeric
## Measurement Nominal
## 1 West Africa 16800
## 2 East Africa 12000
## 3 Southern Africa 7200
## 4 North Africa 3600
## 5 Central Africa 6000

## REGION

## Value

Label Province or region

## Type Numeric

## Measurement Nominal


## REGION_NEW_BOT
## Value Count
Label Grouping of Census Districts by Administrative
Districts: Urban centers and regional districts
(Botswana Only)

## Type Numeric
## Measurement Nominal
## 140 SOUTHERN 114
## 141 CENTRAL 333
## 142 NORTH WEST 114
## 143 GHANZI 29
## 144 FRANCISTOWN 53
## 145 GABARONE 126
## 146 JWANEG 10
## 147 KGALAGADI 30
## 148 KGALTENG 62
## 149 KWENENG 200
## 150 LOBATSE 15
## 151 NORTH EAST 35


## 152 SELIBE PHIKWE 22
## 153 SOUTH EAST 57
## Missing
## Values
## System   44400

## LOCATION.LEVEL.1

## Value

## Label Location Level 1

## Type String

## Measurement Nominal


## LOCATION.LEVEL.2

## Value

## Label Location Level 2

## Type String

## Measurement Nominal


## LOCATION.LEVEL.3

## Value

## Label Location Level 3

## Type String

## Measurement Nominal


## LOCATION.LEVEL.4

## Value

## Label Location Level 4

## Type String

## Measurement Nominal


## LOCATION.LEVEL.5

## Value

## Label Location Level 5

## Type String

## Measurement Nominal


## TOWNVILL

## Value

Label EA Name

## Type String

## Measurement Nominal




## MUNI_NAME

## Value

Label Name of the municipality/locality

## Type String

## Measurement Nominal


## CONST_NAME

## Value

Label Name of the electoral district

## Type String

## Measurement Nominal


## EA_GPS_LA

## Value

Label GPS Latitude in EA

## Type Numeric

## Measurement Scale

## Valid 45600

## Missing 0

## Mean -0.8571520995


## EA_GPS_LO

## Value

Label GPS Longitude in EA

## Type Numeric

## Measurement Scale

## Valid 45600

## Missing 0

## Mean 13.8281494024


## EA_GPS_OTHER
## Value Count
Label GPS in EA captured using other software
## Type String
## Measurement Nominal
## 45600

## EANUMB

## Value

Label EA Number

## Type Numeric

## Measurement Nominal




## EANUMB_AB

## Value

Label EA Unique Number

## Type Numeric

## Measurement Nominal


## EA_COMMENT
## Value Count
Label Supervisor comment about the EA
## Type String
## Measurement Nominal
## 44566
## 80% ON THE BEACH,
## THE REST IN
## INDEPENDENCE
## SQUARE AND THE
## MIRAMAR HOTEL
## 8
## ACCESS TO THE EA
## WAS DENIED, AN
## EMAIL REQUEST WAS
## SENT BUT NO
## RESPONSE RECEIVED
## 1
## ÁREA SELECIONADA
## INABITADA
## 7
## BLOCAGE
## ADMINISTRATIF,
## RÉSIDENCE DES
## HAUTES AUTORITÉS
## 12
## BLOCAGE PAR LE
## MARABOUT, REFUS
## D’ENQUÊTE
## 9
## COMPLETELY
## DESERTED, ONLY 2
## BARNS USED
## OCCASIONALLY
## 6
## COMPLETELY
## DESERTED, VERY FAR
## FROM DISTRICT HQ,
## VERIFIED NO ONE
## LIVES THERE
## 12


## COMPLETELY
## INACCESSIBLE,
## FENCED, NO ONE
## LIVES THERE
## 10
## COMPLETELY
## UNINHABITABLE,
## COVERED BY
## NHANGAU FOREST
## AND AGRICULTURE
## AREA
## 13
## COULD NOT FIND EA.
## LANDMARKS ON
## MAP NOT VISIBLE
## 2
## DIFÍCIL ACESSO COM
## TRANSPORTE RARO
## 10
## EA FULL OF SHOPS,
## FEW HOUSEHOLDS
## 10
## EA HAS 36
## HOMESTEADS
## 7
## EA HAS FEW
## HOMESTEADS
## 11
## EA HAS FEW
## HOUSEHOLDS,
## INCLUDES POLICE
## AND MILITARY
## HOUSING
## 2
## EA IN CITY BUSINESS
## DISTRICT WITH
## POLICE HOUSING,
## TOO FEW
## HOMESTEADS FOR
## SURVEY
## 8
## EA IN CITY BUSINESS
## DISTRICT, ONE ROYAL
## COMPANY BLOCK,
## ACCESS DENIED
## AFTER
## QUESTIONNAIRE
## REVIEW
## 6
## EA IN CITY
## INDUSTRIAL AREA,
## MOST RESIDENTS
## RELOCATED,
## REMAINING TOO
## FEW FOR SURVEY
## 31


## EA IN TOWN
## BUSINESS DISTRICT,
## FEW HOUSEHOLDS
## 7
## EA INSIDE RIVER,
## PEOPLE LIVE ONLY
## ALONG RIVERBANK
## OUTSIDE BOUNDARY
## 13
## EA UNREACHABLE
## DUE TO BRIDGE CUT
## OFF
## 8
## EA UNREACHABLE
## DUE TO HEAVY
## RIVER.
## 13
## ENTIRE EA OCCUPIED
## BY MAPUTO
## RESERVE, NO
## INHABITANTS
## 5
## ENTIRELY FENCED,
## NO HOUSEHOLDS
## 9
## ENTRY WAS REFUSED
## AT THE EA
## 4
## ENTRY WAS REFUSED
## AT THE EA, AN EMAIL
## REQUEST WAS SENT
## BUT THERE WAS NO
## RESPONSE
## 1
## GATED COMMUNITY
## NEEDING
## PRESIDENTIAL
## PERMISSION
## 12
## INACCESSIBLE EA   22
## INSECURITÉ
## (GROUPES ARMÉS VS
## ARMÉE NATIONALE)
## 173
## INSECURITY   22
## LA ZD A ÉTÉ
## REMPLACÉE EN
## RAISON DE
## L'INSÉCURITÉ
## 7
## LA ZD A ÉTÉ
## SUBSTITUÉE CAR LA
## POPULATION A DÉJÀ
## DÉSERTÉ LA LOCALITÉ
## 8


## LAND WAS BOUGHT
## OFF AND SO PEOPLE
## VACCATED THE AREA
## 3
## LAND WRANGLES IN
## THE EA. THE PEOPLE
## CHASED THE
## FIELDWORKERS
## AWAY
## 3
## LOCALITÉ NON
## ACCESSIBLE (PONT
## DÉTRUIT PAR LES
## PLUIES)
## 9
## LOGISTICAL
## DIFFICULTY
## 11
## LOGISTICAL
## DIFFICULTY, SAFETY
## ON WATER
## 27
## MÉNAGES
## INSUFFISANTS
## 44
## MOST HOMES ARE
## CATTLE POSTS
## 7
## MOST HOMES ARE
## HOLIDAY RENTALS
## 17
## NEVER INHABITED,
## ONLY MOUNTAINS
## 8
## NO MAP FOR THAT
## EA
## 6
## NO PERMANENT
## HOUSEHOLDS WERE
## FOUND
## 2
## NO SETTLEMENTS IN
## THE EA
## 16
## NOT ENOUGH
## HOUSEHOLDS TO
## CONDUCT 8
## INTERVIEWS
## (BUSINESS AREA)
## 6
## ON N'A PAS TROUVÉ
## LA ZD
## 19
## ONLY 4 HOUSEHOLDS
## FOUND, CARETAKERS
## ONLY, REFUSED TO
## PARTICIPATE
## 8


## ONLY ARTISANAL
## MINERS PRESENT,
## TEAM ATTACKED,
## AUTHORITIES
## ADVISED NOT TO
## RETURN
## 13
## ORIGINAL EA
## INACCESSIBLE
## 15
## ORIGINAL EA
## INSECURE
## 4
## POLICE CAMP,
## MAKING
## PERMISSIONS HARD
## TO OBTAIN.
## 6
## POPULATION
## DISPLACED
## (TERRORIST ATTACK)
## 29
## POPULATION LEFT 3
## YEARS AGO DUE TO
## TERRORIST THREATS,
## AREA NOW
## DESERTED FOREST
## 7
## POPULATION
## RESETTLED DUE TO
## SESAME
## PLANTATION, ONLY 4
## CARETAKER
## HOUSEHOLDS
## FOUND
## 7
## REFUS POUR
## EXTREMISTE
## RELIGIEUX
## 8
## SECURITY SECTOR   7
## THE AREA IS AN OLD
## RETIRED VILLAGE
## WITH PRIVATE
## RESIDENCES ONLY,
## SECURITY MANAGER
## CONSENT IS
## REQUIRED AND
## ACCESS WAS DENIED
## 1
## THE EA CONSISTS OF
B&Bs, GUEST
## HOUSES, A GOLF
## 1


## COURSE, AND A
## LODGE
## THE EA HAS CHINESE
## RESIDENTS WHO ARE
## NOT SA CITIZENS
## AND DO NOT MEET
## SURVEY CRITERIA
## 0
## THE EA IS A
## BARRACKS
## 2
## THE EA WAS IN AN
## ARMY BARRACKS,
## AND WE WERE NOT
## ALLOWED TO
## CONDUCT
## INTERVIEWS
## 6
## THE ORIGINAL EA
## INCLUDED PRISONS,
## GOVERNMENT
## OFFICES, AND
## BUSINESSES
## 14
## THE ORIGINAL EA
## WAS
## INSTITUTIONALIZED
## 10
## THE ORIGINAL EA
## WAS NON-
## RESIDENTIAL
## 11
## THE ORIGINAL EA
## WERE
## INSTITUTIONAL
## HOUSEHOLDS
## 6
## THE PRIMARY EA IS A
## MINING AND
## INDUSTRIAL AREA
## 2
## THERE WAS NO SIGN
## OF LIFE IN THE EA
## 0
## UNINHABITABLE,
## LOCATED IN SUGAR
## CANE FIELDS OF
## MAFAMBISSE
## 10


## WORRIERS
## ATTACKED THE
## VILLAGE AND THE
## PEOPLE WERE
## DISPLACED
## 15
## ZD INACCESSIBLE   131
## ZD INACCESSIBLE À
## CAUSE
## D'INONDATION
## 5
## ZONE À RISQUE   45
## ZONE D'INSÉCURITÉ,
## HABITÉE PAR DES
## DAHALO, ENCLAVÉE
## AVEC INTERDITS
## CULTURELS,
## INACCESSIBLE.
## 6
## ZONE D'INSÉCURITÉ,
## HABITÉE PAR DES
## DAHALO,
## INACCESSIBLE.
## 4
## ZONE D'INSÉCURITÉ,
## HABITÉE PAR DES
## DAHALO, SANS
## TRANSPORT.
## 8
## ZONE INACCESSIBLE
## EN RAISON DE LA
## MONTÉE DU FLEUVE
## CONGO
## 4

## EA_SVC_A
## Value Count
Label EA-SVC-A. Electricity grid in the PSU/EA
## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 0 No 12833
## 1 Yes 32596
9 Can't determine 135

## EA_SVC_A_GPS_LA
## Value Count
Label EA-SVC-A-GPS-LA. Electricity grid in the PSU/EA: GPS
## Latitude

## Type Numeric


## Measurement Scale
## Valid 45600
## Missing 0
## Mean 2842.5523566166
## -1.00000000 Missing 35
## .00000000 No 3621
9997.00000000 Not applicable 12969

## EA_SVC_A_GPS_LO
## Value Count
Label EA-SVC-A-GPS-LO. Electricity grid in the PSU/EA: GPS
## Longitude

## Type Numeric
## Measurement Scale
## Valid 45600
## Missing 0
## Mean 2852.4022053136
## -1.00000000 Missing 35
## .00000000 No 3621
9997.00000000 Not applicable 12969

## EA_SVC_A_PHOTO
## Value Count
Label EA-SVC-A-PHOTO. Electricity grid in the PSU/EA: Photo
## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 0 No 11873
## 1 Yes 20723
7 Not applicable 12969

## EA_SVC_B
## Value Count
Label EA-SVC-B. Piped water system in the PSU/EA
## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 0 No 21187
## 1 Yes 23667
9 Can't determine 712

## EA_SVC_B_GPS_LA
## Value Count


Label EA-SVC-B-GPS-LA. Piped water system in the PSU/EA:
GPS Latitude

## Type Numeric
## Measurement Scale
## Valid 45600
## Missing 0
## Mean 4800.9852320693
## -1.00000000 Missing 35
## .00000000 No 5178
9997.00000000 Not applicable 21898

## EA_SVC_B_GPS_LO
## Value Count
Label EA-SVC-B-GPS-LO. Piped water system in the PSU/EA:
GPS Longitude

## Type Numeric
## Measurement Scale
## Valid 45600
## Missing 0
## Mean 4806.3037577874
## -1.00000000 Missing 35
## .00000000 No 5178
9997.00000000 Not applicable 21898

## EA_SVC_B_PHOTO
## Value Count
Label EA-SVC-B-PHOTO. Piped water system in the PSU/EA:
## Photo

## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 0 No 12604
## 1 Yes 11063
7 Not applicable 21898

## EA_SVC_C
## Value Count
Label EA-SVC-C. Sewage system in the PSU/EA
## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 0 No 32959
## 1 Yes 11225


9 Can't determine 1381

## EA_SVC_C_GPS_LA
## Value Count
Label EA-SVC-C-GPS-LA. Sewage system in the PSU/EA: GPS
## Latitude

## Type Numeric
## Measurement Scale
## Valid 45600
## Missing 0
## Mean 7528.7931667338
## -1.00000000 Missing 35
## .00000000 No 2923
9997.00000000 Not applicable 34340

## EA_SVC_C_GPS_LO
## Value Count
Label EA-SVC-C-GPS-LO. Sewage system in the PSU/EA: GPS
## Longitude

## Type Numeric
## Measurement Scale
## Valid 45600
## Missing 0
## Mean 7530.5633395581
## -1.00000000 Missing 35
## .00000000 No 2923
9997.00000000 Not applicable 34340

## EA_SVC_C_PHOTO
## Value Count
Label EA-SVC-C-PHOTO. Sewage system in the PSU/EA:
## Photo

## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 0 No 6687
## 1 Yes 4538
7 Not applicable 34340

## EA_SVC_D
## Value Count
Label EA-SVC-D. Mobile phone service in the PSU/EA
## Type Numeric


## Measurement Ordinal
## -1 Missing 35
## 0 No 12429
## 1 Yes 32148
9 Can't determine 988

## EA_SVC_D_GPS_LA
## Value Count
Label EA-SVC-D-GPS-LA. Mobile phone service in the
PSU/EA: GPS Latitude

## Type Numeric
## Measurement Scale
## Valid 45600
## Missing 0
## Mean 2941.8283054493
## -1.00000000 Missing 35
## .00000000 No 10948
9997.00000000 Not applicable 13417

## EA_SVC_D_GPS_LO
## Value Count
Label EA-SVC-D-GPS-LO. Mobile phone service in the
PSU/EA: GPS Longitude

## Type Numeric
## Measurement Scale
## Valid 45600
## Missing 0
## Mean 2947.9602111456
## -1.00000000 Missing 35
## .00000000 No 10948
9997.00000000 Not applicable 13417

## EA_SVC_D_PHOTO
## Value Count
Label EA-SVC-D-PHOTO. Mobile phone service in the
PSU/EA: Photo

## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 0 No 21025
## 1 Yes 11123
7 Not applicable 13417



## EA_SVC_E
## Value Count
Label EA-SVC-E.  Borehole or tubewell in PSU/EA
## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 0 No 22920
## 1 Yes 20746
9 Can't determine 1899

## EA_SVC_E_GPS_LA
## Value Count
Label EA-SVC-E-GPS-LA. Borehole or tubewell in PSU/EA:
GPS Latitude

## Type Numeric
## Measurement Scale
## N Valid 45600
## Missing 0
## Mean 5442.3388684742
## -1.00000000 Missing 35
## .00000000 No 3429
9997.00000000 Not applicable 24819

## EA_SVC_E_GPS_LO
## Value Count
Label EA-SVC-E-GPS-LO. Borehole or tubewell in PSU/EA:
GPS Longitude

## Type Numeric
## Measurement Scale
## N Valid 45600
## Missing 0
## Mean 5444.1576059709
## -1.00000000 Missing 35
## .00000000 No 3429
9997.00000000 Not applicable 24819

## EA_SVC_E_PHOTO
## Value Count
Label EA-SVC-E-PHOTO. Borehole or tubewell in PSU/EA:
## Photo

## Type Numeric
## Measurement Ordinal
## -1 Missing 35


## 0 No 7837
## 1 Yes 12909
7 Not applicable 24819

## EA_FAC_A
## Value Count
Label EA-FAC-A. Post office in the PSU/EA
## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 0 No 39185
## 1 Yes 5815
9 Can't determine 566

## EA_FAC_A_GPS_LA
## Value Count
Label EA-FAC-A-GPS-LA. Post office in the PSU/EA: GPS
## Latitude

## Type Numeric
## Measurement Scale
## Valid 45600
## Missing 0
## Mean 8714.9986302861
## -1.00000000 Missing 35
## .00000000 No 2245
9997.00000000 Not applicable 39750

## EA_FAC_A_GPS_LO
## Value Count
Label EA-FAC-A-GPS-LO. Post office in the PSU/EA: GPS
## Longitude

## Type Numeric
## Measurement Scale
## Valid 45600
## Missing 0
## Mean 8715.7055848116
## -1.00000000 Missing 35
## .00000000 No 2245
9997.00000000 Not applicable 39750

## EA_FAC_A_PHOTO
## Value Count
Label EA-FAC-A-PHOTO. Post office in the PSU/EA: Photo


## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 0 No 4087
## 1 Yes 1728
7 Not applicable 39750

## EA_FAC_B
## Value Count
Label EA-FAC-B. School in the PSU/EA
## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 0 No 10478
## 1 Yes 34445
9 Can't determine 642

## EA_FAC_B_GPS_LA
## Value Count
Label EA-FAC-B-GPS-LA. School in the PSU/EA: GPS Latitude
## Type Numeric
## Measurement Scale
## Valid 45600
## Missing 0
## Mean 2439.1244166490
## -1.00000000 Missing 35
## .00000000 No 6144
9997.00000000 Not applicable 11120

## EA_FAC_B_GPS_LO
## Value Count
Label EA-FAC-B-GPS-LO. School in the PSU/EA: GPS
## Longitude

## Type Numeric
## Measurement Scale
## Valid 45600
## Missing 0
## Mean 2444.4195965315
## -1.00000000 Missing 35
## .00000000 No 6144
9997.00000000 Not applicable 11120

## EA_FAC_B_PHOTO


## Value Count
Label EA-FAC-B-PHOTO. School in the PSU/EA: Photo
## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 0 No 14393
## 1 Yes 20052
7 Not applicable 11120

## EA_FAC_C
## Value Count
Label EA-FAC-C. Police station in the PSU/EA
## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 0 No 32933
## 1 Yes 12044
9 Can't determine 588

## EA_FAC_C_GPS_LA
## Value Count
Label EA-FAC-C-GPS-LA. Police station in the PSU/EA: GPS
## Latitude

## Type Numeric
## Measurement Scale
## Valid 45600
## Missing 0
## Mean 7348.9826771691
## -1.00000000 Missing 35
## .00000000 No 5328
9997.00000000 Not applicable 33521

## EA_FAC_C_GPS_LO
## Value Count
Label EA-FAC-C-GPS-LO. Police station in the PSU/EA: GPS
## Longitude

## Type Numeric
## Measurement Scale
## Valid 45600
## Missing 0
## Mean 7350.8694357651
## -1.00000000 Missing 35
## .00000000 No 5328


9997.00000000 Not applicable 33521

## EA_FAC_C_PHOTO
## Value Count
Label EA-FAC-C-PHOTO. Police station in the PSU/EA: Photo
## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 0 No 8636
## 1 Yes 3408
7 Not applicable 33521

## EA_FAC_D
## Value Count
Label EA-FAC-D. Health Clinic in the PSU/EA
## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 0 No 23067
## 1 Yes 21482
9 Can't determine 1016

## EA_FAC_D_GPS_LA
## Value Count
Label EA-FAC-D-GPS-LA. Health Clinic in the PSU/EA: GPS
## Latitude

## Type Numeric
## Measurement Scale
## Valid 45600
## Missing 0
## Mean 5281.0369709470
## -1.00000000 Missing 35
## .00000000 No 5295
9997.00000000 Not applicable 24083

## EA_FAC_D_GPS_LO
## Value Count
Label EA-FAC-D-GPS-LO. Health Clinic in the PSU/EA: GPS
## Longitude

## Type Numeric
## Measurement Scale
## Valid 45600
## Missing 0


## Mean 5283.2525727662
## -1.00000000 Missing 35
## .00000000 No 5295
9997.00000000 Not applicable 24083

## EA_FAC_D_PHOTO
## Value Count
Label EA-FAC-D-PHOTO. Health Clinic in the PSU/EA: Photo
## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 0 No 10648
## 1 Yes 10834
7 Not applicable 24083

## EA_FAC_E
## Value Count
Label EA-FAC-E. Market stalls in the PSU/EA
## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 0 No 21635
## 1 Yes 23047
9 Can't determine 883

## EA_FAC_E_GPS_LA
## Value Count
Label EA-FAC-E-GPS-LA. Market stalls in the PSU/EA: GPS
## Latitude

## Type Numeric
## Measurement Scale
## Valid 45600
## Missing 0
## Mean 4937.2674731753
## -1.00000000 Missing 35
## .00000000 No 5477
9997.00000000 Not applicable 22518

## EA_FAC_E_GPS_LO
## Value Count
Label EA-FAC-E-GPS-LO. Market stalls in the PSU/EA: GPS
## Longitude

## Type Numeric


## Measurement Scale
## Valid 45600
## Missing 0
## Mean 4941.8357376160
## -1.00000000 Missing 35
## .00000000 No 5477
9997.00000000 Not applicable 22518

## EA_FAC_E_PHOTO
## Value Count
Label EA-FAC-E-PHOTO. Market stalls in the PSU/EA: Photo
## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 0 No 11006
## 1 Yes 12041
7 Not applicable 22518

## EA_FAC_F
## Value Count
Label EA-FAC-F. Bank or money services in the PSU/EA
## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 0 No 24810
## 1 Yes 20144
9 Can't determine 611

## EA_FAC_F_GPS_LA
## Value Count
Label EA-FAC-F-GPS-LA. Bank or money services in the
PSU/EA: GPS Latitude

## Type Numeric
## Measurement Scale
## Valid 45600
## Missing 0
## Mean 5573.8344045221
## -1.00000000 Missing 35
## .00000000 No 4805
9997.00000000 Not applicable 25421

## EA_FAC_F_GPS_LO
## Value Count


Label EA-FAC-F-GPS-LO. Bank or money services in the
PSU/EA: GPS Longitude

## Type Numeric
## Measurement Scale
## Valid 45600
## Missing 0
## Mean 5576.6263663935
## -1.00000000 Missing 35
## .00000000 No 4805
9997.00000000 Not applicable 25421

## EA_FAC_F_PHOTO
## Value Count
Label EA-FAC-F-PHOTO. Bank or money services in the
PSU/EA: Photo

## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 0 No 9869
## 1 Yes 10275
7 Not applicable 25421

## EA_FAC_F2
## Value Count
Label EA-FAC-F2. Social/govt center/office in PSU/EA
## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 0 No 37029
## 1 Yes 7550
9 Can't determine 987

## EA_FAC_F2_GPS_LA
## Value Count
Label EA-FAC-F2-GPS-LA. Social/govt center/office in
PSU/EA: GPS Latitude

## Type Numeric
## Measurement Scale
## Valid 45600
## Missing 0
## Mean 8334.2909603234
## -1.00000000 Missing 35
## .00000000 No 3200


9997.00000000 Not applicable 38016

## EA_FAC_F2_GPS_LO
## Value Count
Label EA-FAC-F2-GPS-LO. Social/govt center/office in
PSU/EA: GPS Longitude

## Type Numeric
## Measurement Scale
## Valid 45600
## Missing 0
## Mean 8336.0767801230
## -1.00000000 Missing 35
## .00000000 No 3200
9997.00000000 Not applicable 38016

## EA_FAC_F2_PHOTO
## Value Count
Label EA-FAC-F2-PHOTO. Social/govt center/office in
PSU/EA: Photo

## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 0 No 5095
## 1 Yes 2455
7 Not applicable 38016

## EA_FAC_G
## Value Count
Label EA-FAC-G. Paid transport in the PSU/EA
## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 0 No 16458
## 1 Yes 27910
9 Can't determine 1197

## EA_FAC_G_GPS_LA
## Value Count
Label EA-FAC-G-GPS-LA. Paid transport in the PSU/EA: GPS
## Latitude

## Type Numeric
## Measurement Scale
## Valid 45600


## Missing 0
## Mean 3870.9962384117
## -1.00000000 Missing 35
## .00000000 No 8995
9997.00000000 Not applicable 17656

## EA_FAC_G_GPS_LO
## Value Count
Label EA-FAC-G-GPS-LO. Paid transport in the PSU/EA: GPS
## Longitude

## Type Numeric
## Measurement Scale
## Valid 45600
## Missing 0
## Mean 3875.8714041359
## -1.00000000 Missing 35
## .00000000 No 8995
9997.00000000 Not applicable 17656

## EA_FAC_G_PHOTO
## Value Count
Label EA-FAC-G-PHOTO. Paid transport in the PSU/EA: Photo
## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 0 No 16372
## 1 Yes 11537
7 Not applicable 17656

## EA_SEC_A
## Value Count
Label EA-SEC-A. Police in the PSU/EA
## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 0 No 30982
## 1 Yes 14321
9 Can't determine 262

## EA_SEC_B
## Value Count
Label EA-SEC-B. Soldiers/army in the PSU/EA
## Type Numeric


## Measurement Ordinal
## -1 Missing 35
## 0 No 40851
## 1 Yes 4392
9 Can't determine 322

## EA_SEC_C
## Value Count
Label EA-SEC-C. Roadblocks by police/army in the PSU/EA
## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 0 No 41109
## 1 Yes 4144
9 Can't determine 312

## EA_SEC_D
## Value Count
Label EA-SEC-D. Customs checkpoints in the PSU/EA
## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 0 No 43885
## 1 Yes 1327
9 Can't determine 354

## EA_SEC_E
## Value Count
Label EA-SEC-E. Roadblocks by private security/local
community in the PSU/EA

## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 0 No 43282
## 1 Yes 1870
9 Can't determine 414

## EA_ROAD_A
## Value Count
Label EA-ROAD-A. Road surface at start point
## Type Numeric
## Measurement Ordinal
## -1 Missing 35


## 1 Earth 20189
2 Unpaved gravel 5334
3 Unpaved stone/muram 3384
4 Paved tar/concrete 15723
7 Not Applicable/Not reachable by road 936

## EA_ROAD_B
## Value Count
Label EA-ROAD-B. Road surface last 5 km
## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 1 Earth 14119
2 Unpaved gravel 5083
3 Unpaved stone/muram 3362
4 Paved tar/concrete 21836
7 Not Applicable/Not reachable by road 1165

## EA_ROAD_C
## Value Count
Label EA-ROAD-C. Road condition last 5 km
## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 1 Impassable 958
2 Very poor 7650
## 3 Poor 7105
## 4 Fair 11796
## 5 Good 11464
6 Very good 6433
7 Not applicable 159

## CONSULT_A_EA
## Value Count
Label CONSULT-A-EA. Infrastructure Consultation in the EA:
## Interviewers

## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 0 No 9586
## 1 Yes 35980

## CONSULT_B_EA


## Value Count
Label CONSULT-B-EA. Infrastructure Consultation in the EA:
## Local Residents

## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 0 No 7869
## 1 Yes 37697

## CONSULT_C_EA
## Value Count
Label CONSULT-C-EA. Infrastructure Consultation in the EA:
## Local Leaders

## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 0 No 23858
## 1 Yes 21707

## CONSULT_D_EA
## Value Count
Label CONSULT-D-EA. Infrastructure Consultation in the EA:
## Others

## Type Numeric
## Measurement Ordinal
## -1 Missing 35
## 0 No 44953
## 1 Yes 613

## CONSULT_EA_OTHER
## Value Count
Label CONSULT-EA-OTHER. Infrastructure Consultation in
the EA: Others (Verbatim)

## Type String
## Measurement Nominal
## 44987
## BODA BODA   17
## BOUTIQUIER   8
## CHAPEIROS
## (COBRADORES DE
## CHAPA
## 10
## CHAUFFEUR DE
## MOTO
## 6


## CHAUFFEUR DE TAXI   9
## COBRADOR DE
## CHAPA
## 5
## COMERCIANTES
## PASSAGEIROS
## 10
## CONDUCTEUR   7
## CONSTRUCTION
## WORKER
## 0
## CONSTRUCTION
## WORKERS
## 7
## DIRETOR DE ESCOLA   4
## DRIVERS   2
## FUNCIONÁRIOS,
## INSTITUTO POLIT
## 8
## GOOGLE MAPS   13
## HERBAL MEDICINE
## PATIENTS FROM
## 3
## IMAM DE LA ZD   34
## INFIRMIER DE
## TOUNVRE
## 6
## JOVEM LÍDER   4
## LA GENDARMERIE   9
## MARKET WOMEN
## FROM NEIGHBORING
## 5
## MOTO TAXI   6
## MOTOQUEIROS   9
## NEARBY
## CONSTRUCTION
## WORKERS
## 12
## NON RÉSIDENTS   5
## NURSE   6
## NURSES   7
## ONGS LOCAIS   8
## ONGS NACIONAIS E
## INTERNACIONAI
## 9
## PASSANT   16
## PASSANTS   79
## PASSERS-BY   7
## PEDREIRO   7
## PEOPLE FROM
## NEIGHBORING EA
## 9
## PERSONNE CIVILE   21
## POLICE   6


## POLICE OFFICER   13
## PRIMARY SCHOOL
## HEAD TEACHER
## 7
## PRIVATE SECURITY
## OFFICER
## 47
## PROFESSOR   9
## QUARTIER MOBILE   17
## SCHOOL HEAD
## TEACHER
## 17
## SCHOOL TEACHERS   7
## SECURITY OFFICER   9
## SECURITY OFFICER
## AND CARETAKER
## 1
## SUBDIRETOR DE
## ESCOLA
## 37
## TAXISTA   7
## TEACHER   4
## TEACHER IN THE
## SCHOOL
## 7
## TÉCNICO DE SAÚDE   16
## TRADERS   5
## UN VENDEUR
## AMBULANT À MOTO
## 4
## UN VENDEUR
## AMBULANT NON
## RÉSIDENT
## 5
## VENDEUR   7
## VIGILES   9
## VISITEURS   12

## NOCALL_1
## Value Count
Label Reason for Unsuccessful Call Household 1
## Type Numeric
## Measurement Nominal
## -1 Missing 0
1 Refused to be interviewed 3041
2 Person selected was never at home after at least two
visits
## 823
3 Household/Premises empty for the survey period after
at least two visits
## 1965
4 Not a citizen/Spoke only a foreign language 282
5 Deaf/Did not speak a survey language 221


6 Did not fit gender quota 2003
7 No adults in household 1774
## 8 Other (specify) 48
9997 Interview was successful 35442

NOCALL_1Other
## Value Count
Label Reason for Unsuccessful Call Household 1 (Verbatim)
## Type String
## Measurement Nominal
## 45551
## DID NOT
## UNDERSTAND
## MULTIPLE
## QUESTIONS
## 1
## DOMESTIC WORKER   1
## DRUNK   1
## EXCEEDED AGE LIMIT   1
## FUNERAL   1
## IMMEUBLES
## INACCESSIBLE
## 0
## MALADE   2
## MENTAL HEALTH
## ISSUE
## 0
## MENTALLY
## HANDICAPPED
## 1
## MENTALLY UNSTABLE   1
## NO ACCESS   4
## NOT ELIGIBLE
## MENTALLY
## 1
## NOT PART OF THE
## FAMILY
## 0
## NOT RESIDENTIAL
## (B&B)
## 0
## OLD   0
## OUTSIDE EA
## BOUNDARY
## 2
## OUTSIDE
## ENUMERATION AREA
## 3
## RESPONDENT WAS
## ACTING SUSPICIOUS
## 0
## RESPONDENT'S
## BROTHER REFUSED
## 1


## ROBBERY RISK   0
## SECURITY DOES NOT
## ALLOW US
## 2
## SICK   20
## TOO OLD   2
## TROP VIEUX   1
## UNSAFE   1
## VISITOR   1
## VISITOR IN THE
## HOME
## 0
## VISITORS   1

## NOCALL_2
## Value Count
Label Reason for Unsuccessful Call Household 2
## Type Numeric
## Measurement Nominal
## -1 Missing 0
1 Refused to be interviewed 1154
2 Person selected was never at home after at least two
visits
## 283
3 Household/Premises empty for the survey period after
at least two visits
## 1003
4 Not a citizen/Spoke only a foreign language 131
5 Deaf/Did not speak a survey language 75
6 Did not fit gender quota 815
7 No adults in household 568
## 8 Other (specify) 18
9997 Interview was successful 41552

NOCALL_2Other
## Value Count
Label Reason for Unsuccessful Call Household 2 (Verbatim)
## Type String
## Measurement Nominal
## 45582
## COMPANY   2
## DOENTE, NÃO PODE
## RESPONDER
## 2
## DRUNK   1
## MALADE   3
## NO ACCESS   3
## NOT MENTALLY FIT   2


## SICK   5
## UNACCESSIBLE DUE
## TO DOGS
## 0
## VISITORS   0

## NOCALL_3
## Value Count
Label Reason for Unsuccessful Call Household 3
## Type Numeric
## Measurement Nominal
## -1 Missing 0
1 Refused to be interviewed 465
2 Person selected was never at home after at least two
visits
## 166
3 Household/Premises empty for the survey period after
at least two visits
## 499
4 Not a citizen/Spoke only a foreign language 49
5 Deaf/Did not speak a survey language 49
6 Did not fit gender quota 404
7 No adults in household 249
## 8 Other (specify) 5
9997 Interview was successful 43714

NOCALL_3Other
## Value Count
Label Reason for Unsuccessful Call Household 3 (Verbatim)
## Type String
## Measurement Nominal
## 45595
## DISABLED   0
## MENTAL INCAPACITY   1
## NO ACCESS   1
## PERTURBAÇÃO
## MENTAL
## 1
## SICK   0
## TOO OLD   0
## VISITOR   1
## VISITORS   0

## NOCALL_4
## Value Count
Label Reason for Unsuccessful Call Household 4
## Type Numeric


## Measurement Nominal
## -1 Missing 0
1 Refused to be interviewed 265
2 Person selected was never at home after at least two
visits
## 91
3 Household/Premises empty for the survey period after
at least two visits
## 302
4 Not a citizen/Spoke only a foreign language 51
5 Deaf/Did not speak a survey language 32
6 Did not fit gender quota 174
7 No adults in household 134
## 8 Other (specify) 4
9997 Interview was successful 44545

NOCALL_4Other
## Value Count
Label Reason for Unsuccessful Call Household 4 (Verbatim)
## Type String
## Measurement Nominal
## 45596
## DRUNK   1
## NO ACCESS   1
## PERSON WITH
## INTELLECTUAL
## DISABILITY
## 0
## SICK   2
## UNACCESSIBLE DUE
## TO DOGS
## 0

## NOCALL_5
## Value Count
Label Reason for Unsuccessful Call Household 5
## Type Numeric
## Measurement Nominal
## -1 Missing 0
1 Refused to be interviewed 156
2 Person selected was never at home after at least two
visits
## 55
3 Household/Premises empty for the survey period after
at least two visits
## 201
4 Not a citizen/Spoke only a foreign language 10
5 Deaf/Did not speak a survey language 16
6 Did not fit gender quota 121


7 No adults in household 76
## 8 Other (specify) 2
9997 Interview was successful 44963

NOCALL_5Other
## Value Count
Label Reason for Unsuccessful Call Household 5 (Verbatim)
## Type String
## Measurement Nominal
## 45598
## DID NOT
## UNDERSTAND THE
## SURVEY
## 1
## SICK   1
## UNSAFE   0
## VISITOR   1

## NOCALL_6
## Value Count
Label Reason for Unsuccessful Call Household 6
## Type Numeric
## Measurement Nominal
## -1 Missing 0
1 Refused to be interviewed 92
2 Person selected was never at home after at least two
visits
## 44
3 Household/Premises empty for the survey period after
at least two visits
## 135
4 Not a citizen/Spoke only a foreign language 10
5 Deaf/Did not speak a survey language 13
6 Did not fit gender quota 91
7 No adults in household 36
## 8 Other (specify) 1
9997 Interview was successful 45179

NOCALL_6Other
## Value Count
Label Reason for Unsuccessful Call Household 6 (Verbatim)
## Type String
## Measurement Nominal
## 45599
## SICK   1



## NOCALL_7
## Value Count
Label Reason for Unsuccessful Call Household 7
## Type Numeric
## Measurement Nominal
## -1 Missing 0
1 Refused to be interviewed 68
2 Person selected was never at home after at least two
visits
## 16
3 Household/Premises empty for the survey period after
at least two visits
## 115
4 Not a citizen/Spoke only a foreign language 6
5 Deaf/Did not speak a survey language 4
6 Did not fit gender quota 59
7 No adults in household 19
## 8 Other (specify) 1
9997 Interview was successful 45312

NOCALL_7Other
## Value Count
Label Reason for Unsuccessful Call Household 7 (Verbatim)
## Type String
## Measurement Nominal
## 45599
## NO ACCESS   1

## NOCALL_8
## Value Count
Label Reason for Unsuccessful Call Household 8
## Type Numeric
## Measurement Nominal
## -1 Missing 0
1 Refused to be interviewed 44
2 Person selected was never at home after at least two
visits
## 11
3 Household/Premises empty for the survey period after
at least two visits
## 82
4 Not a citizen/Spoke only a foreign language 7
5 Deaf/Did not speak a survey language 3
6 Did not fit gender quota 29
7 No adults in household 26
## 8 Other (specify) 0
9997 Interview was successful 45398



NOCALL_8Other
## Value Count
Label Reason for Unsuccessful Call Household 8 (Verbatim)
## Type String
## Measurement Nominal
## 45600

## NOCALL_9
## Value Count
Label Reason for Unsuccessful Call Household 9
## Type Numeric
## Measurement Nominal
## -1 Missing 0
1 Refused to be interviewed 33
2 Person selected was never at home after at least two
visits
## 7
3 Household/Premises empty for the survey period after
at least two visits
## 60
4 Not a citizen/Spoke only a foreign language 10
5 Deaf/Did not speak a survey language 2
6 Did not fit gender quota 23
7 No adults in household 13
## 8 Other (specify) 0
9997 Interview was successful 45451

## NOCALL_9OTHER
## Value Count
Label Reason for Unsuccessful Call Household 9 (Verbatim)
## Type String
## Measurement Nominal
## 45600

## NOCALL_10
## Value Count
Label Reason for Unsuccessful Call Household 10
## Type Numeric
## Measurement Nominal
## -1 Missing 0
1 Refused to be interviewed 25
2 Person selected was never at home after at least two
visits
## 9


3 Household/Premises empty for the survey period after
at least two visits
## 46
4 Not a citizen/Spoke only a foreign language 3
5 Deaf/Did not speak a survey language 1
6 Did not fit gender quota 20
7 No adults in household 14
## 8 Other (specify) 0
9997 Interview was successful 45482

## NOCALL_10OTHER
## Value Count
Label Reason for Unsuccessful Call Household 10 (Verbatim)
## Type String
## Measurement Nominal
## 45600

## NOCALL_11
## Value Count
Label Reason for Unsuccessful Call Household 11
## Type Numeric
## Measurement Nominal
## -1 Missing 0
1 Refused to be interviewed 20
2 Person selected was never at home after at least two
visits
## 3
3 Household/Premises empty for the survey period after
at least two visits
## 37
4 Not a citizen/Spoke only a foreign language 5
5 Deaf/Did not speak a survey language 0
6 Did not fit gender quota 11
7 No adults in household 12
## 8 Other (specify) 0
9997 Interview was successful 45512

## NOCALL_11OTHER
## Value Count
Label Reason for Unsuccessful Call Household 11 (Verbatim)
## Type String
## Measurement Nominal
## 45600

## NOCALL_12
## Value Count


Label Reason for Unsuccessful Call Household 12
## Type Numeric
## Measurement Nominal
## -1 Missing 0
1 Refused to be interviewed 19
2 Person selected was never at home after at least two
visits
## 1
3 Household/Premises empty for the survey period after
at least two visits
## 28
4 Not a citizen/Spoke only a foreign language 4
5 Deaf/Did not speak a survey language 1
6 Did not fit gender quota 9
7 No adults in household 12
## 8 Other (specify) 0
9997 Interview was successful 45525

## NOCALL_12OTHER
## Value Count
Label Reason for Unsuccessful Call Household 12 (Verbatim)
## Type String
## Measurement Nominal
## 45600

## NOCALL_13
## Value Count
Label Reason for Unsuccessful Call Household 13
## Type Numeric
## Measurement Nominal
## -1 Missing 0
1 Refused to be interviewed 14
2 Person selected was never at home after at least two
visits
## 7
3 Household/Premises empty for the survey period after
at least two visits
## 20
4 Not a citizen/Spoke only a foreign language 2
5 Deaf/Did not speak a survey language 0
6 Did not fit gender quota 14
7 No adults in household 8
## 8 Other (specify) 0
9997 Interview was successful 45534

## NOCALL_13OTHER
## Value Count


Label Reason for Unsuccessful Call Household 13 (Verbatim)
## Type String
## Measurement Nominal
## 45600

## NOCALL_14
## Value Count
Label Reason for Unsuccessful Call Household 14
## Type Numeric
## Measurement Nominal
## -1 Missing 0
1 Refused to be interviewed 13
2 Person selected was never at home after at least two
visits
## 2
3 Household/Premises empty for the survey period after
at least two visits
## 17
4 Not a citizen/Spoke only a foreign language 2
5 Deaf/Did not speak a survey language 0
6 Did not fit gender quota 6
7 No adults in household 13
## 8 Other (specify) 0
9997 Interview was successful 45546

## NOCALL_14OTHER
## Value Count
Label Reason for Unsuccessful Call Household 14 (Verbatim)
## Type String
## Measurement Nominal
## 45600

## NOCALL_15
## Value Count
Label Reason for Unsuccessful Call Household 15
## Type Numeric
## Measurement Nominal
## -1 Missing 0
1 Refused to be interviewed 11
2 Person selected was never at home after at least two
visits
## 2
3 Household/Premises empty for the survey period after
at least two visits
## 16
4 Not a citizen/Spoke only a foreign language 1
5 Deaf/Did not speak a survey language 0


6 Did not fit gender quota 10
7 No adults in household 7
## 8 Other (specify) 0
9997 Interview was successful 45553

## NOCALL_15OTHER
## Value Count
Label Reason for Unsuccessful Call Household 15 (Verbatim)
## Type String
## Measurement Nominal
## 45600

## NOCALL_16
## Value Count
Label Reason for Unsuccessful Call Household 16
## Type Numeric
## Measurement Nominal
## -1 Missing 0
1 Refused to be interviewed 9
2 Person selected was never at home after at least two
visits
## 2
3 Household/Premises empty for the survey period after
at least two visits
## 12
4 Not a citizen/Spoke only a foreign language 4
5 Deaf/Did not speak a survey language 0
6 Did not fit gender quota 6
7 No adults in household 6
## 8 Other (specify) 0
9997 Interview was successful 45560

## NOCALL_16OTHER
## Value Count
Label Reason for Unsuccessful Call Household 16 (Verbatim)
## Type String
## Measurement Nominal
## 45600

## NOCALL_17
## Value Count
Label Reason for Unsuccessful Call Household 17
## Type Numeric
## Measurement Nominal
## -1 Missing 0


1 Refused to be interviewed 7
2 Person selected was never at home after at least two
visits
## 3
3 Household/Premises empty for the survey period after
at least two visits
## 15
4 Not a citizen/Spoke only a foreign language 2
5 Deaf/Did not speak a survey language 0
6 Did not fit gender quota 8
7 No adults in household 5
## 8 Other (specify) 0
9997 Interview was successful 45561

## NOCALL_17OTHER
## Value Count
Label Reason for Unsuccessful Call Household 17 (Verbatim)
## Type String
## Measurement Nominal
## 45600

## NOCALL_18
## Value Count
Label Reason for Unsuccessful Call Household 18
## Type Numeric
## Measurement Nominal
## -1 Missing 0
1 Refused to be interviewed 5
2 Person selected was never at home after at least two
visits
## 1
3 Household/Premises empty for the survey period after
at least two visits
## 10
4 Not a citizen/Spoke only a foreign language 2
5 Deaf/Did not speak a survey language 0
6 Did not fit gender quota 8
7 No adults in household 7
## 8 Other (specify) 0
9997 Interview was successful 45567

## NOCALL_18OTHER
## Value Count
Label Reason for Unsuccessful Call Household 18 (Verbatim)
## Type String
## Measurement Nominal
## 45600



## NOCALL_19
## Value Count
Label Reason for Unsuccessful Call Household 19
## Type Numeric
## Measurement Nominal
## -1 Missing 0
1 Refused to be interviewed 8
2 Person selected was never at home after at least two
visits
## 0
3 Household/Premises empty for the survey period after
at least two visits
## 6
4 Not a citizen/Spoke only a foreign language 1
5 Deaf/Did not speak a survey language 0
6 Did not fit gender quota 4
7 No adults in household 5
## 8 Other (specify) 0
9997 Interview was successful 45575

## NOCALL_19OTHER
## Value Count
Label Reason for Unsuccessful Call Household 19 (Verbatim)
## Type String
## Measurement Nominal
## 45600

## NOCALL_20
## Value Count
Label Reason for Unsuccessful Call Household 20
## Type Numeric
## Measurement Nominal
## -1 Missing 0
1 Refused to be interviewed 1
2 Person selected was never at home after at least two
visits
## 0
3 Household/Premises empty for the survey period after
at least two visits
## 0
4 Not a citizen/Spoke only a foreign language 1
5 Deaf/Did not speak a survey language 0
6 Did not fit gender quota 1
7 No adults in household 0
## 8 Other (specify) 0
9997 Interview was successful 45597



NOCALL_20Other
## Value Count
Label Reason for Unsuccessful Call Household 20 (Verbatim)
## Type String
## Measurement Nominal
## 45600

## DATEINTR

## Value

Label Date of interview

## Type Numeric

## Measurement Scale

## Valid 45600

## Missing 0

## Mean 02.09.24


## STRTIME

## Value

Label Time interview started

## Type Numeric

## Measurement Scale

## Valid 45600

## Missing 0

## Mean 13:18


## Q1
## Value Count
## Label Q1. Age
## Type Numeric
## Measurement Scale
## Valid 45600
## Missing 0
## Mean 38.53
## -1 Missing 0
## 998 Refused 5
999 Do not know 11

## Q2

## Value

Label Q2. Language spoken in home

## Type Numeric

## Measurement Nominal




## Q2OTHER
## Value Count
Label Q2other. Language spoken in home (verbatim)
## Type String
## Measurement Nominal
## 45263
## AGONYIN   0
## AGOUNA   6
## ANDOH   3
## ANGAS   2
## ANII   1
## APPOLO   1
## ATABA   2
## BA MAIGE   1
## BABULE   2
## BACHAMA   2
## BAKO   1
## BAKOR   1
## BAKOULE   2
## BAKWE   2
## BALANTA   3
## BALANTE   5
## BAMBARA   2
## BANDA   1
## BARAWA   0
## BARBANCHI   2
## BASARE   0
## BHOJPURI   7
## BIMOBA   1
## BOCHI   1
## BOESMAN   1
## BOKYI   0
## BOLANCI   3
## BOMITABA   1
## BONI   0
## BONI, AWEER   0
## BRIFO   3
## BUSANGA   1
## CHAMBA   0
## CHIBARUE   5
## CHINYUNGWE   1
## CHISSENGA   4


## CHITAWALA   2
## CHOKOSI/CHAKOSI   1
## CREO/KRIO   3
## CRÉOLE   0
## DJAMALA   5
## DJERMA   2
## DONDO   0
## EBAS   0
## EBRIE   5
## EFUTU   1
## EKAJUK   2
## EKPA   1
## ETSAKO   1
## FALI   2
## FOMI   1
## FOULANI   1
## FULANI   1
## GANGOULOU   2
## GNANGA   2
## GUAN   1
## GWANDARA   0
## GWANTU   1
## HAOUSSA   0
## HIGGI   4
## HINDI   4
## IBAAS   2
## IBAGWA AKA   1
## IBIVIE   1
## IGBANI   0
## IGEDE   0
## IKA   4
## IMIAKEBU   1
## ISUKA   0
## ITSEKIRI   6
## IVIE   5
## IZZI   6
## KABRE   0
## KAJU   1
## KAKANDA   3
## KAKWA   4
## KANU   0
## KARONE   1
## KHOEKHOE   3


## KIFUMBIRWA   1
## KILBA   1
## KILWANA   2
## KINKENGUE   1
## KORO   1
## KOTOKOLI   4
## KOUELE   1
## KOUYOU   3
## KROBO   2
## KUMAM   3
## KUPA   10
## KWALE   0
## LALI   2
## LIKOUBA   0
## LINGALA   0
## LOBI   1
## LOKPA   5
## LUBWISI   1
## LUKISGINYI   0
## LULUULI   0
## LUSIKI   0
## MADA   0
## MAGACHI   2
## MAGAWA   1
## MAHOUKA/MAHOU   4
## MAIGECIN   1
## MAKOUEIN   1
## MAMPROUSSI   1
## MATEWE   2
## MATSUWA   2
## MBOCHI   2
## MBOKO   2
## MBOSI   2
## MBUBE   0
## MFOM   3
## MISSING   9
## MIX
## ZULU/XHOSA/SOTHO
## 0
## MOSSI   6
## MOYAYA   0
## MOYE   3
## MPIMBI   0
## MUNA   0


## MVUTE   2
## N’GOKALA   1
## NAFANA   1
## NDOKI   2
## NDZEBI   1
## NGOA   6
## NGOKALA   1
## NINGO   0
## NINZO   3
## NYANKPA   3
## NYEKPA   3
## NYEMBA   1
## NZEMA   1
## OBUKPA   2
## ODIENNEKA   1
## OKPELLA   5
## OWAN   2
## PEULH   6
## RIBINAWA   6
## RUBWISI   0
## RUGUNGU   1
## RUNYARUTEMBE   0
## RUNYARWANDA   2
## SAHWI   1
## SAMARE   0
## SAN   2
## SANAGA   1
## SEKGATLA   3
## SENGWATO   1
## SETEBELE   0
## SETSWAPONG   2
## SHANGANI   10
## SHENG   0
## SXHOZA   3
## TAGBANA   5
## TAMBERMA   4
## TELUGU   0
## TOKO   1
## TURKA   1
## UKWANI   0
## URDU   0
## UWANO   1
## UWANU   1


## WANGARA   0
## WARRI   1
## WASA   1
## WOBE   5
## WURKUM   3
## WURKUN   0
## YAANA   1
## YAGBA   1
## YAKURR   1
## YANGA   1
## YANM   0
## YASAWA   2
## YOM   2
## ZABARMA   2
## ZOH   1

## Q3
## Value Count
Label Q3. Overall direction of the country
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Going in the wrong direction 26472
2 Going in the right direction 17952
## 8 Refused 88
9 Don't know 1087

## Q4A
## Value Count
Label Q4a. Country’s present economic condition
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Very bad 14652
2 Fairly bad 12037
3 Neither good nor bad 5428
4 Fairly good 9527
5 Very good 3468
## 8 Refused 18
9 Don't know 469

## Q4B
## Value Count


Label Q4b. Your present living conditions
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Very bad 11034
2 Fairly bad 11268
3 Neither good nor bad 8151
4 Fairly good 11751
5 Very good 3322
## 8 Refused 15
9 Don't know 59

## Q5A
## Value Count
Label Q5a. Country’s economic condition compared to 12
months ago

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Much worse 9254
## 2 Worse 13856
## 3 Same 11259
## 4 Better 9263
5 Much better 1555
## 8 Refused 11
9 Don’t know 402

## Q5B
## Value Count
Label Q5b. Your living conditions compared to 12 months
ago

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Much worse 7233
## 2 Worse 12407
## 3 Same 13602
## 4 Better 10450
5 Much better 1773
## 8 Refused 9
9 Don’t know 125

## Q6


## Value Count
Label Q5b. Country’s economic condition in 12 months’ time
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Much worse 5944
## 2 Worse 7312
## 3 Same 6961
## 4 Better 15717
5 Much better 6454
## 8 Refused 26
9 Don’t know 3186

## Q7A
## Value Count
Label Q7a. How often gone without food
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 19079
1 Just once or twice 7952
2 Several times 9674
3 Many times 6709
## 4 Always 2128
## 8 Refused 17
9 Don't know 40

## Q7B
## Value Count
Label Q7b. How often gone without water
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 19424
1 Just once or twice 6505
2 Several times 8281
3 Many times 6782
## 4 Always 4566
## 8 Refused 5
9 Don't know 37

## Q7C
## Value Count


Label Q7c. How often gone without medical care
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 15877
1 Just once or twice 7916
2 Several times 9968
3 Many times 7742
## 4 Always 3949
## 8 Refused 6
9 Don't know 141

## Q7D
## Value Count
Label Q7d. How often gone without cooking fuel
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 21584
1 Just once or twice 7870
2 Several times 8431
3 Many times 4936
## 4 Always 2621
## 8 Refused 6
9 Don't know 153

## Q7E
## Value Count
Label Q7e. How often gone without cash income
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 9389
1 Just once or twice 6123
2 Several times 10443
3 Many times 11534
## 4 Always 7874
## 8 Refused 30
9 Don't know 208

## Q8A
## Value Count
Label Q8a. Requested assistance from family


## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 No 24178
1 Yes, once or twice 7819
2 Yes, several times 9964
3 Yes, often 3601
8 Refused to answer 10
9 Don't know 28

## Q8B
## Value Count
Label Q8b. Requested assistance from friends or neighbours
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 No 30611
1 Yes, once or twice 6322
2 Yes, several times 6562
3 Yes, often 2080
8 Refused to answer 7
9 Don't know 17

## Q8C
## Value Count
Label Q8c. Requested assistance from religious or
community group

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 No 40153
1 Yes, once or twice 2601
2 Yes, several times 2063
3 Yes, often 746
8 Refused to answer 9
9 Don't know 29

## Q9
## Value Count
Label Q9. How often felt unsafe walking in neighbourhood
## Type Numeric
## Measurement Ordinal
## -1 Missing 0


## 0 Never 24007
1 Just once or twice 7399
2 Several times 7259
3 Many times 4406
## 4 Always 2435
## 8 Refused 1
9 Don’t know 94

## Q10A
## Value Count
Label Q10a. Freedom to say what you think
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Not at all free 6892
2 Not very free 8405
3 Somewhat free 12107
4 Completely free 17704
## 8 Refused 41
9 Don’t know 450

## Q10B
## Value Count
Label Q10b. Freedom to join any political organization
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Not at all free 4156
2 Not very free 4974
3 Somewhat free 10043
4 Completely free 23981
## 8 Refused 174
9 Don’t know 1072
9994 Not asked in country 1200

## Q10C
## Value Count
Label Q10c. Freedom to choose who to vote for
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Not at all free 2781
2 Not very free 3101


3 Somewhat free 8407
4 Completely free 30619
## 8 Refused 94
9 Don’t know 598

## Q11A
## Value Count
Label Q11a. Joined others to request action from
government

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 No 38576
1 Yes, once or twice 2689
2 Yes, several times 2711
3 Yes, often 1511
## 8 Refused 32
9 Don't know 81

## Q11B
## Value Count
Label Q11b. Contacted media to share your views
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 No 42904
1 Yes, once or twice 1180
2 Yes, several times 954
3 Yes, often 508
## 8 Refused 6
9 Don't know 48

## Q11C
## Value Count
Label Q11c. Posted about politics or community affairs on
social media

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 No 42843
1 Yes, once or twice 975
2 Yes, several times 1134
3 Yes, often 551


## 8 Refused 12
9 Don't know 85

## Q11D
## Value Count
Label Q11d. Attend a demonstration or protest march
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 No 42535
1 Yes, once or twice 1635
2 Yes, several times 944
3 Yes, often 432
## 8 Refused 15
9 Don't know 40

## Q12A
## Value Count
Label Q12a. Contact MP
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 39466
1 Only once 2911
2 A few times 2084
## 3 Often 934
8 Refused to answer 29
9 Don’t know 177

## Q12B
## Value Count
Label Q12b. Contact political party official
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 36419
1 Only once 3696
2 A few times 2851
## 3 Often 1274
8 Refused to answer 28
9 Don’t know 131
9994 Not asked in country 1200



## Q12C
## Value Count
Label Q12c. Contact traditional leader
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 26385
1 Only once 3597
2 A few times 4423
## 3 Often 3730
8 Refused to answer 21
9 Don’t know 244
9994 Not asked in country 7200

## Q13A
## Value Count
Label Q13a. Voting in the most recent national election
## Type Numeric
## Measurement Nominal
## -1 Missing 0
0 I did not vote 12169
1 I was too young to vote 1515
2 I can’t remember whether I voted 303
3 I voted in the election 31503
8 Refused to answer 47
9 Don’t know 62

## Q13B
## Value Count
Label Q13b. Intend to vote in the next national election (if
too young)

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 No 293
## 1 Yes 1101
7 Not applicable 41729
8 Refused to answer 2
9 Don't know 75
9994 Not asked in country 2400

## Q13C
## Value Count


Label Q13c. Reason for not voting
## Type Numeric
## Measurement Nominal
## -1 Missing 0
1 Not registered to vote 3710
2 Not interested in politics or voting 2155
3 Did not have time to vote 1659
4 Did not like any of the parties or candidates 458
5 Elections don’t make a difference/ are not effective 777
6 Do not trust the electoral commission and electoral
process
## 352
7 Tried to vote but could not for some reason (e.g. could
not find polling station, name not on voters’ register,
or pre
## 889
8 Some other reason 2070
9 Don’t know/cannot remember 72
97 Not applicable 33431
98 Refused to Answer 28
9994 Not asked in country 0

## Q13D
## Value Count
Label Q13d. Reason not registered to vote
## Type Numeric
## Measurement Nominal
## -1 Missing 0
1 Did not have time to register 1142
2 Not interested in politics or voting 390
3 Registration process is too complicated/ demanding 312
4 Was too young to register 1011
5 Elections don’t make a difference/ are not effective 102
6 Do not trust the electoral commission and electoral
process
## 33
7 Did not register for some other reason 662
8 Refused to Answer 6
9 Don’t know/cannot remember 52
97 Not applicable 41889

## Q14
## Value Count
Label Q14. Lower voting age
## Type Numeric
## Measurement Ordinal


## -1 Missing 0
1 Strongly disagree 16189
## 2 Disagree 11883
3 Neither agree nor disagree 1136
## 4 Agree 8418
5 Strongly agree 7265
8 Refused to Answer 26
9 Don't know 683

## Q15
## Value Count
Label Q15. Freeness and fairness of the last national election
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Not free and fair 9327
2 Free and fair, but with major problems 7308
3 Free and fair, but with minor problems 10026
4 Completely free and fair 15277
8 Do not understand question 309
9 Don’t know 3215
98 Refused to answer 137

## Q16A
## Value Count
Label Q16a. How likely powerful find out your vote
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
0 Not at all likely 21776
1 Not very likely 8713
2 Somewhat likely 7292
3 Very likely 5590
## 8 Refused 54
9 Don’t know 2176

## Q16B
## Value Count
Label Q16b. Last national election: fear political intimidation
or violence

## Type Numeric
## Measurement Ordinal
## -1 Missing 0


0 A lot 4616
## 1 Somewhat 4008
2 A little bit 6375
3 Not at all 29838
## 8 Refused 61
9 Don’t know 703

## Q17
## Value Count
Label Q17. Government bans organizations vs join any
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
2 Agree with 1 14654
3 Agree with 2 29190
5 Agree with neither 848
8 Refused to answer 61
9 Don’t know 847

## Q18A
## Value Count
Label Q18a. Media free to publish vs government control
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
2 Agree with 1 29738
3 Agree with 2 14511
5 Agree with neither 650
8 Refused to answer 41
9 Don’t know 661

## Q18B
## Value Count
Label Q18b. Media checks government vs avoid negative
reporting

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
2 Agree with 1 32630
3 Agree with 2 11785
5 Agree with neither 509
8 Refused to answer 63
9 Don’t know 613



## Q19
## Value Count
Label Q19. Govt gets things done vs govt accountable to
citizens

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
2 Agree with 1 17260
3 Agree with 2 26985
5 Agree with neither 616
8 Refused to answer 45
9 Don’t know 693

## Q20
## Value Count
Label Q20. Elected officials follow voter demands vs follow
own ideas

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
2 Agree with 1 35329
3 Agree with 2 9514
5 Agree with neither 428
8 Refused to answer 34
9 Don’t know 296

## Q21A
## Value Count
Label Q21a. Reject one-party rule
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Strongly disapprove 21543
## 2 Disapprove 12911
3 Neither approve nor disapprove 972
## 4 Approve 5620
5 Strongly approve 3838
## 8 Refused 46
9 Don’t know 670

## Q21B
## Value Count


Label Q21b. Reject military rule
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Strongly disapprove 17987
## 2 Disapprove 11597
3 Neither approve nor disapprove 1802
## 4 Approve 8278
5 Strongly approve 5020
## 8 Refused 72
9 Don’t know 844

## Q21C
## Value Count
Label Q21c. Reject one-man rule
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Strongly disapprove 22819
## 2 Disapprove 13394
3 Neither approve nor disapprove 1328
## 4 Approve 4707
5 Strongly approve 2588
## 8 Refused 48
9 Don’t know 715

## Q22
## Value Count
Label Q22. Support for democracy
## Type Numeric
## Measurement Nominal
## -1 Missing 75
1 STATEMENT 3: For someone like me, it doesn’t matter
what kind of government we have.
## 7193
2 STATEMENT 2: In some circumstances, a non-
democratic government can be preferable.
## 7616
3 STATEMENT 1: Democracy is preferable to any other
kind of government.
## 29331
## 8 Refused 61
9 Don't know 1325

## Q23
## Value Count


Label Q23. Choose leaders through elections vs other
methods

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
2 Agree with 1 33580
3 Agree with 2 11227
5 Agree with neither 357
8 Refused to answer 34
9 Don’t know 402

## Q24
## Value Count
Label Q24. Political parties divisive vs many parties needed
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
2 Agree with 1 15507
3 Agree with 2 28897
5 Agree with neither 654
8 Refused to answer 52
9 Don’t know 490

## Q25
## Value Count
Label Q25. Democracy needs political party turnover vs ok if
one party always wins

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
2 Agree with 1 23332
3 Agree with 2 20883
5 Agree with neither 588
8 Refused to answer 53
9 Don’t know 743

## Q26A
## Value Count
Label Q26a. Parliament makes laws vs president does
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
2 Agree with 1 31268


3 Agree with 2 10246
5 Agree with neither 1980
8 Refused to answer 69
9 Don’t know 837
9994 Not asked in country 1200

## Q26B
## Value Count
Label Q26b. President monitored by parliament vs free to
act on own

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
2 Agree with 1 29913
3 Agree with 2 13524
5 Agree with neither 381
8 Refused to answer 49
9 Don’t know 533
9994 Not asked in country 1200

## Q27
## Value Count
Label Q27. Opposition parties examine government vs
cooperate

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
2 Agree with 1 11851
3 Agree with 2 31555
5 Agree with neither 517
8 Refused to answer 52
9 Don’t know 424
9994 Not asked in country 1200

## Q28
## Value Count
Label Q28. President free to act vs obey the laws and courts
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
2 Agree with 1 10538
3 Agree with 2 29998
5 Agree with neither 735


8 Refused to answer 77
9 Don’t know 652
9994 Not asked in country 3600

## Q29
## Value Count
Label Q29. Presidential two term limit vs no term limits
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
2 Agree with 1 32696
3 Agree with 2 11436
5 Agree with neither 757
8 Refused to answer 60
9 Don’t know 651

## Q30
## Value Count
Label Q30. Death penalty is fair punishment vs never
justified

## Type Numeric
## Measurement Ordinal
## -1 Missing 1200
2 Agree with 1 25428
3 Agree with 2 17745
5 Agree with neither 793
8 Refused to answer 54
9 Don’t know 380

## Q31A
## Value Count
Label Q31a. Armed forces never intervene vs when leaders
abuse power

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
2 Agree with 1 18402
3 Agree with 2 25075
5 Agree with neither 1111
8 Refused to answer 75
9 Don’t know 937

## Q31B


## Value Count
Label Q31b. Military intervention and restoration of civilian
rule

## Type Numeric
## Measurement Nominal
## -1 Missing 0
1 Statement 3: The military should rule for as long as
they think it is best for the country.
## 8143
2 Statement 2: The military should plan a gradual
transition back to civilian rule when the country is
ready, which might
## 12892
3 Statement 1: The military should always restore
civilian rule as soon as possible.
## 15262
4 None of the above 1964
7 Not applicable 0
## 8 Refused 71
9 Don’t know 1268
94 Not asked in country 0
9994 Not asked in country 6000

## Q32
## Value Count
Label Q32. Extent of democracy
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Not a democracy 8101
2 A democracy, with major problems 14626
3 A democracy, but with minor problems 13749
4 A full democracy 7475
8 Do not understand question/Do not understand what
'democracy' is
## 779
9 Don’t know 830
## 98 Refused 41

## Q33
## Value Count
Label Q33. Satisfaction with democracy
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
0 The country is not a democracy 909
1 Not at all satisfied 13271


2 Not very satisfied 13054
3 Fairly satisfied 12193
4 Very satisfied 5083
## 8 Refused 53
9 Don’t know 1037

## Q34A
## Value Count
Label Q34a. How often president ignores laws
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 11485
## 1 Rarely 10974
## 2 Often 10492
## 3 Always 6843
## 8 Refused 161
9 Don’t know 4445
9994 Not asked in country 1200

## Q34B
## Value Count
Label Q34b. How often president ignores parliament
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 12679
## 1 Rarely 10882
## 2 Often 10216
## 3 Always 6200
## 8 Refused 148
9 Don’t know 4275
9994 Not asked in country 1200

## Q34C
## Value Count
Label Q34c. How often judges/magistrates prioritize political
influence over law

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 7736
## 1 Rarely 11004


## 2 Often 14282
## 3 Always 8767
## 8 Refused 104
9 Don’t know 3708

## Q34D
## Value Count
Label Q34d. How often people treated unequally under law
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 7155
## 1 Rarely 10062
## 2 Often 15526
## 3 Always 11183
## 8 Refused 79
9 Don’t know 1595

## Q34E
## Value Count
Label Q34e. How often officials unpunished
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 6918
## 1 Rarely 11109
## 2 Often 15489
## 3 Always 10064
## 8 Refused 85
9 Don’t know 1935

## Q34F
## Value Count
Label Q34f. How often ordinary people unpunished
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 17082
## 1 Rarely 11629
## 2 Often 8157
## 3 Always 7280
## 8 Refused 75
9 Don’t know 1376



## Q35
## Value Count
Label Q35. How free is news media
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
0 Not at all free 7080
1 Not very free 12698
2 Somewhat free 14457
3 Completely free 9769
8 Refused to answer 46
9 Don’t know 1551

## Q36A
## Value Count
Label Q36a. MPs listen
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 22079
1 Only sometimes 14648
## 2 Often 4861
## 3 Always 2602
## 8 Refused 43
9 Don’t know 1367

## Q36B
## Value Count
Label Q36b. Local government councillors listen
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 17165
1 Only sometimes 13663
## 2 Often 6230
## 3 Always 3305
## 8 Refused 14
9 Don’t know 1623
9994 Not asked in country 3600

## Q37A
## Value Count


Label Q37a. Trust president
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
0 Not at all 11562
1 Just a little 10434
## 2 Somewhat 8741
3 A lot 12437
## 8 Refused 249
9 Don’t know/Haven’t heard enough to say 977
9994 Not asked in country 1200

## Q37B
## Value Count
Label Q37b. Trust parliament/national assembly
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
0 Not at all 13455
1 Just a little 13430
## 2 Somewhat 9846
3 A lot 7233
## 8 Refused 119
9 Don’t know/Haven’t heard enough to say 1517

## Q37C
## Value Count
Label Q37c. Trust national electoral commission
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
0 Not at all 14229
1 Just a little 11120
## 2 Somewhat 9087
3 A lot 7862
## 8 Refused 113
9 Don’t know/Haven’t heard enough to say 1987
9994 Not asked in country 1200

## Q37D
## Value Count
Label Q37d. Trust your elected local government council
## Type Numeric


## Measurement Ordinal
## -1 Missing 0
0 Not at all 11730
1 Just a little 12942
## 2 Somewhat 8918
3 A lot 6552
## 8 Refused 54
9 Don’t know/Haven’t heard enough to say 1804
94 Not asked in country 0
9994 Not asked in country 3600

## Q37E
## Value Count
Label Q37e. Trust the ruling party
## Type Numeric
## Measurement Ordinal
## -1 Missing 1200
0 Not at all 12867
1 Just a little 10196
## 2 Somewhat 7467
3 A lot 6854
## 8 Refused 177
9 Don’t know/Haven’t heard enough to say 838
94 Not asked in country 0
9994 Not asked in country 6000

## Q37F
## Value Count
Label Q37f. Trust opposition political parties
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
0 Not at all 14461
1 Just a little 12818
## 2 Somewhat 7907
3 A lot 3947
## 8 Refused 196
9 Don’t know/Haven’t heard enough to say 1470
9994 Not asked in country 4800

## Q37G
## Value Count
Label Q37g. Trust police


## Type Numeric
## Measurement Ordinal
## -1 Missing 0
0 Not at all 12741
1 Just a little 12324
## 2 Somewhat 10243
3 A lot 9825
## 8 Refused 51
9 Don’t know/Haven’t heard enough to say 415

## Q37H
## Value Count
Label Q37h. Trust army
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
0 Not at all 7277
1 Just a little 9953
## 2 Somewhat 10619
3 A lot 16576
## 8 Refused 63
9 Don’t know/Haven’t heard enough to say 1111

## Q37I
## Value Count
Label Q37i. Trust courts of law
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
0 Not at all 10618
1 Just a little 13314
## 2 Somewhat 11270
3 A lot 8932
## 8 Refused 65
9 Don’t know/Haven’t heard enough to say 1400

## Q37J
## Value Count
Label Q37j. Trust Ministry of Health or public health agency
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
0 Not at all 7334


1 Just a little 12599
## 2 Somewhat 12477
3 A lot 12430
## 8 Refused 47
9 Don’t know/Haven’t heard enough to say 714

## Q37K
## Value Count
Label Q37k. Trust traditional leaders
## Type Numeric
## Measurement Ordinal
## -1 Missing 115
0 Not at all 6107
1 Just a little 8977
## 2 Somewhat 9344
3 A lot 12379
## 8 Refused 39
9 Don’t know/Haven’t heard enough to say 1441
9994 Not asked in country 7200

## Q37L
## Value Count
Label Q37l. Trust religious leaders
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
0 Not at all 5620
1 Just a little 10270
## 2 Somewhat 10821
3 A lot 18244
## 8 Refused 71
9 Don’t know/Haven’t heard enough to say 575

## Q37M
## Value Count
Label Q37m. Trust non-governmental organisations or civil
society organisations

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
0 Not at all 7033
1 Just a little 12322
## 2 Somewhat 12573


3 A lot 10186
## 8 Refused 71
9 Don’t know/Haven’t heard enough to say 3415

## Q38A
## Value Count
Label Q38a. Corruption: office of the Presidency
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 None 6479
1 Some of them 16495
2 Most of them 9476
3 All of them 6972
## 8 Refused 293
9 Don't know/ Haven’t heard 4685
9994 Not asked in country 1200

## Q38B
## Value Count
Label Q38b. Corruption: Members of Parliament
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 None 4679
1 Some of them 18244
2 Most of them 11346
3 All of them 6743
## 8 Refused 203
9 Don't know/ Haven’t heard 4386

## Q38C
## Value Count
Label Q38c. Corruption: Civil servants
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 None 3995
1 Some of them 21039
2 Most of them 11937
3 All of them 5233
## 8 Refused 131
9 Don't know/ Haven’t heard 3265



## Q38D
## Value Count
Label Q38d. Corruption: local government councillors
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 None 4745
1 Some of them 18817
2 Most of them 9641
3 All of them 5158
## 8 Refused 106
9 Don't know/ Haven’t heard 3533
94 Not asked in country 0
9994 Not asked in country 3600

## Q38E
## Value Count
## Label Q38e. Corruption: Police
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 None 3811
1 Some of them 17507
2 Most of them 13745
3 All of them 8344
## 8 Refused 145
9 Don't know/ Haven’t heard 2047

## Q38F
## Value Count
Label Q38f. Corruption: Judges and Magistrates
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 None 4650
1 Some of them 19596
2 Most of them 11098
3 All of them 6202
## 8 Refused 128
9 Don't know/ Haven’t heard 3926

## Q38G


## Value Count
Label Q38g. Corruption: Tax officials
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 None 4255
1 Some of them 17367
2 Most of them 11582
3 All of them 7271
## 8 Refused 139
9 Don't know/ Haven’t heard 4986

## Q38H
## Value Count
Label Q38h. Corruption: traditional leaders
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 None 8870
1 Some of them 17467
2 Most of them 6168
3 All of them 2838
## 8 Refused 82
9 Don't know/ Haven’t heard 2975
9994 Not asked in country 7200

## Q38I
## Value Count
Label Q38i. Corruption: religious leaders
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 None 13787
1 Some of them 21192
2 Most of them 5462
3 All of them 2208
## 8 Refused 113
9 Don't know/ Haven’t heard 2838

## Q38J
## Value Count
Label Q38j. Corruption: business executives
## Type Numeric


## Measurement Ordinal
## -1 Missing 115
## 0 None 4684
1 Some of them 20281
2 Most of them 11703
3 All of them 5103
## 8 Refused 96
9 Don't know/ Haven’t heard 3618

## Q38K
## Value Count
Label Q38k. Corruption: non-governmental organizations or
civil society organizations

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 None 8370
1 Some of them 21898
2 Most of them 6615
3 All of them 2796
## 8 Refused 102
9 Don't know/ Haven’t heard 5819

## Q39A
## Value Count
Label Q39a. Level of corruption
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Increased a lot 18397
2 Increased somewhat 5322
3 Stayed the same 10366
4 Decreased somewhat 6434
5 Decreased a lot 3181
## 8 Refused 60
9 Don’t know 1840

## Q39B
## Value Count
Label Q39b. Ordinary people can report corruption without
fear

## Type Numeric
## Measurement Nominal


## -1 Missing 0
0 Can report without fear 11681
1 Risk retaliation or other negative consequences 32629
## 8 Refused 59
9 Don’t know 1231

## Q40A
## Value Count
Label Q40a. Contact with public clinic or hospital
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 No 17978
## 1 Yes 27593
7 Not applicable 0
8 Refused to answer 4
9 Don't know 25

## Q40B
## Value Count
Label Q40b. Difficulty to obtain medical care
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Very easy 3602
## 2 Easy 9820
## 3 Difficult 8408
## 4 Very Difficult 5727
7 No contact / Not applicable 18007
## 8 Refused 6
9 Don't know 29

## Q40C
## Value Count
Label Q40c. Pay bribe for medical care
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 21467
1 Once or twice 2775
2 A few times 1885
## 3 Often 1397
7 No contact / Not applicable 18007


## 8 Refused 16
9 Don't know 52

## Q40D
## Value Count
Label Q40d. Problems with public clinic: lack of
medicine/supplies

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 7912
1 Once or twice 5659
2 A few times 6490
## 3 Often 7487
7 No contact 18007
8 Refuse to answer 2
9 Don't know 44

## Q40E
## Value Count
Label Q40e. Problems with public clinic: absence of medical
personnel

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 11967
1 Once or twice 5388
2 A few times 5700
## 3 Often 4466
7 No contact 18007
8 Refuse to answer 5
9 Don't know 67

## Q40F
## Value Count
Label Q40f. Problems with public clinic: long waiting time
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 5638
1 Once or twice 4973
2 A few times 6434
## 3 Often 10497


7 No contact 18007
8 Refuse to answer 4
9 Don't know 46

## Q40G
## Value Count
Label Q40g. Problems with public clinic: poor condition of
facilities

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 11194
1 Once or twice 4780
2 A few times 5518
## 3 Often 5802
7 No contact 18007
8 Refuse to answer 19
9 Don't know 279

## Q40H
## Value Count
Label Q40h. Problems with public clinic: high cost impact on
care

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 8875
1 Once or twice 4379
2 A few times 5957
## 3 Often 7441
7 No contact 17590
8 Refuse to answer 13
9 Don't know 144
9994 Not asked in country 1200

## Q41A
## Value Count
Label Q41a. Have medical aid coverage
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 No 35284
## 1 Yes 8855


7 Not applicable 0
8 Refused to answer 8
9 Don't know 253
9994 Not asked in country 1200

## Q41B
## Value Count
Label Q41b. Type of medical aid coverage
## Type Numeric
## Measurement Nominal
## -1 Missing 6
1 Private health insurance, for example, through an
employer, a hospital, or that you purchased yourself
that does not com
## 2224
2 Public sector insurance scheme, for example a civil
service or military insurance scheme
## 1346
3 National health insurance provided by the
government
## 4196
4 Community-based or mutual health insurance 797
5 Some other answer 193
## 7 Not Applicable 35545
8 Refused to Answer 9
9 Don’t know 85
9994 Not asked in country 1200

## Q41C
## Value Count
Label Q41c. Satisfaction with medical aid
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Not at all satisfied 892
2 Not very satisfied 1552
3 Fairly satisfied 3594
4 Very satisfied 2736
7 Not applicable 35545
8 Refused to Answer 3
9 Don’t know 78
9994 Not asked in country 1200

## Q41D
## Value Count
Label Q41d. Reason for no medical aid coverage


## Type Numeric
## Measurement Nominal
## -1 Missing 0
0 No health insurance schemes in this area/ in the
country
## 3584
1 Not aware of any health insurance schemes 7894
2 Don’t trust health insurance schemes 1865
3 Do not know how to enroll/too complicated 3788
4 Do not need health insurance/belief in good health/
too young to need health insurance
## 827
5 Cannot afford it 12301
6 Religious beliefs/God is my health insurance provider 310
7 Too old to care about health insurance 414
8 Pre-existing health conditions 230
88 Some other reason 2768
97 Not applicable 9116
98 Refused to Answer 42
99 Don’t know 1262
9994 Not asked in country 1200

## Q42A
## Value Count
Label Q42a. Worry about affording medical care
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
0 Not at all 5219
1 A little 6295
## 2 Somewhat 9496
3 A lot 24383
8 Refused to Answer 14
9 Don't know 193

## Q42B
## Value Count
Label Q42b. Government should ensure healthcare for all
even if more taxes

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Strongly disagree 5268
## 2 Disagree 6052
3 Neither agree nor disagree 1882


## 4 Agree 14398
5 Strongly agree 17654
8 Refused to Answer 13
9 Don't know 333

## Q43
## Value Count
Label Q43. Parents mandated to vaccinate children vs
personal choice

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
2 Agree with 1 35703
3 Agree with 2 9559
5 Agree with neither 172
8 Refused to answer 5
9 Don’t know 162

## Q44A
## Value Count
Label Q44a. Tried to obtain identity document
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 No 28544
## 1 Yes 17007
7 Not applicable 0
8 Refused to answer 8
9 Don't know 41

## Q44B
## Value Count
Label Q44b. Difficulty to obtain identity document
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Very easy 2521
## 2 Easy 5936
## 3 Difficult 4492
## 4 Very Difficult 4042
7 No contact / Not applicable 28593
## 8 Refused 2
9 Don't know 14



## Q44C
## Value Count
Label Q44c. Pay bribe for identity document
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 11967
1 Once or twice 2553
2 A few times 1291
## 3 Often 1159
7 No contact / Not applicable 28593
## 8 Refused 17
9 Don't know 19

## Q45A
## Value Count
Label Q45a. Requested assistance from the police
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 No 39866
## 1 Yes 5692
7 Not applicable 0
8 Refused to answer 12
9 Don't know 29

## Q45B
## Value Count
Label Q45b. Difficulty to obtain police assistance
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Very easy 775
## 2 Easy 1963
## 3 Difficult 1599
## 4 Very Difficult 1348
7 No contact / Not applicable 39907
## 8 Refused 2
9 Don't know 5

## Q45C
## Value Count


Label Q45c. Pay bribe to receive police assistance
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 3626
1 Once or twice 927
2 A few times 575
## 3 Often 552
7 No contact / Not applicable 39907
## 8 Refused 6
9 Don't know 6

## Q45D
## Value Count
Label Q45d. Contact with police in other situations
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 27525
1 Once or twice 6957
2 A few times 5327
## 3 Often 5632
7 No contact / Not applicable 0
## 8 Refused 14
9 Don't know 144

## Q45E
## Value Count
Label Q45e. Pay bribe to avoid problem with police
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 11260
1 Once or twice 2886
2 A few times 1856
## 3 Often 1863
7 No contact / Not applicable 27684
## 8 Refused 12
9 Don't know 38

## Q46PT1OTHER
## Value Count
Label Q46pt1other. MIP - 1st response (verbatim other)


## Type String
## Measurement Nominal
## 45485
## ABSENCE DE MÉDIA   1
## ABSENCE DE
## RELIGION
## 0
## ABSENCE OF FAMILY
## ROLE MODELS IN THE
## COMMUNITY
## 0
## ACESSO DE
## ESTRANGEIROS À
## CIDADANIA
## GUINEENSE
## 1
## AIR POLLUTION   0
## APPLICATION DE LA
## LOI ISLAMIQUE
## (CHARIA)
## 1
## BANIR LE NOUVEL
## ORDRE MONDIAL
## 1
## BORDER CONTROL   2
## BORDER OPENING   0
## BURUNDI REFUGEES
## SHOULD GO BACK
## HOME
## 1
## CLOSED BORDER   2
## COASTAL EROSION   0
## CONFLIT RELIGIEUX   1
## DECLINE IN YOUTH
## MORALS
## 0
## DRAINAGE IN FLOOD-
## PRONE AREAS
## 0
## ÉDUCATION SOCIALE   1
## ELEPHANTS ARE A
## CONSTANT THREAT
## 1
## EMIGRAÇÃO   2
## EXPULSION DE LA
## FRANCE DEMANDÉE
## 1
## FAMILY BREAKDOWN   3
## FERMETURE DES
## FRONTIÈRES
## 2
## FOLLOWING UP THE
## TRUTH
## 2
## FREE CROSS-BORDER   0


## FRONTIÈRES PEU
## CONTRÔLÉES
## 1
## FUITE DES CERVEAUX   1
## HARMS OF SOCIAL
## MEDIA
## 1
## HOME AFFAIRS ISSUE   1
## HONEST WORSHIP   2
## IL N'Y A PAS
## D'AVENIR RADIEUX
## POUR NOTRE JEUNE
## GÉNÉRATION ET LA
## PLUPART D'ENTRE
## EUX QUITTENT
## MAURICE
## 2
## ILLEGAL YOUTH
## MIGRATION
## 0
## IMMIGRATION &
## FOREIGN INFLUENCE
## 2
## IMMIGRATION
## CLANDESTINE
## 1
## IMMIGRATION
## CLANDESTINE DES
## TUNISIENS
## 2
## IMMIGRATION ISSUE   7
## IMPOSER LES LOIS DE
## L’ISLAM
## 2
## INCONSCIENCE DANS
## LA SOCIÉTÉ
## 1
## INCREASE IN
## NUMBER OF
## FOREIGNERS
## 0
## INCREASE WILDLIFE
## DAMAGE
## COMPENSATION
## 0
## JE N’AI PAS ENCORE
## ÉTÉ EMBAUCHE
## APRÈS VINGT ANS DE
## TRAVAIL, PAR LA
## SOCIÉTÉ SUCRE
## IVOIRE ZUENOULA
## 1
## L'IMMIGRATION   2
## LA DÉFORESTATION   2


## LA SPOLIATION DU
## PAYS PAR LES
## ÉTRANGERS
## 2
## LACK OF PARENT-
## CHILD TIME
## 1
## LACK OF TIMELY
## GOVERNMENT
## ASSISTANCE DURING
## DISASTERS
## 1
## LAZINESS AMONG
## BATSWANA
## 0
## LE PÈLERINAGE (HAJJ)   1
## LE PROBLÈME DES
## CHECKPOINTS
## ILLÉGAUX DES
## ARMÉES
## 1
## LE PROBLÈME DES
## FRONTIÈRES. LES
## ÉTRANGERS QUI
## ENTRENT VIENNENT
## AVEC BEAUCOUP DE
## PROBLÈMES
## 1
## LES DÉPLACÉS QUI
## COUPENT LES
## ARBRES EN
## DÉSORDRE
## 2
## LES ÉTRANGERS   2
## LES ÉTRANGERS
## SONT TROP DANS LE
## PAYS
## 1
## LES IMMIGRANTS
## VENANT DE
## L'AFRIQUE
## 1
## LES TRADITIONS
## PÈSENT SUR NOTRE
## DÉVELOPPEMENT
## 2
## LIMITATION OF
## SOCIAL MEDIA USE
## 2
## MANAGEMENT OF
## NATURAL DISASTERS
## LIKE FLOODING
## 0


## MANQUE
## D’INFORMATIONS
## SUR LES NOUVELLES
## DU PAYS
## 1
## MANQUE DE
## CONFIANCE DANS LA
## SOCIÉTÉ
## 1
## MANQUE DE
## MORALE
## 1
## MIGRANTS
## ÉTRANGERS
## 1
## MIGRATION
## IRRÉGULIÈRE DES
## HAOUSSA
## 1
## MISINFORMATION
## FROM MEDIA
## 1
## NO PROPER
## DRAINAGE, FLOODS
## ALL OVER
## 0
## NOISE POLLUTION   1
## NORMALIZATION
## WITH ISRAEL
## 2
## OPEN BORDERS   2
## OVERPOPULATION   1
## PANNES À LA RADIO
## NATIONALE : UN
## OBSTACLE À
## L’INFORMATION
## 1
## PARENTAL
## AUTHORITY
## UNDERMINED BY
## CHILDREN'S RIGHTS
## 1
## PRÉVALOIR LA
## MÉRITOCRATIE
## 2
## PRÉVENTION DE
## L'IMMIGRATION
## ILLÉGALE
## 2
## PROBLÈMES DE
## CIVISME
## 1
## PROMOUVOIR
## L’ISLAM
## 1
## REDUCE ILLEGAL
## IMMIGRATION
## 2


## RÉDUCTION DU
## MONTANT DE LA
## DOT
## 1
## REJET DES
## TANZANIENS
## 2
## RETOUR À L'ISLAM
## AUTHENTIQUE
## 3
## RISING SOCIAL
## ISSUES
## 12
## THREAT TO
## SEYCHELLES'
## SOVEREIGNTY
## 1
## TOO MANY
## REFUGEES
## 1
## TOUS LES ASPECTS
## DE LA VIE
## QUOTIDIENNNE
## 2
## TRADITION   1
## TROP DE RÉFUGIÉS   2
## VOYAGE À
## L'ETRANGER
## 2
## WE HAVE LOST OUR
## CULTURE AND
## IDENTITY
## 0
## WEAK IMMIGRATION
## POLICIES
## 1
## WILD ANIMALS   1
## WILDLIFE CONFLICT
## WITH LOCAL PEOPLE
## 0
## YOUTH UNWILLING
## TO WORK
## 1

## Q46PT1
## Value Count
Label Q46pt1. Most important problems - 1st response
## Type Numeric
## Measurement Nominal
## -1 Missing 0
0 Nothing/ No problems 118
1 Management of the economy 1673
2 Wages, incomes and salaries 737
## 3 Unemployment 6697
## 4 Poverty/ Destitution 1584
5 Rates and taxes 275


## 6 Loans / Credit 199
## 7 Farming/ Agriculture 968
8 Food shortage/ Famine 2815
## 9 Drought 438
## 10 Land 88
## 11 Transportation 234
## 12 Communications 67
## 13 Infrastructure / Roads 3462
## 14 Education 2504
## 15 Housing 288
## 16 Electricity 1725
17 Water supply 3913
18 Orphans/ Street children/ Homeless children 51
## 19 Services (other) 539
## 20 Health 5285
## 21 AIDS 8
## 22 Sickness / Disease 90
23 Crime and security 2771
## 24 Corruption 1618
25 Political violence 68
26 Political instability/ Political divisions/ Ethnic tensions 163
## 27 Discrimination/ Inequality 115
28 Gender issues / Women’s rights 131
29 Democracy/ Political rights 373
## 30 War (international) 2
31 Civil war 126
32 Agricultural marketing 206
33 Climate change 132
## 34 COVID-19 1
35 Increasing cost of living 4420
## 900 Drogues 224
901 Inondation/système de drainage 79
1580 Shortage of basic food products in the market 84
## 1680 Drugs 226
9995 Other responses 117
## 9998 Refused 704
9999 Don’t know 284

## Q46PT2OTHER
## Value Count
Label Q46pt2other. MIP - 2nd response (verbatim other)
## Type String
## Measurement Nominal


## 45485
## A BIODIVERSIDADE   1
## ACCÉLÉRER LA
## DÉLIVRANCE DES
## VISAS
## 2
## AGE LIMIT
## REDUCTION
## 3
## ALLOW EMPLOYEES
## TO TRAVEL TO
## SOUTH AFRICA
## FREELY WITHOUT A
## PASSPORT
## 1
## BAN ALCOHOL
## IMPORTS
## 1
## BEAUCOUP DE
## POINTS DE
## CONTRÔLE DOIVENT
## ÊTRE RÉDUITS
## 1
## BORDER OPENING   0
## CHILDBIRTH
## CONTROL
## 0
## CHINESE DEALINGS
## IN ZIMBABWE ARE
## NOT BENEFICIAL FOR
## US
## 1
## CHINESE
## EXPLOITATION OF
## OUR RIVERS
## 1
## COMMUNITY MORAL
## INSTITUTIONS
## 0
## CORRUPTION
## MORALE
## 1
## CRIAÇÃO DE MAIS
## EMPREGO
## 1
## CULTURAL
## DIFFICULTIES
## 0
## CUTTING TREES   1
## DANGEROUS
## ANIMALS IN STREETS
## 1
## DESTRUCTION   1
## DISORDERLY YOUTH   0
## EARTHQUAKES AND
## LANDSLIDES
## 1


## EASE CROSS-BORDER
## MOVEMENT
## 1
## ENABLE FREE
## MOVEMENT TO
## SOUTH AFRICA
## 1
## ENTRY TO MALAWI
## ONLY WITH VALID
## DOCUMENTS
## 1
## EVIDENCE-BASED
## DECISION MAKING
## 2
## EXODE RURAL   1
## EXPATS FAVORED
## OVER SEYCHELLOIS
## 1
## FACILITER
## L’ÉMIGRATION DES
## JEUNES
## 1
## FAKE NEWS   0
## FAMILY   0
## FOREST CLEARING
## NEAR HOUSES
## 0
## FRONTEIRA FECHADA
## CABO VERDE-
## PORTUGAL
## 0
## FUITE DES CERVEAUX   0
## GARANTIR LE
## RESPECT DES DROITS
## DES TRAVAILLEURS
## 2
## HUMAN-WILDLIFE
## CONFLICT
## 0
## ILLEGAL MIGRATION   1
## ILLEGAL MIGRATION
## CAUSING YOUTH
## DEATHS
## 1
## ILLEGAL YOUTH
## MIGRATION
## 1
## IMMIGRATION
## ILLÉGALE
## 1
## IMMIGRATION ISSUE   9
## IMPROVE
## IMMIGRATION
## SERVICES
## 2


## INCREASE IN
## DEPENDENCY,
## ESPECIALLY AMONG
## POLYGAMOUS
## FAMILIES
## 0
## INCREASED HUMAN-
## WILDLIFE CONFLICTS
## 0
## L'APPLICATION
## TIKTOK CAUSE UNE
## MAUVAISE
## RÉPUTATION AU
## PAYS
## 0
## L'AVENIR DES
## ENFANTS EST
## INCONNU
## 1
## L'ÉGOÏSME   1
## L'IMMIGRATION   3
## LA MIGRATION
## IRRÉGULIÈRE
## 2
## LA PRÉSERVATION
## DU STATUT DE LA
## CLASSE
## INTELLECTUELLE
## 1
## LA RIGUEUR   1
## LACK OF
## LEGALIZATION OF
## SOCIAL MEDIA
## 1
## LE CIVISME   1
## LES LOBBIES   2
## LET NATIONALS
## ACCESS MABIRA
## 0
## LET THE PEOPLE IN
## THE AREA UTILISE
## THE FOREST RESERVE
## WITHOUT
## RESTRICTIONS
## 0
## LIMITED
## TECHNOLOGY
## ACCESS
## 0
## LUTTER CONTRE
## L’EXPLOITATION DES
## EMPLOYEURS
## 0
## MANQUE DE
## MORALE
## 1


## MENDIANTS   1
## MORAL DECAY   0
## MORE TEENAGERS
## ON THE STREETS
## 0
## OPEN BORDERS   0
## OPEN OUR BORDER   0
## OPENING OF
## BORDERS
## 1
## OPENING OF CROSS-
## BORDER
## 0
## PARENTS
## IRRESPONSABLES
## 1
## PERTE DE RESPECT
## DES AÎNÉS PAR LES
## JEUNES
## 1
## POLLUTION   1
## POOR PARENTING   1
## PRÉVENIR
## L'IMMIGRATION
## CLANDESTINE
## 1
## PRÉVISIONS
## MÉTÉOROLOGIQUES
## PLUS PRÉCISES POUR
## PRENDRE DES
## PRÉCAUTIONS
## AVANT DE SORTIR
## TRAVAILLER
## 3
## PROMOVER
## EMPRESAS DE
## QUALIDADE
## 0
## REBATIR LE
## CAMEROUN AVEC LA
## SPIRITUALITÉ
## 1
## REDUCE FOREIGNERS   7
## RÉDUCTION DU
## MONTANT DE LA
## DOT
## 1
## RÉDUIRE LES
## OBSTACLES AU
## MARIAGE LIÉS AUX
## DIFFICULTÉS
## ÉCONOMIQUES
## 1
## RELIGION   1


## REMOVE BARRIERS
## TO CROSSING THE
## BORDER
## 2
## RENFORCER LE
## CIVISME
## 0
## RESOLVER A
## QUESTÃO
## MIGRATÓRIA,
## COMBATENDO A
## IMIGRAÇÃO ILEGAL
## NO PAÍS
## 1
## RETIREMENT AGE
## LIMIT
## 1
## SEGUNDO VISTO   1
## SENSIBILISATION DE
## LA POPULATION
## 1
## SEPARAÇÃO
## FAMILIAR
## 1
## SEYCHELLOIS
## UNWILLING TO
## WORK
## 0
## SOCIAL AND
## WELFARE PROBLEMS
## IN FAMILIES
## 2
## SOCIAL ISOLATION   0
## SOCIAL MEDIA   1
## SOCIAL PROBLEMS   12
## SOCIAL PROBLEMS
## BETWEEN FAMILIES
## 1
## STOP CYLINDER
## CIRCULATION
## 0
## STOP ILLEGAL
## FOREIGNERS
## 0
## STRENGTHENING
## ISLAM IN THE
## COUNTRY
## 1
## STRICT BORDER
## CONTROL
## 1
## SUIVRE LES CONSEILS
## ISLAMIQUES
## 1
## SUPERSTITION   0


## THE GOVERNMENT
## SHOULD SIMPLIFY
## THE PROCESS FOR
## CROSSING COUNTRY
## BORDERS
## 2
## TOO MANY EXPAT
## WORKERS
## 1
## TOO MANY MIGRANT
## WORKERS
## 1
## TOO MUCH
## IMMIGRATION
## 0
## TROP D'ACTIVITÉS DE
## JEU
## 0
## TROP DE
## BANGLADAIS
## TRAVAILLENT À
## MAURICE, CERTAINS
## SANS PAPIERS, LE
## GOUVERNEMENT
## DOIT CESSER DE
## PRENDRE DES
## BANGLADAIS POUR
## TRAVAILLER À
## MAURICE
## 1
## TROP DE JEUNES
## QUITTENT LE PAYS
## CAR IL N'Y A AUCUNE
## ASSURANCE D'UN
## AVENIR MEILLEUR
## 1
## VISITA ZONA POBRE   0
## WILD ANIMALS
## THREATEN CHILDREN
## 0
## WITCHCRAFT   0
## YOUTH LACK
## RESPECT
## 0

## Q46PT2
## Value Count
Label Q46pt2. Most important problems - 2nd response
## Type Numeric
## Measurement Nominal
## -1 Missing 0
0 Nothing/ No problems 0
1 Management of the economy 1068


2 Wages, incomes and salaries 851
## 3 Unemployment 4349
## 4 Poverty/ Destitution 1427
5 Rates and taxes 351
## 6 Loans / Credit 316
## 7 Farming/ Agriculture 1242
8 Food shortage/ Famine 1953
## 9 Drought 342
## 10 Land 129
## 11 Transportation 392
## 12 Communications 155
## 13 Infrastructure / Roads 3334
## 14 Education 3930
## 15 Housing 491
## 16 Electricity 2495
17 Water supply 3533
18 Orphans/ Street children/ Homeless children 78
## 19 Services (other) 691
## 20 Health 6536
## 21 AIDS 18
## 22 Sickness / Disease 90
23 Crime and security 2359
## 24 Corruption 1094
25 Political violence 38
26 Political instability/ Political divisions/ Ethnic tensions 133
## 27 Discrimination/ Inequality 184
28 Gender issues / Women’s rights 210
29 Democracy/ Political rights 461
## 30 War (international) 3
31 Civil war 32
32 Agricultural marketing 250
33 Climate change 139
## 34 COVID-19 1
35 Increasing cost of living 3372
## 900 Drogues 122
901 Inondation/système de drainage 84
1580 Shortage of basic food products in the market 79
## 1680 Drugs 112
9995 Other responses 115
9996 No further reply 3042
## 9998 Refused 0
9999 Don’t know 0



## Q46PT3OTHER
## Value Count
Label Q46pt3other. MIP - 3rd response (verbatim other)
## Type String
## Measurement Nominal
## 45494
## ATTITUDE TOWARDS
## NATIONAL DUTY
## 1
## AUTONOMISATION
## DES ÎLES
## 1
## BORDER CONTROL
## NEEDED
## 0
## BORDER OPENING   0
## CHRISTIANITY AT ITS
## PEAK
## 1
## CLOSED BORDERS   1
## CLOSURE OF
## BORDERS
## 1
## COMUNICAÇÃO
## SOCIAL PARA O POVO
## 1
## CONTRE
## L'IMMIGRATION
## 0
## DECLINE IN VALUES   0
## DÉFICIENCE MORALE   0
## DEFORESTATION   1
## DEPENDENCY
## AMONG MANY
## FAMILIES
## 0
## DEPORTATION   0
## DÉSTRUCTION DES
## RIVIÈRES PAR LES
## CHINOIS POUR L'OR
## 1
## DIFFICULTÉ DE
## TRAVERSER LES
## FRONTIÈRES
## 1
## DIFFICULTY IN
## GETTING
## PERMISSION TO
## CROSS BORDERS FOR
## BUSINESS
## 0
## DISHONESTY IN
## SOCIETY
## 1
## DISTANCE AVEC MA
## MÈRE
## 0


## EARTHQUAKE   1
## ÉLÉPHANTS
## DÉVASTENT LES
## CULTURES
## 1
## ÉMIGRATION DES
## GENS COMPÉTENTS
## À L'EXTÉRIEUR
## 1
## ÉMIGRATION DES
## JEUNES
## 0
## ENCADRER LE
## SERVICE MILITAIRE
## ET LES VACANCES
## MILITAIRES
## OBLIGATOIRES
## 1
## EXPATRIATE   0
## FACILITER
## L’OBTENTION DES
## VISAS
## 2
## FAILURE TO ADHERE
## TO RELIGION
## 1
## FAMILY ISSUES   3
## FERMETURE DE LA
## FRONTIÈRE
## 1
## FORÇA   1
## FUITE DES CERVEAUX   1
## HIGH COSTS OF
## ACCESS TO THE HOLY
## SITE
## 2
## HOME AFFAIRS ISSUE   1
## IMIGRAÇÃO   1
## IMMIGRATION   2
## IMMIGRATION
## CLANDESTINE
## 2
## IMMIGRATION ISSUE   6
## IMMIGRATION TOO
## MUCH
## 1
## INCONSCIENCE
## SOCIALE
## 0
## INTELLECTUAL
## IMMATURITY
## 1
## INTERDICTION DE
## L'IMMIGRATION
## 1
## INVESTIR NA
## JUVENTUDE
## 1


## JE VEUX ME MARIER   0
## L'ABSENCE DE
## CONSCIENCE
## 1
## L'ÉMIGRATION   1
## LA CROYANCE EN
## DIEU
## 0
## LA FUITE DES
## CERVEAUX
## 1
## LA MALTRAITANCE
## ANIMALE
## 1
## LA MÉTÉO MAURICE
## EST COMME UNE
## BLAGUE, LEURS
## PRÉVISIONS
## MÉTÉOROLOGIQUES
## SONT L'OPPOSÉ DE
## CE QU'ILS DISENT
## 1
## LA PUNITION
## CORPORELLE SUR LES
## ENFANTS DOIT ÊTRE
## AUTORISÉE
## 1
## LAND POLLUTION   0
## LE DÉRACINEMENT
## CULTUREL DE LA
## JEUNESSE
## 2
## LE PÈLERINAGE (HAJJ)   0
## LES CARBURANTS   1
## LES CITOYENS
## MANQUENT DE
## CONFIANCE
## 1
## LIBRE CIRCULATION   0
## LOSS OF NATIONAL
## IDENTITY
## 1
## LUTTE CONTRE LE
## CÉLIBAT
## 2
## LUTTER CONTRE
## L'IMMIGRATION
## CLANDESTINE
## 1
## LUTTER CONTRE
## L’ÉMIGRATION
## CLANDESTINE
## 4
## LUTTER CONTRE LA
## MIGRATION
## CLANDESTINE
## 1


## MAIOR
## RESPONSABILIZAÇÃO
## DOS PAIS
## 0
## MANY IMMIGRANTS
## ARE ILLEGAL
## 1
## MANY
## UNDOCUMENTED
## REFUGEES
## 1
## MAUVAISES
## COMPORTEMENT
## DES JEUNES
## 1
## MENTALITÉ DES
## INDIVIDUS
## 1
## MENTALITÉ DES
## POPULATIONS
## LOCAUX
## 1
## MORAL EROSION   0
## NATIONALISATION   1
## NÉGLIGENCE DE LA
## RELIGION
## 0
## NEIGHBOURHOOD
## SOCIAL PROBLEM
## 1
NGOs SHOULD BE
## FREE TO HELP
## 0
## OPEN BORDERS   1
## OPENING OF
## BORDERS
## 0
## ORGANIZAÇÃO DO
## PAÍS
## 2
## OUVERTURE DE
## FRONTIÈRE POUR LA
## LIBRE CIRCULATION
## DES BIENS
## 1
## OUVERTURE DES
## FRONTIÈRES
## 2
## PARENTING   1
## PARTAGE DE L’AIDE
## AUX BESOINS, MAIS
## PAS PAR LE
## GOUVERNEMENT
## 1
## PAYS OCCIDENTAUX   1
## PEOPLE DON'T
## KNOW JESUS
## 1


## POLLUTION   1
## POOR CONDITIONS
## FOR IMMIGRANTS
## 1
## POPULATION   3
## PRESERVATION OF
## LOCAL TRADITION
## AND CULTURE
## 1
## PRIORITÉ AUX
## CONGOLAIS POUR
## LES POSTES
## 1
## PROBLÈME AVEC LA
## COMMUNAUTÉ
## INTERNATIONALE
## 3
## PROBLÈME LITIGIEUX   0
## PROTECTION DES
## RICHESSES
## CULTURELLES
## 1
## RÉDUCTION DE LA
## POPULATION DANS
## LE VILLAGE
## 1
## RÉDUIRE LA DURÉE
## DE LA GARDE À VUE
## DANS LES PRISONS
## 1
## RÉDUIRE LES
## RÉFUGIÉS POUR LES
## BOULOTS
## 0
## REFUGEES   0
## REOPENING OF
## CLOSED BORDERS
## 2
## RIEN N'EST BIEN   1
## RURAL-URBAN
## MIGRATION LEAVING
## VACANT HOMES
## 0
## SERVICE MILITAIRE
## ET VACANCES
## MILITAIRES
## OBLIGATOIRES
## 1
## SOCIAL ILLS   0
## SOCIAL ISOLATION   0
## SOCIAL PROBLEMS   2
## SOCIAL PROBLEMS IN
## FAMILIES
## 0
## SOIS REMPLI
## SPIRITUELLEMENT
## 1


## SPIRITUAL DECLINE &
## BLACK MAGIC
## 0
## SURVEILLANCE DES
## PROGRAMMES TV
## 1
## SYNDICAT DU
## TRAVAIL
## 1
## TECHNOLOGY
## ADDICTION
## 1
## TOO MUCH SOCIAL
## ILLS
## 1
## TRAVELING
## PROBLEMS
## 0
## TROP DE TOURISTES
## DANS LE PAYS
## 1
## URBANISATION   1
## WITCHCRAFT   1
## YOUTH LACK ETHICS
## & MANNERS
## 1
## YOUTH SOCIAL
## PROBLEMS
## 2

## Q46PT3
## Value Count
Label Q46pt3. Most important problems - 3rd response
## Type Numeric
## Measurement Nominal
## -1 Missing 0
0 Nothing/ No problems 0
1 Management of the economy 898
2 Wages, incomes and salaries 749
## 3 Unemployment 3810
## 4 Poverty/ Destitution 1303
5 Rates and taxes 304
## 6 Loans / Credit 345
## 7 Farming/ Agriculture 1306
8 Food shortage/ Famine 1411
## 9 Drought 268
## 10 Land 132
## 11 Transportation 579
## 12 Communications 153
## 13 Infrastructure / Roads 3495
## 14 Education 4139
## 15 Housing 574


## 16 Electricity 2160
17 Water supply 2815
18 Orphans/ Street children/ Homeless children 121
## 19 Services (other) 789
## 20 Health 5230
## 21 AIDS 19
## 22 Sickness / Disease 81
23 Crime and security 2327
## 24 Corruption 1150
25 Political violence 64
26 Political instability/ Political divisions/ Ethnic tensions 138
## 27 Discrimination/ Inequality 218
28 Gender issues / Women’s rights 169
29 Democracy/ Political rights 476
## 30 War (international) 0
31 Civil war 40
32 Agricultural marketing 230
33 Climate change 148
## 34 COVID-19 4
35 Increasing cost of living 2585
## 900 Drogues 102
901 Inondation/système de drainage 77
1580 Shortage of basic food products in the market 31
## 1680 Drugs 90
9995 Other responses 109
9996 No further reply 6965
## 9998 Refused 0
9999 Don’t know 0

## Q47A
## Value Count
Label Q47a. Handling managing the economy
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Very badly 17365
2 Fairly badly 12024
3 Fairly well 11586
4 Very well 3047
## 8 Refused 48
9 Don't know / Haven’t heard enough to say 1529

## Q47B


## Value Count
Label Q47b. Handling improving living standards of the poor
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Very badly 20510
2 Fairly badly 12971
3 Fairly well 9073
4 Very well 2305
## 8 Refused 42
9 Don't know / Haven’t heard enough to say 699

## Q47C
## Value Count
Label Q47c. Handling creating jobs
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Very badly 23366
2 Fairly badly 11193
3 Fairly well 7868
4 Very well 2487
## 8 Refused 30
9 Don't know / Haven’t heard enough to say 656

## Q47D
## Value Count
Label Q47d. Handling keeping prices stable
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Very badly 25282
2 Fairly badly 11928
3 Fairly well 6229
4 Very well 1685
## 8 Refused 27
9 Don't know / Haven’t heard enough to say 449

## Q47E
## Value Count
Label Q47e. Handling narrowing income gaps
## Type Numeric
## Measurement Ordinal


## -1 Missing 0
1 Very badly 22612
2 Fairly badly 13420
3 Fairly well 6482
4 Very well 1764
## 8 Refused 47
9 Don't know / Haven’t heard enough to say 1275

## Q47F
## Value Count
Label Q47f. Handling reducing crime
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Very badly 17268
2 Fairly badly 9924
3 Fairly well 12835
4 Very well 4810
## 8 Refused 33
9 Don't know / Haven’t heard enough to say 730

## Q47G
## Value Count
Label Q47g. Handling improving basic health services
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Very badly 13018
2 Fairly badly 11635
3 Fairly well 16029
4 Very well 4338
## 8 Refused 18
9 Don't know / Haven’t heard enough to say 562

## Q47H
## Value Count
Label Q47h. Handling addressing educational needs
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Very badly 11902
2 Fairly badly 10538
3 Fairly well 16828


4 Very well 5715
## 8 Refused 22
9 Don't know / Haven’t heard enough to say 595

## Q47I
## Value Count
Label Q47i. Handling providing water and sanitation services
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Very badly 16431
2 Fairly badly 10718
3 Fairly well 13226
4 Very well 4779
## 8 Refused 27
9 Don't know / Haven’t heard enough to say 419

## Q47J
## Value Count
Label Q47j. Handling fighting corruption
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Very badly 17303
2 Fairly badly 11362
3 Fairly well 11083
4 Very well 3698
## 8 Refused 103
9 Don't know / Haven’t heard enough to say 2051

## Q47K
## Value Count
Label Q47k. Handling maintaining roads and bridges
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Very badly 14884
2 Fairly badly 9789
3 Fairly well 14629
4 Very well 5764
## 8 Refused 37
9 Don't know / Haven’t heard enough to say 498



## Q47L
## Value Count
Label Q47l. Handling providing a reliable supply of electricity
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Very badly 15487
2 Fairly badly 9028
3 Fairly well 14063
4 Very well 6326
## 8 Refused 31
9 Don't know / Haven’t heard enough to say 665

## Q47M
## Value Count
Label Q47m. Handling preventing or resolving violent
conflict

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Very badly 11088
2 Fairly badly 11167
3 Fairly well 15829
4 Very well 5110
## 8 Refused 65
9 Don't know / Haven’t heard enough to say 2341

## Q48A
## Value Count
## Label Q48a. Performance: President
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Strongly disapprove 9119
## 2 Disapprove 10001
## 3 Approve 14735
4 Strongly approve 7847
## 8 Refused 423
9 Don’t know or haven't heard enough to say 2274
9994 Not asked in country 1200

## Q48B
## Value Count


Label Q48b. Performance: MP/National Assembly rep
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Strongly disapprove 10281
## 2 Disapprove 13979
## 3 Approve 13207
4 Strongly approve 3198
## 8 Refused 199
9 Don’t know or haven't heard enough to say 3535
9994 Not asked in country 1200

## Q48C
## Value Count
Label Q48c. Performance: local government councillor
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Strongly disapprove 8814
## 2 Disapprove 12335
## 3 Approve 13822
4 Strongly approve 3617
## 8 Refused 103
9 Don’t know or haven't heard enough to say 3309
94 Not asked in country 0
9994 Not asked in country 3600

## Q49A
## Value Count
Label Q49a. Community leaders effective in promoting
young leaders

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Strongly disagree 9656
## 2 Disagree 11681
3 Neither Agree or disagree 2229
## 4 Agree 14604
5 Strongly agree 5841
8 Refused to Answer 28
9 Don't know 1560

## Q49B


## Value Count
Label Q49b. Men have more right to job
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Strongly disagree 15132
## 2 Disagree 10909
3 Neither Agree or disagree 1940
## 4 Agree 9655
5 Strongly agree 7556
8 Refused to Answer 24
9 Don't know 383

## Q50
## Value Count
Label Q50. Priorities for investment in youth programs
## Type Numeric
## Measurement Nominal
## -1 Missing 0
1 Job creation 21975
## 2 Education 7442
3 Jobs training 6147
4 Access to business loans 5681
5 Social services for youth, for example, to improve
health and prevent drug abuse
## 3780
6 None of the above/some other programs 218
7 Government should not increase its spending on
programs to help young people
## 142
8 Refused to answer 6
9 Don’t know 210

## Q51
## Value Count
Label Q51. Men only as leaders vs women leaders
## Type Numeric
## Measurement Ordinal
## -1 Missing 114
2 Agree with 1 10971
3 Agree with 2 33614
5 Agree with neither 613
8 Refused to answer 23
9 Don’t know 265



## Q52A
## Value Count
Label Q52a. Girls miss school because boys' education
prioritized

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 30066
## 1 Rarely 9340
## 2 Often 4100
## 3 Always 1655
8 Refused to answer 19
9 Don’t know 421

## Q52B
## Value Count
Label Q52b. Girl students face discrimination, harassment
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 17966
## 1 Rarely 13455
## 2 Often 9499
## 3 Always 2947
8 Refused to answer 33
9 Don’t know 1700

## Q52C
## Value Count
Label Q52c. Women face harassement in public places
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 17714
## 1 Rarely 13986
## 2 Often 9372
## 3 Always 3270
8 Refused to answer 31
9 Don’t know 1227

## Q52D
## Value Count


Label Q52d. Women prevented from paid employment by
family

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 20934
## 1 Rarely 13140
## 2 Often 7718
## 3 Always 2633
8 Refused to answer 35
9 Don’t know 1141

## Q53A
## Value Count
Label Q53a. Police/courts do enough to protect women/girls
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Need to do much more 22987
2 Need to do somewhat more 12563
3 Doing enough 8879
8 Refused to answer 23
9 Don’t know 1148

## Q53B
## Value Count
Label Q53b. People believe women/girls' complaints
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Not at all likely 5958
2 Not very likely 8825
3 Somewhat likely 15422
4 Very likely 14206
8 Refused to answer 23
9 Don’t know 1166

## Q54
## Value Count
Label Q54. Preferred resolution source for legal problems
## Type Numeric
## Measurement Nominal
## -1 Missing 55


0 Nowhere / I would not try to resolve it / There is no
place to go / No hope of chance for resolution
## 1348
1 A traditional leader or traditional court 9900
2 The police 18524
3 A lawyer 1449
4 A legal aid service 1011
5 A local court 2955
6 A mediator, arbitrator, or counsellor, or service for
“alternative dispute resolution”
## 549
7 Religious leaders 766
8 Family members 2809
## 9 Prayer / God 730
## 10 Elders 1881
11 Political leaders 2193
12 Government official 697
## 95 Other 148
98 Refused to answer 67
99 Don’t know 517

Q54Other
## Value Count
Label Q54other. Preferred resolution source for legal
problems (verbatim)

## Type String
## Measurement Nominal
## 45452
## A JUSTIÇA COMPLICA
## AINDA MAIS
## 1
## ADMINISTRATION   2
## AFFAIRES SOCIALES   1
## AMI DE LA
## PERSONNE DONT JE
## SUI
## 1
## AMICALEMENT   3
## AMIS   8
## ANY PERSON FROM
## MY AREA
## 1
## ARMY   1
## ASSOCIATION   1
## ASSOCIATION DES
## JEUNES
## 1
## BUREAU D'EMPLOI   1
## BY MYSELF   4


## CENTRO DE ACESSO
## À JUSTIÇA
## 2
## CHARLATAN   1
## COMITÊ   2
## COMMISSION DE
## DROIT L'HOMME
## 1
## COMMUNITY
## GROUPS
## 1
## COORDENADOR DO
## BAIRRO
## 5
## DEPENDS ON THE
## ISSUE
## 1
## DEPENDS ON THE
## PROBLEM
## 0
## DISCUSS FIRST   2
## DJARGA   1
## FRIEND   1
## FRIENDS   3
## GESTOR   1
## HE FIGHTS FOR
## HIMSELF
## 0
## I GO TO MY BOSS
## THAT RECRUITED
## 2
## IMMEDIATE
## SUPERVISOR
## 0
## IMPRENSA   0
## INSPECTION DU
## TRAVAIL
## 3
## IRÃ   1
## IT DEPENDS   2
## JE N'AI PAS DES
## PROBLÈMES
## 5
## JUSTIÇA COM AS
## PRÓPRIAS MÃO
## 1
## LA PERSONNE
## PROCHE DE LA PERSO
## 1
## LABOR OFFICE   1
## LES AMIS   2
## LÍDER TRADICIONAL   1
## MEDIA   2
## MES AMIS   2
## MÍDIA SOCIAL   2
## MOI MÊME   23


## MUSASA PROJECT   1
## MY DIRECTOR AT THE
## OFFICE
## 2
## NEIGHBOR   0
## NEIGHBORS   4
## NEIGHBOUR   1
## NEIGHBOURS   1
## NGO   1
## NOTRE PRÉSIDENTE
## DES FEMMES
## 1
## OMA   0
## OMM -
## ORGANIZAÇÃO DA
## MULHER
## 0
## ORGANISATION NON
## GOUVERNEMENTA
## 1
## ORGANISATIONS OR
## NGOS
## 15
## OTHER BUSINESS
## PEOPLE
## 0
## PROFESSEUR   1
## QUELQU'UN À QUI
## ON FAIT CONFI
## 1
## RADIO   1
## REDE SOCIAL   1
## RESOLVING OUR
## ISSUES INTERNALL
## 1
## ROAD STATION   0
## SOCIAL MEDIA   2
## SYNDICAT   2
## SYNDICATS   1
## TALK TO MEDIA
## LEADERS
## 0
## THE PERSON
## INVOLVED
## 1
## TO THE COMPANY   1
## TV   3
## UN NGANGAN   0
## UNE ASSOCIATION
## COMMUNALE
## 1
## VOISINS   1
## WOMAN AND MAN
## NETWORK
## 8


## WOMEN NETWORK   1
## WOMEN'S AFFAIRS   1

## Q55A
## Value Count
Label Q55a. Access to legal support
## Type Numeric
## Measurement Ordinal
## -1 Missing 115
0 Not at all likely 10042
1 Not very likely 9638
2 Somewhat likely 14862
3 Very likely 9229
## 8 Refused 54
9 Don’t know 1660

## Q55B
## Value Count
Label Q55b. Affordability of legal support
## Type Numeric
## Measurement Ordinal
## -1 Missing 115
0 Not at all likely 12201
1 Not very likely 10848
2 Somewhat likely 13123
3 Very likely 7754
## 8 Refused 66
9 Don’t know 1494

## Q55C
## Value Count
Label Q55c. Affordability of court case
## Type Numeric
## Measurement Ordinal
## -1 Missing 115
0 Not at all likely 13898
1 Not very likely 10541
2 Somewhat likely 11872
3 Very likely 8137
## 8 Refused 52
9 Don’t know 984

## Q55D


## Value Count
Label Q55d. Court case: Timeliness of resolution
## Type Numeric
## Measurement Ordinal
## -1 Missing 115
0 Not at all likely 11069
1 Not very likely 12471
2 Somewhat likely 13224
3 Very likely 6362
## 8 Refused 55
9 Don’t know 2304

## Q55E
## Value Count
Label Q55e. Court case: Fairness of  resolution
## Type Numeric
## Measurement Ordinal
## -1 Missing 115
0 Not at all likely 9413
1 Not very likely 10425
2 Somewhat likely 15045
3 Very likely 8233
## 8 Refused 67
9 Don’t know 2302

## Q56
## Value Count
Label Q56. Awareness of legal aid services
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 No 33559
## 1 Yes 11291
7 Not applicable 0
8 Refused to answer 12
9 Don't know 738

## Q57A
## Value Count
Label Q57a. Confidence in obtaining justice
## Type Numeric
## Measurement Ordinal
## -1 Missing 0


0 Not at all confident 7962
1 Not very confident 13694
2 Somewhat confident 15777
3 Very confident 7005
8 Refused to Answer 34
9 Don’t know 1129

## Q57B
## Value Count
Label Q57b. Severity of penalties for crimes by ordinary
people

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 1 Too Lenient 5975
2 About right 22238
3 Too harsh 15007
8 Refused to Answer 58
9 Don’t know / Haven’t heard enough to say 2321

## Q58
## Value Count
Label Q58. Severity of penalties for crimes by powerful
people

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Too lenient 22052
2 About right 16268
3 Too harsh 4480
8 Refused to Answer 82
9 Don’t know / Haven’t heard enough to say 2718

## Q59A
## Value Count
Label Q59a. Severity of droughts
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Much more severe 14929
2 Somewhat more severe 8408
3 Stayed the same 7845
4 Somewhat less severe 6937


5 Much less severe 5994
8 Refused to answer 15
9 Don’t know 1472

## Q59B
## Value Count
Label Q59b. Severity of flooding
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Much more severe 9012
2 Somewhat more severe 7083
3 Stayed the same 10105
4 Somewhat less severe 7924
5 Much less severe 9905
8 Refused to answer 18
9 Don’t know 1555

## Q59C
## Value Count
Label Q59c. Severity of crop failure
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Much more severe 14608
2 Somewhat more severe 8707
3 Stayed the same 7776
4 Somewhat less severe 6111
5 Much less severe 5532
8 Refused to answer 48
9 Don’t know 2817

## Q59D
## Value Count
Label Q59d. Severity of mudslides or landslides
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Much more severe 3896
2 Somewhat more severe 3455
3 Stayed the same 7335
4 Somewhat less severe 3950
5 Much less severe 5372


8 Refused to answer 31
9 Don’t know 2361
94 Not asked in country 0
9994 Not asked in country 19200

## Q59E
## Value Count
Label Q59e. Severity of land or soil erosion
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Much more severe 5545
2 Somewhat more severe 5017
3 Stayed the same 8341
4 Somewhat less severe 4583
5 Much less severe 5292
8 Refused to answer 32
9 Don’t know 2390
94 Not asked in country 0
9994 Not asked in country 14400

## Q60A
## Value Count
Label Q60a. Heard about climate change
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 No 19464
## 1 Yes 25761
7 Not applicable 0
8 Refused to answer 6
9 Don't know 369

## Q60B
## Value Count
Label Q60b. Climate change: affecting country
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Much better 1083
2 Somewhat better 2665
3 Neither/ no change / about the same 1251
4 Somewhat worse 8314


5 Much worse 11767
## 7 Not Applicable 19838
## 8 Refused 4
9 Don’t know / Haven’t heard enough to say 677

## Q61A
## Value Count
Label Q61a. Climate change: main cause
## Type Numeric
## Measurement Nominal
## -1 Missing 0
1 Human activity, like cutting down forests, or burning
fuel and other activities that pollute the atmosphere
## 16422
2 Natural weather patterns or natural processes 5318
3 Both human activity and natural processes 3041
4 Some other reason 296
5 None of these 114
7 Not applicable 19838
8 Refused to Answer 7
9 Don’t know / Haven’t heard enough 564

## Q61B
## Value Count
Label Q61b. Main responsibility for causing climate change
## Type Numeric
## Measurement Nominal
## -1 Missing 0
1 The people, businesses and government of country 11162
2 People, businesses and governments in other parts of
the world
## 11915
3 None of these 1686
7 Not applicable 19838
8 Refused to Answer 8
9 Don’t know / Haven’t heard enough 991

## Q62A
## Value Count
Label Q62a. Government must act now to limit climate
change

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Strongly disagree 2312


## 2 Disagree 3600
3 Neither Agree or disagree 1075
## 4 Agree 11093
5 Strongly agree 7256
7 Not applicable 19838
8 Refused to answer 21
9 Don't know/Haven't heard enough to say 404

## Q62B
## Value Count
Label Q62b. Rich countries must act now to limit climate
change

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Strongly disagree 1203
## 2 Disagree 2123
3 Neither Agree or disagree 975
## 4 Agree 11453
5 Strongly agree 9503
7 Not applicable 19838
8 Refused to answer 21
9 Don't know/Haven't heard enough to say 482

## Q62C
## Value Count
Label Q62c. Rich countries should contribute to climate
adaptation costs

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Strongly disagree 1006
## 2 Disagree 1844
3 Neither Agree or disagree 970
## 4 Agree 11336
5 Strongly agree 10040
7 Not applicable 19838
8 Refused to answer 26
9 Don't know/Haven't heard enough to say 539

## Q62D
## Value Count


Label Q62d. Who primarily responsible for limiting climate
change

## Type Numeric
## Measurement Nominal
## -1 Missing 21
0 None of these / No one / Climate change can’t be
stopped or doesn’t need to be addressed
## 703
## 1 Ordinary Citizens 4772
2 Business and industry 2753
3 The government of country 9559
4 Rich or developed countries 6729
5 Traditional leaders 543
6 Someone else 269
7 Not applicable 19838
8 Refused to answer 8
9 Don’t know 406

## Q63A
## Value Count
Label Q63a. Ban tree cutting for firewood/charcoal even if
fuel more costly

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Strongly disagree 8802
## 2 Disagree 10594
3 Neither agree nor disagree 2086
## 4 Agree 14073
5 Strongly agree 9099
8 Refused to answer 29
9 Don’t know 917

## Q63B
## Value Count
Label Q63b. Require cleaner fuel cookstoves even if more
costly

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Strongly disagree 9295
## 2 Disagree 11236
3 Neither agree nor disagree 2805
## 4 Agree 13495


5 Strongly agree 7791
8 Refused to answer 31
9 Don’t know 947

## Q63C
## Value Count
Label Q63c. Invest in infrastructure for climate resilience
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Strongly disagree 2109
## 2 Disagree 3733
3 Neither agree nor disagree 1586
## 4 Agree 19631
5 Strongly agree 17434
8 Refused to answer 34
9 Don’t know 1073

## Q63D
## Value Count
Label Q63d. Pressure rich countries to provide climate
change aid

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Strongly disagree 2412
## 2 Disagree 4316
3 Neither agree nor disagree 1702
## 4 Agree 20531
5 Strongly agree 14998
8 Refused to answer 45
9 Don’t know 1596

## Q63E
## Value Count
Label Q63e. Promote electric taxis/buses even if more costly
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Strongly disagree 5129
## 2 Disagree 6589
3 Neither agree nor disagree 1488
## 4 Agree 7842


5 Strongly agree 4276
8 Refused to answer 25
9 Don’t know 1050
94 Not asked in country 0
9994 Not asked in country 19200

## Q63F
## Value Count
Label Q63f. Invest in wind/solar energy even if more costly
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Strongly disagree 3537
## 2 Disagree 5575
3 Neither agree nor disagree 1940
## 4 Agree 16190
5 Strongly agree 10996
8 Refused to answer 44
9 Don’t know 1317
94 Not asked in country 0
9994 Not asked in country 6000

## Q64A
## Value Count
Label Q64a. Climate change adaptation: change water
consumption

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 No 29743
## 1 Yes 15428
8 Refused to answer 60
9 Don't know 369

## Q64B
## Value Count
Label Q64b. Climate change adaptation: change outdoor
work

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 No 30769
## 1 Yes 14267


8 Refused to answer 73
9 Don't know 491

## Q64C
## Value Count
Label Q64c. Climate change adaptation: move to another
place

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 No 36662
## 1 Yes 8510
8 Refused to answer 75
9 Don't know 352

## Q64D
## Value Count
Label Q64d. Climate change adaptation: change livestock
rearing

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 No 25900
## 1 Yes 8929
7 Not applicable 9219
## 8 Refused 42
9 Don’t know 309
9994 Not asked in country 1200

## Q64E
## Value Count
Label Q64e. Climate change adaptation: change crops or
food

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 No 31815
## 1 Yes 12983
8 Refused to answer 151
9 Don't know 650

## Q65A
## Value Count


Label Q65a. Radio news
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 11405
1 Less than once a month 2551
2 A few times a month 4591
3 A few times a week 10543
4 Every day 16451
## 8 Refused 9
9 Don't know 49

## Q65B
## Value Count
Label Q65b. Television news
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 15461
1 Less than once a month 2494
2 A few times a month 3672
3 A few times a week 7482
4 Every day 16405
## 8 Refused 1
9 Don't know 86

## Q65C
## Value Count
Label Q65c. Newspaper news
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 32602
1 Less than once a month 3563
2 A few times a month 3445
3 A few times a week 3403
4 Every day 2240
## 8 Refused 4
9 Don't know 342

## Q65D
## Value Count
Label Q65d. Social media news


## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 18360
1 Less than once a month 1595
2 A few times a month 2655
3 A few times a week 6490
4 Every day 16269
## 8 Refused 7
9 Don't know 223

## Q65E
## Value Count
Label Q65e. Other internet news sources
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 22969
1 Less than once a month 2061
2 A few times a month 3029
3 A few times a week 6232
4 Every day 10892
## 8 Refused 6
9 Don't know 411

## Q66
## Value Count
Label Q66. China's influence on economy
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 None 2611
1 A little 6171
## 2 Somewhat 10125
3 A lot 18751
## 8 Refused 22
9 Don’t know / Haven’t heard enough 7920

## Q67A
## Value Count
Label Q67a. Influence of country: Former colonial power
## Type Numeric
## Measurement Ordinal


## -1 Missing 0
1 Very negative 7322
2 Somewhat negative 6524
3 Neither positive nor negative 2688
4 Somewhat positive 11661
5 Very positive 6577
## 8 Refused 110
9 Don’t know 9517
9994 Not asked in country 1200

## Q67B
## Value Count
Label Q67b. Influence of country: China
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Very negative 3338
2 Somewhat negative 4595
3 Neither positive nor negative 2473
4 Somewhat positive 15150
5 Very positive 12955
## 8 Refused 83
9 Don’t know 7007

## Q67C
## Value Count
Label Q67c. Influence of country: United States
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Very negative 3975
2 Somewhat negative 5000
3 Neither positive nor negative 3335
4 Somewhat positive 14081
5 Very positive 9455
## 8 Refused 115
9 Don’t know 9639

## Q67D
## Value Count
Label Q67d. Influence of country: Russia
## Type Numeric
## Measurement Ordinal


## -1 Missing 0
1 Very negative 4433
2 Somewhat negative 6164
3 Neither positive nor negative 4406
4 Somewhat positive 10530
5 Very positive 5696
## 8 Refused 142
9 Don’t know 14229

## Q67E
## Value Count
Label Q67e. Influence of country: India
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Very negative 3650
2 Somewhat negative 5315
3 Neither positive nor negative 4688
4 Somewhat positive 12052
5 Very positive 5775
## 8 Refused 137
9 Don’t know 13983

## Q67F
## Value Count
Label Q67f. Influence of organization: African Union
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Very negative 2426
2 Somewhat negative 3603
3 Neither positive nor negative 3242
4 Somewhat positive 15110
5 Very positive 9822
## 8 Refused 125
9 Don’t know 11272

## Q67G
## Value Count
Label Q67g. Influence of organization: Regional organisation
## Type Numeric
## Measurement Ordinal
## -1 Missing 0


1 Very negative 2878
2 Somewhat negative 3573
3 Neither positive nor negative 2743
4 Somewhat positive 14486
5 Very positive 10203
## 8 Refused 113
9 Don’t know 10404
9994 Not asked in country 1200

## Q67H
## Value Count
Label Q67h. Influence of organization: European Union
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Very negative 3557
2 Somewhat negative 4402
3 Neither positive nor negative 3039
4 Somewhat positive 13518
5 Very positive 9343
## 8 Refused 138
9 Don’t know 11603

## Q68
## Value Count
Label Q68. Main country/organization contributing to
mitigation of COVID-19

## Type Numeric
## Measurement Nominal
## -1 Missing 0
0 None of them / No country or organization helped 1321
1 The African Union or the African Center for Disease
Control, known as the African CDC
## 4163
## 2 China 13363
3 United States of America 7293
## 4 Russia 1040
5 Europe, like the European Union or former colonial
power
## 5472
## 6 India 1422
7 Some other answer 974
8 Refused to answer 49
9 Don’t know / Haven’t heard enough 10504



## Q69A
## Value Count
Label Q69a. Awareness of Russia-Ukraine war
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 No 13149
## 1 Yes 31890
7 Not applicable 0
8 Refused to answer 25
9 Don't know 536

## Q69B
## Value Count
Label Q69b. Support which side in Russia-Ukraine war
## Type Numeric
## Measurement Nominal
## -1 Missing 0
1 Be neutral 22807
2 Side with Russia 4327
3 Side with Ukraine 2566
4 Support one / don’t know which side 886
7 Not applicable 13710
8 Refused to answer 85
9 Don’t know 1218

## Q70A
## Value Count
Label Q70a. Regional organisation recognizes our country's
needs/interests

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Strongly disagree 3202
## 2 Disagree 5938
3 Neither Agree or disagree 2197
## 4 Agree 17577
5 Strongly agree 6256
7 Not applicable 0
8 Refused to answer 106
9 Don't know/Haven't heard enough to say 9123
9994 Not asked in country 1200



## Q70B
## Value Count
Label Q70b. African Union recognizes our country's
needs/interests

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Strongly disagree 2700
## 2 Disagree 5494
3 Neither Agree or disagree 2606
## 4 Agree 18307
5 Strongly agree 7416
7 Not applicable 0
8 Refused to answer 128
9 Don't know/Haven't heard enough to say 8949

## Q70C
## Value Count
Label Q70c. African countries should have greater influence
in international bodies

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Strongly disagree 1765
## 2 Disagree 3057
3 Neither Agree or disagree 1831
## 4 Agree 17454
5 Strongly agree 14859
7 Not applicable 0
8 Refused to answer 117
9 Don't know/Haven't heard enough to say 6517

## Q71A
## Value Count
Label Q71a. Considered emigration to other country
## Type Numeric
## Measurement Ordinal
## -1 Missing 46
0 Not at all 24645
1 A little bit 4994
## 2 Somewhat 4167
3 A lot 11479
8 Don’t know 128


9 Refused to answer 141

## Q71B
## Value Count
Label Q71b. Most likely country for emigration
## Type Numeric
## Measurement Nominal
## -1 Missing 0
1 Most prominent country in the region 2499
2 Another country in the region 1065
3 Elsewhere in Africa 1059
## 4 Europe 6772
5 North America (i.e. USA or Canada) 5795
6 Central or South America 625
## 7 Middle East 482
8 Asia i.e., China, Russia 584
## 9 Australia 769
10 Outside of Africa (place not specified) 820
97 Not applicable 24728
98 Refused to answer 46
99 Don’t know 355

## Q72
## Value Count
Label Q72. Most important reason for emigrating
## Type Numeric
## Measurement Nominal
## -1 Missing 0
1 Find work/better job/better work opportunities 10348
2 Economic hardship 4065
3 Lower taxes at destination 145
4 Poverty/Destitution 1946
5 Poor infrastructure/services 146
6 Better business prospects 927
8 Better democratic environment/Personal
freedom/Human rights/Civil liberties
## 402
9 Political persecution 40
10 Religious persecution 47
11 Civil war/Threat of civil war/Violent
conflicts/Extremism
## 98
12 Crime or personal/family insecurity 106
13 Better schools for children 233
14 Better medical services for family 183


15 To pursue an education 883
16 To accompany family members who are moving for
work
## 125
17 To join spouse/family members who have already
migrated
## 194
18 Travel / Tourism / Adventure / Experience other
cultures
## 675
19 Natural disasters, including drought, flooding, etc. 47
20 Disease outbreaks 36
100 Economic factors 0
200 Political factors 0
300 Social factors 0
## 400 Disasters 0
9995 Some other answer Specify 18
9997 Not applicable 24728
9998 Refused to answer 26
9999 Don’t know 181

Q72Other
## Value Count
Label Q72other. Most important reason for emigrating
## (verbatim)

## Type String
## Measurement Nominal
## 45582
## BETTER LIVING
## STANDARD
## 0
## CORRUPTION   1
## DEATH OF LOVED
## ONES
## 1
## GARANTIR L'AVENIR
## DE MA FAMILL
## 2
## INJUSTICE DANS LA
## RÉGION
## 1
## LA SITUATION DE LA
## TUNISIE
## 1
## LE PAYS VA MAL   1
## MANQUE D'AMOUR
## ET DE SOCIALISM
## 1
## MEILLEUR AVENIR
## POUR LES ENFAN
## 2


## MEILLEURE
## MENTALITÉ /
## ENTOURA
## 3
## MEILLEURE QUALITÉ
## DE VIE
## 2
## PARCE QUE TOUT EST
## MAUVAIS ICI
## 1
## POUR DES RAISONS
## PERSONNELLES
## 2
## RAISONS
## PERSONNELLES
## 0
## RÉALISER LE
## PÈLERINAGE
## 1
## RELIGIOUS (HAJJ)   1

## Q73A
## Value Count
Label Q73a. Economic impact of foreign migrants
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
0 Very bad 10564
1 Fairly bad 9579
2 Neither good nor bad 4110
3 Fairly good 13520
4 Very good 6834
8 Refused to answer 20
9 Don’t know 974

## Q73B
## Value Count
Label Q73b. Admit more or fewer job seekers
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
0 No job seekers at all 6677
1 Fewer job seekers 22325
2 About the same 8578
3 More job seekers 7013
8 Refused to answer 45
9 Don’t know 962

## Q73C


## Value Count
Label Q73c. Admit more or fewer refugees
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
0 No refugees at all 8924
1 Fewer refugees 22852
2 About the same 7599
3 More refugees 5224
8 Refused to answer 41
9 Don’t know 961

## Q73D
## Value Count
Label Q73d. Difficulty to move across borders
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Very difficult 12881
## 2 Difficult 15976
## 3 Easy 7749
4 Very easy 2869
8 Refused to answer 22
9 Don’t know/Haven’t heard enough to say 6103

## Q74
## Value Count
Label Q74. Awareness of AfCFTA
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 No 38925
## 1 Yes 5683
7 Not applicable 0
8 Refused to answer 18
9 Don't know 973

## Q75
## Value Count
Label Q75. Preferred trading partners
## Type Numeric
## Measurement Nominal
## -1 Missing 0


0 None of the above, don’t want open trade 473
1 Regional countries only 3682
2 All African countries 8942
3 All countries globally 30213
4 Some other answer 600
8 Refused to answer 36
9 Don’t know 1653

## Q76A
## Value Count
Label Q76a. Promoting trade vs protecting local producers
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
2 Agree with 1 28399
3 Agree with 2 15678
5 Agree with neither 689
8 Refused to answer 28
9 Don’t know 806

## Q76B
## Value Count
Label Q76b. Allow free movement in region vs limit cross-
border movement

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
2 Agree with 1 25605
3 Agree with 2 18159
5 Agree with neither 765
8 Refused to answer 20
9 Don’t know 1051

## Q82
## Value Count
Label Q82. Respondent's race
## Type Numeric
## Measurement Nominal
## -1 Missing 0
## 1 Black / African 2095
## 2 White / European 107
3 Coloured / Mixed race 137
## 4 Arab / Lebanese / North African 0


5 South Asian (Indian, Pakistani, etc.) 58
6 East Asian (Chinese, Korean, Indonesian, etc.) 2
9994 Not asked in the country 43200
## 9995 Other 0
9998 Refused to answer 0
9999 Don’t know 0

Q82Other
## Value Count
Label Q82other. Respondent's race (verbatim)
## Type String
## Measurement Nominal
## 45600
## KHOISAN   0

## Q83A

## Value

Label Q83a. Ethnic community, cultural group or tribe

## Type Numeric

## Measurement Nominal


Q83AOther

## Value

Label Q83aother. Ethnic community, cultural group or tribe
## (verbatim)

## Type String

## Measurement Nominal


## Q83B
## Value Count
Label Q83b. Ethnic group treated unfairly by government
## Type Numeric
## Measurement Ordinal
## -1 Missing 1304
## 0 Never 20076
## 1 Sometimes 8375
## 2 Often 3812
## 3 Always 2280
## 7 Not Applicable 2566
## 8 Refused 38
9 Don’t know 1149
9994 Not asked in country 6000



## Q83C
## Value Count
Label Q83c. Ethnic or national identity
## Type Numeric
## Measurement Ordinal
## -1 Missing 1913
1 I feel only (ethnic group) 2336
2 I feel more (ethnic group) than (national identity) 2846
3 I feel equally (national identity) and (ethnic group) 16016
4 I feel more (national identity) than (ethnic group) 3430
5 I feel only (national identity) 11494
7 Not applicable 1370
## 8 Refused 36
9 Don't know 159
94 Not asked in the country 0
9994 Not asked in country 6000

## Q84
## Value Count
Label Q84. Frequency of pregnancy termination in your
community

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 1 Often 10235
## 2 Occasionally 8850
## 3 Rarely 10986
## 4 Never 10074
8 Refused to answer 390
9 Don’t know 5065

## Q85A
## Value Count
Label Q85a. Justify pregnancy termination due to rape or
close relative

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Always justified 11047
2 Sometimes justified 10382
3 Never justified 21086
8 Refused to answer 532
9 Don’t know 1352


94 Not asked in country 0
9994 Not asked in country 1200

## Q85B
## Value Count
Label Q85b. Justify pregnancy termination due to health
endangerment

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Always justified 15128
2 Sometimes justified 13747
3 Never justified 15273
8 Refused to answer 366
9 Don’t know 1086

## Q85C
## Value Count
Label Q85c. Justify pregnancy termination due to economic
hardships

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Always justified 5344
2 Sometimes justified 9311
3 Never justified 29602
8 Refused to answer 364
9 Don’t know 980

## Q85D
## Value Count
Label Q85d. Justify preganancy termination for any reason
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Always justified 4560
2 Sometimes justified 8235
3 Never justified 31332
8 Refused to answer 396
9 Don’t know 1077

## Q86A
## Value Count


Label Q86a. Accessibility of contraceptives regardless of
marital status

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Strongly disagree 9260
## 2 Disagree 7534
3 Neither agree nor disagree 1185
## 4 Agree 15090
5 Strongly agree 11146
8 Refused to answer 546
9 Don’t know 839

## Q86B
## Value Count
Label Q86b. Accessibility of contraceptives regardless of age
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Strongly disagree 11196
## 2 Disagree 9006
3 Neither agree nor disagree 1539
## 4 Agree 13223
5 Strongly agree 9093
8 Refused to answer 674
9 Don’t know 869

## Q86C
## Value Count
Label Q86c. Continue girls education even if pregnancy or
children

## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Strongly disagree 3156
## 2 Disagree 3282
3 Neither agree nor disagree 1256
## 4 Agree 17561
5 Strongly agree 19532
8 Refused to answer 303
9 Don’t know 509

## Q86D


## Value Count
Label Q86d. Teach sex education in schools
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Strongly disagree 5688
## 2 Disagree 4012
3 Neither agree nor disagree 1251
## 4 Agree 15640
5 Strongly agree 17816
8 Refused to answer 553
9 Don’t know 640

## Q86E
## Value Count
Label Q86e. Women's autonomy in marriage decisions
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Strongly disagree 4502
## 2 Disagree 5491
3 Neither agree nor disagree 1161
## 4 Agree 18141
5 Strongly agree 15930
8 Refused to answer 152
9 Don’t know 223

## Q86F
## Value Count
Label Q86f. Women's autonomy in reproductive decisions
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Strongly disagree 6788
## 2 Disagree 8066
3 Neither agree nor disagree 2188
## 4 Agree 15146
5 Strongly agree 12952
8 Refused to answer 162
9 Don’t know 298

## Q87A
## Value Count


Label Q87a. Trust relatives
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
0 Not at all 2819
1 Just a little 5903
## 2 Somewhat 7887
3 A lot 28866
8 Refused to answer 31
9 Don’t know 95

## Q87B
## Value Count
Label Q87b. Trust neighbours
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
0 Not at all 7239
1 Just a little 11898
## 2 Somewhat 14049
3 A lot 12294
8 Refused to answer 16
9 Don’t know 104

## Q87C
## Value Count
Label Q87c. Trust other citizens
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
0 Not at all 8758
1 Just a little 14729
## 2 Somewhat 13644
3 A lot 8113
8 Refused to answer 20
9 Don’t know 337

## Q87D
## Value Count
Label Q87d. Trust people from other religions
## Type Numeric
## Measurement Ordinal
## -1 Missing 0


0 Not at all 9560
1 Just a little 13793
## 2 Somewhat 13896
3 A lot 7992
8 Refused to answer 30
9 Don’t know 329

## Q87E
## Value Count
Label Q87e. Trust people from other ethnic groups
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
0 Not at all 7711
1 Just a little 13465
## 2 Somewhat 13323
3 A lot 7074
8 Refused to answer 34
9 Don’t know 394
94 Not asked in country 0
9994 Not asked in country 3600

## Q88A
## Value Count
Label Q88a. Neighbours: people of different religion
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Strongly dislike 4028
2 Somewhat dislike 3262
3 Would not care 14469
4 Somewhat  like 13271
5 Strongly like 10361
## 8 Refused 18
9 Don’t know 192

## Q88B
## Value Count
Label Q88b. Neighbours: people of different ethnicity
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Strongly dislike 2083


2 Somewhat dislike 3088
3 Would not care 13031
4 Somewhat  like 13261
5 Strongly like 10225
## 8 Refused 19
9 Don’t know 293
94 Not asked in country 0
9994 Not asked in country 3600

## Q88C
## Value Count
Label Q88c. Neighbours: homosexuals
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Strongly dislike 30621
2 Somewhat dislike 4192
3 Would not care 6261
4 Somewhat  like 2260
5 Strongly like 1440
## 8 Refused 136
9 Don’t know 689

## Q88D
## Value Count
Label Q88d. Neighbours: immigrants and foreign workers
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Strongly dislike 5205
2 Somewhat dislike 5098
3 Would not care 14849
4 Somewhat  like 12852
5 Strongly like 7190
## 8 Refused 29
9 Don’t know 377

## Q88E
## Value Count
Label Q88e. Neighbours: people who support a different
political party

## Type Numeric
## Measurement Ordinal


## -1 Missing 0
1 Strongly dislike 4192
2 Somewhat dislike 4140
3 Would not care 17271
4 Somewhat  like 11784
5 Strongly like 7745
## 8 Refused 50
9 Don’t know 418

## Q88F
## Value Count
Label Q88f. Neighbours: refugees fleeing persecution
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Strongly dislike 7961
2 Somewhat dislike 5701
3 Would not care 13866
4 Somewhat  like 10979
5 Strongly like 6488
## 8 Refused 42
9 Don’t know 564

## Q89A
## Value Count
Label Q89a. Close to political party
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
0 No (does NOT feel close to ANY party) 25911
1 Yes (feels close to a party) 17334
8 Refused to answer 859
9 Does not know 297
9994 Not asked in country 1200

## Q89B

## Value

Label Q89b. Which party

## Type Numeric

## Measurement Nominal


Q89BOther
## Value Count


Label Q89bother. Which party (verbatim)
## Type String
## Measurement Nominal
## 45382
## 11 CANDIDATS   2
## ACRT RENOUVEAU   1
## ACTION NATIONALE
## POUR LE
## DÉVELOPPEMENT
## 1
## ACTION POUR LA
## RÉPUBLIQUE, LE
## DÉVELOPPEMENT ET
## LA DÉMOCRATIE
## 0
## ADJS   1
## AFRICAN POLITICAL
## PARTY (APP)
## 0
## AL WASAT   1
## ALL OF THEM   0
## ALL POLITICAL
## PARTIES
## 1
## ALLIANCE
## DÉMOCRATIQUE ET
## RÉPUBLICAINE
## (ADERE)
## 2
## ALLIANCE
## LIBÉRATION
## 2
## ALLIANCE SOCIALISTE   1
## AMUSSI   1
## ANY PARTY OTHER
## THAN ZANU-PF
## 4
## APM MALIKO DE
## MODIBO KADIOGUE
## 0
## ASSIMI GOÏTA   2
## AVI (ASA VITA
## IFAMPITSARANA)
## 2
## AZIMIO   1
## BARKA   1
## BASOTHO TENSION
## MOVEMENT (BTM)
## 1
## BATIR   1
## BENKA   0
## BLOC PATRIOTIQUE
## UNI (BPU)
## 1


## BOTH NPP AND NDC   0
## BOUBACAR CAMARA   2
## CCM   1
## CHAMA CHA SIKI   0
## CHRISTIAN   0
## CITIZENS FIRST (CF)   2
## CODO   1
## COMITÉ POUR LA
## TRANSITION ET LA
## DÉMOCRATIE (CTD)
## 6
## COMMUNIST PARTY
## OF KENYA
## 1
## CONVENTION
## NATIONALE
## DÉMOCRATIQUE ET
## SOCIALE
## 2
## CONVERGENCE
## DÉMOCRATIQUE
## BOKK
## 1
## CPR   1
## DIKWANKWETLA
## PARTY
## 0
## DMP   2
## ESSA FAAL   2
## FIRAISANKINA   1
## FO TE MOGO BAN   2
## FORCE DES INTÈGRES
## POUR LA
## DÉMOCRATIE ET LA
## LIBERTÉ (FIDEL)
## 0
## FREEDOM   3
## FSNC   3
## FUTURE PARTY   0
## GABON D'ABORD   2
## GASCAR FENOSOA   1
## GASIKARA MIJORO   1
## GHANA UNION
## MOVEMENT
## 0
## HAUT CONSEIL
## BERABICHE
## 0
## HURI   1
## INDÉPENDANT   2
## INDEPENDENT   2


## INITIATIVE POUR LA
## RÉSURGENCE DU
## MOUVEMENT
## ABOLITIONNISTE
## (IRA)
## 2
## IRMAR   2
## KABAKA   0
## KADIMOU   1
## KADIMU   1
## KAIS SAIED   5
## KENYA KWANZA   0
## KENYA UNION PARTY   1
## L'ALLIANCE   2
## LA PIROGUE PARTI
## INDÉPENDANT
## 1
## LALYANS NOUVO
## SESEL
## 1
## LE COMITÉ
## NATIONAL DU
## RASSEMBLEMENT
## POUR LE
## DÉVELOPPEMENT
## (CNRD)
## 5
## LES PATRIOTES   1
## LES SOUVERAINISTES   3
## MAGUETTE SÈNE   0
## MAISON DES
## PAYSANS
## 1
## MAME BOYE DIAO   1
## MANAGER HAJA   0
## MBOLLOW KUNDA   1
## MDG   1
## MDR   5
## MDRERE   1
## MFM   2
## MK MOVEMENT   0
## MOHOMATEMENG   3
## MOUVEMENT   0
## MOUVEMENT DE
## REDRESSEMENT
## NATIONAL (MRN)
## 2
## MOUVEMENT DES
## GÉNÉRATIONS CA
## 1


## MOUVEMENT
## POPULAIRE
## DÉMOCRATIQUE DE
## GUINÉE (MPDG)
## 2
## MOVEMENT FOR
## CHANGE
## 0
## MOVIMENTO PARA
## CAUÉ
## 0
## MPSC   1
## MTS (MALAGASY
## TONGA SAINA)
## 0
## MVDP   1
## NEMA   0
## NEW PATRIOTIC
## PARTY
## 0
## NIDAA TOUNES   2
## NOUVEL ÉLAN
## PATRIOTIQUE (NEP)
## 1
## NOUVELLE FORCE
## DÉMOCRATIQUE
## (NFD)
## 0
## NOUVELLE FORCE
## DÉMOCRATIQUE DE
## GUINÉE (NFD)
## 1
## NOUVELLE GUINÉE
## (NG)
## 0
## NOVA DEMOCRACIA   1
## OPPOSITION   2
## OPPOSITION PARTY   3
## PAA   0
## PAIGC   1
## PAP (PEOPLE ACTION
## PARTY)
## 1
## PARTI D'OPPOSITION   0
## PARTI DE L'UNITÉ ET
## DU PROGRÈS (PUP)
## 2
## PARTI
## DÉMOCRATIQUE
## POUR LE
## CHANGEMENT (PDC)
## 2
## PARTI DU
## RENOUVEAU
## DÉMOCRATIQ
## 0


## PARTI ÉCOLOGISTE   2
## PARTI GABONAIS DE
## PROGRÈS (PGP)
## 1
## PARTI SOCIAL-
## DÉMOCRATE (PSD)
## 1
## PARTI UNION ET
## SOLIDARITÉ (US)
## 0
## PARTI WIEM   0
## PARTIDO LUZ   0
## PARTIS WULEZI   1
## PATRICE TALON   1
## PCD   3
## PDP   3
## PEUPLE UNIS   3
## PÔLE
## DÉMOCRATIQUE
## MODERNISTE
## 1
## PPR   1
## PRÉSIDENT MAMADI
## DOUMBOUYA
## 5
## PTG   24
## RAPID   1
## RASSEMBLEMENT
## POUR LA PATRIE ET
## LA MODERNITÉ
## (RPM)
## 3
## RASSEMBLEMENT
## POUR LA
## RESTAURATION
## (RPG)
## 1
## RASSEMBLEMENT
## POUR LE GABON
## (RPG)
## 0
## RCD   1
## RCR   1
## RJP   1
## RPSD   15
## SOCIAUX-
## DÉMOCRATES
## GABONAIS (SDG)
## 0
## TAMBATRA   0
## THE NEW DEMOCRAT   0
## THE NEW FORCE
## MOVEMENT
## 0


## TMH   0
## TOGO AUTREMENT   1
## TONSE ALLIANCE   1
## UFP (UNION POUR LA
## FRATERNITÉ
## 2
## UNION DU PEUPLE
## GABONAIS (UPG)
## 8
## UNION POUR LA
## RÉPUBLIQUE (UPR)
## 2
## UNITED AFRICAN
## TRANSFORMATION
## 2
## UNITED KWACHA
## ALLIANCE (UKA)
## 2

## Q90A
## Value Count
Label Q90a. Own radio
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
0 No, no one in the household owns 12032
1 Someone else in household owns 8480
2 Yes (personally owns) 24893
## 8 Refused 18
9 Don’t know 177

## Q90B
## Value Count
Label Q90b. Own television
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
0 No, no one in the household owns 15022
1 Someone else in household owns 6955
2 Yes (personally owns) 23495
## 8 Refused 12
9 Don’t know 116

## Q90C
## Value Count
Label Q90c. Own motor vehicle, car or motorcycle
## Type Numeric
## Measurement Ordinal


## -1 Missing 0
0 No, no one in the household owns 22556
1 Someone else in household owns 11330
2 Yes (personally owns) 11521
## 8 Refused 21
9 Don’t know 171

## Q90D
## Value Count
Label Q90d. Own computer
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
0 No, no one in the household owns 29249
1 Someone else in household owns 7093
2 Yes (personally owns) 8843
## 8 Refused 25
9 Don’t know 389

## Q90E
## Value Count
Label Q90e. Own bank account
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
0 No, no one in the household owns 19895
1 Someone else in household owns 7590
2 Yes (personally owns) 17204
## 8 Refused 49
9 Don’t know 862

## Q90F
## Value Count
Label Q90f. Own mobile phone
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
0 No, no one in the household owns 2621
1 Someone else in household owns 3976
2 Yes (personally owns) 38940
## 8 Refused 9
9 Don’t know 54



## Q90G
## Value Count
Label Q90g. Own mobile money account
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
0 No, no one in the household owns 11349
1 Someone else in household owns 5945
2 Yes (personally owns) 27350
## 8 Refused 44
9 Don’t know 912

## Q90H
## Value Count
Label Q90h. Mobile phone access to internet
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
0 No (Does not have Internet access) 14544
1 Yes (Has Internet access) 24313
7 Not applicable (does not personally have mobile
phone)
## 6660
## 8 Refused 11
9 Don’t know 71

## Q90I
## Value Count
Label Q90i. How often use a mobile phone
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 Never 3698
1 Less than once a month 842
2 A few times a month 1379
3 A few times a week 4029
4 Every day 35590
## 8 Refused 5
9 Don't know 56

## Q90J
## Value Count
Label Q90j. How often use the internet
## Type Numeric


## Measurement Ordinal
## -1 Missing 0
## 0 Never 17872
1 Less than once a month 1802
2 A few times a month 2692
3 A few times a week 7264
4 Every day 15750
## 8 Refused 14
9 Don't know 206

## Q91A
## Value Count
Label Q91a. Location of toilet or latrine
## Type Numeric
## Measurement Nominal
## -1 Missing 0
0 None, no latrine available 3484
1 Inside the house 15440
2 Inside the compound 17417
3 Outside the compound 9206
8 Refused to answer 11
9 Don't know 42

## Q91B
## Value Count
Label Q91b. Location of main water source
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
1 Inside the house 11321
2 Inside the compound 12416
3 Outside the compound 21692
8 Refused to answer 33
9 Don't know 139

## Q92
## Value Count
Label Q92. Source of water for household use
## Type Numeric
## Measurement Nominal
## -1 Missing 0
1 Piped public or community water system 22473
4 Tubewell or borehole 9034


5 Dug well that is protected 5016
6 Dug well that is not protected 2996
7 Spring that is protected 1187
8 Spring that is unprotected 1162
## 9 Rainwater 403
10 Bottled water 164
11 Purchased from a cart or truck 811
13 Surface water, like a river, dam, lake, pond, stream,
canal, or irrigation channel
## 2143
95 Some other source 88
98 Refused to answer 12
99 Don’t know 112

Q92Other
## Value Count
Label Q92other. Source of water for household use
## (verbatim)

## Type String
## Measurement Nominal
## 45512
## A NEARBY PRISON
## TAP
## 1
## AGUA DA CASA DE
## FAMILIA
## 1
## APANHAM ÁGUA EM
## OUTRAS ZONAS
## 3
## ASSOCIATION DE
## L'EAU
## 19
## AUCUNE SOURCE   1
## BUSCA AGUA EM
## CASA DE VIZINHOS
## 0
## BUSCA AGUA EM
## VIZINHOS
## 0
## CASA DA FAMILIA   2
## CASA DE VEZINHO   3
## CASA DE VIZINHO   0
## CASA VIZINHO   1
## CENTINA   3
## CHAFAFIS   1
## CHAFARIS   1
## CHEZ LES VOISINS   1
## CISTERNA   2


## COMPRA NA CASA
## DO VIZINHO
## 0
## DA CASA DA VIZINHA   2
## DA CASA SOGRA AO
## LADO DA CASA
## 1
## FRANCO'S FARM   1
## FROM KANYE WITH
## HER CAR
## 1
## FROM NEIGHBORS   0
## FROM OTHER
## RELATIVES' HOUSES
## 0
## FROM TOWN   0
## GET WATER IN THE
## NEXT VILLAGE
## 4
## MAJWANENG,
## VILLAGE CLOSE TO CA
## 4
## NA CASA DE
## FAMILIARES
## 1
## NA CASA ONDE
## TRABALHA
## 2
## NA VIZINHANÇA   3
## NÃO TEM NA ZONA   1
## NEARBY SETTLEMENT   1
## NEARBY VILLAGE   1
## NEIGHBORS   8
## NEXT DOOR   2
## NO WATER IN THE
## YARD
## 0
## NO WATER SOURCE   0
## OTHER FAMILY
## MEMBERS
## 1
## PRIVATE PIPED
## WATER
## 1
## PRIVATE TAP IN THE
## HOUSEHOLD
## 3
## PURCHASE ON
## PRIVATE PIPELINE
## 2
## QUINTAL DO
## VIZINHO
## 1
## QUINTAL VIZINHO   1
## SESE VILLAGE, 35
## KILOMETERS FR
## 0
## VIZINHO   0


## VIZINHOS   3
## WATER TANK   3
## WATER TANK FROM
## A DIFFERENT CO
## 1

## Q93A
## Value Count
Label Q93a. Electric connection from mains
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 No 18097
## 1 Yes 27465
8 Refused to answer 5
9 Don't know 32

## Q93B
## Value Count
Label Q93b. Electricity available from mains
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 1 Never 668
## 2 Occasionally 4148
3 About half of the time 2987
4 Most of the time 9757
5 All of the time 9875
## 7 Not Applicable 18135
## 8 Refused 1
9 Don't know 28

## Q93C
## Value Count
Label Q93c. Other source of electricity: available
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
## 0 No 34948
## 1 Yes 10584
7 Not applicable 0
8 Refused to answer 23
9 Don't know 45



## Q93D
## Value Count
Label Q93d. Other source of electricity: type
## Type Numeric
## Measurement Nominal
## -1 Missing 0
1 Batteries or power bank 1016
## 2 Generator 1254
3 Solar panels 7380
4 Wind power 64
5 Hydro power 409
## 6 Biogas 56
## 95 Other 145
96 Multiple sources 45
97 Not applicable 35016
98 Refused to answer 22
99 Don’t know 192

Q93DOther
## Value Count
Label Q93dother. Other source of electricity: type
## (verbatim)

## Type String
## Measurement Nominal
## CENTLEC   0
## 45454
## AMADER   3
## BOUGIE   2
## CANDIEIRO
## PETRÓLEO
## 0
## CANDLE   10
## CANDLES   4
## CANISTER   1
## COMMUNITY
## CURRENT
## 2
## COURANT DU VOISIN   2
## D-LIGHT   0
## DRY GRASS   0
## ELECTRICITY
## SUPPLIED BY
## COMPAN
## 0
## ERONGORED   2


## ILLEGAL
## CONNECTION
## 10
## ILLEGAL
## CONNECTIONS
## 1
## JONGON ENERGY
## POWER JEP
## 4
## LAMP   0
## LAMPADA   1
## LAMPE   5
## LAMPE À PÉTROLE   1
## LAMPE
## RECHARGEABLE
## 1
## LAMPE SOLAIRE   2
## LAMPE TEMPÊTE   5
## LAMPE TORCHE   3
## LANTERNE   1
## LUZ ROUBADO   1
## MUNICIPALITY   21
## NORED   5
## OSHAKATI PREMIER   2
## OSHAKATI PREMIUM   1
## PARAFFIN   1
## PARAFFIN LAMP   2
## PÉTROLE   16
## PHONE   1
## PHONES TORCH   0
## RACCORDÉ PAR UN
## MÉNAGE
## 1
## RECHARGEABLE
## LIGHTS
## 2
## SERVICE PRIVÉ   1
## SHARED FROM
## FAMILY
## 1
## SOCIÉTÉ ANGLO
## GOLD ASHANTI (
## 0
## SOLAR LAMPS   0
## TORCH   5
## TORCHE   17
## TORCHE CHINOISE   5
## TORCHE, LAMPE   1
## TOURCH   0
## TRADITIONAL TIN
## LIGHTING
## 0


## VIZINHANÇA   0

## Q94A
## Value Count
Label Q94a. Employment status
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
0 No (not looking) 15926
## 1 No (looking) 15475
2 Yes, part time 4669
3 Yes, full time 9500
## 8 Refused 18
9 Don’t know 12

## Q94B
## Value Count
Label Q94b. Occupation of respondent
## Type Numeric
## Measurement Nominal
## -1 Missing 0
0 Never had a job 3543
## 1 Student 4297
2 Housewife / homemaker 4579
3 Agriculture / farming / fishing / forestry 10095
4 Trader / hawker / vendor 5108
## 5 Retail / Shop 1960
6 Unskilled manual worker (e.g., cleaner, laborer,
domestic help, unskilled manufacturing worker)
## 5261
7 Artisan or skilled manual worker (e.g., trades like
electrician, mechanic, machinist or skilled
manufacturing worker)
## 4209
8 Clerical or secretarial 687
## 9 Supervisor / Foreman / Senior Manager 539
10 Security services (police, army, private security) 1002
11 Mid-level professional (e.g., teacher, nurse, mid-level
government officer)
## 2637
12 Upper-level professional (e.g., banker/finance, doctor,
lawyer, engineer, accountant, professor, senior-level
government
## 1190
## 9995 Other 140
## 9998 Refused 177
9999 Don’t know 177



Q94BOther
## Value Count
Label Q94bother. Occupation of respondent (verbatim)
## Type String
## Measurement Nominal
## 45459
## APPRENTI   2
## APPRENTICE   0
## BÉNÉVOLE DANS UN
## CENTRE DE SANTÉ
## 1
## ELDERLY   2
## ENTREPRISE DE
## CONSTRUCTION DE
## BATIMENTS
## 0
## HUSTLING   1
## IMMIGRATION   0
## IMMOBILIER   1
## LABORATOIRE DE
## MINE
## 0
## LANDLORD   0
## MANY DIFFERENT
## KINDS
## 0
## MARABOUT   3
## MENTOR   2
## NGO EMPLOYEE   1
## NON SPÉCIFIÉ   4
## OLD AGE   0
## OLD AGE PENSIONER   1
## PART TIME JOBS   1
## PASTEUR   2
## PASTOR   11
## PENSIONER   15
## PENSIONISTA   4
## PRIEST   1
## REFORMADO   15
## REFORMADO DE
## SOCIAV
## 0
## RETIRED   22
## RETRAITÉ   5
## RETRAITE   0
## SELF-EMPLOYED   27
## STAGIAIRE   1


## STAGIAIRE DANS UNE
## CLINIQUE
## 0
## TOO OLD TO WORK   7
## UNEMPLOYED   5
## VOLUNTEER   1
## VOLUNTEER WORK   2
## VVMC   1

## Q94C
## Value Count
Label Q94c. Preferred job sector
## Type Numeric
## Measurement Nominal
## -1 Missing 0
1 Working in government or public sector 10041
2 Working for a private company, industry, or business 5100
3 Working for a non-government organization 2525
4 Starting your own business 24516
5 None of the above / Something else 2597
8 Refused to answer 92
9 Don’t know 730

## Q94D
## Value Count
Label Q94d. Main barrier to youth employment
## Type Numeric
## Measurement Nominal
## -1 Missing 0
0 Youth do not face barriers to getting employment 1441
1 Lack of adequate training or preparation 11735
2 Lack of experience required by employers 8348
3 Youth are unwilling to work certain jobs (e.g., in
agriculture or difficult jobs)
## 7570
4 Youth lack of entrepreneurial skills or motivation 4969
5 There is a mismatch between education qualifications
and job requirements
## 6182
6 Some other barrier 3215
8 Refused to answer 53
9 Don’t know 2087

## Q94E
## Value Count
Label Q94e. Main barrier to women's employment


## Type Numeric
## Measurement Nominal
## -1 Missing 0
0 Women do not face barriers to entering or moving up
in the workforce
## 4126
1 It is not socially accepted for women to work outside
the home.
## 4516
2 Women lack the necessary education or skills 8436
3 Lack of childcare 7595
4 Employers prefer to hire men 8782
5 Lack of remote or flexible work arrangements 6479
6 Some other barrier 3013
8 Refused to Answer 67
9 Don’t know 2586

## Q95
## Value Count
Label Q95. Who decides how money is used
## Type Numeric
## Measurement Nominal
## -1 Missing 0
1 You make the decisions yourself 18099
2 Your spouse makes the decisions 3588
3 You make the decisions jointly with your spouse 14614
4 You make the decisions jointly with other family
members
## 6002
5 Other family members make the decisions without
you
## 1246
6 None of the above / Some other response 163
7 Not applicable / No earnings 1614
8 Refused to answer 101
9 Don’t know 174

## Q96
## Value Count
Label Q96. Education of respondent
## Type Numeric
## Measurement Ordinal
## -1 Missing 0
0 No formal schooling 5504
1 Informal schooling only (including Koranic schooling) 1716
2 Some primary schooling 6246
3 Primary school completed 5649


4 Intermediate school or Some secondary school / high
school
## 10035
5 Secondary school / high school completed 7919
6 Post-secondary qualifications, other than university
e.g. a diploma or degree from a polytechnic or college
## 2673
7 Some university 2126
8 University completed 3007
## 9 Post-graduate 500
## 98 Refused 96
99 Don’t know 128

## Q97
## Value Count
Label Q97. Religion of respondent
## Type Numeric
## Measurement Nominal
## -1 Missing 0
## 0 None 2249
1 Christian only (i.e., respondents says only “Christian”,
without identifying a specific sub-group)
## 7330
## 2 Catholic 8767
## 3 Orthodox 240
## 4 Coptic 72
## 5 Anglican 1020
## 6 Lutheran 698
## 7 Methodist 546
## 8 Presbyterian 459
## 9 Baptist 442
## 10 Quaker / Friends 11
## 11 Mennonite 12
## 12 Evangelical 1708
13 Pentecostal (e.g., “Born Again” and/or “Saved”) 2112
14 Independent (e.g., “African Independent Church”) 637
## 15 Jehovah’s Witness 298
## 16 Seventh Day Adventist 784
17 Mormon/Latter Day Saints 33
18 Muslim only (i.e., respondents says only “Muslim”,
without identifying a specific sub-group)
## 13639
19 Sunni only (i.e., respondents says only “Sunni” or
“Sunni Muslim”, without identifying a specific sub-
group)
## 627
## 20 Ismaeli 69
## 21 Mouridiya Brotherhood 198


## 22 Tijaniya Brotherhood 337
## 23 Qadiriya Brotherhood 57
## 24 Shia 11
25 Traditional / ethnic religion 620
## 26 Hindu 629
## 27 Bahai 5
28 Agnostic (Do not know if there is a God) 7
29 Atheist (Do not believe in a God) 61
## 30 Dutch Reformed 56
## 31 Calvinist 430
32 Church of Christ 343
## 33 Zionist Christian Church 772
## 34 Jewish 13
## 100 Christianisme Celeste 18
## 1793 Zéphirin (lassiste) 0
## 1795 Ngundza 3
## 1797 Louzolo Amour 1
## 9995 Other 34
## 9998 Refused 133
9999 Don't know 119

Q97Other
## Value Count
Label Q97other. Religion of respondent (verbatim)
## Type String
## Measurement Nominal
## 45566
## BOUDDHISME   1
## BOUDHISTE   3
## CONFRÉRIE LAYÈNE   2
## ÉGLISE LUMIÈRE   1
## FAITH OF UNITY   5
## HALF CHRISTIAN,
## HALF MUSLIM
## 0
## MAISON DU SALUT
## DE GUÉRISON ET DE
## DÉLIVRANCE
## 0
## MARATHI   2
## REVIVAL CHURCH   0
## TAMIL   4
## TAMOUL   11
## TÉLÉGOU   2
## TEMPLE   0


## TENT OF GOD
## MINISTRY
## 1
## TOUTES RELIGIONS   0
## UNIVERSAL CHURCH   0

## Q98

## Value

Label Q98. Vote for which party

## Type Numeric

## Measurement Nominal


Q98Other
## Value Count
Label Q98other. Vote for which party (verbatim)
## Type String
## Measurement Nominal
## 45250
## A STRONG
## OPPOSITION PARTY
## THAT FORMS AFTER
## CCC
## 0
## ACRT RENOUVEAU   1
## ACTION SA   0
## AL WASAT   1
## ALLIANCE
## DÉMOCRATIQUE ET
## RÉPUBLICAINE
## (ADERE)
## 2
## ALLIANCE
## LIBÉRATION
## 1
## ANC   1
## ANDP   2
## ANY OPPOSITION
## PARTY
## 5
## ANY OTHER PARTY   1
## ANY OTHER PARTY
## OR CANDIDATE WITH
## A CONVINCING
## MANIFESTO
## 1
## ANY OTHER
## POLITICAL PARTY
## 3
## ANY PARTY EXCEPT
## ZANU-PF
## 4


## ANY PARTY WHO
## CAN HELP ME
## 0
## ANY POLITICAL
## PARTY
## 1
## APM MALIKO   0
## AUCUN   1
## AUTRE PARTI –
## D’ESPOIR
## 0
## AUTRE QUE
## DIOMAYE
## 1
## AZIMIO   2
## BÂTIR   3
## BERTRAND NZIMBI   2
## BETTER CANDIDATE
## THAN THE CURRENT
## PARTY
## 0
## BULLETIN NUL   1
## BULLETIN VIDE   1
## CAD   1
## CANDIDAT
## INDÉPENDANT
## 10
## CELUI DE SON PROF   1
## CELUI QUI M'AIDERA   1
## CELUI QUI ME
## DONNERA DE
## L'ARGENT
## 4
## CHEDA   0
## CHOOSING A GOOD
## LEADER, NOT A
## PARTY
## 0
## COMMUNIST PARTY
## OF KENYA
## 1
## CONVENTION
## NATIONALE
## DÉMOCRATIQUE ET
## SOCIALE
## 1
## DEMOCRATIC
## ALLIANCE PARTY
## (DAP)
## 4
## DIKWANKWETLA
## PARTY
## 0
## DIREITA   1
## DMP DE BRIGITTE
## ADJAMAGBO
## 1


## DON'T VOTE FOR THE
## PARTY BUT
## STRENGTH OF A
## CANDIDATE
## 0
## EM BRANCO   1
## ESSA FAAL   1
## FIVOHY   1
## FLOATING MEMBER   1
## FREEDOM PARTY   0
## FSNC   9
## FUTURE PARTY   1
## GASCAR FENOSOA   1
## GHANA UNION
## MOVEMENT
## 1
## GUY MARIUS SAGNA   1
## HUGUES MBADINGA
## MADIYA
## 2
## HURI   1
## I WILL VOTE FOR
## WHOEVER GIVES ME
## MONEY
## 0
## I WOULD VOTE BCP
## FOR A COUNCILLOR
## AND BDP FOR AN MP
## 2
## INDÉPENDANT   25
## INDEPENDENT   12
## INDEPENDENT
## CANDIDATE
## 3
## INDEPENDENT
## CANDIDATES
## 3
## INDEPENDENT PARTY   0
## INITIATIVE POUR LA
## RÉSURGENCE DU
## MOUVEMENT
## ABOLITIONNISTE
## (IRA)
## 2
## ISABEL DOS SANTOS   1
## JE FERAI UN
## BULLETIN NUL
## 1
## JE SOUHAITE UN
## NOUVEAU
## CANDIDAT, PAS
## CELUI DU RÉGIME
## ACTUEL
## 1


## JE VOTE CELUI QUI
## GARANTIT MES
## BESOINS
## 3
## JUBANTI   1
## KABAKA   0
## KADIMOU   1
## KENYA KWANZA   1
## L'OPPOSITION   7
## LA PARTIE DONT LA
## TRANSITION VA
## REPRÉSENTER
## 1
## LALYANS NOUVO
## SESEL
## 2
## LE CANDIDAT DE
## MON CONJOINT
## 6
## LE CANDIDAT DES
## MILITAIRES
## 6
## LE CANDIDAT DU
## CHEF DE FRACTION
## 0
## LE CANDIDAT DU
## CHEF DE VILLAGE
## 2
## LE CHOIX DE NOTRE
## CHEF DE VILLAGE
## 1
## LE MAIRE DE NOTRE
## COMMUNE
## 2
## LE MÊME CANDIDAT
## QUE MON MARI
## 1
## LES SOUVERAINISTES   3
## MAGUETTE SÈNE   0
## MAMA JEUNE   0
## MAME BOYE DIAO   1
## MANAGER HAJA   0
## MASHINANI   1
## MDG   1
## MDR   3
## MDRERE   1
## MFM   1
## MISSING   51
## MK MOVEMENT   0
## MOI MÊME   1
## MOI-MÊME   0
## MOUSSA DADICE
## CAMARA
## 0


## MOUVEMENT   0
## MOUVEMENT
## D'ÉMANCIPATION
## SOCIALISTE DES
## PEUPLES (MESP)
## 2
## MOUVEMENT
## DÉMOCRATIQUE
## LIBÉRAL (MODEL)
## 0
## MOUVEMENT DES
## GÉNÉRATIONS
## CAPABLES (MGC)
## 1
## MOUVEMENT
## POPULAIRE DE
## LIBÉRATION (MPL)
## 2
## MOUVEMENT
## POPULAIRE
## DÉMOCRATIQUE DE
## GUINÉE (MPDG)
## 2
## MOVEMENT FOR
## CHANGE
## 0
## MPSC   1
## MTS (MALAGASY
## TONGA SAINA)
## 0
## NÃO TEM PARTIDO   1
## NENHUM   4
## NENHUM PARTIDO   1
## NEUTRE   1
## NEW OPPOSITION
## PARTY
## 1
## NEW
## REVOLUTIONARY
## FORC
## 0
## NOUVEAU PARTI   2
## NOUVELLE GUINÉE   0
## NOUVELLE VISION   1
## NPP   1
## ONDO OSSA   1
## OPPOSITION   3
## OPPOSITION PARTIES   3
## PAA   0
## PAP (PEOPLE ACTION
## PARTY)
## 1


## PARTI DE L'UNITÉ ET
## DU PROGRÈS (PUP)
## 6
## PARTI
## DÉMOCRATIQUE DE
## GUINÉE (PDG RDA)
## 2
## PARTI
## DEMOCRATIQUE ET
## SOCIALISTE POUR
## L'ALTERNANCE AU
## TCHAD
## 1
## PARTI DES
## DÉMOCRATES POUR
## L'ESPOIR (PADES)
## 1
## PARTI DU
## RENOUVEAU
## DÉMOCRATIQUE
## (PRD)
## 0
## PARTI MALIN   5
## PARTI MARTIN
## LUTHER KING
## 1
## PARTI POUR LE
## DÉVELOPPEMENT ET
## LA SOLIDARITÉ
## SOCIALE (PDS)
## 1
## PARTIDO LUZ   1
## PAS DE PIÈCE
## D’IDENTITÉ
## 2
## PCD   4
## PERSONNE   1
## PEUPLE UNIS   3
## PTG   12
## RASSEMBLEMENT
## POUR LA PATRIE ET
## LA MODERNITÉ
## (RPM)
## 1
## RASSEMBLEMENT
## POUR LE GABON
## (RPG)
## 1
## RAYMOND NDONG
## SIMA
## 2
## RENIQUE   0
## RÉPUBLIQUE DES
## VALEURS (BOUBACAR
## CAMARA)
## 2


## RPSD   12
## SOCIAUX-
## DÉMOCRATES
## GABONAIS (SDG)
## 0
## TOGO AUTREMENT
## DE FULBERT ATTITSO
## 1
## TOUT SAUF DIOMAYE
## ET SONKO
## 1
## TRAVAIL ET
## ACCOMPLISSEMENT
## (ABDELLATIF EL
## MEKKI)
## 1
## TSY MIANKINA   2
## UFP   2
## UN NON MILITAIRE   1
## UN NOUVEAU PARTI   1
## UN NOUVEAU PARTI
## DE RÉFORME
## 0
## UNE NOUVELLE
## PERSONNE
## 2
## UNION DES
## DÉMOCRATES POUR
## LA RENAISSANCE DE
## LA GUINÉE (UDRG)
## 1
## UNION DES FORCES
## DÉMOCRATIQUES DE
## GUINÉE (NFD)
## 1
## UNION DU PEUPLE
## GABONAIS (UPG)
## 5
## UNION ET
## SOLIDARITÉ (US)
## 0
## UNION POUR LA
## RÉPUBLIQUE (UPR)
## 8
## VOTE BASED ON
## CANDIDATE'S TYPE
## AND PERSONALITY,
## NOT PARTY
## 0
## VOTE FOR A GOOD
## LEADER, NOT THE
## PARTY
## 1
## VOTE FOR CURRENT
## LEADER, NOT A
## PARTY
## 1


## VOTES FOR A
## PERSON, NOT A
## PARTY
## 3
## WANT A LEADER,
## NOT BASED ON
## PARTY
## 0
## WHICHEVER PARTY
## HE IS TOLD TO VOTE
## FOR
## 0
## WILL NOT VOTE FOR
## A PARTY, BUT A
## GOOD CANDIDATE
## 1
## WILL VOTE FOR
## SOMEONE WHO
## MAKES COMMUNITY
## CHANGES, NOT A
## PARTY.
## 2
## WOULD HAVE LIKED
## TO VOTE FOR
## KENNEDY
## 0
## YOUSSEF CHAHED   1

## Q99
## Value Count
Label Q99. Perceived survey sponsor
## Type Numeric
## Measurement Nominal
## -1 Missing 0
0 No one 642
1 “Afrobarometer" or national partner 19628
2 Research company / organization / program, but not
national partner
## 2117
3 Non-government or religious organization 1955
## 4 University / School / College 1012
5 Private company 961
## 6 Media 349
7 Political party or politician 1465
8 Government (including any government official,
government agency or ministry, or any other part of
government named by t
## 11096
9 International organization or another country 401
## 10 God 353
## 95 Other 48
98 Refused to answer 102


99 Don’t know 5472

Q99Other
## Value Count
Label Q99other. Perceived survey sponsor (verbatim)
## Type String
## Measurement Nominal
## 45555
## BANK   0
## BANK OF GHANA   0
## CARING PEOPLE   0
## CELLOU DALEIN   1
## CENTRE FOR SOCIAL
## RESEARCH WITH
## GOVERNMENT
## 1
## CERTAS PESSOAS   1
## CHANCE   2
## CONCERNED
## CITIZENS
## 1
## ECOWAS   1
## ELECTORAL
## COMMISSION
## 1
## ENQUÊTEUR   3
## ENUMERATOR   1
## EUROPEAN UNION   0
## FOMOS ENVIADOS
## POR OUTROS PAÍSES
## 1
## INSTITUT NATIONAL
## DE LA STATISTIQUE
## 2
## INTERVIEWER   0
## L'INSTANCE
## SUPÉRIEURE
## INDÉPENDANTE
## POUR LES ÉLECTIONS
## 2
## LA CONAC   2
## LES FRANCS-MAÇONS   1
## LUSAKA   1
## MEU CHEFE   2
## NOUVEL ORDRE
## MONDIAL
## 1
## PERSONNE   1


## PERSONNES QUI
## VEULENT NOUS
## AIDER
## 3
## SCAMMERS   0
## SOUTHERN AFRICAN
## DEVELOPMENT
## COMMUNITY (SADC)
## 1
## SPIES   6
## STAKEHOLDERS IN
## DEVELOPMENT
## POLICIES
## 1
## THE COMMUNITY   3
## UNION AFRICAINE   6
## UNITED NATIONS   0
## VOLUNTARY WORK   0

## Q100
## Value Count
Label Q100. Willing to participate in follow-up surveys
## Type Numeric
## Measurement Nominal
## -1 Missing 0
## 0 No 15993
## 1 Yes 26063
7 Not applicable [Respondent does not have a mobile
phone number]
## 2344
9994 ="Not asking in country" 1200

## ENDTIME

## Value

Label Time interview ended

## Type Numeric

## Measurement Scale

## Valid 45600

## Missing 0

## Mean 14:39


## LENGTH

## Value

Label Length of interview

## Type Numeric

## Measurement Scale

## Valid 45600



## Missing 0

## Mean 80.17


## LENGTH_INT
## Value Count
Label Interview length calculated excluding break
## Type Numeric
## Measurement Nominal
## 0 No 43342
## 1 Yes 1058
## 39   1
## 47   1
## 48   1
## 50   2
## 51   4
## 52   1
## 53   3
## 54   4
## 55   3
## 56   5
## 57   5
## 58   4
## 59   10
## 60   4
## 61   4
## 62   5
## 63   9
## 64   6
## 65   15
## 66   6
## 67   14
## 68   10
## 69   12
## 70   13
## 71   15
## 72   16
## 73   18
## 74   14
## 75   15
## 76   12
## 77   22
## 78   13
## 79   17


## 80   19
## 81   21
## 82   26
## 83   29
## 84   29
## 85   23
## 86   22
## 87   31
## 88   19
## 89   25
## 90   24
## 91   25
## 92   31
## 93   24
## 94   0
## 94   22
## 95   28
## 96   19
## 97   21
## 98   15
## 99   25
## 100   23
## 101   20
## 102   16
## 103   11
## 104   15
## 105   16
## 106   11
## 107   16
## 108   12
## 109   14
## 110   12
## 111   7
## 112   4
## 113   13
## 114   13
## 115   9
## 116   12
## 117   13
## 118   13
## 119   9
## 120   9
## 121   7


## 122   6
## 123   11
## 124   4
## 125   5
## 126   12
## 127   4
## 128   10
## 129   3
## 130   7
## 131   2
## 132   2
## 133   3
## 134   4
## 135   5
## 136   4
## 137   4
## 138   1
## 139   3
## 140   1
## 141   5
## 142   4
## 143   4
## 144   3
## 145   5
## 146   6
## 147   1
## 148   3
## 149   4
## 150   1
## 151   5
## 152   2
## 153   0
## 154   2
## 155   1
## 156   2
## 157   0
## 158   2
## 159   2
## 160   4
## 161   1
## 164   1
## 165   1
## 166   1


## 167   1
## 168   2
## 170   1
## 179   1
## 193   1
## 199   2
## 202   2
## 206   1
## 208   1
## 233   2

## Q101
## Value Count
Label Q101. Respondent's gender
## Type Numeric
## Measurement Nominal
## 1 Man 22956
## 2 Woman 22644

## Q102
## Value Count
Label Q102. Language of interview
## Type Numeric
## Measurement Nominal
## 1 English 5660
## 2 Français 7297
## 3 Portuguese 4876
## 4 Swahili 1903
## 5 Arab 367
## 100 Ajagbé 128
## 101 Baatonum 84
## 102 Dendi 46
## 103 Ditamari 10
## 104 Fongbé 362
## 105 Fulfuldé 15
## 106 Yoruba 93
## 140 Setswana 953
## 220 Crioulo 17
## 260 Akan 433
261 Ewe/Anlo 32
262 Ga/Dangbe 7
263 Dagbani/Mampruli 47
264 Dagaare/Waale 16


265 Frafra/Gruni/Taln/Nabt 32
## 300 Kikuyu 31
## 301 Luo 40
## 303 Kamba 11
## 304 Kalenjin 6
## 305 Somali 4
## 340 Sesotho 1178
## 380 Liberian English 537
## 420 Malgache (officiel) 753
421 Malgache avec spécificité régionale 447
## 460 Chitumbuka 131
## 461 Chichewa 1060
## 501 Bambara 975
## 513 Peulh / Fulfulde 3
## 516 Soninké / Sarakollé 29
## 517 Sonrhaï 31
## 518 Tamasheq 2
## 540 Sena 0
## 542 Changana 20
## 543 Makua 41
## 580 Afrikaans 80
## 581 Oshiwambo 195
## 582 Otjiherero 48
## 620 Hausa 445
## 621 Igbo 53
## 622 Yoruba 112
## 623 Pidgin English 98
## 660 Wolof 894
661 Pulaar ou Toucouleur 30
## 700 Afrikaans 11
## 701 Xhosa 50
## 702 Pedi 10
## 703 Sotho 10
## 704 Tswana 14
## 706 Zulu 156
## 780 Luganda 352
781 Runyankore or Rukiga 128
782 Runyoro/Rutooro 136
## 783 Lusoga 119
## 784 Lumasaaba 42
## 787 Ateso 48
788 Langi or Acholi 115
## 789 Alur 17


## 790 Lugbara 56
## 791 Japadhola 12
## 798 Sabiny 3
## 799 Ngakarimojong 29
## 820 Bemba 461
821 Nyanja/Chewa 277
## 822 Tonga 86
## 823 Kaonde 56
## 824 Lozi 65
## 860 Ndebele 173
## 861 Shona 931
## 900 Créole 1177
## 930 Krio 1062
## 931 Mende 100
## 932 Themne 27
## 1143 Ben, Moba 82
## 1144 Ewé 320
## 1150 Kabyè 45
## 1160 Tem, Kotokoli 52
## 1220 Fulfuldé 104
## 1221 Pidgin 3
## 1276 Dioula 8
## 1301 Maninka 272
## 1302 Kpèlè 42
## 1303 Kissié 33
## 1304 Poular 306
## 1305 Soussou 275
## 1500 Moroccan Arabic (darija) 1200
## 1580 Tunisian Arabic 1200
1620 siSwati 954
## 1680 Creole 1125
## 1750 Umbundu 15
## 1752 Chokwe 15
## 1754 Nganguela 4
## 1755 Kwanhama 17
## 1780 Lingala 130
## 1781 Kituba 133
## 1800 Mandinka 445
## 1801 Fula 69
## 1802 Wolof 338
## 1803 Jola 10
## 1840 Crioulo 992
1880 Arabe /Hassaniya 1052


## 1881 Pular 79
## 1883 Soninké 19
## 3001 Gourane 24
## 3002 Kanembou 95
## 3003 Ngambaye 137
## 3040 Shikomori 632
## 9995 Other 25

Q102Other
## Value Count
Label Q102other. Language of interview (verbatim)
## Type String
## Measurement Nominal
## 45575
## ENGLISH, SETSWANA   1
## FANG   2
## FULA   2
## GRUMA   0
## GRUSI   1
## GUERZE   1
## KOKOMBA   0
## KONO   2
## KUSAAL   6
## KUSASI   0
## LANGUES
## OFFICIELLES ET
## RÉGIONALES
## 0
## LIKPAKPAN   2
## MANDINGA   0
## MANIAN   0
## MANO   1
## NZEBI   0
## SISSALI   2
## SISWATI   0
## SUSU   3
## TOMA   1
## YANM   0

## Q103
## Value Count
Label Q103. Others present
## Type Numeric
## Measurement Nominal


1 No one 31140
2 Spouse only 2766
3 Children only 5849
4 Another adult/a few others 5213
5 Small crowd 632

## Q104A
## Value Count
Label Q104a. Check with others
## Type Numeric
## Measurement Ordinal
## 0 No 44093
## 1 Yes 1507

## Q104B
## Value Count
Label Q104b. Influence by others
## Type Numeric
## Measurement Ordinal
## 0 No 44523
## 1 Yes 1077

## Q104C
## Value Count
Label Q104c. Approached by community/party
representatives

## Type Numeric
## Measurement Ordinal
## 0 No 44789
## 1 Yes 811

## Q104D
## Value Count
Label Q104d. Feel threatened
## Type Numeric
## Measurement Ordinal
## 0 No 45193
## 1 Yes 407

## Q104E
## Value Count
Label Q104e. Physically threatened
## Type Numeric


## Measurement Ordinal
## 0 No 45366
## 1 Yes 234

## Q106A
## Value Count
Label Q106a. Respondent friendly
## Type Numeric
## Measurement Ordinal
## 1 Friendly 40902
2 In between 4395
## 3 Hostile 304

## Q106B
## Value Count
Label Q106b. Respondent interested
## Type Numeric
## Measurement Ordinal
## 1 Interested 38759
2 In between 5952
## 3 Bored 889

## Q106C
## Value Count
Label Q106c. Respondent cooperative
## Type Numeric
## Measurement Ordinal
## 1 Cooperative 40131
2 In between 5202
## 3 Uncooperative 267

## Q106D
## Value Count
Label Q106d. Respondent patient
## Type Numeric
## Measurement Ordinal
## 1 Patient 38259
2 In between 5910
## 3 Impatient 1431

## Q106E
## Value Count
Label Q106e. Respondent at ease


## Type Numeric
## Measurement Ordinal
1 At ease 38637
2 In between 5984
## 3 Suspicious 978

## Q106F
## Value Count
Label Q106f. Respondent honest
## Type Numeric
## Measurement Ordinal
## 1 Honest 39776
2 In between 5612
## 3 Misleading 213

## Q108

## Value

## Label Q108. Interviewer Number

## Type String

## Measurement Nominal


## Q109

## Value

Label Q109. Interviewer’s age

## Type Numeric

## Measurement Scale

## Valid 45600

## Missing 0

## Mean 32.45


## Q110
## Value Count
Label Q110. Interviewer’s gender
## Type Numeric
## Measurement Nominal
## 1 Man 20505
## 2 Woman 25095

## Q111
## Value Count
Label Q111. Interviewer’s race
## Type Numeric
## Measurement Nominal


## 1 Black / African 2329
## 2 White / European 0
3 Coloured / Mixed race 71
## 4 Arab / Lebanese / North African 0
5 South Asian (Indian, Pakistani, etc.) 0
6 East Asian (Chinese, Korean, Indonesian, etc.) 0
9994 Not asked in the country 43200
## 9995 Other 0
9999 Don’t know 0

## Q111OTHER
## Value Count
Label Q111Other. Interviewer’s race (verbatim)
## Type String
## Measurement Nominal
## 45600

## Q112

## Value

Label Q112. Interviewer's home language

## Type Numeric

## Measurement Nominal


## Q112OTHER
## Value Count
Label Q112Other. Interviewer's home language (verbatim)
## Type String
## Measurement Nominal
## 45197
## ABOURE   30
## EWE DE VOLTA
## REGION
## 22
## JALONKÉ   53
## KONGO   29
## KOYO   23
## LINGALA   64
## MBETI   35
## MEZIME   14
## MOGHAMO   49
## MOSHIE   12
## TAGBANAN   17
## TEKE   20
## YAKA   35



## Q113

## Value

Label Q113. Interviewer's ethnic group or tribe

## Type Numeric

## Measurement Nominal


## Q113OTHER
## Value Count
Label Q113Other. Interviewer's ethnic group or tribe
## (verbatim)

## Type String
## Measurement Nominal
## 45267
## ABOURE   30
## BORANA   22
## BUH   50
## DIVERSAS   29
## EWE DE VOLTA
## REGION
## 22
## FRANÇAIS   22
## KAKA   40
## MEZIME   14
## MISTA   10
## MOSHIE   12
## NAKERE   62
## TUMBATU   19

## Q114
## Value Count
Label Q114. Interviewer's education
## Type Numeric
## Measurement Ordinal
3 Primary school completed 90
4 Some secondary school / high school 648
5 Secondary school / high school completed 5455
6 Post-secondary qualifications, other than university
e.g. a diploma or degree from a polytechnic or college
## 5154
7 Some university 6919
8 University completed 23104
9 Post graduate 4230

## Q115_1



## Value

Label Q115. Other spoken languages_first

## Type Numeric

## Measurement Nominal


## Q115_2

## Value

Label Q115. Other spoken languages_second

## Type Numeric

## Measurement Nominal


## Q115_3

## Value

Label Q115. Other spoken languages_third

## Type Numeric

## Measurement Nominal


## Q115_4

## Value

Label Q115. Other spoken languages_fourth

## Type Numeric

## Measurement Nominal


## Q115_5

## Value

Label Q115. Other spoken languages_fifth

## Type Numeric

## Measurement Nominal


## Q115_6

## Value

Label Q115. Other spoken languages_sixth

## Type Numeric

## Measurement Nominal


## Q115_7
## Value Count
Label Q115. Other spoken languages_seventh
## Type Numeric
## Measurement Nominal
## 1 English 0
## 4 Swahili 0
## 260 Akan 0


261 Ewe/Anlo 0
262 Ga/Dangme 0
263 Dagbani/Mampruli 0
## 264 Gonja 0
265 Dagaare/Waale 0
266 Frafra/Gruni/Taln/Nabt 0
## 267 Kusaal 0
268 Grusi/kasem/Nankani 0
## 501 Bambara 0
## 503 Bobo 0
## 505 Dogon 0
## 507 Kakolo 0
## 509 Malinké 0
## 513 Peulh / Fulfude 0
## 516 Soninké / Sarakollé 0
## 517 Sonrhaï 0
## 518 Tamasheq 0
## 540 Makua 0
## 541 Sena 0
## 542 Ndau 0
## 543 Changana 0
## 545 Chope 0
## 546 Bitonga 0
## 547 Makonde 0
## 548 Chuabo 0
## 550 Lomue 0
## 551 Shona 0
## 552 Xitswa 0
## 553 Xironga 0
## 554 Chichewa 0
## 555 Cinyungwe 5
## 556 Ciyao 0
## 558 Kimwani 0
## 620 Hausa 0
## 621 Igbo 0
## 622 Yoruba 0
## 623 Pidgin English 0
## 625 Ebira 0
## 630 Tiv 0
## 633 Edo 0
## 634 Igala 0
## 636 Idoma 0
## 638 Ikwere 0


## 700 Afrikaans 35
## 701 Ndebele 0
## 702 Xhosa 0
## 703 Pedi 0
## 704 Sotho 0
## 705 Tswana 0
## 706 Swazi 17
## 707 Venda 0
## 708 Zulu 36
709 Shangaan/Tsonga 39
## 780 Luganda 0
## 781 Runyankore 0
## 782 Runyoro 0
## 783 Lusoga 0
## 784 Lumasaaba 0
## 785 Lukhonzo 15
## 786 Lunyole 0
## 787 Ateso 0
## 788 Acholi 0
## 789 Alur 0
## 790 Lugbara 0
## 791 Madi 0
## 792 Japadhola 0
## 793 Lusamia 0
## 794 Lugwere 0
## 795 Rukiga 4
## 796 Rutooro 21
## 797 Langi 8
## 798 Kupsabinyi 0
## 799 Ngakarimojong 0
## 820 Bemba 0
## 821 Nyanja 0
## 822 Tonga 0
## 823 Lozi 0
## 824 Chewa 0
## 825 Nsenga 0
## 827 Kaonde 0
## 828 Luvale 0
## 829 Namwanga 0
## 830 Lunda 0
## 835 Ngoni 104
## 839 Chokwe 60
## 840 Mbunda 0


## 860 Ndebele 0
## 861 Shona 0
## 862 Zezuru 0
## 863 Korekore 0
## 864 Karanga 0
## 865 Manyika 0
## 866 Ndau 0
## 1140 Adja 0
## 1143 Ben, Moba 0
## 1144 Ewé 0
## 1146 Gourma 0
## 1147 Haoussa 0
## 1150 Kabyè 0
## 1152 Lama, Lamba 0
## 1153 Mina, Guen 0
1154 N’Tcha, Bassar 0
## 1155 Nawdem, Losso 1
## 1157 Ouatchi 0
## 1160 Tem, Kotokoli 0
## 1300 Mano 0
## 1301 Maninka 0
## 1303 Kpèlè 0
## 1304 Kissié 0
## 1305 Poular 0
## 1307 Soussou 0
## 1840 Crioulo 0
## 1841 Balanta 0
## 1843 Bijagós 0
## 1844 Fula 0
## 1845 Felupe 0
## 1847 Mandinga 0
## 1848 Manjaco 0
## 1850 Papel 0
## 9995 Other 32
9996 No further response 45224

## Q115_8
## Value Count
Label Q115. Other spoken languages_eighth
## Type Numeric
## Measurement Nominal
## 1 English 0
## 4 Swahili 0


## 540 Makua 0
## 541 Sena 0
## 542 Ndau 0
## 543 Changana 0
## 545 Chope 0
## 546 Bitonga 0
## 547 Makonde 0
## 548 Chuabo 0
## 550 Lomue 0
## 551 Shona 0
## 552 Xitswa 0
## 553 Xironga 0
## 554 Chichewa 0
## 555 Cinyungwe 0
## 556 Ciyao 0
## 558 Kimwani 0
## 700 Afrikaans 0
## 701 Ndebele 0
## 702 Xhosa 0
## 703 Pedi 0
## 704 Sotho 0
## 705 Tswana 35
## 706 Swazi 0
## 707 Venda 0
## 708 Zulu 17
709 Shangaan/Tsonga 0
## 780 Luganda 0
## 781 Runyankore 0
## 782 Runyoro 0
## 783 Lusoga 0
## 784 Lumasaaba 0
## 785 Lukhonzo 0
## 786 Lunyole 0
## 787 Ateso 0
## 788 Acholi 0
## 789 Alur 0
## 790 Lugbara 0
## 791 Madi 0
## 792 Japadhola 0
## 793 Lusamia 0
## 794 Lugwere 0
## 795 Rukiga 15
## 796 Rutooro 4


## 797 Langi 0
## 798 Kupsabinyi 0
## 799 Ngakarimojong 8
## 820 Bemba 0
## 821 Nyanja 0
## 822 Tonga 0
## 823 Lozi 0
## 824 Chewa 0
## 825 Nsenga 0
## 827 Kaonde 0
## 828 Luvale 0
## 829 Namwanga 0
## 830 Lunda 0
## 835 Ngoni 0
## 839 Chokwe 0
## 840 Mbunda 60
## 1140 Adja 0
## 1143 Ben, Moba 0
## 1144 Ewé 0
## 1146 Gourma 0
## 1147 Haoussa 0
## 1150 Kabyè 0
## 1152 Lama, Lamba 0
## 1153 Mina, Guen 0
1154 N’Tcha, Bassar 0
## 1155 Nawdem, Losso 0
1156 Ngam-Gam 1
## 1157 Ouatchi 0
## 1160 Tem, Kotokoli 0
## 1840 Crioulo 0
## 1841 Balanta 0
## 1843 Bijagós 0
## 1844 Fula 0
## 1845 Felupe 0
## 1847 Mandinga 0
## 1848 Manjaco 0
## 1850 Papel 0
## 9995 Other 0
9996 No further response 45461

## Q115_9
## Value Count
Label Q115. Other spoken languages_ninth


## Type Numeric
## Measurement Nominal
## 1 English 0
## 4 Swahili 0
## 540 Makua 0
## 541 Sena 0
## 542 Ndau 0
## 543 Changana 0
## 545 Chope 0
## 546 Bitonga 0
## 547 Makonde 0
## 548 Chuabo 0
## 550 Lomue 0
## 551 Shona 0
## 552 Xitswa 0
## 553 Xironga 0
## 554 Chichewa 0
## 555 Cinyungwe 0
## 556 Ciyao 0
## 558 Kimwani 0
## 700 Afrikaans 0
## 701 Ndebele 0
## 702 Xhosa 0
## 703 Pedi 0
## 704 Sotho 0
## 705 Tswana 0
## 706 Swazi 0
## 707 Venda 0
## 708 Zulu 0
709 Shangaan/Tsonga 0
## 780 Luganda 0
## 781 Runyankore 0
## 782 Runyoro 0
## 783 Lusoga 0
## 784 Lumasaaba 0
## 785 Lukhonzo 0
## 786 Lunyole 0
## 787 Ateso 0
## 788 Acholi 0
## 789 Alur 0
## 790 Lugbara 0
## 791 Madi 0
## 792 Japadhola 0


## 793 Lusamia 0
## 794 Lugwere 0
## 795 Rukiga 0
## 796 Rutooro 15
## 797 Langi 0
## 798 Kupsabinyi 0
## 799 Ngakarimojong 0
## 820 Bemba 0
## 821 Nyanja 0
## 822 Tonga 0
## 823 Lozi 0
## 824 Chewa 0
## 825 Nsenga 0
## 827 Kaonde 0
## 828 Luvale 0
## 829 Namwanga 0
## 830 Lunda 0
## 835 Ngoni 0
## 839 Chokwe 0
## 840 Mbunda 0
## 1140 Adja 0
## 1143 Ben, Moba 0
## 1144 Ewé 0
## 1146 Gourma 0
## 1147 Haoussa 0
## 1150 Kabyè 0
## 1152 Lama, Lamba 0
## 1153 Mina, Guen 0
1154 N’Tcha, Bassar 0
## 1155 Nawdem, Losso 0
1156 Ngam-Gam 0
## 1157 Ouatchi 0
## 1160 Tem, Kotokoli 1
## 1840 Crioulo 0
## 1841 Balanta 0
## 1843 Bijagós 0
## 1844 Fula 0
## 1845 Felupe 0
## 1847 Mandinga 0
## 1848 Manjaco 0
## 1850 Papel 0
## 9995 Other 0
9996 No further response 45584



## Q115_10
## Value Count
Label Q115. Other spoken languages_tenth
## Type Numeric
## Measurement Nominal
## 1 English 0
## 4 Swahili 0
## 540 Makua 0
## 541 Sena 0
## 542 Ndau 0
## 543 Changana 0
## 545 Chope 0
## 546 Bitonga 0
## 547 Makonde 0
## 548 Chuabo 0
## 550 Lomue 0
## 551 Shona 0
## 552 Xitswa 0
## 553 Xironga 0
## 554 Chichewa 0
## 555 Cinyungwe 0
## 556 Ciyao 0
## 558 Kimwani 0
## 700 Afrikaans 0
## 701 Ndebele 0
## 702 Xhosa 0
## 703 Pedi 0
## 704 Sotho 0
## 705 Tswana 0
## 706 Swazi 0
## 707 Venda 0
## 708 Zulu 0
709 Shangaan/Tsonga 0
## 780 Luganda 0
## 781 Runyankore 0
## 782 Runyoro 0
## 783 Lusoga 0
## 784 Lumasaaba 0
## 785 Lukhonzo 0
## 786 Lunyole 0
## 787 Ateso 0
## 788 Acholi 0


## 789 Alur 0
## 790 Lugbara 0
## 791 Madi 0
## 792 Japadhola 0
## 793 Lusamia 0
## 794 Lugwere 0
## 795 Rukiga 0
## 796 Rutooro 0
## 797 Langi 0
## 798 Kupsabinyi 0
## 799 Ngakarimojong 0
## 1140 Adja 0
## 1143 Ben, Moba 0
## 1144 Ewé 0
## 1146 Gourma 0
## 1147 Haoussa 0
## 1150 Kabyè 0
## 1152 Lama, Lamba 0
## 1153 Mina, Guen 0
1154 N’Tcha, Bassar 0
## 1155 Nawdem, Losso 0
1156 Ngam-Gam 0
## 1157 Ouatchi 0
## 1160 Tem, Kotokoli 0
## 1840 Crioulo 0
## 1841 Balanta 0
## 1843 Bijagós 0
## 1844 Fula 0
## 1845 Felupe 0
## 1847 Mandinga 0
## 1848 Manjaco 0
## 1850 Papel 0
## 9995 Other 0
9996 No further response 45600

## Q115OTHER
## Value Count
Label Q115Other. Other spoken languages (verbatim)
## Type String
## Measurement Nominal
## 44084
## ABOURE   30
## ANGLAIS   393


## ANGLAIS, TURC   40
## BAKOKO   63
## BAMBARA   53
## BHOJPURI   55
## BUH   50
## DJIMINI   30
## ENGLISH   143
## FOULBÉ   50
## GUIDAR   3
## HAUSA   48
## HINDI   93
## HINDI, BHOJPURI   40
## INGLÊS   27
## ITALIEN   63
## JALONKÉ   53
## KISUNDI   32
## KIYAKA   35
## KONO   42
## LOKPA   20
## LOLO   32
## MBOSI   31
## MOSHI   12
## NAFAANA   15
## NINZOM,ABU   62

--- 
title: "NCHRP 08-123: Census Transportation Data Field Guide for Transportation Applications"
author: "Cambridge Systematics"
date: "2021-12-08"
site: bookdown::bookdown_site
documentclass: book
bibliography: [book.bib, packages.bib]
# url: your book url like https://bookdown.org/yihui/bookdown
# cover-image: path to the social sharing image like images/cover.jpg
description: |
  This is a minimal example of using the bookdown package to write a book.
  The HTML output format for this example is bookdown::bs4_book,
  set in the _output.yml file.
biblio-style: apalike
csl: chicago-fullnote-bibliography.csl
---

# Introduction

The central role that transportation plays in the U.S. economy is reflected in this comment from the National Surface Transportation Policy and Revenue Study Commission – _"The American economy works, in large measure, because shippers, manufacturers, and service providers have a transportation system that provides many ways to access labor and move raw materials and finished products. Individuals are able to travel to workplaces, shopping, educational institutions, recreation, medical care, and other locations critical to their quality of life."_

The changes brought about by technology and especially the smartphone revolution with its impacts on online shopping and the emergence of transportation network companies have upended the way people live, work, shop, and play with profound implications for transportation investment, policy, and operational decisions. One example of this change is the decrease in the proportion of licensed drivers among the 55 and under age cohorts in 2014 compared to 19831F . These changes in travel behavior need to be measured accurately to ensure that policy decisions happen in a data driven context. Collecting data on travel behavior is also becoming more challenging and is hampered by low survey response rates or high rates of survey attrition. Therefore, it is critical to quilt different sources of travel behavior data to provide estimates in a consistent, reliable, and sustainable manner. The FHWA report on data availability and gaps related to our understanding of travel behavior highlights the need for data fusion techniques to overcome these gaps2F . Census data, even in this age of big data, offer tremendous value and insights to help overcome the data availability and gaps identified by FHWA. The various data products released by the Census Bureau and its extensions provide information and insights that will help arrive at data driven policy decisions to address these changes. 


## History of the Census

The Census is enshrined in the U.S. Constitution as stated in Article I, Section 2, clause 3: “For a government of the people to function, the people must be counted”. The Founders wanted an “enumeration” to occur within three years of the first meeting of Congress, and then “within every subsequent Term of ten Years, in such Manner as they shall by Law direct.” On March 1, 1790, President George Washington signed legislation into law—the "1790 Census Act"—assigning U.S. marshals the task of conducting the nation's first Census. Marshals and their assistants traveled throughout the 13 states, districts of Kentucky, Maine, Vermont, and the Southwest Territory (Tennessee) using rudimentary forms of their own design to collect the name of each head of household along with a numeric count of every household's free White males aged 16 and older, free White males under 16, free White females, all other free persons, and slaves as of the first Monday of August 1790. At its conclusion, the 1790 Census found that the United States was home to 3,929,214 people. The largest urban places were New York City, NY (33,131 residents); Philadelphia, PA (28,522); Boston, MA (18,320); and Baltimore, MD (13,503).

Twenty years later, Congress added the collection of manufacturing data to the 1810 Census. The Census expanded further with the first questions about the nation's agricultural pursuits in 1820. In 1840, Congress added the collection of governments' data about schools and school attendance. Beginning in 1850, marshals listed the name of every free person on the Census schedule, and the number of demographic inquiries grew to include questions to collect data about individuals' profession, place of birth, and marital status.

The Census Act of 1880 replaced the U.S. marshals and their assistants—who conducted the Censuses since 1790—with specially-hired and trained enumerators. These Census enumerators collected so much data during the 1880 Census that it took a decade to complete its tabulation and publication. Anticipating an even greater volume of data in 1890, former Census Bureau employee and inventor Herman Hollerith received a contract to supply mechanical tabulators to speed data processing and tabulation. Enumerators used a separate schedule for each family during the 1890 Census and collected even more detailed data about individuals' family, employment, health, education, and home ownership than in previous years. One hundred years after the United States conducted its first Census, the 1890 Census reported the nation had grown to nearly 63 million. 
Recognizing the need to maintain a permanent, specially-trained workforce charged with collecting the nation's demographic, economic, agriculture and governments data, Congress made the U.S. Census Bureau a permanent agency in 1902. The  Census Bureau could now plan population Censuses every 10 years as well as mid-decade Censuses and surveys, including more frequent Censuses of manufacturers and special Censuses of war commodities during World War I.

Following the 1929 Stock Market Crash and the start of the Great Depression, the 1930 Census included a "standard" questionnaire that collected demographic, citizenship, occupation, employment, and veterans status data.  A supplemental questionnaire also collected additional data to help the government better understand the impact that the economic crisis had on America's workers. The 1940 Census was the first in which the Census Bureau used statistical sampling to collect additional data about the population without unduly increasing the overall burden on respondents and data processing. While visiting each household, the enumerators asked 5 percent of the nation's population (i.e., those people whose name fell on the schedule's "sample lines") questions like their parents' place of birth, mother tongue, veterans status, and for women, the number of marriages, age at first marriage, and number of children ever born. Subsequent Censuses added sample questions including the means of transportation to work (1960), occupation 5 years ago (1970), ancestry/ethnic origin (1980), and grandparents as caregivers (2000). In 2005, the annual American Community Survey replaced the sample questions on the decennial Census questionnaires. As a result, the 2010 Census used a single, 10-question form for the nearly 309 million people it counted.

Over its 230 year history, the decennial Census has recorded the United States' remarkable growth from its origins as a rural, farming nation in 1790 to the world's third most populous country (behind China and India), which provided goods and services valued at $21.73 trillion in the fourth quarter of 2019. Figure \@ref(fig:timeline) shows a timeline of the Census since 1790.

<div class="figure">
<img src="images/Census_timeline.png" alt="Census Timeline since 1790" width="428" />
<p class="caption">(\#fig:timeline)Census Timeline since 1790</p>
</div>
Source: U.S. Census Bureau

## History of Transportation in the Census

The inclusion of transportation items is a fairly recent occurrence in the history of the decennial Census. Questions pertaining to transportation did not appear until 1960 when three such questions were asked on a 25-percent sample basis. The population items in 1960 included questions on each worker's place of work (city, county, and state) and means of transportation to work. The housing items included a question on the number of automobiles available for use by the members of each household. The principal impetus for adding the question on place of work to the 1960 Census was the need for data on commuting interchanges for use as an indicator of economic integration between large cities and their suburbs as part of the criteria for delineating metropolitan statistical areas. The commuting data from the Census were certainly of interest to transportation planners, but urban transportation planning in the early 1960s was still being done on the basis of locally conducted origin-destination surveys (See Figure \@ref(fig:c60))

<div class="figure">
<img src="images/c60.png" alt="1960 Census Transportation Questions" width="640" />
<p class="caption">(\#fig:c60)1960 Census Transportation Questions</p>
</div>
 Source:	https://www.census.gov/history/pdf/1960censusquestionnaire-2.pdf.
 
By 1970, with the development by the Census Bureau of Address Coding Guides (ACGs) and Dual Independent Map Encoding (DIME) files, interest in the Census as a source of transportation planning data increased considerably. The ACGs and DIME files provided the capability of geographically coding place-of-work addresses within the urbanized portion of metropolitan areas down to the level of the Census block. The 1970 Census again asked questions on place of work, means of transportation to work, and automobile availability. However, the place-of-work question asked for the actual street address of the respondent's workplace, and these addresses were coded to Census blocks within the areas covered by ACGs and DIME files. The DOT contracted with the Bureau of the Census to create a series of special tabulations in a transportation planning package. Metropolitan Planning Organizations (MPOs) obtained the data tabulated for their traffic zones on a cost-reimbursable basis.

Between 1970 and 1980, several developments resulted in a significant expansion in the number of transportation items included in the decennial Census. The energy crisis of the early 1970s and the subsequent ongoing concern for the nation's supply of nonrenewable energy sources brought about a sharp increase in the need for statistics for transportation planning and policy formulation. From 1975 to 1977, under the sponsorship of the DOT, the Census Bureau conducted for the first time journey-to-work surveys in 60 metropolitan areas and a national survey in 1975, all as part of the Annual Housing Survey. 

In recognition of the growing need for analysis of these data, a Journey-to-Work Statistics Branch was created within the bureau's Population Division to carry out the technical planning and developmental work pertaining to the collection, processing, tabulation, and analysis of journey-to-work data from the decennial Census and periodic surveys. Also, during the decade, the cost of conducting metropolitan origin-destination surveys increased rapidly, and the DOT began to encourage local agencies to look to the decennial Census as an alternative source for cost effective transportation planning data.

Thus, due to the significant increase in the need for transportation data at all levels of government, the 1980 Census included eight transportation items: six population questions and two housing questions. On the population side, in addition to questions on place of work and means of transportation to work, the 1980 Census asked about carpooling arrangements, the number of riders in the carpool, travel time from home to work, and whether persons had a disability that limited or prevented their use of public transportation. On the housing side, the automobile availability question was supplemented with an additional question on the number of light trucks and vans available for use by members of each household.

Once again for the 1980 Census, the DOT contracted with the Census Bureau to create a series of special tabulations in a Transportation Planning Package. MPOs obtained the data tabulated for their traffic analysis zones on a cost-reimbursable basis. To increase the utility of the Census data for local transportation planning, the Census Bureau developed an innovative procedure to assign incomplete place-of-work responses to Census blocks so that they too could be tabulated at the traffic analysis zone level (See Figure \@ref(fig:c80)).

<div class="figure">
<img src="images/c80.png" alt="1980 Census Transportation Questions" width="640" />
<p class="caption">(\#fig:c80)1980 Census Transportation Questions</p>
</div>
Source:	https://www.Census.gov/history/pdf/1980_long_questionnaire.pdf

In contrast to the 1980 Census, the 1990 decennial Census did not break up the household vehicle availability question into two separate questions but rather treated it as a single question and included information about travel mode, work location, carpool as well as two new questions on departure time to work and travel time to work. The  2000 decennial Census, the last year of the long form, had the same transportation related questions as the 1990 decennial Census which were asked of one in six households. 

Since 2000, the long form is no longer available and transportation related questions are being asked by the American Community Survey (ACS) which samples one in forty households on a rolling basis. 

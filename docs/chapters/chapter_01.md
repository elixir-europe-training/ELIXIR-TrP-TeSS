## More background information about TeSS
During the ELIXIR-EXCELERATE project, the TeSS platform has been established as the key application for bioinformatics training events and material aggregation. During a period of further adoption of the TeSS platform as such on the international level e.g. in Australia and in the Netherlands, it became obvious that the implementation of individual automatic content scrapers for more than 30 content providers lead to an enormous diversity of the code base and finally to a maintenance challenge. Therefore, during the last two to three years, a strategic reorientation of the automated harvesting procedure has been proposed and implemented in TeSS using the Bioschemas profiles for Course, CourseInstance and TrainingMaterial. This approach will put the content providers in a more prominent position since they are in turn responsible for a more structured delivery of more comprehensive metadata of their training events and material to TeSS as the aggregation platform. In the longer run, this will increase the quality level of the aggregated resources and its usefulness to TeSS user base.

`TODO: Would be insteresting to add a box explaining the specificity of each?` 

Content providers looking to promote use of particular tools and databases via their course offering or the specific training material can find information about them in other ELIXIR registries, such as [bio.tools](https://bio.tools) for tools and web services  and [FAIRsharing.org](https://fairsharing.org) for databases, standards and policies . Lately, such registries started to track training relating to the resources they list. Therefore, it is mutually beneficial that TeSS provides the relevant links, allowing users to search for resource-specific training; and the resource pages in bio.tools and FAIRsharing that contain reciprocal links for users to discover relevant training in TeSS.

`TODO: Are TeSS, BioTools and FAIRsharing connected? In content?`

Related to the provisioning of persistent identifiers, TeSS provides the Digital Object Identifier (DOI) as a unique means to identify training material. Given that minting services by e.g. university libraries are not yet broadly available for teaching and learning material in contrast to research datasets and collections, associated workflows, software and models, we recommend to use services like OSF or zenodo to get own unique, persistent URLs and DOIs.

Given the engagement of the ELIXIR Train the Trainer instructor's community to create a vibrant environment for reciprocal support and exchange of experiences via the ELIXIR Train the Trainer programme, the TeSS content providers are encouraged to  follow best-practice guidance on course and training material development (Via et al., 2020). Therefore, we recommend applying the Bloom hierarchy of cognitive skills to formulate the Learning objectives for the courses as well as for training material. For more detailed information about our pedagogical model, please browse to the course material of the [ELIXIR Train the Trainer course](https://github.com/TrainTheTrainer/ELIXIR-EXCELERATE-TtT). 

## Scenario 1: Searching for training events in TeSS

Training resources (both events and materials) may be searched in TeSS in several ways. If you are on the main page of TeSS, a general search can be performed based on keywords, which will return separate lists of events and materials. Alternatively, events or materials can be searched for independently of each other. This second approach allows more precise filtering on several parameters (e.g., event type, country, and target audience) alone or in combination.

![screenshot for TeSS page with search box](https://github.com/elixir-europe-training/ELIXIR-TrP-TeSS/blob/main/docs/assets/images/GxGphHo.png)

In this protocol, we provide examples of searches for specific events or materials. Be aware that by searching for events, the standard search returns only future events. If you want to include past events, you need to click the **Show past event** button. 

**********************

 
Please navigate to [TeSS](https://tess.elixir-europe.org) and follow the steps shown below.

1. Select Events in the top menu.
2. **Search for** ‘Single-cell’ as the keyword in the search text box on the right side of the page. **You can click on the magnifier icon or press Enter**.
3. Click on the **Show past events** button **at the bottom of the side menu**. Click on 'Filters' if you do not see this side menu due to your browser being non-fullscreen.
4. On the side menu, scroll down to the Country facet. We will select the United Kingdom.
5. On the side menu, scroll to the facet Target audience. Select ‘Graduate students’.
6. As a result, you get the list of training events about single-cell data analysis available in the United Kingdom for Graduate students.
7. Change the sort filter to 'Latest' in order to see an anti-chronological listing of the events.

At any time you may remove any of the filters you applied to reduce stringency of your search.

Please proceed to the next step to see the results.

**********************

At any time you may remove any of the filters you applied to reduce stringency of your search.

In June 2023, we found 13 past events with this search query.  

Have a look at the URL to understand how you could query TeSS via the API.

https://tess.elixir-europe.org/events?country=United+Kingdom&include_expired=true&q=single-cell&target_audience=Graduate+students&sort=late

Let's have a look at the documentation of the API: https://tess.elixir-europe.org/api/json_api#tag/events

Here you see all the query parameters. In our query, we have been using several of these parameters and concatenated them.

1. First, we used the free text query parameter `q` and set it to `single-cell`. 
2. Second, we used the `include_expired` parameter and set it to `true`. 
3. Third, we used the `country[]` parameter and set it to "United+Kingdom". Note that you need to replace the space by a `+` sign. 
4. Fourth, we used the `target_audience[]` parameter and set it to `Graduate+students". 
5. To change the sorting, use the `sort` parameter. You have 5 options, we have used `late` to sort by date, latest to earliest (events only).  

If you would like to get the events from France, too, you'd need to add yet another query with `country[]=France`.

To get the full query, you need to concatenate all the individual queries with an ambersand `&`. 

## Scenario 2: Searching for e-learning materials in TeSS

E-learning resources are a specific type of training materials in TeSS which are displayed on the dedicated section **E-learning** on the main TeSS page. 

![screenshot for TeSS page with search box](https://github.com/elixir-europe-training/ELIXIR-TrP-TeSS/blob/main/docs/assets/images/CXt2MEE.jpg)

But you can also perform a specific search on the Materials page filtering on 'Resource type' and retrieve e-learning material by specifying the value 'e-learning'.

*********************

Please navigate to [TeSS](https://tess.elixir-europe.org).

1.	Select Materials in the top menu.

2.	Enter a keyword in the search text box on the right side of the page. We will enter ‘Data retrieval’.

3.	On the side menu, select a difficulty level. We will select ‘Beginner’.

4.	Scroll to the facet ‘Resource type’ and select ‘e-learning’.

5.	You get the list of training materials about data retrieval intended for a beginner level audience whereby the resource has been tagged as e-learning material. At any time you may remove any of the filters you applied to reduce stringency of your search.


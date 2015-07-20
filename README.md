ContentMine Workshop at the University of Bath
==============

![ContentMine logo](https://github.com/ContentMine/ebi_workshop_20141006/raw/master/setup/CM_logo.png)

## Register [here] (http://www.eventbrite.com/e/text-data-mining-for-biologists-registration-17603659018) (registration is FREE, places limited to 25 )

#### Location: Room 3.7, Building 3 West, University of Bath
#### Date: 28th July 2015

|28th July 2015          | 
:---------------:         | 
|Training Workshop      | 
|10:00 - 17:30          |  

## <img src="http://www.biddlestudios.com/images/twitter_favicon.png" alt="twitter logo" style="width:10px;height:10px"> \#BathMining
Contact us via [@TheContentMine] (https://twitter.com/TheContentMine) or ross.mounce@gmail.com


### Trainers:

- Ross Mounce [@rmounce](https://twitter.com/rmounce)
- Peter Murray-Rust [@petermurrayrust](https://twitter.com/petermurrayrust)
- The ContentMine Team [@TheContentMine] (https://twitter.com/TheContentMine)

### Please read the [Pre-workshop Installation Instructions] (https://github.com/ContentMine/SciDataCon2014/blob/master/Info/README.md) 
##### We would also appreciate your [feedback](https://docs.google.com/forms/d/1nCaM6_sA-clrWDoNzdua5Luxg8bV7dcBMj82pERIIpQ/viewform)

### Workshop Purpose
Content mining technologies hold much potential for maximising discovery and reuse of research as well as generating novel scientific discoveries through automatedly searching, indexing and analysing the scientific literature. 

This workshop aims to educate and engage researchers and research-related professionals in the UK who are interested in using these technologies for their work in the biological sciences. In turn this will help to provide demonstrable examples of the benefits of content mining.

Participants will be instructed in use and custom development of tools in the ContentMine pipeline before having the opportunity to apply these skills for their own needs.

### Workshop Objectives
1. Raise awareness of content mining among researchers.
2. Train 20-25 researchers in using the ContentMine pipeline tools.
3. Promote legal and responsible content mining practices.

### Anticipated Workshop Outcomes
1. Research or assessment performed using ContentMine tools by a proportion of workshop participants.
2. Production of new journal scraper definitions. 
3. Continuing collaboration with participants and the ContentMine project.
4. One or more ContentMine trainers recruited from pool of participants, increasing the reach of training for content mining.

### Intended Audience

This one day event is intended for researchers or research-related staff who are not currently heavily involved in text and data mining but have at least some pre-existing computational skills. At minimum we expect familiarity with a command line interface. Experienced developers are also extremely welcome. We expect participants to be researchers working in the fields of life science and biomedicine. All our examples and activities will therefore be geared to biological and biomedical sciences. Open Access content in the Europe PMC repository will be the primary source material for this workshop. 


### Training Workshop Agenda
| Times           | Session                 |
| ----            | -------                 |
|10:00      |**Introductions**            |
|10:10      |**What is content mining?** <ul><li>Overview presentation from ContentMine staff</li></ul>|
|10:30      |**Think like a content miner** <ul><li>Hands-on activity facilitated by ContentMine staff introducing entity extraction techniques, precision and recall.</li></ul>|
|11:00      |**Scraping and the anatomy of scrapers** <ul><li>Hands-on activity facilitated by ContentMine staff including use of quickscrape and custom scraper development.</li></ul>|
|12:00      |**Entity recognition using AMI** <ul><li>Hands-on activity facilitated by ContentMine staff  including extracting species names from OA papers using AMI-species.</li></ul>|
|13:00      |**Lunch**|
|13:30      |**Introduction to regular expressions and AMI-regex** <ul><li>Hands-on activity facilitated by ContentMine staff  including regex creation in groups and use of AMI-regex.</li></ul>|
|15:00      |**Legality of content mining: what can I mine?** <ul><li> Presentation and Q&A by ContentMine staff covering copyright, database and contract law. Special attention will be paid to the UK copyright exception </li></ul>|
|15:30      |**Responsible content mining: how should I mine?** <ul><li> Presentation and Q&A by ContentMine staff covering  server limits, online scraping etiquette and responsible technology use.</li></ul>|
|16:00    |**Hackday pitches and forming teams** <ul><li>Presentations by individuals and groups followed by discussion in newly formed teams facilitated by ContentMine staff.</li></ul>|
|18:00 onwards|**Informal social event** <ul><li>Move as a group to nearby pub or late opening cafe to discuss hackday projects.</li></ul>| Reservation confirmed at the Euston Flyer from 18:00 onwards.  

### Workshop Hackday and Policy Panel Session Agenda
| Times           | Session                 |
| ----            | -------                 |
|09:00            |**Hacking in teams**     |
|13:00            |**Lunch**                |
|13:30            |**Hacking in teams**     | 
|15:30            |**Coffee Break**<ul><li>Arrival of policy panel session attendees</ul></li>|
|15:45            |**Introduction to content mining**<ul><li>Presentation delivered by Peter Murray-Rust to new attendeess</ul></li>|
|16:00            |**Presentation of hackday projects**<ul><li>Presentations delivered by participants, including future scope for development of their projects.</ul></li>|
|16:30            | **Panel discussion on accelerating uptake of content mining.**<ul><li>Panel and Q&A with audience including workshop participants.</ul></li>|
|17:30            | **Event close**|

### Documentation

The primary means of communication and taking notes during the workshop will be via this [Etherpad] (http://pads.cottagelabs.com/p/contentmine_wellcometrust2014). 

If you're not familiar with Etherpads, it's easy - you just type! Your writing will show up in a different colour to other people's and you can associate the colour with your name by clicking the person icon in the top right corner of the screen.

### Potential Hackday Projects

Tasks within these projects range from non-technical e.g. putting together a bag of words to retrieve documents related to a certain research area through to technically challenging even for skilled developers. 

1. Find Wellcome Trust funded papers and visualise their associated MeSH heading or other topic indicators in a tag cloud to indicate areas with which Wellcome funding is most associated.
2. Find Wellcome funded Open Access (OA) papers and compare subject set to main tag cloud.
Use document sectioning with ContentMine pipeline to search for mentions of “Wellcome Trust” in acknowledgements section on a daily basis.
3. Find Wellcome funded papers and visualise or summarise by publisher.
4. Build custom scrapers for journals and publishers with which attendees publish.
5. Retrieve documents relate to Wellcome Trust areas of interest using a bag-of-regex system. Compile lists of words and phrases then search cached OA literature or daily RSS feeds from publishers. ContentMine have been experimenting with this system for terms related to Ebola and (in a separate project) agriculture. The results have been very interesting in terms of facts extracted.
6. Co-location of entities (both within document and within sentence).  
  * We can currently extract species and chemistry in standalone modules.
  * The AMI-regex module allows content miners to search for specific terms or relatively easily described patterns e.g. microRNAs, primers.
  * This allows us to pull out co-occurrences of plants and herbivores, chemicals and mosquitoes etc. This feature is not fully functioning but is a development priority.
7. Custom searches using regular expressions module AMI-regex to expand the keyword searches offered by most custom/saved search systems. This is especially poweful if sectioning is offered. Custom prototype would be a challenging project e.g. for EuropePMC or daily output of PLOS.
8. Developing a system for feeding facts from Wellcome funded CC-BY publications into Wikidata and Wikipedia to maximise access. This would likely involve generating a feed which Wikipedia editors can follow and then add facts manually. It could make use of custom searches and co-location.

## Click [here](https://groups.google.com/d/forum/contentmine-workshops) to be advised of future ContentMine Workshops  

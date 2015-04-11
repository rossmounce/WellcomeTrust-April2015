# Extension projects

These are projects which could form the basis of group (or solo) work at the workshops. They are feasible, at least in part and valuable

## Scrapers

### Hindawi

This CC-BY publisher has a large set of journals all created with the same technology and of high quality. Example 
http://www.hindawi.com/journals/ija/2015/426387/ 
from their agronomy journal.

NOTE: The XML is not directly visible so cannot be scraped with `quickscrape` 

``resources needed: about 1-2 hours , using mainstream quickscrape technology``

### Acta Crystallographica

Very high quality (crystallographic) publishing. Acta Cryst E (http://journals.iucr.org/e/ ) is CC-BY. 
Excellent for developing template-based fact extractions.

``resources needed: about 1-2 hours , using mainstream quickscrape technology``

### Repository (OAI) 

It may be useful to scrape OAI repositories or CORE.

``resources needed: familiarity with repo architecture/s and a sense of adventure. May be able to do this through single RESTful apis.``

## AMI plugins

### Licence and metadata

Strong need for this (the Winnower has offered help). Should be possible to start by using `regex` and `identifier` plugins 
without developing code. When the project is scoped we may need a specific plugin - PMR can create a shell. Will need Eclipse/Java developer
but no heavy programming.

``resources needed: Initially a set of regexes and other templates using existing ami-regex and ami-identifier. scrapers for several journals. 1 person with mnowledge of bibliographic metadata and licences will be useful Next step would be hacker comfortable with running Eclipse/maven and developing a simple AMI plugin (PMR will provide a skeleton). PMR will devote time to getting this going. ``

## identifier lookup

We have a prototype to lookup identifiers for resources which have RESTful apis. The ENA/Genbank example works. This could be extended to (say) DOI or ORCID, PDB codes, ATCC, etc. 

``resources needed: familiarity with an identifier system and its remote resource. 1 person familiar with REST will be useful. It may be possible to work with the current lookup system though there will probably be bugs and need for enhancements.``

## named entity lookup

We have prototyped entity lookup in Wikidata (for species). In principle this should work for other objects (e.g. places, diseases)

``resources needed: familiarity with Wikidata or other Wikimedia resources. (PMR can provide some amateur help).``

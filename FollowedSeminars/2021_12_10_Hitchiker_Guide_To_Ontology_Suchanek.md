```
---
event_url: https://www.eurecom.fr/en/seminar/105119
---
```

# 2021 12 10 - A Hitchhiker’s Guide to Ontology - Fabian M. Suchanek

https://suchanek.name/work/publications/desires-2021.pdf

https://sesame.mathnum.inrae.fr/sites/default/files/2019-04/FabianSuchanekPresentation.pdf

## Abstract : 

Knowledge bases are an important asset in many of today's AI-based  applications, including personal assistants and search engines. In this  talk, I will give an overview of our recent work in this area. I will  first talk about our main project, the YAGO knowledge base. In this  context, I will present different methods of information extraction, in  particular also the extraction of beliefs and causal relationships. I  will then talk about the incompleteness of knowledge bases. We have  developed several techniques to estimate how much data is missing in a  knowledge base, as well as rule mining methods to derive that data. I  will then present our work on efficient querying of knowledge bases.  Finally, I will talk about applications of knowledge bases in the domain of computational creativity and the digital humanities, as well as  about our methods for explainable 



AI. Bio : Fabian M. Suchanek is a full professor at the Telecom Paris University  in France. Fabian developed inter alia the YAGO knowledge base, one of  the largest public general-purpose knowledge bases. This earned him a  honorable mention of the SIGMOD dissertation award and the Test of Time  Award of The Web Conference (WWW 2018). His interests include  information extraction, automated reasoning, and knowledge bases. Fabian has published more than 100 scientific articles, among others at ISWC,  VLDB, SIGMOD, WWW, CIKM, ICDE, and SIGIR, and his work has been cited  more than 12,000 times. Data Science Seminars:  https://ds.eurecom.fr/seminars/ https://mediaserver.eurecom.fr/channels/#data-science-seminars  (internal)    

## Carrier path

From a post-doc at Microsoft via Inria research center to Professor Associated at Telecom 

The money-freedom-permanent trade-off

## Little tales of Elvis Presley

Apple Siri / Amazon Echo / IBM Watson -> Based on KB

A KB for query answering / knowledge integration 
Need to be constructed !
About Human handmade KB

The use of Wikipédia, a well known project, with a truth authority. Allready well formated

But : categories given to entity really  chaotic...

So Yago ! 

## Building yago

* At the beginning :
  * A wikipedia categorisation refined with Wordnet for top categories 
* Wikidata : used for fact labeling
  * but a messy taxonomy
* Last yago release :
  * Wikidata + Schema.org + Constraints 

## Yago applications examples

* Commercial products market flow analysis
  * The use of tf-idf for gettings products names
  * The use of the UPC code of the product
* Can be also applied on : books / chemical products / email spam dictionnary...

## KB limitations

things that are not in a KB 
the example of a polemic people who are described only by facts...



## The NORDF project

https://suchanek.name/work/research/nordf/nordf/index.html

* 2020 : Non named entities : the silent majority : about concepts *
* 2021 : The vague expressions (scalar/quanti/subjectives)
* 2021 : Deep learning, but shallow reasoning : on incompletness of facts (not enough examples)
*  The AMIE strategy for prunin
* Incompleteness of entities : using the Benford law and the longtail modelling for finding cities not in KB
* Query and Grep fast search : from SPARQL to algebra. 
  * Optimising the query thanks to alg and transforming it into grep bash scripts
  * not inovative but really efficient 
  * Use case : searching a needle in a haystack
  * https://www.thomasrebele.org/projects/bashlog/
* Correcting KB : Using the wikidata fixes history for dynamic data correcting
  * using conflies log
* Mining rules using transformer
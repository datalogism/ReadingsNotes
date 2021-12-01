# T7 : Tech-taxonomy with a text to text transfer learning

You Zuo & Kim Gerdes

## Quick Summary

* The aim of this work was to try to automate classification of patents in partnership with the Inria start up : qatent.

* The tech taxonomy of the patent are by definition hierarchical, two types of relations are of two types :

  * hyperonym (towards the more general)
  * Hyponym (towards the more specific)

* Their wanted first to extend the patent taxonomy with :

  * Wikidata classification (need to be cleaned)
  * Wordnet 

  But their seems too general, for this reason their also extend it with the CPC classification. Despite this one must be processed because each category is either describe by a list of categories included (easy to process into a tree), but could be also described by a text

  

* Two works where involved : 

  * Hyperonym prediction
    * comparison of models : 
      * The CRIM : learn a projection matrix from a query to hyperonym embedding using fasttext as reprentation (for solving OOV problem)
      * transE : a translating model 
      * hypo2hyper : LSTM model based on seq2seq model with long attention that generate hyperonym path
      * the T5 model : by prefixing input by the keyphrase "predict hyperonym"
    * Metrics : Hits@k score (a measure taking in account the hierarchicallity of the data and the MRR)
  * A term recognizer : using the Span Categorizer + the NER of Spacy and the T5 model

* For next their also think to use the Hearst pattern as relation extractors.

* A good question asked was about the outperformance of the model on others. 

  * The T5 is know as a "universal" model allowing to not be obliged to fine tuning model 
  * BERT wasn't inside the model comparison : is in this case T5 better than a good fine tuning adapted to this downstream task ?

  ## Reflexive part

* By watching this presentation i was allowed to discovering the T5 model that i didn't know. 

* This seminar was the occasion to familiar my self with Hypernyms detection problematic that i already felt by discovering specific work of other DBpedia chapters : [Entityclassifier.eu](https://ner.vse.cz/thd/)  is for example a project developed for extending the DBpedia spotlight by extracting... hyperonyms !

* Another thing is linked to the last DBpedia Spanish chapter presentation, this one was focused on classification improvement of the DBpedia object... This one was based on random forest classifier based on only categorical and numerical variables...  Using this kind of DL model is for sure a good idea for involving for example the abstracts for solving that task

* I allready have to solve in company a kind of hierarchical classification of document (websites in a given taxonomy), but I was totally unaware of the metrics used during the presentation

* Finally the last ongoing projection about the Hearst patterns was for me very interesting , by considering my tiny experience on relation extraction, because the seems to shift from a DL paradigm to a Symbolic fashion one... 
```

---

title: Tuan Lai, Heng Ji, and ChengXiang Zhai. 2022. Improving Candidate Retrieval with Entity Profile Generation for Wikidata Entity Linking. In Findings of the Association for Computational Linguistics: ACL 2022, pages 3696–3711, Dublin, Ireland. Association for Computational Linguistics.

---

``` 

# Knowledge Enhanced Contextual word Representations   

## ABTRACT

 Entity linking (EL) is the task of linking entity mentions in a document to referent entities in a knowledge base (KB). Many previous studies focus on Wikipedia-derived KBs. There is little work on EL over Wikidata, even though it is the most extensive crowdsourced KB. The scale of Wikidata can open up many new real-world applications, but its massive number of entities also makes EL challenging. To effectively narrow down the search space, we propose a novel candidate retrieval paradigm based on entity profiling. Wikidata entities and their textual fields are first indexed into a text search engine (e.g., Elasticsearch). During inference, given a mention and its context, we use a sequence-to-sequence (seq2seq) model to generate the profile of the target entity, which consists of its title and description. We use the profile to query the indexed search engine to retrieve candidate entities. Our approach complements the traditional approach of using a Wikipedia anchor-text dictionary, enabling us to further design a highly effective hybrid method for candidate retrieval. Combined with a simple cross-attention reranker, our complete EL framework achieves state-of-the-art results on three Wikidata-based datasets and strong performance on TACKBP-2010.
 
 ## Context
 
 Massive nb of entities 
 Wikidata > Wikipedia
 Indexed text based model on WIkipedia not possible on other Wikidata entities
 
 ## Solution
 
 Seq2seq generator of profile for a given Wikidata entity > Title + Desc
 
 Framework :
- Dict based approach
- Profiled based 
 + Attention T cross-attention reranker

### 1.  Dict based approach

Mention entity prior probability on Wikipedia 

### 2.  Dict based approach 

As input : Mention + context
To BART + seq2seq
As output : profile with title and desc

> Elastic search query based on severals scores :
* sim (title - alias - text)
* sim( title - alias - generated text)


### 3. Hybrid model

Combine list of candidates with Gradient boosted treee (GBT)
sim : Levenstein - JaroWinkler 
nb of common words (context - alias)
nb of common words mention context - entity name  - alias)


### 4. Reranker

Candidate generated : Ini Rank | [TITLE] | title | [ALIAS] | alias | [DESC] | desc | [CAT] | cat | </s>
Mention : [s] | Left context | [m] | input mention | [/m] | right context | </s>
Transformer reranker 
Score

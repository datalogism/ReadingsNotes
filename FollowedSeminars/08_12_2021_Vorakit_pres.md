# Fine-Grained Classification of Polarized and Propagandist Text in News Articles and Political Debates *(FR: Classification Fine de Textes Polarisés et de Propagande Issus d’Articles d’Actualité et de Débats Politiques)*

**Vorakit Vorakitphan**

## Abstract

In recent years, disinformation has become more viral, mainly due to its spread online on social media, leading to potential threatening  consequences for the society. Heterogeneous forms of online  disinformation are possible, i.e., deliberately manipulated or  fabricated content with the intentional aim of creating conspiracy  theories, rumours, or misbehaved stances and judgements, for instance,  in news articles, and political discourse and debates. One of many  instances of online disinformation, and certainly one of the most  dangerous ones, is propaganda. This disinformation instance represents  an effective but often misleading communication strategy which is  employed to promote a certain viewpoint to the audience, for instance in the political context. The need to effectively and automatically  identify, classify and understand such phenomenon is becoming a urgent  need. In this thesis, I tackle this issue and I propose a fine-grained  classification approach of polarized and propagandist text in news  articles and political debates. More precisely, as the audience’  perceptions are perceived differently depending on the context, the  source of information, the audience background and preferences, a  discussed topic can deviate or polarize the audience into a  partisanship. This thesis firstly investigates such polarization given a use-case in a political scenario using Aspects-Based Sentiment Analysis to verify how extensively these methods can be employed to gain  insights from the political posts on social media. The thesis discusses  the design and evaluation of a number of techniques in extracting the  main features of propagandist text in the area of Natural Language  Processing (NLP) where sentiment analysis, persuasion techniques,  message simplicity, and ultimately argumentation are proposed and  thoroughly investigated. The findings in this thesis show that such  features can capture particular characteristics of propaganda in texts.  Furthermore, these features are employed to tackle the NLP tasks of  propaganda detection and classification through the design and  implementation of a neural architecture to classify fine-grained  propaganda techniques. The work in this thesis goes beyond the  state-of-the-art of current systems for fine-grained propaganda  detection and classification. Various Machine Learning approaches  ranging from feature-based logistic regression to recent neural  architectures have been experimented on standard benchmarks in  propaganda detection. As a result, a full pipeline in propaganda  detection and classification is presented where the task of detecting  the propagandist text snippets obtained .71 F1-score, and the  transformer-based architecture obtained an average of .67 F1-score for  the task of propaganda technique classification, outperforming the  state-of-the-art systems. This pipeline is demonstrated with a  proof-of-concept tool called PROTECT. Finally, as a last contribution of this thesis, I carried out the creation of a new annotated linguistic  resource. This resource is annotated with 6 types of propaganda  techniques, which breaks down into 14 sub-categories of propaganda in  the political debates of the US presidential campaigns from 1960 to  2016. The data set I built contains 1666 instances of propagandist text.

## Background

fake news / virality / harmfull

Misinformation / Desinformation / Malinformation

pandemic -> Infodemic
Level of classification

Propaganda detection : The origin of the post not included in analysis ?

Context polarisation : by polarity / emotion
VAP -> valience / aroussal / dominance

Model use : Elmo/ LSTM/ Sigmoid classif of sentences
Classification of newspaper sources

VAD modelisation

Key-concept and Sub concepts -> How are they selected (by hand)

From polarisation to semantic  argument features

sentence / fragment = span ?

Feature : psychology And linguistic 

	* Historic politics
	* claims / evidence argumentation

Lexicons ?
Argumentation ? Better without ?
BERT model evaluation :

-> classif better just with logistic reg ?!
Ironic detection problems 

Repetition segmentation problems

* Politics / debates conversation 60-2016 debates   12 debates...
  -> Time period problem and few data

  Double layer of annotation
  6cat and 14 sub cats

Links : schopenhauer

Inception tools for annotation : https://inception-project.github.io/
The overlapping spans of anotations
Protect tool : where is it ?

Perspectives :
pb of heteregenous sources

virality indexes

Todorov link ?
Long transformer ? Transphrastique pb 
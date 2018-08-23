
# DEEP learning in bio NLP

### background
Named entity recognition (NER) is an important technique that promises to improve information classification and retrieval in biomedical natural language processing (NLP). However, existing approaches primarily rely on either laborious manual curation or feature engineering. Here we adopt deep learning techniques in NLP and repurpose the vast amount of entity-freetext pairs available in the Sequence Read Archive (SRA) to train a scalable NER model. 


Packages: nltk, spacy, keras, tensorflow

###  jupyter notebooks
Click to go to corresponding jupyter-notebook

|Code| Usage| 
|:--------------:|------:|
|[deep_sra_predict.ipynb](deep_sra_predict.ipynb)|Classify text entity using the trained NER model|
|deep_sra_train.ipynb| Train an entity recognition model using SRA meta data |

Auxilary notebooks that probably not used in manuscripts
|Code| Usage| 
|:--------------:|------:|
|downloadFromPMC.ipynb|download the pubmed text|
|train_pmc_word2vec.ipynb| Train a word2vec model based on pubmed text|
|mergeEntities.ipynb| merge similar entities|
|nGramClassification_batch.ipynb| predict NER based on all possible sentence segments |

### data location 

Please download the data from the following websites:

|Data location| Usage|
|:--------------:|------:|
|https://www.synapse.org/#!Synapse:syn11421651 | all SRS annotations|
| https://www.synapse.org/#!Synapse:syn11421649 | all SRX annotations|
|ftp://ftp.ncbi.nlm.nih.gov/pub/pmc/PMC-ids.csv.gz|PUBMED ID conversions|

### Manuscript
It's still half baked at the moment. Hopefully it be fully baked and yummy in a month. 

* [Manuscript in google doc](https://docs.google.com/document/d/1sbm9L8-OCVZ_qoPqwZyedE5uL4I9k0Hg7znZn6El_l0/edit)

* [Figures in google doc](https://docs.google.com/presentation/d/1ibOSUvBroJp1_zET_pJOAOJ6aGRFVuYSWKJC5h4soKA/edit#slide=id.p)

### dependency
if u have anaconda, install relevant packages using command line: 




```python
[I'm an inline-style link](https://www.google.com)

[I'm an inline-style link with title](https://www.google.com "Google's Homepage")

[I'm a reference-style link][Arbitrary case-insensitive reference text]

[I'm a relative reference to a repository file](../blob/master/LICENSE)

[You can use numbers for reference-style link definitions][1]

Or leave it empty and use the [link text itself].

URLs and URLs in angle brackets will automatically get turned into links. 
http://www.example.com or <http://www.example.com> and sometimes 
example.com (but not on Github, for example).

Some text to show that the reference links can follow later.

[arbitrary case-insensitive reference text]: https://www.mozilla.org
[1]: http://slashdot.org
[link text itself]: http://www.reddit.com

```


```python
!pip install keras gensim  nltk spacy tensorflow

```



### License
This work is under Creative Commons Attribution license. This work is unpublished at the moment. Please attribute this work by citing the github page. 


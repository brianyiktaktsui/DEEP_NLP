
# DEEP learning in bio NLP

### background
Named entity recognition (NER) is an important technique that promises to improve information classification and retrieval in biomedical natural language processing (NLP). However, existing approaches primarily rely on either laborious manual curation or feature engineering. Here we adopt deep learning techniques in NLP and repurpose the vast amount of entity-freetext pairs available in the Sequence Read Archive (SRA) to train a scalable NER model. 


###  jupyter notebooks

|Code| Usage| 
|:--------------:|------:|
|downloadFromPMC.ipynb|download the pubmed text|
|train_pmc_word2vec.ipynb| Train a word2vec model based on pubmed text|
|keras_on_sra_data.ipynb| Train an entity recognition model using SRA meta data |

### data location 

Please download the data from the following websites:

|Data location| Usage|
|:--------------:|------:|
|https://www.synapse.org/#!Synapse:syn11421651 | all SRS annotations|
| https://www.synapse.org/#!Synapse:syn11421649 | all SRX annotations|
|ftp://ftp.ncbi.nlm.nih.gov/pub/pmc/PMC-ids.csv.gz|PUBMED ID conversions|

### dependency
if u have anaconda, install relevant packages using command line: 




```python
!pip install keras gensim  nltk spacy tensorflow

```



### License
This work is under Creative Commons Attribution license. This work is unpublished at the moment. Please attribute this work by citing the github page. 


#### scratch
Please ignore the bottom parts, it's just for my convenience. 


```python
!jupyter nbconvert --to markdown README.ipynb
!git add README.md
!git commit -m "updated: README"
!git push 
```

    [NbConvertApp] Converting notebook README.ipynb to markdown
    [NbConvertApp] Writing 5297 bytes to README.md


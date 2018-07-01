
# DEEP learning in bio NLP

### background
Natural Languague Processing (NLP) used to be one of the most feature engineering intense fields like Computer Vision. 
Deep learning so far has been hugely successful in computer vision undoubtly. 
From my undergrad to phd, I have personally been mind blown by deep learning has transformed the paradigm of vision field. It used to take years of painful feature engineering to gain modest improvements. Now it take only day(s) to write <100 lines of code to yield an accuracy that finds real world applications in days. 

NLP is somewhat undergoing the same transformation. The particular field in consideration in here is biological NLP (bioNLP).
Biological text is complicated and most of the current bio NLP approaches rely on manual feature engineering. For example, in tokenization, synonyms of gene names idealistically can map to the same token, but gene names are inherently getting updated for human over time. 
On of the most successful story in NLP is Google. 

The key characteristic of why Google beat the competition was that the search was curation free.




###  notebooks

|Code| Usage| 
|:--------------:|------:|
|downloadFromPMC.ipynb|download the pubmed text|
|train_pmc_word2vec.ipynb| Train a word2vec model based on pubmed text|
|keras_on_sra_data.ipynb| Train an entity recognition model using SRA meta data |

|Data| Usage|
|:--------------:|------:|
|https://www.synapse.org/#!Synapse:syn11421651 | all SRS annotations|
| https://www.synapse.org/#!Synapse:syn11421649 | all SRX annotations|
|ftp://ftp.ncbi.nlm.nih.gov/pub/pmc/PMC-ids.csv.gz|PUBMED ID conversions|

### depending packages
if u have anaconda, simply: 




```python
!pip install keras gensim  nltk spacy tensorflow

```



### License
This work is under Creative Commons Attribution license. This work is unpublished at the moment. Please attribute this work by citing the github page. 


automatically update the notebook with data

# scratch
Please ignore the bottom parts, it's just for my convenience. 


```python
!jupyter nbconvert --to markdown README.ipynb

```


```python
#!git add README.md
```


```python
!git commit -m "put most files in "
```


```python
!git push 
```

### status 
retraining the word2vec models

training the word2vec using the entire PMC now: 
train_pmc_word2vec.ipynb



```bash
%%bash
cd ./Data/
wget ftp://ftp.ncbi.nlm.nih.gov/pub/pmc/PMC-ids.csv.gz
```


```python
!gunzip -c ./Data/PMC-ids.csv.gz | head
```

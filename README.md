
# DEEP learning in bio NLP

### background
Named entity recognition (NER) is an important technique that promises to improve information classification and retrieval in biomedical natural language processing (NLP). However, existing approaches primarily rely on either laborious manual curation or feature engineering. Here we adopt deep learning techniques in NLP and repurpose the vast amount of entity-freetext pairs available in the Sequence Read Archive (SRA) to train a scalable NER model. 


###  jupyter notebooks

|Code| Usage| 
|:--------------:|------:|
|deep_sra_predict.ipynb|Classify text entity using the trained NER model|
|deep_sra_train.ipynb| Train an entity recognition model using SRA meta data |
|downloadFromPMC.ipynb|download the pubmed text|
|train_pmc_word2vec.ipynb| Train a word2vec model based on pubmed text|


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
    [NbConvertApp] Writing 5133 bytes to README.md
    [master 3cd167e] updated: README
     1 file changed, 59 insertions(+), 7 deletions(-)
    warning: push.default is unset; its implicit value has changed in
    Git 2.0 from 'matching' to 'simple'. To squelch this message
    and maintain the traditional behavior, use:
    
      git config --global push.default matching
    
    To squelch this message and adopt the new behavior now, use:
    
      git config --global push.default simple
    
    When push.default is set to 'matching', git will push local branches
    to the remote branches that already exist with the same name.
    
    Since Git 2.0, Git defaults to the more conservative 'simple'
    behavior, which only pushes the current branch to the corresponding
    remote branch that 'git pull' uses to update the current branch.
    
    See 'git help config' and search for 'push.default' for further information.
    (the 'simple' mode was introduced in Git 1.7.11. Use the similar mode
    'current' instead of 'simple' if you sometimes use older versions of Git)
    
    Counting objects: 3, done.
    Delta compression using up to 96 threads.
    Compressing objects: 100% (3/3), done.
    Writing objects: 100% (3/3), 840 bytes | 0 bytes/s, done.
    Total 3 (delta 2), reused 0 (delta 0)
    remote: Resolving deltas: 100% (2/2), completed with 2 local objects.[K
    To git@github.com:brianyiktaktsui/DEEP_NLP.git
       d6443b7..3cd167e  master -> master



```python
!git mv nGramClassification_simple.ipynb deep_sra_predict.ipynb
```


```python
!git commit -m "file renaming"
!git push 
```

    [master d6443b7] file renaming
     1 file changed, 0 insertions(+), 0 deletions(-)
     rename nGramClassification_simple.ipynb => deep_sra_predict.ipynb (100%)
    warning: push.default is unset; its implicit value has changed in
    Git 2.0 from 'matching' to 'simple'. To squelch this message
    and maintain the traditional behavior, use:
    
      git config --global push.default matching
    
    To squelch this message and adopt the new behavior now, use:
    
      git config --global push.default simple
    
    When push.default is set to 'matching', git will push local branches
    to the remote branches that already exist with the same name.
    
    Since Git 2.0, Git defaults to the more conservative 'simple'
    behavior, which only pushes the current branch to the corresponding
    remote branch that 'git pull' uses to update the current branch.
    
    See 'git help config' and search for 'push.default' for further information.
    (the 'simple' mode was introduced in Git 1.7.11. Use the similar mode
    'current' instead of 'simple' if you sometimes use older versions of Git)
    
    Counting objects: 2, done.
    Delta compression using up to 96 threads.
    Compressing objects: 100% (2/2), done.
    Writing objects: 100% (2/2), 237 bytes | 0 bytes/s, done.
    Total 2 (delta 1), reused 0 (delta 0)
    remote: Resolving deltas: 100% (1/1), completed with 1 local object.[K
    To git@github.com:brianyiktaktsui/DEEP_NLP.git
       d7eb444..d6443b7  master -> master


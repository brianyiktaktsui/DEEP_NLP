
# DEEP learning in bio NLP

### background
Named entity recognition (NER) is an important technique that promises to improve information classification and retrieval in biomedical natural language processing (NLP). However, existing approaches primarily rely on either laborious manual curation or feature engineering. Here we adopt deep learning techniques in NLP and repurpose the vast amount of entity-freetext pairs available in the Sequence Read Archive (SRA) to train a scalable NER model. 


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
if u have anaconda, install relevant packages using command line: 




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

    [NbConvertApp] Converting notebook README.ipynb to markdown
    [NbConvertApp] Writing 2486 bytes to README.md



```python
!ls 
```

    Data			      model
    NCBI_harmonized_names.ipynb   nGramClassification_simple.ipynb
    NCIT_parsing.ipynb	      pmc_word2_vec
    README.ipynb		      pubmed
    README.md		      read_embedding_matrix.ipynb
    Results			      read_word_vector_matrix.ipynb
    Thesaurus.txt		      semantic_count.csv
    Untitled.ipynb		      testPhraseMatcher.ipynb
    Untitled9.ipynb		      tmp.tsv
    analyzeBioNLPEmbedding.ipynb  tmp.txt
    analyzeSRAEntities.ipynb      tmpResults
    downloadFromPMC.ipynb	      tmpResults.xlsx
    downloadPubmed.ipynb	      track_word_count_and_embedding_size.ipynb
    download_wordvectors.ipynb    train_pmc_word2vec.ipynb
    keras_on_sra_data.ipynb       train_pmc_word2vec.py
    keras_on_sra_data_old.ipynb   wikipedia-pubmed-and-PMC-w2v
    merge.pmc		      wikipedia-pubmed-and-PMC-w2v.bin
    mergeEntities.ipynb



```python
#README.ipynb README.md keras_on_sra_data.ipynb
!git add README.md

```


```python
!git commit -m "updated: README"
```

    On branch master
    Your branch is up-to-date with 'origin/master'.
    Changes not staged for commit:
    	[31mmodified:   train_pmc_word2vec.ipynb[m
    
    Untracked files:
    	[31m.ipynb_checkpoints/[m
    	[31mData/[m
    	[31mNCBI_harmonized_names.ipynb[m
    	[31mNCIT_parsing.ipynb[m
    	[31mResults/[m
    	[31mThesaurus.txt[m
    	[31mUntitled.ipynb[m
    	[31mUntitled9.ipynb[m
    	[31manalyzeBioNLPEmbedding.ipynb[m
    	[31manalyzeSRAEntities.ipynb[m
    	[31mdownloadFromPMC.ipynb[m
    	[31mdownloadPubmed.ipynb[m
    	[31mdownload_wordvectors.ipynb[m
    	[31mkeras_on_sra_data_old.ipynb[m
    	[31mmerge.pmc[m
    	[31mmergeEntities.ipynb[m
    	[31mmodel/[m
    	[31mpmc_word2_vec/[m
    	[31mpubmed/[m
    	[31mread_embedding_matrix.ipynb[m
    	[31mread_word_vector_matrix.ipynb[m
    	[31msemantic_count.csv[m
    	[31mtestPhraseMatcher.ipynb[m
    	[31mtmp.tsv[m
    	[31mtmp.txt[m
    	[31mtmpResults.xlsx[m
    	[31mtrack_word_count_and_embedding_size.ipynb[m
    	[31mtrain_pmc_word2vec.py[m
    	[31mwikipedia-pubmed-and-PMC-w2v.bin[m
    	[31mwikipedia-pubmed-and-PMC-w2v/[m
    
    no changes added to commit



```python
!git push 
```

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
    
    Everything up-to-date


### status 
retraining the word2vec models

training the word2vec using the entire PMC now: 
train_pmc_word2vec.ipynb



```bash
%%bash
cd ./Data/
#wget ftp://ftp.ncbi.nlm.nih.gov/pub/pmc/PMC-ids.csv.gz
```


```python
!gunzip -c ./Data/PMC-ids.csv.gz | head
```

    
    
    
    
    
    
    
    
    
    
    
    gzip: stdout: Broken pipe


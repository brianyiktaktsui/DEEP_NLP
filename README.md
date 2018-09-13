
# DEEP learning in bio NLP

### Background
Named entity recognition (NER) is an important technique that promises to improve information classification and retrieval in biomedical natural language processing (NLP). However, existing approaches primarily rely on either laborious manual curation or feature engineering. Here we adopt deep learning techniques in NLP and repurpose the vast amount of entity-freetext pairs available in the BioSample to train a scalable NER model. 

###  Jupyter notebooks

Key notebooks

|Code| Usage| 
|:--------------:|------:|
|[mergeEntities](mergeEntities.ipynb)| Merge all the highly similar BioSample entities using cosine similarities|
|[deep_sra_train_and_test](deep_sra_train.ipynb)| Train an entity recognition model using SRA meta data with entity groupings from [mergeEntities](mergeEntities.ipynb) |
|[deep_sra_predict](deep_sra_predict.ipynb)|Classify text entity using the trained NER model|
|[Parsing and merging of BioSample data](https://github.com/brianyiktaktsui/Skymap#metadata-download-parse-and-merge-sra-meta-data)| --- |

Independent validation

|Code|Usage|
|:--------------:|------:|
| [validationDataGenration.ipynb](validationDataGenration.ipynb) | validation data generation for comparison against curation and Metamap |
|[NER in batch](nGramClassification_batch_vote.ipynb)| predict NER based on all possible sentence segments |
|[scoreAgainstManualCuration_entity_membership](scoreAgainstManualCuration_entity_membership.ipynb)| score against manual curation|

Auxilary notebooks that probably not used or not critical towards understanding of manuscripts

|Code| Usage| 
|:--------------:|------:|
|downloadFromPMC.ipynb|download the pubmed text|
|train_pmc_word2vec.ipynb| Train a word2vec model based on pubmed text, used the pretrained one in the manuscript at the end|
|[uploadToSynapse](./uploadToSynapse.ipynb)||



### Data location 

Please download the data from the following websites:

|File name| Usage|
|:--------------:|------:|
|[allSRS.pickle.gz](https://www.synapse.org/#!Synapse:syn15661259) | all BioSample SRS annotations|
|[word vectors](http://evexdb.org/pmresources/vec-space-models/wikipedia-pubmed-and-PMC-w2v.bin)| Spacy word vector model|
|[meta data](https://www.synapse.org/#!Synapse:syn15661261)| bioSample to Study mapping table |
|[pretrained models](https://www.synapse.org/#!Synapse:syn15661259)| pretrained LSTM and Spacy word models  

|Unused data location| Usage|
|:--------------:|------:|
| https://www.synapse.org/#!Synapse:syn15661258 | all SRX annotations|
|https://www.synapse.org/#!Synapse:syn16805240 |PUBMED ID conversions|


|Manuscript auxilary data| Description | 
|---|---|
|[Machine annotated validation  data](Data/validation_data/validation_prediction_description.1535393121.334881.html) | Example output of deep NER annotations from [NER in batch](nGramClassification_batch_vote.ipynb)|
|[Data curated using dataturk](https://dataturks.com/projects/btsui/Deep%20NLP%20description)| | 


### Manuscript
[Preprint titled "Creating a scalable deep learning based Named Entity Recognition Model for biomedical textual data by repurposing BioSample free-text annotations
" is available at the bioAriv.](https://www.biorxiv.org/content/early/2018/09/12/414136)
### Dependency
If u have anaconda, install relevant packages using following command lines: 
* `conda env create -f environment.yml `
* `source activate deep_nlp_cpu`



### License
This work is under Creative Commons Attribution license. 


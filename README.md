
# DEEP learning in bio NLP

### background
Named entity recognition (NER) is an important technique that promises to improve information classification and retrieval in biomedical natural language processing (NLP). However, existing approaches primarily rely on either laborious manual curation or feature engineering. Here we adopt deep learning techniques in NLP and repurpose the vast amount of entity-freetext pairs available in the BioSample to train a scalable NER model. 

###  jupyter notebooks

**key notebooks**

|Code| Usage| 
|:--------------:|------:|
|[mergeEntities](mergeEntities.ipynb)||
|[deep_sra_train_and_test](deep_sra_train.ipynb)| Train an entity recognition model using SRA meta data |
|[deep_sra_predict](deep_sra_predict.ipynb)|Classify text entity using the trained NER model|

Independent validation

|Code|Usage|
|:--------------:|------:|
| [validationDataGenration.ipynb](validationDataGenration.ipynb) | validation data |
|[NER in batch](nGramClassification_batch_vote.ipynb)| predict NER based on all possible sentence segments |

Auxilary notebooks that probably not used in manuscripts

|Code| Usage| 
|:--------------:|------:|
|downloadFromPMC.ipynb|download the pubmed text|
|train_pmc_word2vec.ipynb| Train a word2vec model based on pubmed text|
|mergeEntities.ipynb| merge similar entities|
|[scoreAgainstManualCuration_entity_membership](scoreAgainstManualCuration_entity_membership.ipynb)| score against manual curation|
[Parsing and merging of SRA data](https://github.com/brianyiktaktsui/Skymap#download-parse-and-merge-sra-meta-data)

### data location 

Please download the data from the following websites:

|Data location| Usage|
|:--------------:|------:|
|https://www.synapse.org/#!Synapse:syn11421651 | all SRS annotations|
| https://www.synapse.org/#!Synapse:syn11421649 | all SRX annotations|
|ftp://ftp.ncbi.nlm.nih.gov/pub/pmc/PMC-ids.csv.gz|PUBMED ID conversions|

[Machine annotated validation  data](Data/validation_data/validation_prediction_description.1535393121.334881.html)
### Manuscript

### dependency
if u have anaconda, install relevant packages using following command lines: 
* `conda env create -f environment.yml `
* `source activate deep_nlp_cpu`



### License
This work is under Creative Commons Attribution license. This work is unpublished at the moment. Please attribute this work by citing the github page. 


# Tracking Progress in Rich Context

[The Coleridge Initiative](https://coleridgeinitiative.org/richcontext) 
at NYU has been researching [*Rich Context*](https://coleridgeinitiative.org/richcontext)
to enhance search and discovery of datasets used in scientific research – see the 
[_Background Info_](https://github.com/Coleridge-Initiative/rclc/wiki/Background-Info) 
section for more details.
Partnering with experts throughout academia and industry, NYU-CI has
worked to leverage the closely adjacent fields of NLP/NLU, knowledge
graph, recommender systems, scholarly infrastructure, data mining from
scientific literature, dataset discovery, linked data, open vocabularies,
metadata management, data governance, and so on.
Leaderboards are published here on GitHub to track _state-of-the-art_ 
(SOTA) progress among the top results.

---

## Leaderboard 1

### Entity Linking for Datasets in Publications

The first challenge is to identify the datasets used in research
publications, initially focused on the problem of 
[_entity linking_](https://nlpprogress.com/english/entity_linking.html).
Research papers generally mention the datasets they've used, although there
are limited formal means to describe that metadata in a machine-readable way.
The goal here is to predict a set of dataset IDs for each publication.
The dataset IDs within the corpus represent the set of all possible datasets
which will appear.

Identifying dataset mentions typically requires:

  * extracting text from an open access PDF
  * some NLP parsing of the text
  * feature engineering (e.g., attention to where text is located in a paper)
  * modeling to identify up to 5 datasets per publication

See [_Evaluating Models for Entity Linking with Datasets_](https://github.com/Coleridge-Initiative/rclc/wiki/Evaluating-Models-for-Entity-Linking-with-Datasets)
for details about how the `Top5uptoD` leaderboard metric is calculated.

### Current SOTA

|  source | precision | entry | code | paper | corpus | submitted | notes | 
| ------------- | :-----:| :----: | :----: | :----: | :----: | :----: | --- |
| [LARC](https://github.com/LARC-CMU-SMU) [@philipskokoh](https://github.com/philipskokoh) | 0.7836 | [ipynb](https://github.com/LARC-CMU-SMU/rclc_2019_baseline/blob/master/src/rclc_2019_entity_indicative_naive_bayes_baseline.ipynb) | [repo]( https://github.com/LARC-CMU-SMU/rclc_2019_baseline) | [RCC_1](https://github.com/LARC-CMU-SMU/coleridge-rich-context-larc) | [v0.1.5](https://github.com/Coleridge-Initiative/rclc/releases/tag/v0.1.5) | 2019-09-26 | RCLC baseline experiment using RCC_1 approach |
| [KAIST](https://www.kaist.ac.kr/html/en/index.html) [@HaritzPuerto](https://github.com/HaritzPuerto) | 0.6319 | [ipynb](https://github.com/HaritzPuerto/rclc_2019_baseline/blob/master/project/RCLC.ipynb) | [repo](https://github.com/HaritzPuerto/rclc_2019_baseline) | [RCC_1](https://coleridgeinitiative.org/assets/docs/RCC/kaist.pptx) | [v0.1.5](https://github.com/Coleridge-Initiative/rclc/releases/tag/v0.1.5) | 2019-11-01 | model trained a different dataset using [DocumentQA](https://github.com/allenai/document-qa) and [Ultra-Fine Entity Typing](https://github.com/uwnlp/open_type) -- NB: this approach is able to identify new datasets |

---

## Instructions

  * [How To Participate](https://github.com/Coleridge-Initiative/rclc/wiki/How-To-Participate)
  * [Corpus Description](https://github.com/Coleridge-Initiative/rclc/wiki/Corpus-Description)
  * [Download Resource Files](https://github.com/Coleridge-Initiative/rclc/wiki/Downloading-Resource-Files)
  * [Background Info](https://github.com/Coleridge-Initiative/rclc/wiki/Background-Info)
  * [Workflow Stages](https://github.com/Coleridge-Initiative/rclc/wiki/Workflow-Stages)
  * [Glossary Terms](https://github.com/Coleridge-Initiative/rclc/wiki/Glossary-Terms)

Use of open source and open standards are especially important to
further the cause for effective, reproducible research. 
We're hosting this competition to focus on the research challenges
of specific machine learning use cases encountered within Rich Context – see the 
[_Workflow Stages_](https://github.com/Coleridge-Initiative/rclc/wiki/Workflow-Stages)
section. 

If you have any questions about the Rich Context leaderboard 
competition – and especially if you identify any problems in the 
corpus (e.g., data quality, incorrect metadata, broken links, etc.) – 
please use the GitHub issues for this repo and pull requests to 
report, discuss, and resolve them.

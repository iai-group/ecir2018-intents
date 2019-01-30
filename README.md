# Towards an Understanding of Entity-Oriented Search Intents

This repository provides resources developed within the following article:

> D. Garigliotti and K. Balog. Towards an Understanding of Entity-Oriented Search Intents. In Advances in Information Retrieval - Proceedings of the 40th European Conference on Information Retrieval (ECIR '18), Grenoble, France. Springer. March 2018. [DOI: 10.1007/978-3-319-76941-7_57](https://link.springer.com/chapter/10.1007/978-3-319-76941-7_57)

**You can get the author version of the article [here](https://arxiv.org/abs/1802.08010).**

### Abstract

> *Entity-oriented search deals with a wide variety of information needs, from displaying direct answers to interacting with services. In this work, we aim to understand what are prominent entity-oriented search intents and how they can be fulfilled. We develop a scheme of entity intent categories, and use them to annotate a sample of queries. Specifically, we annotate unique query refiners on the level of entity types. We observe that, on average, over half of those refiners seek to interact with a service, while over a quarter of the refiners search for information that may be looked up in a knowledge base.* 


## Collection of categorized type-level refiners

In `annotation_output/refiners_categorization.tsv`, we provide the output of our annotation experiment conducted by crowdsourcing (details in the paper): a large collection of type-level refiners, annotated with intent categories.

  - Each row of the TSV file corresponds to a (`[type]`, `refiner`) pair (stored in the 1st and 2nd columns, resp.), which an intent category is assigned to (3rd column) by majority agreement.
  - The confidence score of a row (4th column) is calculated simply as the number of judgments for that category normalized by the total of annotations for its pair. As detailed in the paper, each instance was annotated by at least 3 judges (5 at most, if necessary to reach a majority agreement, using dynamic judgments). For each type, we only retain an annotated refiner if at least three annotators agreed on the majority category.

Below, an excerpt of this annotation output:

```
Type	Intent	Top_judged_category	Judgment_rate_(confidence)
[airport]	official website	website	1.0
[airport]	facebook	website	1.0
[airport]	weather	service	1.0
[airport]	to train station	service	1.0
[airport]	zip code	property	1.0
[airport]	logo	property	1.0
[airport]	china	other	0.75
[airport]	crash	other	0.6
...
```

## Crowdsourcing experiment

We used crowdsourcing to annotate type-level refiners with intent categories. 

  - For each annotation instance we displayed workers with the query, indicating its entity type and refiner, and asked them to select one of the four intent categories (details in the paper).

Below, screenshots of the annotation job on Crowdflower.

![Experiment Layout 1-4](https://github.com/iai-group/ecir2018-intents/blob/master/images/exp_layout_1-4.png)
![Experiment Layout 2-4](https://github.com/iai-group/ecir2018-intents/blob/master/images/exp_layout_2-4.png)
![Experiment Layout 3-4](https://github.com/iai-group/ecir2018-intents/blob/master/images/exp_layout_3-4.png)
![Experiment Layout 4-4](https://github.com/iai-group/ecir2018-intents/blob/master/images/exp_layout_4-4.png)


## Citation

If you use the resources presented in this repository, please cite:

```
@InProceedings{Garigliotti:2018:TAU,
 author =     {Garigliotti, Dar{\'i}o
   and Balog, Krisztian},
 title =      {Towards an Understanding of Entity-Oriented Search Intents},
 booktitle =  {Advances in Information Retrieval - Proceedings of the 40th European Conference on IR Research},
 series =     {ECIR '18},
 year =       {2018},
 pages =      {644--650},
 publisher =  {Springer},
 doi =        {10.1007/978-3-319-76941-7_57},
}
```


## Contact

Should you have any questions, please contact Darío Garigliotti at dario.garigliotti[AT]uis.no (with [AT] replaced by @).

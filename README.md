# Towards an Understanding of Entity-Oriented Search Intents

This repository provides resources developed within the following paper:

> D. Garigliotti and K. Balog. Towards an Understanding of Entity-Oriented Search Intents. In ECIR'18, March 2018.

These resources allow to reproduce the results presented in the paper.


## Annotated sample of type-level refiners

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

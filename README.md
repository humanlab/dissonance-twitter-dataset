# Dissonance Twitter Dataset
Dataset collected from annotating tweets for within-person dissonance, as described the paper [Transfer and Active Learning for Dissonance Detection: Addressing the Rare Class Challenge](https://arxiv.org/abs/2305.02459). 

The annotators used the following flowchart as a guide: 
![annotation guidelines](./annotation_format/Annotation_Guidelines.jpg)

Tweets were parsed into discourse units, and marked as Belief (Thought or Action) or Other, and pairs of beliefs within the same tweet were relayed to annotators for Dissonance annotation.
![annotation process](./annotation_format/annotation_process.jpg)



## The data in this repository is organized as follows:

* `train_small.json`: Small train set as described in Section 4.4 of the paper, containing 2924 examples (6.29% dissonance)
* `train_big.json`: Big train set as described in Section 4.4 of the paper, containing 6649 examples (10.40% dissonance)
* `dev.json`: The final development set as described in Section 3.1, containing 1484 examples (10.24% dissonance)
* `test.json`: The final test set as described in Section 3.1, containing 1456 examples (10.30% dissonance)


## Data Format:

* Each example has a unique id.
* The message attribute contains the entire message so that it provides the context of the belief units.
* The two belief discourse units are recorded for each message in the fields "du1" and "du2" respectively.
* The discourse units in a "message" are marked using angled brackets "<" and ">".
* Each example is labelled with C (Consonance), D (Dissonance) and N (Neither/Other).


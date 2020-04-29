# [WIP] ud120 Projects 2.0

The aim of this repo is to improve original starter project code for students taking
[Intro to Machine Learning](https://classroom.udacity.com/courses/ud120) on Udacity with
python 3.8, conda managing and jupyter notebooks


## Mini-Projects

- [Lesson 2: Naive Bayes Mini-Project](./lesson-2-naive-bayes/nb_author_id.ipynb)
- [Lesson 3: SVM Mini-Project](./lesson-3-svm/svm_author_id.ipynb)
- [Lesson 4: Decision Trees Mini-Project](./lesson-4-decision-tree/dt_author_id.ipynb)
- [Lesson 5: Choose Your own Algorithm Mini Project](./lesson-5-choose-your-own/your_algorithm.ipynb)
- [Lesson 6: Datasets and Questions Mini-Project](./lesson-6-datasets-questions/explore_enron_data.ipynb)
- [Lesson 7: Regressions Mini-Project](./lesson-7-regression/finance_regression.ipynb)


## Important Notes

### Lesson 3: SVM

In this repo newer version of `scikit-learn` is used. Thus, to get the results expected by the course grader
you need to use `SVC` with `gamma='auto'`, since the default value of gamma changed, see `sklearn.svm.SVC` [docs](https://scikit-learn.org/stable/modules/generated/sklearn.svm.SVC.html):
> Changed in version 0.22: The default value of gamma changed from 'auto' to 'scale'.

For example:

```python
clf = SVC(kernel='linear', gamma='auto')
```

### Lesson 7: Regressions

To get the correct (acceptable by grader) results set `sort_keys='../utils/python2_lesson06_keys.pkl'` for
`feature_format` function. See [this](https://classroom.udacity.com/courses/ud120/lessons/2301748537/concepts/30416086000923)
for detailed explanation:

> [...] This will open up a file in the tools folder with the Python 2 key order.


## Initial Setup

### Clone the repo

```bash
$ git clone https://github.com/trsvchn/ud120-projects-v2.git
$ cd ud120-projects-v2
```

### Set up conda environment

#### Download and install anaconda

[link](https://www.anaconda.com/distribution/)

#### Create environment

```bash
$ conda env create -f environment.yml
```

#### Activate environment via

```bash
$ conda activate ud120
```

### Run starter script to check env and download required data

```bash
$ python ./utils/starter.py
```

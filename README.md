# Japanese Text-Emoticon Data

## Introduction
Japanese text-emoticon data is a dataset of Japanese messages, each including one emoticon. This repository contains training and test data used in [1].

If you use this dataset in your work, please cite our paper:

```
@article{URABE2021102414,
title = {Find right countenance for your input—Improving automatic emoticon recommendation system with distributed representations},
journal = {Information Processing & Management},
volume = {58},
number = {1},
pages = {102414},
year = {2021},
issn = {0306-4573},
doi = {https://doi.org/10.1016/j.ipm.2020.102414},
url = {https://www.sciencedirect.com/science/article/pii/S0306457320309092},
author = {Yuki Urabe and Rafal Rzepka and Kenji Araki},
}
```

## Dataset
- train_20210126.pkl
Training data contains 124,359 sets of message-emoticon.
- test_20210126.pkl
Training data contains 37,622 sets of message-emoticon.

The datasets are comprised of "text", "emoticon", "textEmotion", "textPolarity", "emoEmotion", and "emoPolarity".
- text: Japanese message
- emoticon: an emoticon which was inserted after the message
- textEmotion: emotion type of the emotional expression in a message (if exists). The values contained in this column are, "joy (喜)", "like (好)", "relief (安)", "anger (怒)", "dislike (厭)", "fear (恐)", "sad (哀)", "amaze (驚)", "shy (恥)", "excite (昂)", and "None (無)".
- textPolarity: polarity type of the emotional expression in a message (if exists). The values contained in this column are, "positive (ポジティブ)", "negative (ネガティブ", "others (その他)", and "None (無)".
- emoEmotion: emotion type of the emoticon.
- emoPolarity: polarity type of the emoticon.


## How to load data
Environment
- Python (> 3.6)
- Pandas (1.2.3)

```python
import pandas as pd
df = pd.read_pickle('train_20210126.pkl')
```

See Example.ipynb for details.

## Licenses
The dataset is distributed under the terms of the Creative Commons Attribution-ShareAlike 3.0.

## Reference
[1] Y. Urabe, R. Rafal, and K. Araki: Find right countenance for your input—Improving automatic emoticon recommendation system with distributed representations, Information Processing & Management, Volume 58, Issue 1, 2021, https://www.sciencedirect.com/science/article/pii/S0306457320309092

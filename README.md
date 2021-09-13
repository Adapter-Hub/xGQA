# xGQA
This reporistory contains the test-dev data of the paper ["xGQA: Cross-lingual Visual Question Answering"](https://arxiv.org/).

## Overview
The repository is structured as follows:
- **`data/zero_shot/`** contains the xGQA test-dev files for all 8 languages
- **`data/few_shot/`** contains the new standard splits for few shot learning. The number in the file name indicates how many distinct images the split includes. i.e. `train_10.json` implies that this subset contains questions about 10 distinct images.

## Zero-Shot Results
Zero-shot transfer results on xGQA when transferring from English GQA. Average accuracy is reported. Mean scores are not averaged over
the source language (English).
| model     | en    | de    | pt    | ru    | id    | bn    | ko    | zh    | mean |
|-----------|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
| M3P       | 58.43 | 23.93 | 24.37 | 20.37 | 22.57 | 15.83 | 16.90 | 18.60 | 20.37|
| OSCAR+Emb | 62.23 | 17.35 | 19.25 | 10.52 | 18.26 | 14.93 | 17.10 | 16.41 | 16.26|
| OSCAR+Ada | 60.30 | 18.91 | 27.02 | 17.50 | 18.77 | 15.42 | 15.28 | 14.96 | 18.27|
| mBERTAda  | 56.25 | 29.76 | 30.37 | 24.42 | 19.15 | 15.12 | 19.09 | 24.86 | 23.25|

## Few-Shot
Few-shot dataset sizes. The GQA test-dev set is split into new development, test sets, and training splits of different sizes. We maintain the distribution of structural types in each split.
| Set        | Test |  Dev | Train |     |     |     |     |      |
|------------|:----:|:----:|:-----:|-----|-----|-----|-----|------|
| #Images    |  300 |   50 |     1 |  5  |  10 |  20 |  25 |   48 |
| #Questions | 9666 | 1422 |    27 | 155 | 317 | 594 | 704 | 1490 |

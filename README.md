# slogan-generation-dataset
Slogan Generation Evaluation Datasets used in the following paper:

> Jin, Yiping, Akshay Bhatia, Dittaya Wanvarie, and Phu TV Le. "Toward Improving Coherence and Diversity of Slogan Generation". Accepted to *Natural Language Engineering*. Cambridge University Press.

[Download paper here](https://yipingnus.github.io/publication/2021-12-13-paper-title-number-7) (as allowed by Cambridge University Press self-archiving policy)

This repo contains a rule-based filtered validation dataset of 5k `<description, slogan>` pairs and a manually curated test dataset of 1k pairs. The dataset construction procedure is described in the Dataset section of the paper. 

## What's in the repo?

1. The validation and test data used in the paper (`valid.csv` and `test-curated.csv`). Note that they're used in the revised manuscript, which I'll update by end September 2021 to Arxiv. The `desc` and `output` columns are the input descriptions and slogans (delexicalized). If you want to lexicalize the input description, you can replace the mask token with the Alias or the company name. 
2. V1 dataset under `/v1` folder. They're deprecated and contain some noise and redundant information. 
3. Diversity human evaluation under the `diversity_eval` folder. Used in Section 7.4 of the revised paper. I also include the notebook to analyze the annotation result.
4. Main human evaluation under the `human_eval` folder. Used in Section 7.5 of the revised paper. I also include the notebook to ana
lyze the annotation result.

## What's not included?

1. **The slogan generation model.** It's being used in a commercial system and I regret I can't share the model publicly.
2. **The full training dataset.** It's relatively simple for you to recrawl the full Kaggle 7M+ dataset. However, it took me over a month on a low-spec cloud instance.

If you use the dataset for your research work, please cite the following manuscript:

```
@article{jin2021generating,
      title={Toward Improving Coherence and Diversity of Slogan Generation}, 
      author={Yiping Jin and Akshay Bhatia and Dittaya Wanvarie and Phu T. V. Le},
      journal={Natural Language Engineering},
      pages={1--33},
      year={In press},
      note={Cambridge University Press}
}
```

If you have any question regarding the dataset or the manuscript, please drop an email to me or create an issue.

# WikiHow-Dataset
WikiHow: A Large Scale Text Summarization Dataset

WikiHow is a new large-scale dataset using the online WikiHow (http://www.wikihow.com/) knowledge base. The dataset is introduced in https://arxiv.org/abs/1810.09305. Please refer to the paper for more information regarding the dataset and its properties.

Each article consists of multiple paragraphs and each paragraph starts with a sentence summarizing it. By merging the paragraphs to form the article and the paragraph outlines to form the summary, the resulting version of the dataset contains more than 200,000 long-sequence pairs.

There are two separate data files containing the articles and their summaries:

The wikihowAll.csv file consisting of the concatenation of all paragraphs as the articles and the bold lines as the reference summaries.:

|Part|Description|
|-------|-------------|
|Title|the title of the article as it appears on the WikiHow knowledge base|
|Headline|the concatenation of all the bold lines (the summary sentences) of all the paragraphs to serve as the reference summary|
|Text|the concatenation of all paragraphs (except the bold lines) to generate the article to be summarized|

The data can be downloaded from the link below:

https://ucsb.box.com/s/ap23l8gafpezf4tq3wapr6u8241zz358


The wikihowSep.csv file consisting of each paragraph and its summary:

|Part|Description|
|-------|-------------|
|Title|the title of the article as it appears on the WikiHow knowledge base|
|Overview|the introduction section of the WikiHow articles represented before the paragraphs corresponding to procedures|
|Headline|the bold line (the summary sentence) of the paragraph to serve as the reference summary|
|Text|the paragraph (except the bold line) to generate the article to be summarized|

This file contains separate paragraphs as the articles and the bold lines corresponding to each paragraph as the reference summary. The data can be downloaded from the link below:

https://ucsb.box.com/s/7yq601ijl1lzvlfu4rjdbbxforzd2oag

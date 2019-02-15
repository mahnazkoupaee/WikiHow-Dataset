# WikiHow-Dataset
WikiHow: A Large Scale Text Summarization Dataset

WikiHow is a new large-scale dataset using the online WikiHow (http://www.wikihow.com/) knowledge base <sup>[*](#footnote1)</sup>. The dataset is introduced in https://arxiv.org/abs/1810.09305. Please refer to the paper for more information regarding the dataset and its properties.

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





<a name="footnote1">*</a>: The articles are provided by wikiHow, a wiki building the world's largest, highest quality how-to manual. Content on wikiHow can be shared under a [Creative Commons License](https://creativecommons.org/licenses/by-nc-sa/3.0/) (CC-BY-NC-SA).


# Data Processing
To process the csv file and create the article files, use process.py. After running this code, you will have a directory of files, each containing an article and its summary sentences. 

The titles.txt file contains the name of all articles in the dataset. Three separate files (all_train, all_val, all_test) contain the titles of the articles used as train/dev/test sets to generate results in the paper. (the titles are derived from the "title" column by extracting and concatenating the alphanumeric values)

Note that the articles are added regularly to the wikihow knowledge base. Therefore, there might be new articles in the csv file which are not in the titles file.

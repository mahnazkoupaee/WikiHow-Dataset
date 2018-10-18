# WikiHow-Dataset
A Large Scale Text Summarization Dataset

WikiHow is a new large-scale dataset using the online WikiHow (http://www.wikihow.com/) knowledge base. Each article consists of multiple paragraphs and each paragraph starts with a sentence summarizing it. By merging the paragraphs to form the article and the paragraph outlines to form the summary, the resulting version of the dataset contains more than 200,000 long-sequence pairs.

The data file is one .csv file consisting of three main parts:

|Part|Description|
|-------|-------------|
|Title|the title of the article as it appears on the WikiHow knowledge base|
|Headline|the concatenation of all the bold lines (the summary sentences) of all the paragraphs serving as the reference summary|
|Text|the conctenation of all paragraphs (except the bold lines) to generate the article to be summarized|

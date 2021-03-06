# CC-100 Dataset

This is the dataset used to train XLM-R. These numbers come from Appendix A (Table 6)
of the [XLM-R paper](https://arxiv.org/abs/1911.02116). The data was created using
CommonCrawl snapshots from January-December 2018.

It's not clear whether the token counts in this CSV file refer to whitespace-delineated words,
or to byte-pair encoded tokens. If you know the answer, please let me know!

See also [http://data.statmt.org/cc-100/](http://data.statmt.org/cc-100/), which bills itself
as an "attempt to recreate the data used in XLM-R", which suggests it may not match exactly. Note that
the file sizes listed on that website report _compressed_ file size, but the numbers
in this csv file report _uncompressed_ file size.

I compared token counts from the CSV file against word counts (using `wc -w`) in the raw
untokenized text files from the website. The numbers are very similar for 2/3 languages,
but this doesn't necessarily mean this was the method for counting tokens in the
paper. 

| Language | Compressed size | Uncompressed Size | Words (wc -w) | Tokens (from table) |
|----------|-----------------|-------------------|---------------|---------------------|
| ug       | 46M             | 377M              |    32,359,813 | 27M                 |
| xh       | 25M             | 111M              |    13,465,828 | 13M                 |
| sw       | 332M            | 1.6G              |   275,281,887 | 275M                |


![Graph of token counts](cc-100.png)
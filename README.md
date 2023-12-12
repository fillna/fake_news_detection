# fake_news_detection

Description of `politicfact_plus.csv`:
=====================================================================
Initially scraped from POLITIFACT.com by Zhixing(Sean) Jiang, have the additional source record inforamtion added by Jun Linwu.

Column 1: the source. <br />
Column 2: the context, when or where. <br />
Column 3: the headline. <br />
Column 4: the label/target. <br />
Column 5: the speaker/author. <br />
Column 6: the documented time. <br />
Column 7: the author's score record. <br />
Column 8: the summary/highlight of the article. <br />
Column 9: the article text. <br />
Column 10-15: the source's score counts. <br />


Description of [Liar Liar Dataset](https://arxiv.org/pdf/1705.00648.pdf): <br />
=====================================================================
Introduced by William Yang, Wang in his paper about “Liar, liar pants on fire.” This is a publicly available dataset made for fake new detection. Overall dataset is about 12.8k and manually labeled with the scrape content from POLITIFACT.com. We used this dataset and combined it with scraped new Politifact data from Jun to do a multiclass bias classification. We will also be using the combined dataset to do some textual analysis such as sentimental analysis. Such a dataset mainly contains a statement of the speaker, the name of the speaker, the context of this statement, and the label. Detail description below:

Column 1: the ID of the statement ([ID].json).<br />
Column 2: the label.<br />
Column 3: the statement.<br />
Column 4: the subject(s).<br />
Column 5: the speaker.<br />
Column 6: the speaker's job title.<br />
Column 7: the state info.<br />
Column 8: the party affiliation.<br />
Columns 9-13: the total credit history count, including the current statement.<br />
  9: barely true counts.<br />
  10: false counts.<br />
  11: half true counts.<br />
  12: mostly true counts.<br />
  13: pants on fire counts.<br />
Column 14: the context (venue / location of the speech or statement).<br />


Description of [Liar Liar Plus Dataset](https://github.com/Tariq60/LIAR-PLUS): <br />
=====================================================================
Created by Alhindi, Petridis and Muresan. This dataset has evidence sentences extracted automatically from the full-text verdict report written by journalists in Politifact. 

Column 1-14: same as the Liar Liar Dataset. <br />
**Column 15: the extracted justification** <br />


Notebook Usage:
=====================================================================
`scrape.ipynb`: to scrape POLITIFACT.com. <br />
`clickbait.ipynb` / `clickbait.py`: train / evaluate / output the clickbait model. <br />
`sentiment.ipynb` / `sentiment.py`: train / evaluate / output the sentiment model. <br />

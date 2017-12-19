## CHI 2018 - Crisis News Sympathy: `datasets`, `queries`, `crowdworker instructions`

Supplementary material (datasets, queries, crowdworker instructions) for the CHI 2018 paper **"Measuring, Understanding, and Classifying News Media Sympathy on Twitter after Crisis Events"**

*Preprint / DOI coming soon!*

___

**A.chi2018_dataset.csv:** Our final annotated, multi-language (English, Arabic, French, German) dataset (N=2,390). Fields include:

```
 $ id_str         : char : tweet ID. N=2390
 $ dataset        : char : Western media coverage of Paris Attacks (FR_western), Arab media coverage of Paris Attacks (FR_arab), Western media coverage of Beirut Attacks (LB_western), Arab media coverage of Beirut Attacks (LB_arab). N=4
 $ country        : char : country and query used ('_en' denotes English, and 'na_' denotes native language). N=15
 $ lang           : char : which language was identified using langid.py (EN, FR, AR, DE). N=4
 $ lang_norm_prob : num  : normalized probability of language identified
 $ na             : char : whether the tweet was rated as 'Not Applicable'
 $ na_conf        : int  : confidence of tweet rated as NA
 $ sentiment      : int  : overall sentiment label (-1, 0, 1)
 $ sentiment_conf : num  : confidence of sentiment label
 $ sympathy       : int  : overall sympathy label (-1, 1)
 $ sympathy_conf  : num  : confidence of sentiment label
 ```

**B.chi2018_news_queries.pdf** : Contains a table that shows: (1) full set of queries (in English and native language) used to crawl Twitter user accounts (2) the total number of Twitter news accounts found (3) the amount and percentage found in each dataset (Beirut, Paris).

**C.chi2018_news_org_summary.csv** : The final list of unique crawled news organizations (N=208). For ethical concerns, we only show the name, user name, the country / query used to retrieve the account, the follower count at the time of crawling, the number of tweets, and our mean and standard deviation scores of crowdsourced labels.

 ```
 $ user_name        : char : Twitter user name
 $ user_screen_name : char : Twitter user screen name
 $ user_description : char : Twitter user description
 $ country/query    : char : country and query used to retrieve this ('_en' denotes English, and 'na_' denotes native language)
 $ follower_count   : num  : User follower count
 $ tweet_count      : num  : Number of tweets tweeted by this account
 $ sentiment_mean   : num  : Mean sentiment score for all tweets by this account
 $ sentiment_sd     : num  : Standard deviation of sentiment score for all tweets by this account
 $ sympathy_mean    : num  : Mean sympathy score for all tweets by this account
 $ sympathy_sd      : num  : Standard deviation of sympathyscore for all tweets by this account
```
**D.chi2018_cf_instructions.pdf:** Crowdsourcing annotation task instructions given to crowdworkers. Translated from English by native (bilingual) speakers into French, Arabic, and German.

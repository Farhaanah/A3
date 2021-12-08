# A3
Document 1- Overview 

The following report details the development of a WebCrawler and two NLP systems that interrogate 500 twitter posts from 26 November 2021, 
when Technical Advisory Group on SARS-CoV-2 Virus Evolution (TAG-VE) convened to assess the virus’ combinations, mutations, and behaviours, 
and publicly classified the Omicron variant- a variant of concern (WHO, 2021). The WebCrawler extracted 500 posts directly from Twitter, a 
social media site with a primary purpose to connect its users, allowing them to share their thoughts with their online network (Forsey, 2021). 

The development of this WebCrawler was to crawl through Twitter to webscrape the keyword ‘coronavirus’ from 26 November 2021. Twitter is part of 
a smaller pool of sites that allows users to legally webscrape it’s sites and collect specific data variables that it allows to be collected, 
with a limitation on how much data can be collected at a time. 
After the collection of data via the WebCrawler, data was pre-processed and two NLP systems were developed for Sentiment Analysis and Topic 
Modelling, respectively. Pre-processing of the Twitter text data involved removing links, mentions and hashtags, tokenized words, removed stop words, 
lemmatized words, removed any non-alpha characters and restricted keeping any words that were greater than two characters using a function adapted 
from Hasdemir, 2020.

The clean data was then used to perform a Sentiment Analysis with VADER (Valence Aware Dictionary for sEntiment Reasoning). VADER is considered a 
fast sentiment, lexicon, rule-based classifier (Singh, 2021). It is a recommended analytical tool for social media texts, indicating the extent to 
which a text is positive or negative, also determining neutral texts, analysing the words present in the given text and categorizing them. The positive 
and negative classified Twitter posts were then used with a Bernoulli Naïve Bayes model classifier to fit the data and assess the classification of 
predictions of future Twitter posts. 

The final NLP task investigated word frequency within the Twitter texts, with specific interest in negative Twitter posts, as these were expectedly 
higher than positive Twitter posts. The 30 most common words were chosen, and a word cloud formulated to visualize their presence in the text. 
These words were used to build an LDA (Latent Dirichlet Allocation) Topic Model, an unsupervised classification approach to cluster similar terms 
and therefore overarching topics that prevail from the 30 most common words from the Twitter texts. 
The full code can be found in this Git-Hub repository.

The goal of the overall outcome was to develop approaches that can assist in the surveillance of social media sentiment and cluster social media 
posts for overall opinion mining. The foundation of this goal was achieved, as the beginning of a solution to be built-on and improved by a larger 
project deployment team that could be used to assist in governance and overall public health strategies in an age where both the infodemic and the 
COVID-19 pandemic are so threatening. 


References :
VentureBeat. (2021). Why unstructured data is the future of data management. https://venturebeat.com/2021/07/22/why-unstructured-data-is-the-future-of-data-management/
Vorhaus, M. (2020). People Increasingly Turn To Social Media For News. Forbes. https://www.forbes.com/sites/mikevorhaus/2020/06/24/people-increasingly-turn-to-social-media-for-news/?sh=35dd8be13bcc
WHO. (2021). Fighting misinformation in the time of COVID-19, one click at a time. https://www.who.int/news-room/feature-stories/detail/fighting-misinformation-in-the-time-of-covid-19-one-click-at-a-time 
WHO. (2021). Classification of Omicron (B.1.1.529): SARS-CoV-2 Variant of Concern. https://www.who.int/news/item/26-11-2021-classification-of-omicron-(b.1.1.529)-sars-cov-2-variant-of-concern 
Forsey, C. (2021). What is Twitter. HubSpot. https://blog.hubspot.com/marketing/what-is-twitter
Hasdemir, B. (2020). EDA + FE and sentiment analysis with TextBlob. https://www.kaggle.com/barishasdemir/eda-fe-and-sentiment-analysis-with-textblob 
Singh, A. (2021). Performing Sentiment Analysis on Tweets using Python. hello ML. https://helloml.org/performing-sentiment-analysis-on-tweets-using-python/ 
Desai, R. (2021). How to scrape millions of tweets using snscrape. Medium. https://medium.com/dataseries/how-to-scrape-millions-of-tweets-using-snscrape-195ee3594721 
Beck, M. (2020). How to Scrape Tweets With snscrape. BetterProgramming. https://betterprogramming.pub/how-to-scrape-tweets-with-snscrape-90124ed006af
EMORY LIBRARIES. (2021). Using Twitter For Research. https://guides.libraries.emory.edu/main/text-data-mining/twitter 
Twitter, Inc. (2021). Twitter Terms of Service. https://twitter.com/en/tos 
Ozcan, S. (2020). tweet-preprocessor 0.6.0. Python Software Foundation. https://pypi.org/project/tweet-preprocessor/#data 
Keiku. (2017). Python remove stop words from pandas dataframe. Stack overflow. https://stackoverflow.com/questions/29523254/python-remove-stop-words-from-pandas-dataframe 
Pawar, K.K. , Shrishrimal, P.P., Deshmukh, R.R. (2015). Twitter Sentimental Analysis: A Review. International Journal of Scientific & Engineering Research, 6(4), 957-964. https://www.researchgate.net/publication/277554643_Twitter_Sentiment_Analysis_A_Review?enrichId=rgreq-c7c1d6cfc13f21710a28b8397cd75834-XXX&enrichSource=Y292ZXJQYWdlOzI3NzU1NDY0MztBUzoyMzU1MzM2NTc5NjQ1NDRAMTQzMzE2NzAwODA5OA%3D%3D&el=1_x_2&_esc=publicationCoverPdf 
Thakkar, H. & Patel, D. (2015). Approaches for Sentimental Analysis on Twitter: A State-of Art Study. Department of Computer Engineering, National Institute of Technology. https://arxiv.org/ftp/arxiv/papers/1512/1512.01043.pdf 
Hatzivassiloglou, V. & Wiebe, J.M., (2000). Effective of adjective orientation and gradabillity on sentence subjectivity. Preceedings of the 18th conference on Computational Linguistics. 1(July), 299-305. https://dl.acm.org/doi/10.3115/990820.990864 
Pak, A. & Paroubek, P. (2010). Twitter Based System: Using Twitter for Disambiguating Sentiment Ambiguous Adjectives. Proceedings of the 5th International Workshop on Semantic Evaluation, ACL, 436-439. https://aclanthology.org/S10-1097.pdf 
Chiathra, V.D. & Sivakumar, R. (2019). Hybrid approach: naïve bayes and sentiment VADER for analysing sentiment of mobile unboxing video comments. International Journal of Electrical and Computer Engineering (IJECE). 9(5), 4452-4459. DOI: 10.11591/ijece.v9i5.pp4452-459 
Sailunaz, K. & Alhajj, R. (2019). Emotion and Sentiment Analysis from Twitter Text. Journal of Computer Science. (36), 101003. https://doi.org/10.1016/j.jocs.2019.05.009 
Campbell, J., Hindle, A., Stroulia, E. (2016). Latent Dirichlet Allocation: Extracting Topics from Software Engineering Data. Elsevier. http://webdocs.cs.ualberta.ca/~hindle1/2016/06Hindle.pdf 
Negara, E.S., Triadi, D., Andryani, R. (2019). Topic Modelling Twitter Data with Latent Dirichlet Allocation Method. Conference Paper. DOI: 10.1109/ICECOS47637.2019.8984523 
Yang, S. & Zhang, H. (2018). Text Mining of Twitter Data Using a Latent Dirichlet Allocation Topic Model and Sentiment Analysis. International Journal of Computer and Information Engineering. 12(7), 525-529. https://www.researchgate.net/publication/335106801_Text_Mining_of_Twitter_Data_Using_a_Latent_Dirichlet_Allocation_Topic_Model_and_Sentiment_Analysis?enrichId=rgreq-a7c60995b06b38b6c69e3b59f4d924a8-XXX&enrichSource=Y292ZXJQYWdlOzMzNTEwNjgwMTtBUzo3OTA3NDkzNDgxMzA4MTZAMTU2NTU0MDc0NDcyMQ%3D%3D&el=1_x_2&_esc=publicationCoverPdf 
Qomariyah, S., Iriawan, N., Fithriasari, K. (2019). Topic modelling Twitter data using Latent Dirichlet Allocation and Latent Semantic Analysis. AIP Conference Proceedings, 2194. https://doi.org/10.1063/1.5139825 
Geek for Geeks. (2018). Replacing strings with numbers in Python for Data Analysis. https://www.geeksforgeeks.org/replacing-strings-with-numbers-in-python-for-data-analysis/ 
Goyal, G. (2021). Twitter Sentiment Analysis- A NLP Use-Case for Beginners. Analytics Vidhya. https://www.analyticsvidhya.com/blog/2021/06/twitter-sentiment-analysis-a-nlp-use-case-for-beginners/ 
Zifchak, R. (2020). LDA Topic modelling with Tweets. Towards data science. https://towardsdatascience.com/lda-topic-modeling-with-tweets-deff37c0e131 
Kapadia, S. (2019). Evaluate Topic Models: Latent Dirichlet Allocation (LDA). Towards data science. https://towardsdatascience.com/evaluate-topic-model-in-python-latent-dirichlet-allocation-lda-7d57484bb5d0 
Kapadia, S. (2019). Topic Modelling in Python: Latent Dirichlet Allocation (LDA). Towards data science. https://towardsdatascience.com/end-to-end-topic-modeling-in-python-latent-dirichlet-allocation-lda-35ce4ed6b3e0 
Bhatt, B. (2021). Scrape Twitter Data or Tweets in Python using snscrape module.[Video]. Youtube. https://www.youtube.com/watch?v=jOqLX_az_Tg

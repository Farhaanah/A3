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



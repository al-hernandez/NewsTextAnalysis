<h1>BBC News Text Analysis</h1>

<h2>Description</h2>
Text analysis was performed on a dataset consisting of 2225 documents from the BBC news website corresponding to stories from 2004-2005.  
<br />
<br />


Analysis goals:
- determine most and least frequently used words (excluding stopwords)
- create a word cloud
- lemmatize the text 
- generate n-grams and tag parts of speech
- creat a topic model of the text

<h2>Technologies Used</h2>

- <b>Python</b>

<h2> Text Preparation</h2>
To prepare the data for analysis, text was converted to lowercase, and any digits, punctuation, stopwords, web links, and email addresses were removed.<br/>


<img width="500" alt="Clean TExt" src="https://github.com/al-hernandez/NewsTextAnalysis/assets/112843657/24f67535-6eba-445e-aeac-c6e33023e057">

<h2>Word Frequency and Lemmatization</h2>
Lemmatization changed both the contents and order of the most/least used words. For example, the original list of the ten most frequently used words had the word "year" in 9th place. After lemmatization, this word moved to 3rd place since both the words "year" and "years" share the same root word.

In regard to the least frequently used words, the contents of the list were drastically altered. The original list conatined words like "leukoencephalopathy" and "restating", but after lemmatization, their frequency count increased, since they are now grouped with similar words. On the other hand, words such as "cassette" do not share a root word, so their frequency count was not increased.<br/>

  Original 10 Most Frequently Used Words               |      Lemmatized 10 Most Frequently Used Words
:-------------------------:|:-------------------------:
<img width="200" src="https://github.com/al-hernandez/NewsTextAnalysis/assets/112843657/c94ecfda-bc02-4b49-9977-c4de971e96f8"> 
<img width="200" src="https://github.com/al-hernandez/NewsTextAnalysis/assets/112843657/ab7530e6-c3c5-43a4-98d0-e0a91707ff2b">

Original 10 Least Frequently Used Words             |      Lemmatized 10 Least Frequently Used Words 
:-------------------------:|:-------------------------:
<img width="270" src="https://github.com/al-hernandez/NewsTextAnalysis/assets/112843657/6ce86486-bf63-47bf-bafa-0a7b7beebf6c">
<img width="200" src="https://github.com/al-hernandez/NewsTextAnalysis/assets/112843657/2623f8b3-96a2-4ed9-97d6-892eb468f340">

<h2>Word Cloud</h2>
The generated word cloud reflects the contents of the top occurring words in the news entries. Therefore, words such as "government", "minister", and "market" are visible. Since the BBC is a news reporting agency, the word "said" is the boldest one in the image.
<br />
<br />
<p align="center"> 
<img width="700" alt="Word Cloud" src="https://github.com/al-hernandez/NewsTextAnalysis/assets/112843657/cbb668f6-8157-4615-881f-72329acc8618">
</p>

<h2>Parts of Speech Tagging</h2>
The tags NN, RB, and JJ have the highest frequency counts and correspond to singular nouns, adverbs, and adjectives. This writing style is to be expected from a news reporting agency, since it deals with factual events while also trying to make them sensational, hence the high number of adverbs and adjectives.
<br />
<br />
<img width="200" alt="Speech Tagging" src="https://github.com/al-hernandez/NewsTextAnalysis/assets/112843657/dfd9ad33-fd21-4749-8b36-43306525328d">

<h2>Topic Model of the Text</h2>
Using Python's Genism module, a topic model of the text was created, which revealed that news stories tend to fall into one of 14 topics. For each topic, the top ten most important words are moderately coherent, with the model receiving a coherence score of .559. Therefore, one can vaguely deduce the meaning of each topic by looking at their top ten most important words. For example, one can deduce that topic 7 is concerned with a sporting event that involved england, wales, and france. One must examine each word in a topic to infer the overall meaning, since looking at the top word alone does not suffice.
<br />
<br />
<p align="center"> 
<img width="700" alt="TopicVis" src="https://github.com/al-hernandez/NewsTextAnalysis/assets/112843657/a3639377-8d45-49ae-b2e6-65ca102d0dc3">
</p>

Based on a visualization of the model, it appears that the 14 topics fall into four groups: economics, sports, technology, and music/film. The majority of the topics fall into the first of these groups. It is also within this group that the most overlap occurs. This overlap might be attribuated to the fact that the topics in these groups contain the same lemmatized words.

Overall, the news articles have a high probability of being represented by topic 1 or 2, which seem to deal with a governmental issue in the UK, and a sporting event, respectively.


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>

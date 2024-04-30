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

  Original Top Ten Words              |      Lemmatized Top Ten Words
:-------------------------:|:-------------------------:
<img width="200" src="https://github.com/al-hernandez/NewsTextAnalysis/assets/112843657/c94ecfda-bc02-4b49-9977-c4de971e96f8"> 
<img width="200" src="https://github.com/al-hernandez/NewsTextAnalysis/assets/112843657/ab7530e6-c3c5-43a4-98d0-e0a91707ff2b">



<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>

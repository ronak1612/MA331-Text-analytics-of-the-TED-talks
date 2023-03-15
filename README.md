# MA331-Text-analytics-of-the-TED-talks

Text analytics of the TED talks by Dan Gilbert and John Hodgman
2112224-Ronak-Chudasama
Introduction
Aim of this report is to compare word frequencies and perform sentiment analyses on the transcripts of two Ted talkers. Following are the details of Ted talkers I am assigned to:

1.Dan Gilbert :
Dan Gilbert is Harvard Psychologist also known as happiness expert[1]. His 2 talks are included in the data sets:

The psychology of your future self - This talk was given in March 2014.It is about how we wrongly assume our future self based on our present self.

The surprising science of happiness - It is talk from Feb 2004.It speaks about concept of how our psychological immune system react to term happiness.

2.John Hodgman :
John Hodgman is a humourist, geek celebrity, former professional literary agent. He is also a write and known as an expert on all world knowledge[1].2 talks of his are included in data set

Aliens, love – where are they? - It was given in Feb 2008. It talks about topics like Alien, physics and then how it was related to his love life.

Design, explained. - It was given in Mar 2012. He explains design of 3 modern objects.

Methods
1. Description:
Data set has 4 rows (4 transcript of authors) and 5 columns(talk_id, headline, text, speaker and views). .

2. Cleaning data
As task is to deal with words, numbers need to be deleted .I have deleted the numbers using stringr package.

3. Extracting words
Then I have used unnest_tokens function to extract words from the text.

4.Identifying top words
Here first I am finding all top words from the transcripts. Table below shows top 6 words used in talk. As expected these are the stop words because we normally use more stop words in our day to day life. So these needs to be filtered. I am using get_stopwords() function to filter these stops words.

5.Comparing speaker’s vocabularies
Next task is to compare vocabularies of both speakers.

6. Sentiment Analysis
Sentiment analysis is used to assign sentiment to each word. This sentiments are anger, fear or surprise.It helps to understand emotions for machine. In this project, I have used nrc lexicon from the textdata package.

nrc lexicon: It is used to compare the frequencies of each emotions present per talk. Confidence interval for each sentiment is calculated later for both talks using log(OR) Where OR is the value of Odds Ratio.[5]

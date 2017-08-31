---
layout: post
title: Metis Week 8
---

## Uncharted Territory: Project Fletcher

The fourth Metis project, known as project Fletcher was open ended. The only requirment was that it involve natural language processing [(NLP)](https://en.wikipedia.org/wiki/Natural_language_processing). NLP is the processing of human generated text or speech by computers in order to do something useful. Applications for NLP are seemingly endless; they range from spam filters to dictation software. NLP is even used in many online recommendation systems. 

For me, this project was uncharted terrority. For my entire career I've built models that take in numeric inputs and return numeric outputs. Nevertheless, I was very excited for this project, having NLP techniques in my toolbox will greatly expand the types of problems I am able to solve a data scientist.

### Legal Blob

I read the news, and I follow politics. That being said, my background is as an engineer and scientist. I had no idea what congressmen and women do on a daily basis. It was my hunch that we only hear about a narrow slice of congressal activity, and that slice tends to be the most sensational and polarizing. For this project, I wanted create a means to sort through the types of legislation passed by congress. In other words, I wanted to create a tool to learn more about congress, and to hopefully make that process fun. The code for this analysis can be found on my [github page](https://github.com/leem99/legal_blob).

#### The Process

There were three basics steps to this projection 1) obtain data, 2) unsupervised modeling, and 3) visualization

##### Obtain Data

In order to analyze what congress does, I first had to obtain data. The data I settled upon was all congressional laws passed between 1995 and 2017. The text of these laws can be found on the U.S Goverment Publishing Office (GPO) [website](https://www.gpo.gov/fdsys/browse/collection.action?collectionCode=PLAW). I scraped all of the texts from the GPO website using BeautifulSoup.

{% include d3/_blob_d3.html %}


success!

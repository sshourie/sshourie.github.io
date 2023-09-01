---
layout: page
title: Web Scraping and Sentiment Analysis 
description: This project involved using selenium to automate data downloading (web scraping) for a lot of advertisements. After that I used pre-trained transformers from HuggingFace to do sentiment analysis on textual repsonses.
img: assets/img/SentimentAnalysis1.png
importance: 2
category: work
giscus_comments: true
---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/sentiment_analysis2.jpg" title="Sentiment Analysis" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Sentiment Analysis on textual data scrapped from Advertisement survey website
</div>

This was a cool project as I had never worked on web scraping before, using selenium automates a lot of manual stuff but you need to think of the tradeoff of writing and debugging code when maybe the manual download process might take <1 hr.

After scrapping the data from the website, I had to do sentiment analysis to show if the textual responses to each advertisement was either "Positive", "Negative" or "Neutral". I tried a few different models, including using GPT-3.5 using the OpenAI api, but I ended up using pre-trained transformers from [huggingFace](https://huggingface.co/cardiffnlp/twitter-roberta-base-sentiment-latest)(RoBERTa model pre-trained for sentiment analysis) as it is free to use, very accurate and scalable for large number of text inputs. The website has a cool interactive tool to see how each input text is classified.

See code on github [here](https://github.com/sshourie/ads-sentiment/tree/main),  note that the code requires credentials to login to ispot.tv

**Tags:** Python, Selenium, NLP
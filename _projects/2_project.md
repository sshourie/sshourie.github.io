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
        {% include figure.html path="sentiment_analysis2.jpg" title="Sentiment Analysis" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Sentiment Analysis on textual data scrapped from Advertisement survey website
</div>

This was a cool project as I had never worked on web scraping before, using selenium automates a lot of manual stuff but you need to think of the tradeoff of writing and debugging code when maybe the manual download process might take <1 hr.

After scrapping the data from the website, I had to do sentiment analysis to show if the textual responses to each advertisement was either "Positive", "Negative" or "Neutral". I tried a few different models, including using GPT-3.5 using the OpenAI api, but I ended up using pre-trained transformers from [huggingFace](https://huggingface.co/cardiffnlp/twitter-roberta-base-sentiment-latest)(RoBERTa model pre-trained for sentiment analysis) as it is free to use, very accurate and scalable for large number of text inputs. The website has a cool interactive tool to see how each input text is classified.

See code on github [here](https://github.com/sshourie/ads-sentiment/tree/main),  note that the code requires credentials to login to ispot.tv

**Tags:** Python, Selenium, NLP



<!-- Every project has a beautiful feature showcase page.
It's easy to include images in a flexible 3-column grid format.
Make your photos 1/3, 2/3, or full width.

To give your project a background in the portfolio page, just add the img tag to the front matter like so:

    ---
    layout: page
    title: project
    description: a project with a background image
    img: /assets/img/12.jpg
    ---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

You can also put regular text between your rows of images.
Say you wanted to write a little bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, *bled* for your project, and then... you reveal its glory in the next row of images.


<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>


The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}
```html
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
```
{% endraw %} -->

---
layout: page
title: Multi-modal Learning
description: Multimodal Learning for improving Non-English Classification tasks
img: assets/img/Multimodal_Intro.png
importance: 4
category: course
---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/Multimodal_Intro.png" title="" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    We use multimodal (image + text) learning to overcome the language disparity that exists between English and non-English languages. The figure illustrates an example of a social media post that is correctly classified in English but misclassified in Spanish. Including the corresponding image leads to correct classification in Spanish as well as other non-English languages
</div>

This project was done as part of the course [CS 7642 Deep Learning](https://www.cc.gatech.edu/classes/AY2023/cs7643_spring/) at Georgia Tech.

We investigated different multi-modal deep learning architectures with a focus on bridging performance gap in classification in English language vs non-English (Hindi in our study) lanugage tasks. 
The term multi-modal here means that we used both textual and image based inputs (modes) while training our classification model.

Our aim was to:
* Conduct a comparative analysis of different text and image networks, to understand which architectures work best. 
* Understand how much images can improve the discrepancy in performance between English and non-English text classification models.

We used CrisisMMD dataset for training and testing our models.

You can read our full report in the [github repository](https://github.com/sshourie/Multimodal_Learning/tree/main), but to be brief we:
1. Trained a ResNet-18, VGG network, and Inception-V3 to compare different deep learning architectures and to compute image embeddings.
2. Fine-Tuned two pre-trained BERT models, DistilmBERT (distilbert-base-multilingual-cased on HuggingFace) to classify the English text and HindiBERT for Hindi (Doiron 2020).
3. Finally we implement a multimodal or fusion classifier that combines the embeddings of both text and image data to perform classification based on the joint modeling of both input modalities.
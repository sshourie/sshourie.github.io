---
layout: page
title: Fashion Outfit Compatibility
description: Fashion recommendation by estimating compatibility of items in an outfit
img: assets/img/OutfitCompatibility1.png
importance: 4
category: projects
---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/OutfitCompatibility1.png" title="Outfit Compatibility Score" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Compute a score to denote the quality of an outfit.
</div>

This project was done as part of the course CSE 6240 Web Search and Text Mining at GeorgiaTech.

In this project, we follow two existing approaches that employ graphs to represent outfits and use modified versions of the Graph neural network (GNN) frameworks. Both Node-wise Graph Neural Network (NGNN) and Hypergraph Neural Network (HGNN) aim to score a set of items according to the outfit compatibility of items

We recreated the two existing architectures and compare their performance on two tasks 
1. Fill-in-the-blank (FITB): finding an item that completes an outfit
2. Compatibility prediction: estimating compatibility of different items grouped as an outfit


You can read our full report in the [github repository](https://github.com/sshourie/Multimodal_Learning/tree/main), but to be brief we used two different methods involving GNNs to create embeddings. A GNN learns a target node’s representation by propagating the neighbouring information in an iterative manner thus ensuring similarity of representation of items linked closely: 
1. The first approach called Node-wise Graph Neural Network (NGNN) improves on GNN by eschewing parameter sharing to capture item characteristics better. It uses the category of the item as a mainstay in message propagation by using weighted edges based on the category of nodes and also using category-specific item representation. Finally, it uses an attention mechanism to score the outfit.
2. The second approach, HGNN (Hypergraph-GNN), uses hyperedges to denote each outfit. A hypergraph is a generalization of a graph in which an edge can join any number of nodes. Using this approach, theoretically, captures more complex interactions between each item in an outfit leading to key features being captured accurately in the embeddings.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/OutfitCompatibility2.png" title="Training NGNN model" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    During the training process for each outfit, we generate embeddings for each items in an outfit using Inception V3 model. Create an outfit graph neural network (GNN) and update item embeddings. Finally we use an attention layer to calculate compatibility score. The loss is caluclated as outfit score vs negative outfit score which is then used to update the network in the backpropogation step.
</div>
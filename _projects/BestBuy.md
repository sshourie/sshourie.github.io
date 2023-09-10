---
layout: page
title: Best Buy Data Competition
description: Forecasting sales for slow moving SKUs
img: assets/img/BestBuy1.jpg
importance: 4
category: projects
---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/BestBuy1.png" title="" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

This project was part of a Data Science competition sponsored by Best Buy. Our team finished second.

#### Project Aim:
* Best Buy stocks hundered of slow-selling SKUs that put a constraint on working capital and sales are difficult to predict.
* Project's aim is to build an accurate and fast forecasting model specifically for slow-selling SKUs

#### Approach:
1. First step of our approach was data cleaning and exploration for which we used Tableau, Excel, and Python
2. We used external features (like Global supply chain pressure index and US interest rates) and lagged features and used feature selection steps (L1 regularization/ stepwise selection)
3. The first model we tried was a time series forecasting method for sparse datasets called Croston's forecasting method.
4. Then we tried different ML models, the best of which was LightGBM with high accuracy on the test dataset and really fast training time


You can read our full report in the [github repository](https://github.com/sshourie/bestbuy/tree/main)
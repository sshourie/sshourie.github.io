---
layout: page
title: Critical Healthcare (SCCM Project) 
description: Project in collaboration with clinicians to address real-world problems in healthcare using existing databases.
img: assets/img/SCCM1.png
importance: 1
category: work
related_publications: #einstein1956investigations, einstein1950meaning
---

This project was part of a [datathon](https://sccm.org/Research/Discovery-Research-Network/datascience/Datathon) with Society of Critical Care Medicine (SCCM), which involved coloration with clinicians and pharmacists to develop a data-driven model for care of critically ill patients using large health record databases.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/sccm-logo.png" title="Society of Critical Care Medicine" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

#### Problem Description:

> Are there differences in sedative agent selection in adult patients on invasive mechanical ventilation based on race or ethnicity.

#### Databases:

We used two critical care databases:[ MIMIC-IV](https://physionet.org/content/mimiciv/2.2/) (Medical Information Mart for Intensive Care) database and the [eICU collborative research database. ](https://eicu-crd.mit.edu/about/eicu/)

#### BigQuery and Colab:

We used [BigQuery](https://console.cloud.google.com/bigquery?project=sccm-datathon) to easily explore the large datasets using SQL.

See example code on my [github](https://github.com/sshourie/SCCM-hackathon/tree/main) repository.

**Tags:** Python, BigQuery, SQL, Healthcare


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

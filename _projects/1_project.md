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
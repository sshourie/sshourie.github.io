---
layout: page
title: Diffusion Limited Aggregation using R programming
description: The problem is based on recreating the snowflake like structure called diffusion limited aggregation (DLA) using R programming and analyzing the effects of stickiness of particles.
img: assets/img/DLA_2.png
# redirect: https://unsplash.com
importance: 3
category: fun
---

# Diffusion Limited Aggregation (DLA):

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/DLA_2.png" title="Diffusion Limited Aggregation" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Cool snowflake like structures
</div>

DLA was first used to describe the diffusion and aggregation of zinc ions in an electrolytic solution onto electrodes. "Diffusion" because the particles forming the structure wander around randomly before attaching themselves ("Aggregating") to the structure. "Diffusion-limited" because the particles are considered to be in low concentrations so they don't come in contact with each other and the structure grows one particle at a time rather then by chunks of particles.

Other examples can be found in coral growth, the path taken by lightning, coalescing of dust or smoke particles, and the growth of some crystals.

Another more colourful description involves a city square surrounded by taverns. Drunks leave the taverns and stagger randomly around the square until they finally trip over one their insensate companions at which time, lulled by the sounds of peaceful snoring, they lie down and fall asleep. The tendril like structure is an aerial view of the sleeping crowd in the morning.

## Detailed Problem statement:

### Introduction

*   This problem is based on the Diffusion Limited Aggregation (DLA) model as described on this [page](https://paulbourke.net/fractals/dla/).

*   Here is an excerpt from the above page, describing the model:

    *   "start with a white image except for a single black pixel in the center. New points are introduced at the borders and randomly (approximation of Brownian motion) walk until they are close enough to stick to an existing   black pixel. A typical example of this is shown below in figure 1. If a point, during its random walk, approaches an edge of the image there are two strategies. The point either bounces off the edge or the image is toroidally bound (a point moving off the left edge enters on the right, a point moving off the right edge enters on the left, similarly for top and bottom). In general new points can be seeded anywhere in the image area, not just around the border without any significant visual difference."

*   Here is a more precise statement of the above description:

    *   Start with a M x M matrix, with all entries as 0 (representing "empty") except for the center cell of the matrix which has a 1 (representing "occupied with a particle").

    *   Choose a cell randomly along the border of the matrix (i.e, along one of its 4 edges), and fill it with a 1. This represents introducing a new particle at the edge of the arena.

    *   Make this particle do a 2D random walk in the empty region of the matrix. In other words, at every iteration, randomly select an empty neighboring cell, and move the particle there, leaving the old cell empty.

    *   Continue the random walk until the particle encounters another particle in an adjacent cell.

    *   The random walk now stops, and the particle remains stuck here forever.

    *   Repeat the above procedure (introducing new particles, random walk, sticking to existing particles) for N particles.

    *   To be clear, only 1 particle does a random walk at a time, and a new one is not introduced until the previous one has found a place to stick to.

*   Refer to figure 1 on the above page to see an example of what the output of such a simulation looks like.

*   Next, refer to the definition of "stickiness" as given just above Figure 6.

*   Refer to Figures 6, 7 and 8 to see the effect of varying stickiness.

### Approach:

See github code and report [here](https://github.com/sshourie/DLA-using-R/tree/master).

1.  My first approach was to create a brute force random walker which moves with an equal probability
    along the four directions. This worked well for small sample sizes but did not scale well to an increase in
    number of particles.

2\. To reduce the run time and taking inspiration from mean reversion present in auto-regressive models, I
created a bias in the random walk for center seeking moves. This drastically reduced the run-time and I
could run the models for a larger N.
Unexpectedly, a star like pattern emerged, as seen in the image below, especially for large number of
particles. I believe that this pattern occurred because the algorithm used introduced a relatively high bias
for center seeking moves. Thus the prevalence of particles along the diagonal and the two axes.

3\. The main problem affecting the time required to generate the DLA is that as the dimension of the
bounding square (M) grows, the particles need to ‘walk’ a lot before they meet the aggregate. So to
reduce the time taken for creating the DLA, I introduced the particles closer to the aggregate along the
minimum bounding circle.

4\. Estimating Stickiness: I calculated "stickiness" using surface area calculations of the particles.

5\. Next I created regressions models to see if any relationship exists between stickiness.

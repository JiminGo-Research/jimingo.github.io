---
layout: page
title: Information Systems Game Day Analytics Competition
description: The most effecitve brand of Super Bowl LVIII on various perspectives
img: assets/img/gdac_logo.png
importance: 3
category: Additional
---

I participated in the <b>Game Day Analytics Challenge</b> hosted by the David Eccles School of Business at the University of Utah. In this competition, our team secured <b>2nd place in the undergraduate division</b>. 
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/gdac_winning.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/gdac_certification.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/gdac_prize.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

Purpose of this study:

Our goal: <b?Which brand delivered the most effective Super Bowl advertisement?</b>

Brief summarization of our strategy:

We first thought about <b?"What makes an ad successful?"</b> and conducted various analyses, including the number of tweets per brand over time, cost per tweet by brand, and sentiment analysis.

However, each analysis raised important questions. For example, in the figure below, which analyzes the number of tweets over time, a notable point is the dramatic increase in tweets related to a specific brand immediately following its advertisement. This raises the question: Which is more effective consistent tweets throughout the entire period, like Marvel, or concentrated bursts of tweets at specific times, like Verizon?

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/gdac_1.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The number of tweets over time for the top 10 brands
</div>

<b>Multi-Criteria Decision Making</b>:

Therefore, we decided to evaluate the effectiveness of the advertisements by considering all the factors comprehensively and chose to use a MCDM model. We used a model that combines AHP and TOPSIS. The weights were determined through the AHP model, while the TOPSIS model was used to evaluate how close the alternatives were to the given criteria in order to identify the most ideal alternative. 

As shown in the structure of the AHP model at the bottom left, we used the number of tweets, cost per tweet, positive tweet ratio, and negative tweet ratio as the criteria. The image on the right shows the brand rankings when more weight is given to each criterion. For example, in the case of Universal, when more weight is given to the number of tweets, it ranks 5th, but when more weight is given to the positive tweet ratio, it drops to 63rd. This analysis suggests that Universal did not receive many positive tweets.

<div class="row justify-content-sm-center">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/gdac_2.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/gdac_3.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Structure of AHP and TOPSIS results
</div>

Upon seeing the experimental results, where the NFL ranked first in all categories, we began to wonder if it was simply because the NFL hosted the game, leading to a higher number of mentions.

Who is the real winner?

If you would like to learn more about this competition, please refer to this link. https://eccles.utah.edu/programs/undergraduate/game-day-ad-analytics/

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

You can also put regular text between your rows of images.
Say you wanted to write a little bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, _bled_ for your project, and then... you reveal its glory in the next row of images.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
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
    {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-4 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
```

{% endraw %}

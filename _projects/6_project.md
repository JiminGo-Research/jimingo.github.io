---
layout: page
title: Developing Simulation-based Integrated Operation Scheduling System
description:
img: "assets/img/electroplating_3.png"
importance: 4
category: Research Project
---

This project is my first lead project in Industrial Intelligence Laboratory at Incheon National University. Based on this work, our team published <a href="/assets/pdf/patent_certification.pdf">patent</a> and awarded an 19th Industrial Engineering Project Competition hosted by Korean Institute of Industrial Engineers(KIIE).

<b>Purpose of this study : </b>

This study was initiated to address the challenges faced by a <a href="http://www.ik-tech.co.kr/eng/" target="_blank">company</a> in South Korea that manufactures and sells plating line. When a request is made to create a plating line capable of producing a specific type of plating within given seconds, <b>the company currently tests its feasibility based solely on the expertise and experience of professionals, without any system in place.</b> The company mentioned that manual scheduling takes anywhere from 3 days to over a week, and <b>they were looking for ways to reduce this time</b>. Additionally, due to the manual nature of the scheduling process, <b>mistakes have occured, such as failing to identify opportunites to reduce the number of hoists.</b> 

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/electroplating_1.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/electroplating_2.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left image shows the actual plating line manufactured by the company. Right displays the scheduling result visualization used by the company.
</div>

<b>Our goal : </b> To address their difficulties, we believed the following three things were necessary:

<b>1. A program that automatically designs plating lines</b> Since the company faced an urgent need to reduce the time required for plating line design, it was clear that an automated system was necessary. We viewed this problem as a type of flow shop scheduling and decided to develop a rule-based algorithm to quickly find a solution.

<b>2. A program for ananlyzing scheduling results</b> Due to reliance on experts, it was difficult to explain to clients why certain designs were necessary to meet given requirement. As shown in the figure above, the scheduling result chart used by the company was not easy to understand at a glance. Therefore, we decided to develop a bottleneck analysis tool and a more user-friendly Gantt chart.

<b>3. Graphic User Interface (GUI)</b> To help the worker understand how the scheduling results actually functioned and enable manufacturing on the factory, we also decided to develop a GUI.

<b>Problem definition : </b>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/electroplating_3.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Example of electroplating line considered by this research
</div>

Here are some <b>assumptions</b> and <b>constraints</b> necessary to understand the problem:

1. Each workpiece goes through all the stages present in the plating line sequentially, and after a process is completed, it moves to the next tank.
2. Each tank can process only one workpiece at a time, and if the deeping time is violated, the item is considered defective.
3. Each hoist can transport only one workpiece at a time, and it is assumed that there will be no stops during the transport process.
4. Hoists must be operated with at least one tank gap between tank.
5. Carriers move at high, medium, or low speed depending on the travel distance, and it takes 10 seconds for ascending and descending
6. If a stage has a significantly longer immersion time compared to others, parallel tanks may be used.
7. Hoist overlapping is allowed when the turnover point is determined in parallel tanks.
8. If the immersion time in a tank is less than 5 seconds, it cannot be a turnover point.
9. Up to three dummy tanks (empty tanks without chemicals, not used in the actual process but employed to avoid collisions between carriers) can be added.

<b>Our method : </b>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/electroplating_4.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Example of electroplating line considered by this research
</div>

<b>Results : </b>

Every project has a beautiful feature showcase page.
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

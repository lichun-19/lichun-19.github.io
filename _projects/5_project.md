---
layout: page
title: Emotional Ocean
description: An Interactive Device to Raise Awareness of Emotional Issues | CSCW 2022
img: assets/img/emotional-full.png
importance: 1
category: Human-Centered
related_publications: false
bibliography: false 
---

### Introduction

<div style="text-align: justify; text-justify: inter-word; margin-top: 1rem; margin-bottom: 3rem;">
    Collaborators | Wei-Hung Hsu, Pei-Yun Tsai, Jia-Rong Chang, Hsun-Pu Chen, and Ying-Yin Chu<br>
    This work originated from the OpenHCI workshop, was nominated for TAICHI—the largest national HCI event in Taiwan—and was later selected for the <strong>CSCW 2022</strong> Demo Session.<br><br>
    We designed a device paired with a mobile app to help workers manage negative emotions and regain focus during critical tasks. The device provides tactile and visual feedback, while the app records the intensity and frequency of presses. This allows users to review their emotional fluctuations over time and better understand their patterns when they look back in the app.
</div>


<div class="row">
<div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/emotional-design.png" title="design" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            Design
        </div>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/emtional-prototype.jpg" title="prototype" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            Prototype
        </div>
    </div>
    
</div>


**Define the painpoints through User study**
<div style="text-align: justify; text-justify: inter-word; margin-top: 0rem; margin-bottom: 1rem;">
We conducted semi-structured interviews (N = 4) to understand the types of stress office workers typically face and the strategies they use to cope. We then applied an affinity diagram to consolidate and analyze the qualitative data. In addition, we performed a literature review to investigate existing stress-relief products and their underlying mechanisms.<br>
<ul>
    <li>Pain Point — Workers struggle to maintain focus on critical tasks due to negative emotions driven by work-related pressure.</li>
</ul>
</div>

**Design concepts**
<div style="text-align: justify; text-justify: inter-word; margin-top: 0rem; margin-bottom: 1rem;">
    Drawing from our user study and supporting literature, we integrated several features into our design:

    <ul>
        <li>Visual feedback — Inspired by calming water ripple effects (Garrett et al., 2019) and warm ambient lighting.</li>

        <li>Haptic feedback — Repetitive, subtle pressing motions help improve focus and reduce anxiety.</li>

        <li>Long-term emotional tracking — The app logs emotional states and visualizes daily “ripples.”</li>
    </ul>
</div>


**Prototype**
<div style="text-align: justify; text-justify: inter-word; margin-top: 0rem; margin-bottom: 3rem;">
We modeled and designed the device casing in Cinema 4D and 3D-printed the components. For sensing, we used a NodeMCU microcontroller paired with an FSR402 pressure sensor to capture the level and frequency of presses. RGB visuals were implemented using WS2812 LEDs, and Wi-Fi connectivity allowed the device to communicate with our prototype web demo so users could customize device lighting. For the mobile interface, we created a high-fidelity prototype using Figma.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/emotional-app1.png" title="emotional-app" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/emotional-app2.png" title="emotional-app" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/emotional-app3.png" title="emotional-app" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    App Interface Demonstration
</div>

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    <div style="position: relative; padding-bottom: 56.25%; height: 0;">
      <iframe
        src="https://www.youtube.com/embed/zm3tcTdbUv0"
        style="position:absolute; top:0; left:0; width:100%; height:100%;"
        frameborder="0"
        allowfullscreen>
      </iframe>
    </div>
  </div>
</div>
<div class="caption">
    Demo Video
</div>


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/emotional-poster.jpg" title="Poster" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Poster
</div>

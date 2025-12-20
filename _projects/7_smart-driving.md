---
layout: page
title: Smart Driving System
description: Embedded Systems Course Final Project | Fall 2023
img: assets/img/embedded_main.png
importance: 2
category: Interactive Systems
related_publications: false
bibliography: false 
---

### Overview
<div style="text-align: justify; text-justify: inter-word; margin-top: 1rem; margin-bottom: 3rem;">
Collaborator | Shou-Ren Chen<br><br>

This Embedded Systems final project explores how real-time sensing, wireless communication, and local computation can be integrated into a compact smart-driving assistant. Our goal was to design a system capable of reading environmental distances, detecting danger, adjusting driving modes, and supporting early-stage autonomous parking through machine learning.<br><br>

Built using an STM32 board, Raspberry Pi 3, PiRacer Pro, and ToF sensors, the system demonstrates multiple embedded concepts—including BLE, PWM motor control, I²C peripherals, multi-threading, HTTP streaming, and ML-based behavioral cloning.
<br><br>
</div>



<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/embedded_main.png" title="embedded main" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Real time display of our system.
</div>

---

### Introduction

<div style="text-align: justify; text-justify: inter-word; margin-top: 1rem; margin-bottom: 3rem;">
This project integrates sensing, communication, control, and machine learning into a compact embedded system. We successfully implemented:<br>
<ul>
    <li>Real-time distance detection</li>
    <li>Driving mode switching</li>
    <li>Danger detection and braking</li>
    <li>FPV video streaming</li>
    <li>Prototype-level auto parking</li>
</ul>
The system demonstrates how embedded technologies—from BLE to PWM to multi-threading—can work together to enhance driving safety and automation.
</div>

---

### Design — System Features & Hardware


<div style="text-align: justify; text-justify: inter-word; margin-top: 1rem; margin-bottom: 3rem;">

<strong>Key Features</strong><br>
<ul>
    <li><strong>Real-Time Distance Measurement</strong> — Using VL53L0X ToF sensor on STM32 to continuously stream distance data via BLE.</li>
    <li><strong>Driving Modes</strong> — Normal Mode (50%) and Parking Mode (22%) for fine motor control.</li>
    <li><strong>Danger Detection</strong> — Automatic braking and warning messages when objects are too close.</li>
    <li><strong>Live FPV Display</strong> — Raspberry Pi camera streaming video via MJPEG over HTTP, with mode and distance overlays.</li>
    <li><strong>Auto Parking (Prototype)</strong> — Behavioral cloning model trained on steering + throttle pairs to imitate human parking behavior.</li>
</ul>
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/embedded_hardware.png" title="Hardware Assembly" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            Hardware setup including STM32, Raspberry Pi 3, PiRacer Pro, ToF sensor, and wide-angle camera. {{ ' ' }}
        </div>
    </div>
</div>

<div style="text-align: justify; text-justify: inter-word; margin-top: 1rem; margin-bottom: 3rem;">

<strong>Hardware Used</strong><br>
<ul>
    <li>STM32L475 + VL53L0X Time-of-Flight Sensor</li>
    <li>Raspberry Pi 3</li>
    <li>PiRacer Pro platform + joystick controller</li>
    <li>Wide-angle FPV camera</li>
</ul>
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/embedded_architecture.png" title="System Architecture" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            Overall architecture of communication and control modules.
        </div>
    </div>
</div>

---
### Core Functionalities

<div style="text-align: justify; text-justify: inter-word; margin-top: 1rem; margin-bottom: 3rem;">

<p><strong>Real-Time Distance Measurement</strong><br>
Using the VL53L0X Time-of-Flight sensor on the STM32, the system measures distance in real time in continuous polling mode. The STM32 updates the value every 300&nbsp;ms and sends the distance to the Raspberry Pi via BLE.</p>

<p><strong>Danger Detection</strong></p>
<ul>
  <li>≥ 400&nbsp;mm → Safe</li>
  <li>100–400&nbsp;mm → Show distance on screen as a proximity warning</li>
  <li>≤ 100&nbsp;mm → Trigger emergency stop and block forward movement</li>
</ul>

<p><strong>Driving Mode Switching</strong><br>
Using the joystick’s <code>B</code> button, the driver can switch between Normal Mode (50% speed) and Parking Mode (22% speed) for finer control in narrow spaces.</p>

<p><strong>FPV Interface</strong></p>
<ul>
  <li>Raspberry Pi camera stream served via Flask using MJPEG</li>
  <li>Overlays show current driving mode and latest distance reading</li>
</ul>

<p><strong>Auto Parking Prototype</strong></p>
<ul>
  <li>Implemented using the DonkeyCar behavioral cloning framework</li>
  <li>CNN predicts steering and throttle from front camera images</li>
  <li>Trained on 10k–31k frames; achieves initial movement but fails on complex turns</li>
</ul>

</div>

More details at our <a href="https://github.com/lawraa/ESLab_SmartParking" target="_blank" rel="noopener">
        github repository</a>.

---
date: 2026-01-10 07:18:43
layout: post
title: "Bacterial Cellulose Bioreactor"
subtitle: Final Project Overview
description: Bioreactor build to model nutrient consumption of bacterial cellulose production.
image: /assets/img/uploads/bioreactor.jpg
optimized_image: /assets/img/uploads/bioreactor.jpg
category: 2.788 Project
tags:
    - sensors
    - data_collection
    - CAD
author: josephmei
paginate: false
---
<div style="padding-left:170px;padding-right:170px;">
    <div style="display:flex;align-items:flex-start;gap:1rem;flex-wrap:wrap;box-sizing:border-box;">
        <img src="/assets/img/uploads/bioreactor.jpg" alt="Featured image" class="post-cover" style="max-width:370px;width:100%;height:auto;flex:0 0 320px;display:block;margin:0 8px 0 0;">
        <div style="flex:1;min-width:200px;border:1px solid #e6e6e6;padding:16px;background:#fbfbfb;border-radius:6px;box-sizing:border-box;">
            <h3 style="margin:0 0 0.5rem;padding-top: 0;">Introduction</h3>
            <p style="margin:0;">Bacterial cellulose (BC) is the most abundant biopolymer on the planet and has significant potential as a sustainable alternative to plastics and leather. Despite these advantages, large-scale BC production remains inefficient and poorly understood, particularly with respect to the media conditions that govern cellulose synthesis.<br>
            <strong>For my <i>Design of Living Systems (2.788)</i> final project, my group and I aimed to model the media conditions involved in BC production to better understand the factors influencing cellulose formation and to identify opportunities for improving production efficiency.</strong></p>
        </div>
    </div>
    <div style="flex:0;">
        <h2 style="margin:0 0 0.5rem;text-align:center; padding-top:20px;">Bioreactor Build</h2>
        <img src="/assets/img/uploads/labeled_bioreactor.png" alt="Featured image" style="max-width:900px;width:100%;height:auto;">
        <h3 style="margin:0 0 0.5rem;padding-top:0px;padding-bottom:0px;">Sensors + Components</h3>
        <p style="margin-top:0; margin-bottom:20px"> Sensors were carefully selected based on their <strong>feasibility for rapid integration</strong> and <strong>relevance to modeling BC production,</strong> avoiding unnecessary measurements that could introduce noise and reduce model accuracy. To maximize data collection, we prioritized sensors that enabled continuous, unattended monitoring over extended periods.</p>
        <div style="display:flex;align-items:flex-start;gap:1rem;flex-wrap:wrap;box-sizing:border-box;">
            <div style="flex:1;min-width:220px;border:1px solid #e6e6e6;padding:16px;background:#fbfbfb;border-radius:6px;box-sizing:border-box;">
                <ul style="line-height:1.2;margin-top:0;padding-left:20px;padding-top:0;padding-bottom:0">
                <li><strong>Temperature Probe:</strong> Temperature relays the kinetics of the reaction for BC production.</li>
                <li><strong>pH Probe:</strong> Gluconic acid is a byproduct of the reaction, making pH an indicator of production. Acidic conditions are also unfavorable to the bacteria, slowing production.</li>
                <li><strong>Optical Sensor:</strong> Gives color readings (Red, Green, Infrared) that can inform pellicle thickness and density.</li>
                <li><strong>Temperature Mat:</strong> Allows for temperature control in determining efficient media conditions. </li>
                <li><strong>Spectrophotometer:</strong> Measures cell culture density at OD600.</li>
                <li><strong>Glucometer:</strong> Measures glucose concentration in the media after a series of dilutons.</li>
                </ul>
            </div>
            <img src="/assets/img/uploads/sensors_bioreactor.png" alt="brake calcs" class="post-cover" style="max-width:450px;width:100%;height:auto;flex:0 0 320px;display:block;margin:0 8px 0 0;">
        </div>
        <br>
        <h3 style="margin:0 0 0.5rem;padding-top:0px;padding-bottom:0px;">CAD + Assembly</h3>
        <section style="display:flex;justify-content:center;align-items:center;gap:60px;flex-wrap:wrap;margin:10px auto;max-width:1200px;">
        <figure style="flex:1 1 45%;max-width:300px;text-align:center;margin:0;">
            <img src="/assets/img/uploads/backpack.jpg" alt="Left image"
                style="width:100%;height:auto;border-radius:12px;display:block;">
            <figcaption style="margin-top:12px;font-size:1rem;color:#555;">
            Backpack setup carrying the circuit boards and electronics
            </figcaption>
        </figure>
        <figure style="flex:1 1 45%;max-width:300px;text-align:center;margin:0;">
            <img src="/assets/img/uploads/wide_view_bioreactor.jpg" alt="Right image"
                style="width:100%;height:auto;border-radius:12px;display:block;">
            <figcaption style="margin-top:12px;font-size:1rem;color:#555;">
            Bioreactor setup with camera and ruler to be implemented for further measurements
            </figcaption>
        </figure>
        <figure style="flex:1 1 45%;max-width:300px;text-align:center;margin:0;">
            <img src="/assets/img/uploads/mounts.jpg" alt="Right image"
                style="width:100%;height:auto;border-radius:12px;display:block;">
            <figcaption style="margin-top:12px;font-size:1rem;color:#555;">
            Early prototypes of backpack and sensor platforms with press-fit mounts
            </figcaption>
        </figure>
        </section>
        <section style="display:flex;justify-content:center;align-items:center;gap:40px;flex-wrap:wrap;margin:40px auto;max-width:1200px;">
            <figure style="flex:1 1 45%;max-width:300px;text-align:center;margin:0;">
                <img src="/assets/img/uploads/cad_bioreactor.png" alt="Left image"
                    style="width:100%;height:auto;border-radius:12px;display:block;">
                <figcaption style="margin-top:12px;font-size:1rem;color:#555;">
                Bioreactor CAD Assembly
                </figcaption>
            </figure>
            <figure style="flex:1 1 45%;max-width:420px;text-align:center;margin:0;">
                <div class="image-carousel" style="max-width:420px;width:100%;height:300px;display:flex;
                            justify-content:center;align-items:center;overflow:hidden;
                            border-radius:8px;position:relative;margin:0 auto;">
                    <img src="/assets/img/uploads/cad_linear.png" class="carousel-image first active" alt="pedal ratio"
                        style="max-width:100%;height:auto;position:absolute;transition:opacity 0.6s ease;opacity:1;">
                    <img src="/assets/img/uploads/cad_backpack.png" class="carousel-image first" alt="brake"
                        style="max-width:100%;height:auto;position:absolute;transition:opacity 0.6s ease;opacity:0;">
                    <img src="/assets/img/uploads/cad_rulermount.png" class="carousel-image first" alt="brake"
                        style="max-width:100%;height:auto;position:absolute;transition:opacity 0.6s ease;opacity:0;">
                    <button class="carousel-btn first-prev"
                            style="position:absolute;top:50%;left:15px;transform:translateY(-50%);
                                    background:rgba(0,0,0,0.4);color:white;border:none;border-radius:50%;
                                    width:40px;height:40px;cursor:pointer;font-size:1.2rem;">‹</button>
                    <button class="carousel-btn first-next"
                            style="position:absolute;top:50%;right:15px;transform:translateY(-50%);
                                    background:rgba(0,0,0,0.4);color:white;border:none;border-radius:50%;
                                    width:40px;height:40px;cursor:pointer;font-size:1.2rem;">›</button>
                </div>
                <figcaption style="margin-top:12px;font-size:1rem;color:#555;">
                (1) Optical sensor mount<br>(2) Backpack for boards<br>(3) Ruler mount
                </figcaption>
            </figure>
        </section>
        <h2 style="margin:0 0 0.5rem;text-align:center; padding-top:20px;">Results</h2>
        <section style="display:flex;justify-content:center;align-items:center;gap:30px;flex-wrap:wrap;margin:10px auto;max-width:1200px;">
        <figure style="flex:1 1 45%;max-width:600px;text-align:center;margin:0;">
            <img src="/assets/img/uploads/temp_data.png" alt="Left image"
                style="width:100%;height:auto;border-radius:12px;display:block;">
            <figcaption style="margin-top:12px;font-size:1rem;color:#555;">
            Temperature of the bioreactor stabilized around 30 degrees, which is optimal for BC production according to literature.
            </figcaption>
        </figure>
        <figure style="flex:1 1 45%;max-width:600px;text-align:center;margin:0;">
            <img src="/assets/img/uploads/pH_data.png" alt="Right image"
                style="width:100%;height:auto;border-radius:12px;display:block;">
            <figcaption style="margin-top:12px;font-size:1rem;color:#555;">
            pH readings were largely stable, with a slight trend towards acidity consistent with gluconic acid buildup.
            </figcaption>
        </figure>
        <figure style="flex:1 1 45%;max-width:600px;text-align:center;margin:0;">
            <img src="/assets/img/uploads/color_data.png" alt="Right image"
                style="width:100%;height:auto;border-radius:12px;display:block;">
            <figcaption style="margin-top:12px;font-size:1rem;color:#555;">
            Color readings increased as the cellulose grew, showing increasing pellicle density.
            </figcaption>
        </figure>
        </section>
        <br>
        <h2 style="margin:0 0 0.5rem;text-align:center; padding-top:20px;">Takeaways</h2>
        <p style="margin-top: 0"> <i>Design of Living Systems</i> was the first graduate-level course I've taken, and I couldn't have asked for a better experience. I was fortunate to work with groupmates who were kind, supportive, and deeply knowledgeable, which made our ambitious project both challenging and rewarding. While unforeseen setbacks limited the scope of what we initially hoped to achieve, the experience allowed me to dive deeply into <strong>sensor operation, PCB design, data processing, and cell culturing</strong>. Most importantly, it was very rewarding carrying a project from start to end, resulting in a functional system capable of generating meaningful results.</p>
        <img src="/assets/img/uploads/goofy_bioreactor.png" alt="Left image"
                style="width:70%;height:auto;border-radius:12px;display:block;">
    </div>
</div>

<script>
    // Helper: Create a reusable carousel controller
    function setupCarousel(side) {
    const images = document.querySelectorAll(`.carousel-image.${side}`);
    let current = 0;
    function showImage(index) {
        images.forEach((img, i) => {
        img.style.opacity = (i === index) ? 1 : 0;
        });
    }
    document.querySelector(`.${side}-next`).addEventListener('click', () => {
        current = (current + 1) % images.length;
        showImage(current);
    });
    document.querySelector(`.${side}-prev`).addEventListener('click', () => {
        current = (current - 1 + images.length) % images.length;
        showImage(current);
    });
    }

    setupCarousel('first');
</script>

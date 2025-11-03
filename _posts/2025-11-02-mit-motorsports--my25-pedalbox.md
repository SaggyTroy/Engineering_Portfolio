---
date: 2025-06-02 07:16:27
layout: post
title: "MIT Motorsports | MY25 Pedalbox"
subtitle: Design Binder
description: Design of pedalbox system for MY25 race car.
image: /assets/img/uploads/pedalbox.jpg
optimized_image:
category: motorsports
tags:
    - structures
    - machining
    - ergonomics
    - CAD
author: josephmei
paginate: false
---

<div style="padding-left:170px;padding-right:170px;">
    <div style="display:flex;align-items:flex-start;gap:1rem;flex-wrap:wrap;box-sizing:border-box;">
        <img src="{{ page.image }}" alt="Featured image" class="post-cover" style="max-width:400px;width:100%;height:auto;flex:0 0 320px;display:block;margin:0 8px 0 0;">
        <div style="flex:1;min-width:220px;border:1px solid #e6e6e6;padding:16px;background:#fbfbfb;border-radius:6px;box-sizing:border-box;">
            <h3 style="margin:0 0 0.5rem;padding-top: 0;">Introduction</h3>
            <p style="margin:0 0 0.5rem;"><strong>MIT Motorsports</strong> is a student-run engineering team dedicated to designing, building, and competing with high-performance electric racecars in the Formula SAE competition.</p>
            <p style="margin:0;">For the Model Year 2025 season, I was tasked with designing a <strong>custom pedalbox</strong> to integrate the throttle, brake, master cylinders, and potentiometers into a single, adjustable platform. This project required balancing structural strength, adjustability, and minimal weight to enhance driver control and vehicle performance.</p>
        </div>
    </div>
    <div style="flex:0;">
        <h3 style="margin:0 0 0.5rem;">Design Overview</h3>
        <p style="margin:0 0 0.5rem;">In the design process, I first started by identifying <strong>key design requirements</strong> that govern the overarching system, using information from the FSAE ruleset, data from an ergonomics testing jig, and feedback from the drivers themselves.</p>
        <div style="display:flex;align-items:flex-start;gap:1rem;flex-wrap:wrap;box-sizing:border-box;">
            <div style="flex:1;min-width:220px;border:1px solid #e6e6e6;padding:16px;background:#fbfbfb;border-radius:6px;box-sizing:border-box;">
                <h4 style="padding-top:0;padding-bottom: 0"> Some Key Design Requirements: </h4>
                <ul style="line-height:1.2;padding-top:0;padding-bottom:0">
                <li><strong>Strength:</strong> Withstand 2000 N of applied force on the brake to ensure reliability during aggressive braking.</li>
                <li><strong>Adjustability:</strong> Provide 6 inches of adjustment to accommodate drivers of varying heights.</li>
                <li><strong>Ergonomics:</strong> The pedals' resting position is 80 degrees from the horizontal, and the throttle must travel a maximum of 30 degrees. The throttle should also provide 300 Newtons of return force for driver feedback.</li>
                <li><strong>Lightweight and Stiff:</strong> Minimize compliance for precise pedal response and reduce weight to improve vehicle dynamics.</li>
                </ul>
            </div>
            <img src="{{ page.image }}" alt="Featured image" class="post-cover" style="max-width:400px;width:100%;height:auto;flex:0 0 320px;display:block;margin:0 8px 0 0;">
        </div>
        <p style="margin:0 0 0.5rem;padding-top: 20px;">I then performed <strong>structural hand calculations</strong> to inform my modeling, drawing FBDs, analyzing shear and bending diagrams, and performing lug analyses. These calculations were used to optimize the mass and geometry of the system components to ensure minimal deflection while being able to withstand the heavy applied loads.</p>
        <img src="{{ page.image }}" alt="Featured image" class="post-cover" style="max-width:400px;width:100%;height:auto;flex:0 0 320px;display:block;margin:0 8px 0 0;">
        <img src="{{ page.image }}" alt="Featured image" class="post-cover" style="max-width:400px;width:100%;height:auto;flex:1;display:block;margin:0 8px 0 0;">
    </div>
</div>


</p>
**Design Process**
Testing: An ergonomics jig was created to evaluate driver preferences for pedal angle heights, positions, and applied forces on the throttle. Data from the jig was incorporated into the design to optimize ergonomics.
Calculations and Modeling: Hand calculations were performed to determine component geometries capable of withstanding calculated loads while minimizing mass. Siemens NX was used to create detailed CAD models, ensuring precise integration of the throttle, brake, master cylinders, and potentiometers.
Manufacturing: All components were custom-designed and manufactured in-house using CNC machinery.

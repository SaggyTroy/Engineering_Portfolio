---
date: 2025-09-02 07:18:43
layout: post
title: "Tendon-Driven Continuum Snake Robot"
subtitle: Design Overview
description: Design of a tendon-driven robot to understand continuum mechanics.
image: /assets/img/uploads/snake.jpg
optimized_image: /assets/img/uploads/snake.jpg
category: personal_projs
tags:
    - snake_robot
    - motor_control
    - continuum_mechanics
    - CAD
author: josephmei
paginate: false
---
<div style="padding-left:170px;padding-right:170px;">
    <div style="display:flex;align-items:flex-start;gap:1rem;flex-wrap:wrap;box-sizing:border-box;">
        <img src="/assets/img/uploads/snake_cropped.jpg" alt="Featured image" class="post-cover" style="max-width:400px;width:100%;height:auto;flex:0 0 320px;display:block;margin:0 8px 0 0;">
        <div style="flex:1;min-width:200px;border:1px solid #e6e6e6;padding:16px;background:#fbfbfb;border-radius:6px;box-sizing:border-box;">
            <h3 style="margin:0 0 0.5rem;padding-top: 0;">Introduction</h3>
            <p style="margin:0;">Over the summer, two friends and I collaboratively designed and built a functional tendon-driven continuum snake robot from scratch using primarily makerspace resources. Our goal was to create a low-cost, highly flexible robotic platform capable of omnidirectional bending and potential applications in inspection, search-and-rescue, or minimally invasive exploration.</p>
        </div>
    </div>
    <div style="flex:0;">
        <h2 style="margin:0 0 0.5rem;text-align:center; padding-top:20px;">Current Progress</h2>
        <h3 style="margin:0 0 0.5rem;padding-top:0px;padding-bottom:0px;">Key Design Features</h3>
        <ul style="margin:10px;">
            <li style="padding:0;"><strong>Spring Steel Backbone</strong>: Provides passive compliance and restores the robot to a straight posture when tendons are relaxed.</li>
            <li style="padding:0;"><strong>3D-printed PLA Segment Cartridges</strong>: A universal joint-inspired design that allows smooth, continuous bending in any direction while maintaining high stiffness along the length.</li>
            <li style="padding:0;"><strong>Metal Wire Tendons</strong>: Runs through the segments and are anchored at the tip. Antagonistic pulling creates precise 2-DOF bending at every point along the body.</li>
            <li style="padding:0;"><strong>Lasercut Acrylic Base Plate</strong>: Serves as a rigid mounting platform for snake robot.</li>
            <li style="padding:0;"><strong>3D-printed Motor Hubs and Press-fit Bushings</strong>: Securely couple four bipolar stepper motors to tendon pulleys.</li>
            <li style="padding:0;"><strong>Mercury Motor SM-42BYG011-25 Steppers</strong>: Selected after empirically testing with a force sensor by measuring the force required to coil the robot around obstacles. These motors were readily available and exceeded the measured torque requirements with good margin.</li>
            <li style="padding:0;"><strong>Linear Optical Sensor (Digikey PN: 1855-1015-ND)</strong>: Analog sensor attached to the robot's head for basic proximity feedback. </li>
        </ul>
        <section style="display:flex;justify-content:center;align-items:center;gap:40px;flex-wrap:wrap;margin:40px auto;max-width:1200px;">
            <figure style="flex:1 1 45%;max-width:300px;text-align:center;margin:0;">
                <img src="/assets/img/uploads/snake_cad.png" alt="Left image"
                    style="width:100%;height:auto;border-radius:12px;display:block;">
                <figcaption style="margin-top:12px;font-size:1rem;color:#555;">
                Mounting Base CAD Assembly
                </figcaption>
            </figure>
            <figure style="flex:1 1 45%;max-width:420px;text-align:center;margin:0;">
                <div class="image-carousel" style="max-width:420px;width:100%;height:300px;display:flex;
                            justify-content:center;align-items:center;overflow:hidden;
                            border-radius:8px;position:relative;margin:0 auto;">
                    <img src="/assets/img/uploads/snake_cropped.jpg" class="carousel-image first active" alt="pedal ratio"
                        style="max-width:100%;height:auto;position:absolute;transition:opacity 0.6s ease;opacity:1;">
                    <img src="/assets/img/uploads/snake2.jpg" class="carousel-image first" alt="brake"
                        style="max-width:100%;height:auto;position:absolute;transition:opacity 0.6s ease;opacity:0;">
                    <img src="/assets/img/uploads/snake_side.jpg" class="carousel-image first" alt="brake"
                        style="max-width:100%;height:auto;position:absolute;transition:opacity 0.6s ease;opacity:0;">
                    <img src="/assets/img/uploads/snake_top.jpg" class="carousel-image first" alt="throttle"
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
                Different Views of Tendon-Driven Robot and Mounting Base
                </figcaption>
            </figure>
        </section>
        <h2 style="margin:0 0 0.5rem;text-align:center; padding-top:20px;">Exciting Developments to Come!</h2>
        <ul style="margin:10px;">
            <li style="padding:0;"><strong>Implement precise piecewise-constant-curvature kinematics and closed-loop control algorithms</strong> for accurate tip positioning and repeatable turning angles.</li>
            <li style="padding:0;"><strong>Upgrade sensing suite</strong>: integrate IMU, improve object detection and reactive obstacle avoidance using the optical sensor (and potentially additional sensors).</li>
            <li style="padding:0;"><strong>Redesign segments and tendons with higher-performance materials</strong> for reduced friction, lower hysteresis, and smaller bend radius.</li>
        </ul>
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

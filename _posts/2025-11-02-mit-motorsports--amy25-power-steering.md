---
date: 2025-11-02 07:09:18
layout: post
title: "MIT Motorsports | AMY25 Power Steering"
subtitle: Design Binder
description: Design of novel power steering system to autonomously actuate a driverless car.
image: /assets/img/uploads/powersteering.png
optimized_image: /assets/img/uploads/powersteering.png
category: motorsports
tags:
    - autonomous_mech
    - machining
    - motors
    - structures
    - CAD
author: josephmei
paginate: false
---

<div style="padding-left:170px;padding-right:170px;">
    <div style="display:flex;align-items:flex-start;gap:1rem;flex-wrap:wrap;box-sizing:border-box;">
        <img src="{{ page.image }}" alt="Featured image" class="post-cover" style="max-width:400px;width:100%;height:auto;flex:0 0 320px;display:block;margin:0 8px 0 0;">
        <div style="flex:1;min-width:220px;border:1px solid #e6e6e6;padding:16px;background:#fbfbfb;border-radius:6px;box-sizing:border-box;">
            <h3 style="margin:0 0 0.5rem;padding-top: 0;">Introduction</h3>
            <p style="margin:0;">For the Model Year 2026 season, my team is pioneering its <strong>first-ever driverless racecar</strong>, a significant leap toward competing in the Formula Student Driverless event. To enable real-world validation of our autonomous algorithms, I led the design, manufacturing, and integration of a <strong>high-torque power steering system</strong> for the MY25 race car. This retrofit replaces manual steering with an electromechanical actuator, enabling precise, rapid control and positioning MIT Motorsports for success in driverless racing. Additionally, as testing for the MY26 vehicle began early in the fall, the project ran over the summer term, offering a valuable opportunity to deliver under tight timelines and manage overlapping commitments.</p>
        </div>
    </div>
    <div style="flex:0;">
        <h2 style="margin:0 0 0.5rem; text-align: center">Sponsorship Outreach</h2>
        <p style="margin:0 0 0.5rem;">Starting off this power steering project required <strong>emailing motor companies for possible sponsorships</strong>. As I was working with a very limited budget off the remaining funds from the MY25 season, securing a motor sponsorship was key to creating a reliable, robust system. After researching and emailing dozens of different companies, I was very fortunate to have secured a sponsorship with <strong>Maxon Motor</strong>, a motor company known for being a leading manufacturer of high-precision, high-quality electric drive systems. With this sponsorship, I not only secured a <strong>motor set valued at over $2500</strong> consisting of a BLDC Flat motor, a planetary gearbox, a MILE encoder, and a high-end motor controller, but I also guaranteed a <strong>continuing partnership and motor supply for the MY26 season.</strong></p>
        <section style="display:flex;justify-content:center;align-items:center;gap:40px;flex-wrap:wrap;margin:40px auto;max-width:1200px;">
        <figure style="flex:1 1 45%;max-width:300px;text-align:center;margin:0;">
            <img src="/assets/img/uploads/motor.jpeg" alt="Left image"
                style="width:100%;height:auto;border-radius:12px;display:block;">
            <figcaption style="margin-top:12px;font-size:1rem;color:#555;">
            EC 90 Flat Brushless DC Motor (PN: 892599)
            </figcaption>
        </figure>
        <figure style="flex:1 1 45%;max-width:300px;text-align:center;margin:0;">
            <img src="/assets/img/uploads/maxon.jpg" alt="Right image"
                style="width:100%;height:auto;border-radius:12px;display:block;">
        </figure>
        <figure style="flex:1 1 45%;max-width:300px;text-align:center;margin:0;">
            <img src="/assets/img/uploads/motor2.jpeg" alt="Right image"
                style="width:100%;height:auto;border-radius:12px;display:block;">
            <figcaption style="margin-top:12px;font-size:1rem;color:#555;">
            Sponsorship Package with Connectors and Motor Configuration
            </figcaption>
        </figure>
        </section>
        <h2 style="margin:0 0 0.5rem; text-align: center">Design Overview</h2>
        <h3 style="margin:0 0 0.5rem;padding-top:0">Laying Out Design Requirements</h3>
        <p style="margin:0 0 0.5rem;">For the design process of power steering, I first started by identifying <strong>key design requirements</strong> that govern the overarching system. To determine the <strong>steering torque</strong> required to actuate the car, I used a force sensor to measure the force required to turn the tires when the car is stationary, providing an upper bound for the torque requirement. To determine the <strong>steering speed</strong>, I used telemetry data from past competitions as well as GoPro footage of drivers on testing trips to get a rough estimate of the max steering speed required by the motor. These measurements allowed me to pick and size a capable motor for the system.</p>
        <div style="display:flex;align-items:flex-start;gap:1rem;flex-wrap:wrap;box-sizing:border-box;">
            <div style="flex:1;min-width:220px;border:1px solid #e6e6e6;padding:16px;background:#fbfbfb;border-radius:6px;box-sizing:border-box;">
                <h4 style="padding-top:0;padding-bottom: 0"> Some Key Design Requirements: </h4>
                <ul style="line-height:1.2;padding-top:0;padding-bottom:0">
                <li><strong>Steering Torque Requirement:</strong> The motor must be able to provide 8.4 Nm of steering torque at peak power.</li>
                <li><strong>Steering Rate:</strong> The motor must be able to spin in the steering column at a speed of 53.92 RPM.</li>
                <li><strong>Range of Motion:</strong> The range of motion of the system must be able to cover the max steering rack travel of 1.5 inches on each side.</li>
                <li><strong>Resolution and Backlash:</strong> Minimize steering backlash in the system by correctly tensioning the belt and limiting the system stack up.</li>
                </ul>
            </div>
            <figure style="max-width:400px;width:100%;margin:40px auto;text-align:center;position:relative;">
            <div style="max-width:400px;width:100%;height:250px;display:flex;
                        justify-content:center;align-items:center;overflow:hidden;
                        border-radius:8px;position:relative;margin:0 auto;">
                <!-- Images -->
                <img src="/assets/img/uploads/telemetry.png" alt="Ergo Design 3"
                    style="max-width:100%;height:auto;position:absolute;transition:opacity 0.6s ease;opacity:1;">
            </div>
            <!-- Caption -->
            <figcaption style="margin-top:0px;font-size:0.95rem;color:#555;">
                MATLAB Script to Parse Through Telemetry Data on Steering Steeing Speed
            </figcaption>
            </figure>
        </div>
        <br>
        <br>
        <p style="margin:0 0 0.5rem;">Below is also a MATLAB Script I created to model the temperature of the motor over time given a constant power input. The script uses basic thermodynamic principles, modeling the system as a thermal circuit using a differential equation.</p>
        <section style="display:flex;justify-content:center;align-items:center;gap:10px;flex-wrap:wrap;margin:0 auto;max-width:1400px;padding:0;">
            <!-- ===== CODE BLOCK (LEFT, WIDER, NO BACKGROUND) ===== -->
            <div style="flex:1 1 65%;max-width:850px;color:#222;
                        padding:0px;font-family:'Courier New', monospace;
                        font-size:0.25rem;line-height:1.15;overflow-x:auto;">
            <pre style="margin:0;"><code>clc; close all; clear
% Motor Thermal Model Simulation
% CHANGE PARAMS HERE
T_a = 25;                        % Ambient temperature (C)
Torque = 8.4;                    % Operating Torque (N/m)
RPM = 53.86;                     % Operating Speed (RPM)
Efficiency = 0.87;               % Max Efficiency
Max_Temp = 125;                  % Max Temp of Windings (C)
R_wh = 1.02;    % Thermal resistance winding-housing (K/W)
R_ha = 1.37;    % Thermal resistance housing-ambient (K/W)
tau_w = 31.9;   % Thermal time constant winding (s)
tau_m = 204;    % Thermal time constant motor (s)
I_nom = 8.72;                 % Nominal Current (A)
R_term = 0.28;                % Terminal Resistance (Ohms)
Key = false;                     % If true --> Calculate with Total Power Loss
                                 % If false --> Calculate with Power Loss in Windings
% -------------------------------------------------------------------
RPM2RadPerSec = 2*pi/60;
RadPerSec = RPM * RPM2RadPerSec; % Operating Speed (rad/s)
P_out = Torque * RadPerSec;      % Output Power (W)
P_in = P_out/Efficiency;         % Input Power (W)
P_lossTot = P_in - P_out;            % Power loss (W)
P_lossWind = I_nom^2 * R_term;          % Power loss in windings (W) I^2 * R_terminal;

if(Key)
    P = P_lossTot;
    fprintf("Calculating w/ Total Power Loss: %.2f W\n" , P_lossTot)
else
    P = P_lossWind;
    fprintf("Calculating w/ Windings Power Loss: %.2f W\n" , P_lossWind)
end

% Thermal capacitances (approximated)
C_w = tau_w / R_wh;  % Winding capacitance (J/K)
C_h = tau_m / R_ha;  % Housing capacitance (J/K)

% Time span for simulation (seconds) - enough to reach steady-state
start_time = 0;
end_time = tau_m * 6;        % Reaches 99.9% of Steady State
tspan = [start_time end_time];

% Initial conditions: start at ambient
T0 = [T_a; T_a];  % [T_winding; T_housing]

% Define the ODE system
odefun = @(t, T) [
    (P - (T(1) - T(2)) / R_wh) / C_w;                  % dT_w/dt
    ((T(1) - T(2)) / R_wh - (T(2) - T_a) / R_ha) / C_h      % dT_h/dt
];

% Solve the ODEs
[t, T] = ode45(odefun, tspan, T0);</code></pre>
            </div>
            <!-- ===== IMAGE (RIGHT, NARROWER) ===== -->
            <figure style="flex:1 1 30%;max-width:400px;text-align:center;margin:0;">
                <img src="/assets/img/uploads/thermal.png" alt="Diagram or reference"
                    style="width:100%;height:auto;display:block;border-radius:8px;">
                <figcaption style="margin-top:12px;font-size:1rem;color:#555;">
                Motor Components Thermal Simulation Visualization
                </figcaption>
            </figure>
        </section>
        <h3 style="margin:0 0 0.5rem;">Structural Calculations</h3>
        <p style="margin:0 0 0.5rem;">Next in the design process, I performed <strong>structural hand calculations</strong> and <strong>belt/pulley selections</strong>. The structural calculations were a simple beam bending problem to determine the internal moment and shear forces as well as the maximum deflection. Resolution and backlash were big concerns for the performance of the autonomous system, so minimizing deflection and ensuring a properly sized and tensioned belt were vital to the design process.</p>
        <figure style="max-width:900px;width:100%;margin:0px auto;text-align:center;position:relative;">
            <div class="image-carousel"
                style="max-width:900px;width:100%;height:600px;display:flex;
                        justify-content:center;align-items:center;overflow:hidden;
                        border-radius:8px;position:relative;margin:0 auto;">
                <!-- Images -->
                <img src="/assets/img/uploads/ps_handcalcs.png" class="carousel-image first active" alt="Ergo Design 3"
                    style="max-width:100%;height:auto;position:absolute;transition:opacity 0.6s ease;opacity:1;">
                <img src="/assets/img/uploads/ps_belt.png" class="carousel-image first" alt="Ergo Design 3B"
                    style="max-width:100%;height:auto;position:absolute;transition:opacity 0.6s ease;opacity:0;">
                <!-- Controls -->
                <button class="carousel-btn first-prev"
                        style="position:absolute;top:50%;left:10px;transform:translateY(-50%);
                            background:rgba(0,0,0,0.4);color:white;border:none;border-radius:50%;
                            width:30px;height:30px;cursor:pointer;">‹</button>
                <button class="carousel-btn first-next"
                        style="position:absolute;top:50%;right:10px;transform:translateY(-50%);
                            background:rgba(0,0,0,0.4);color:white;border:none;border-radius:50%;
                            width:30px;height:30px;cursor:pointer;">›</button>
            </div>
            <!-- Caption -->
            <figcaption style="margin-top:5px;font-size:0.95rem;color:#555;">
                (1) Beam Bending Calculations to Determine the Deflection and Stress of the Mounting Plate. <br>
                (2) Selection Considerations for an HTD Neoprene Belt and Pulley.
            </figcaption>
        </figure>
        <h3 style="margin:0 0 0.5rem;">CAD and Manufacturing</h3>
        <img src="/assets/img/uploads/powersteering.png" alt="Featured image" style="max-width:400px;width:100%;height:auto;">
        <p style="margin:0 0 0.5rem;">Lastly, I used <strong>Onshape</strong> to model the power steering assembly in CAD, going through several design review presentations with the team to arrive to the final product. With the CAD ready, a manufacturing plan was set in place to fabricate all the components in-house, which entailed <strong>waterjetting plates</strong>, <strong>turning spacers</strong>, and <strong>milling pulleys.</strong></p>
        <div style="display:flex;align-items:flex-start;gap:1rem;flex-wrap:wrap;box-sizing:border-box;">
            <div style="flex:1;min-width:220px;border:1px solid #e6e6e6;padding:16px;background:#fbfbfb;border-radius:6px;box-sizing:border-box;">
                <p style="margin:0;">The motor and belt system are mounted to the steering rack using two custom waterjetted plates. The bottom plate features a slotted interface that simplifies alignment and integration with the steering rack. The top plate incorporates a set of precisely positioned slots in an arc, designed to enable accurate belt pretensioning. Pretension is achieved by pivoting the assembly about one bolted joint, allowing controlled adjustment of belt tension and decoupling. </p>
            </div>
            <figure style="max-width:400px;width:100%;margin:40px auto;text-align:center;position:relative;margin-top:0">
            <div class="image-carousel"
                style="max-width:400px;width:100%;height:320px;display:flex;
                        justify-content:center;align-items:center;overflow:hidden;
                        border-radius:8px;position:relative;margin:0 auto;padding-top:0">
                <!-- Images -->
                <img src="/assets/img/uploads/ps_plates.png" class="carousel-image second active" alt="brakecad"
                    style="max-width:100%;height:auto;position:absolute;transition:opacity 0.6s ease;opacity:1;">
                <img src="/assets/img/uploads/ps_topplate.png" class="carousel-image second" alt="Ergo Design 3B"
                    style="max-width:100%;height:auto;position:absolute;transition:opacity 0.6s ease;opacity:0;">
                <img src="/assets/img/uploads/Top_Plate_Drawing.png" class="carousel-image second" alt="Ergo Design 3B"
                    style="max-width:100%;height:auto;position:absolute;transition:opacity 0.6s ease;opacity:0;">\
                <img src="/assets/img/uploads/Bottom_Plate_Drawing.png" class="carousel-image second" alt="Ergo Design 3B"
                    style="max-width:100%;height:auto;position:absolute;transition:opacity 0.6s ease;opacity:0;">
                <!-- Controls -->
                <button class="carousel-btn second-prev"
                        style="position:absolute;top:50%;left:10px;transform:translateY(-50%);
                            background:rgba(0,0,0,0.4);color:white;border:none;border-radius:50%;
                            width:30px;height:30px;cursor:pointer;">‹</button>
                <button class="carousel-btn second-next"
                        style="position:absolute;top:50%;right:10px;transform:translateY(-50%);
                            background:rgba(0,0,0,0.4);color:white;border:none;border-radius:50%;
                            width:30px;height:30px;cursor:pointer;">›</button>
            </div>
            <!-- Caption -->
            <figcaption style="margin-top:8px;font-size:0.95rem;color:#555;">
                (1) Mounting Plates Iso View CAD <br> (2) Mounting Plates with Arc Slots Top View CAD <br> (3) Top Plate Technical Drawing <br> (4) Bottom Plate Technical Drawing
            </figcaption>
            </figure>
        </div>
        <div style="display:flex;align-items:flex-start;gap:1rem;flex-wrap:wrap;box-sizing:border-box;">
            <figure style="max-width:400px;width:100%;margin:40px auto;text-align:center;position:relative;margin-top:0">
            <div class="image-carousel"
                style="max-width:400px;width:100%;height:320px;display:flex;
                        justify-content:center;align-items:center;overflow:hidden;
                        border-radius:8px;position:relative;margin:0 auto;">
                <!-- Images -->
                <img src="/assets/img/uploads/steering_column.jpg" class="carousel-image third active" alt="brakecad"
                    style="max-width:100%;height:auto;position:absolute;transition:opacity 0.6s ease;opacity:1;">
                <img src="/assets/img/uploads/ps_column.png" class="carousel-image third" alt="Ergo Design 3B"
                    style="max-width:100%;height:auto;position:absolute;transition:opacity 0.6s ease;opacity:0;">
                <img src="/assets/img/uploads/match_drill.jpg" class="carousel-image third" alt="Ergo Design 3B"
                    style="max-width:100%;height:auto;position:absolute;transition:opacity 0.6s ease;opacity:0;">
                <!-- Controls -->
                <button class="carousel-btn third-prev"
                        style="position:absolute;top:50%;left:10px;transform:translateY(-50%);
                            background:rgba(0,0,0,0.4);color:white;border:none;border-radius:50%;
                            width:30px;height:30px;cursor:pointer;">‹</button>
                <button class="carousel-btn third-next"
                        style="position:absolute;top:50%;right:10px;transform:translateY(-50%);
                            background:rgba(0,0,0,0.4);color:white;border:none;border-radius:50%;
                            width:30px;height:30px;cursor:pointer;">›</button>
            </div>
            <!-- Caption -->
            <figcaption style="margin-top:8px;font-size:0.95rem;color:#555;">
                (1) Steering Column and Pulley Mounted Together <br> (2) Steering Column and Pulley CAD <br> (3) Manual Mill Setup for Match-drill
            </figcaption>
            </figure>
            <div style="flex:1;min-width:220px;border:1px solid #e6e6e6;padding:16px;background:#fbfbfb;border-radius:6px;box-sizing:border-box;">
                <p style="margin:0;">To enable belt-driven actuation, system components were modified to mount pulleys onto both the steering column and motor shaft. For the steering column, I used a manual mill to match-drill and ream a through-hole in the pulley and column. This created a very smooth, tight, and snug fit for a shoulder bolt to secure the assembly. For the motor shaft, broaching was initially considered to create the keyseat (which would have been awesome) but none of the machine shops had the correct size. Instead, due to budget constraints, I ordered and used an extended-length endmill to machine the keyseat directly into the pulley.</p>
            </div>
        </div>
        <br>
        <div style="display:flex;align-items:flex-start;gap:1rem;flex-wrap:wrap;box-sizing:border-box;">
            <div style="flex:1;min-width:220px;border:1px solid #e6e6e6;padding:16px;background:#fbfbfb;border-radius:6px;box-sizing:border-box;">
                <p style="margin:0;">Several 3D-printed components were fabricated to support various aspects of the system. A column sleeve was printed to act as a spacer, ensuring proper pulley height alignment on the steering column. A custom motor hub and cover were designed to provide light water protection—particularly important given the motor’s outrunner configuration. Additionally, pulley flanges were printed as a precautionary measure to mitigate belt slippage. All parts were produced using a Bambu X1-Carbon printer.</p>
            </div>
            <figure style="max-width:400px;width:100%;margin:40px auto;text-align:center;position:relative;margin-top:0">
            <div class="image-carousel"
                style="max-width:400px;width:100%;height:320px;display:flex;
                        justify-content:center;align-items:center;overflow:hidden;
                        border-radius:8px;position:relative;margin:0 auto;">
                <!-- Images -->
                <img src="/assets/img/uploads/3dp.jpg" class="carousel-image fourth active" alt="brakecad"
                    style="max-width:100%;height:auto;position:absolute;transition:opacity 0.6s ease;opacity:1;">
                <img src="/assets/img/uploads/ps_hub.png" class="carousel-image fourth" alt="Ergo Design 3B"
                    style="max-width:100%;height:auto;position:absolute;transition:opacity 0.6s ease;opacity:0;">
                <img src="/assets/img/uploads/ps_pulley.png" class="carousel-image fourth" alt="Ergo Design 3B"
                    style="max-width:100%;height:auto;position:absolute;transition:opacity 0.6s ease;opacity:0;">
                <!-- Controls -->
                <button class="carousel-btn fourth-prev"
                        style="position:absolute;top:50%;left:10px;transform:translateY(-50%);
                            background:rgba(0,0,0,0.4);color:white;border:none;border-radius:50%;
                            width:30px;height:30px;cursor:pointer;">‹</button>
                <button class="carousel-btn fourth-next"
                        style="position:absolute;top:50%;right:10px;transform:translateY(-50%);
                            background:rgba(0,0,0,0.4);color:white;border:none;border-radius:50%;
                            width:30px;height:30px;cursor:pointer;">›</button>
            </div>
            <!-- Caption -->
            <figcaption style="margin-top:8px;font-size:0.95rem;color:#555;">
                (1) All 3D-printed Components <br> (2) Motor Hub CAD <br> (3) Pulley Flanges CAD
            </figcaption>
            </figure>
        </div>
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
  setupCarousel('second');
  setupCarousel('third');
  setupCarousel('fourth');
</script>

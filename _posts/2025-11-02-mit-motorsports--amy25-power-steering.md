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
            <p style="margin:0;">For the Model Year 2026 season, my team is pioneering its <strong>first-ever driverless racecar</strong>, a significant leap toward competing in the Formula Student Driverless event. To enable real-world validation of our robust autonomous algorithms, I led the design, manufacturing, and integration of a <strong>high-torque power steering system</strong> for the MY25 race car. This retrofit replaces manual steering with an electromechanical actuator, enabling precise, rapid control for autonomous testing and positioning MIT Motorsports for success in driverless racing.</p>
        </div>
    </div>
    <div style="flex:0;">
        <h3 style="margin:0 0 0.5rem;">Sponsorship Outreach</h3>
        <p style="margin:0 0 0.5rem;">Starting off this power steering project required <strong>emailing motor companies for possible sponsorships</strong>. As I was working with a very limited budget off the remaining funds from the MY25 season, securing a motor sponsorship was key to creating a reliable, robust system. After researching and emailing dozens of different companies, I was very fortunate to have secured a sponsorship with <strong>Maxon Motor</strong>, a motor company known for being a leading manufacturer of high-precision, high-quality electric drive systems. With this sponsorship, I not only secured a <strong>motor set valued at over $2500 consisting of a BLDC Flat motor, a planetary gearbox, a MILE encoder, and a high-end motor controller</strong>, but I also guaranteed a <strong>continuing partnership and motor supply for the MY26 season.</strong></p>
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
        <h3 style="margin:0 0 0.5rem;">Design Overview</h3>
        <p style="margin:0 0 0.5rem;">For the design process, I first started by identifying <strong>key design requirements</strong> that govern the overarching system. To determine the <strong>steering torque</strong> required to actuate the car, I used a force sensor to measure the force required to turn the tires when the car is stationary, providing an upper bound for the torque requirement. To determine the <strong>steering speed</strong>, I used telemetry data from past competitions as well as GoPro footage of drivers on testing trips to get a rough estimate of the max steering speed required by the motor. These measurements allowed me to pick and size a capable motor for the system.</p>
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
        <section style="display:flex;justify-content:center;align-items:center;gap:40px;flex-wrap:wrap;margin:40px auto;max-width:1200px;">
        <!-- ===== CODE BLOCK (LEFT) ===== -->
        <section style="display:flex;justify-content:center;align-items:center;gap:40px;flex-wrap:wrap;margin:40px auto;max-width:1400px;">
            <!-- ===== CODE BLOCK (LEFT, WIDER, NO BACKGROUND) ===== -->
            <div style="flex:1 1 65%;max-width:850px;color:#222;
                        padding:10px;font-family:'Courier New', monospace;
                        font-size:0.95rem;line-height:1.5;overflow-x:auto;">
            <pre><code>clc; close all; clear
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
        <p style="margin:0 0 0.5rem;padding-top: 20px;">I then performed <strong>structural hand calculations</strong> to inform my modeling, drawing FBDs, analyzing shear and bending diagrams, and performing lug analyses. These calculations were used to optimize the mass and geometry of the system components to ensure minimal deflection while being able to withstand the heavy applied loads.</p>
        <div class="carousel-pair"
            style="display:flex;justify-content:center;align-items:flex-start;gap:40px;flex-wrap:wrap;margin:20px auto;text-align:center;">
        <!-- ===== LEFT CAROUSEL ===== -->
        <figure style="flex:0 1 480px;max-width:600px;margin:0;position:relative;">
            <div class="image-carousel"
                style="max-width:600px;width:100%;height:250px;display:flex;
                        justify-content:center;align-items:flex-start;overflow:hidden;
                        border-radius:12px;position:relative;margin:0 auto;">
            <img src="/assets/img/uploads/pratio.png" class="carousel-image left active" alt="pedal ratio"
                style="max-width:100%;height:auto;position:absolute;transition:opacity 0.6s ease;opacity:1;">
            <img src="/assets/img/uploads/brake.png" class="carousel-image left" alt="brake"
                style="max-width:100%;height:auto;position:absolute;transition:opacity 0.6s ease;opacity:0;">
            <img src="/assets/img/uploads/throttle.png" class="carousel-image left" alt="throttle"
                style="max-width:100%;height:auto;position:absolute;transition:opacity 0.6s ease;opacity:0;">
            <img src="/assets/img/uploads/base.png" class="carousel-image left" alt="base"
                style="max-width:100%;height:auto;position:absolute;transition:opacity 0.6s ease;opacity:0;">
            <button class="carousel-btn left-prev"
                    style="position:absolute;top:50%;left:15px;transform:translateY(-50%);
                            background:rgba(0,0,0,0.4);color:white;border:none;border-radius:50%;
                            width:40px;height:40px;cursor:pointer;font-size:1.2rem;">‹</button>
            <button class="carousel-btn left-next"
                    style="position:absolute;top:50%;right:15px;transform:translateY(-50%);
                            background:rgba(0,0,0,0.4);color:white;border:none;border-radius:50%;
                            width:40px;height:40px;cursor:pointer;font-size:1.2rem;">›</button>
            </div>
            <figcaption style="margin-top:12px;font-size:1rem;color:#555;">
            Force and Moment Balance to Determine Stress and Deflection in Pedalbox Components
            </figcaption>
        </figure>
        <!-- ===== RIGHT CAROUSEL ===== -->
        <figure style="flex:0 1 480px;max-width:600px;margin:0;position:relative;">
            <div class="image-carousel"
                style="max-width:600px;width:100%;height:250px;display:flex;
                        justify-content:center;align-items:flex-start;overflow:hidden;
                        border-radius:12px;position:relative;margin:0 auto;">
            <img src="/assets/img/uploads/bear1.png" class="carousel-image right active" alt="bearing 1"
                style="max-width:100%;height:auto;position:absolute;transition:opacity 0.6s ease;opacity:1;">
            <img src="/assets/img/uploads/bear2.png" class="carousel-image right" alt="bearing 2"
                style="max-width:100%;height:auto;position:absolute;transition:opacity 0.6s ease;opacity:0;">
            <button class="carousel-btn right-prev"
                    style="position:absolute;top:50%;left:15px;transform:translateY(-50%);
                            background:rgba(0,0,0,0.4);color:white;border:none;border-radius:50%;
                            width:40px;height:40px;cursor:pointer;font-size:1.2rem;">‹</button>
            <button class="carousel-btn right-next"
                    style="position:absolute;top:50%;right:15px;transform:translateY(-50%);
                            background:rgba(0,0,0,0.4);color:white;border:none;border-radius:50%;
                            width:40px;height:40px;cursor:pointer;font-size:1.2rem;">›</button>
            </div>
            <figcaption style="margin-top:12px;font-size:1rem;color:#555;">
            Lug Analyses for Tabs
            </figcaption>
        </figure>
        </div>
        <div style="display:flex;align-items:flex-start;gap:1rem;flex-wrap:wrap;box-sizing:border-box;">
            <div style="flex:1;min-width:220px;border:1px solid #e6e6e6;padding:16px;background:#fbfbfb;border-radius:6px;box-sizing:border-box;">
                <p style="margin:0;">This is an example of a calculation performed to determine the necessary size of the brake pedal. After completing a force and moment balance to determine the reaction forces, various cuts were taken along the pedal to determine the max shear and tensile forces as well as deflection. This then informed the necessary sizing of the pedal's cross-sectional geometry.</p>
            </div>
            <img src="/assets/img/uploads/calcs.png" alt="brake calcs" class="post-cover" style="max-width:600px;width:100%;height:auto;flex:0 0 320px;display:block;margin:0 8px 0 0;">
        </div>
        <br>
        <p style="margin:0 0 0.5rem;padding-top: 20px;">Lastly, after <strong>modeling the pedalbox in CAD using Siemens NX,</strong> I then <strong>manufactured all the components in-house with CNC machinery</strong>, utilizing the lathe, CNC mill, and waterjet to create all the parts with precision.</p>
        <div style="display:flex;align-items:flex-start;gap:1rem;flex-wrap:wrap;box-sizing:border-box;">
            <div style="flex:1;min-width:220px;border:1px solid #e6e6e6;padding:16px;background:#fbfbfb;border-radius:6px;box-sizing:border-box;">
                <p style="margin:0;">An I-beam design for both the brake and throttle pedal was selected to optimize mass while maintaining structural rigidity. Torsional springs are attached to both to ensure smooth return travel. The pedals were machined from a solid aluminum block on a HAAS VF-2 CNC machine utilizing a CAM file. Custom soft jaws for the brake pedal were also created in the HAAS VF-2 to accommodate the multiple machining operations needed for the brake pedal.</p>
            </div>
            <figure style="max-width:400px;width:100%;margin:40px auto;text-align:center;position:relative;">
            <div class="image-carousel"
                style="max-width:400px;width:100%;height:320px;display:flex;
                        justify-content:center;align-items:center;overflow:hidden;
                        border-radius:8px;position:relative;margin:0 auto;">
                <!-- Images -->
                <img src="/assets/img/uploads/brakecad.png" class="carousel-image fourth active" alt="brakecad"
                    style="max-width:100%;height:auto;position:absolute;transition:opacity 0.6s ease;opacity:1;">
                <img src="/assets/img/uploads/throttlecad.png" class="carousel-image fourth" alt="Ergo Design 3B"
                    style="max-width:100%;height:auto;position:absolute;transition:opacity 0.6s ease;opacity:0;">
                <img src="/assets/img/uploads/brakejaws.jpg" class="carousel-image fourth" alt="Ergo Design 3B"
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
                (1) Brake Pedal CAD - (2) Throttle Pedal CAD - (3) Custom-Made Soft Jaws for CNC Milling
            </figcaption>
            </figure>
        </div>
        <div style="display:flex;align-items:flex-start;gap:1rem;flex-wrap:wrap;box-sizing:border-box;">
            <figure style="max-width:400px;width:100%;margin:40px auto;text-align:center;position:relative;">
            <div class="image-carousel"
                style="max-width:400px;width:100%;height:320px;display:flex;
                        justify-content:center;align-items:center;overflow:hidden;
                        border-radius:8px;position:relative;margin:0 auto;">
                <!-- Images -->
                <img src="/assets/img/uploads/tubes.png" class="carousel-image fifth active" alt="brakecad"
                    style="max-width:100%;height:auto;position:absolute;transition:opacity 0.6s ease;opacity:1;">
                <img src="/assets/img/uploads/plugs.png" class="carousel-image fifth" alt="Ergo Design 3B"
                    style="max-width:100%;height:auto;position:absolute;transition:opacity 0.6s ease;opacity:0;">
                <img src="/assets/img/uploads/plugsreal.jpg" class="carousel-image fifth" alt="Ergo Design 3B"
                    style="max-width:100%;height:auto;position:absolute;transition:opacity 0.6s ease;opacity:0;">
                <!-- Controls -->
                <button class="carousel-btn fifth-prev"
                        style="position:absolute;top:50%;left:10px;transform:translateY(-50%);
                            background:rgba(0,0,0,0.4);color:white;border:none;border-radius:50%;
                            width:30px;height:30px;cursor:pointer;">‹</button>
                <button class="carousel-btn fifth-next"
                        style="position:absolute;top:50%;right:10px;transform:translateY(-50%);
                            background:rgba(0,0,0,0.4);color:white;border:none;border-radius:50%;
                            width:30px;height:30px;cursor:pointer;">›</button>
            </div>
            <!-- Caption -->
            <figcaption style="margin-top:8px;font-size:0.95rem;color:#555;">
                (1) Base Cylinders & Tabs CAD - (2) Side Plugs CAD - (3) Side View of Base
            </figcaption>
            </figure>
            <div style="flex:1;min-width:220px;border:1px solid #e6e6e6;padding:16px;background:#fbfbfb;border-radius:6px;box-sizing:border-box;">
                <p style="margin:0;">Steel circular tubes were selected to reduce mass and deflection under applied forces. The tubes were cut to rough length using a cold saw and then precisely turned to their final dimensions on a lathe. Tabs were cut using a waterjet and accurately reamed on a manual mill to minimize system compliance. The tabs were designed to span the tubes, enhancing structural integrity and ensuring proper alignment for welding. Steel plugs were then welded onto the ends of the base tubes to accommodate quick-release pins and shoulder bolts for the adjustment mechanism. Designed for minimal mass, the plugs were precisely turned on a lathe to meet the tight tolerances of the tubes. The rear tube plug was also tapped to secure the shoulder bolt.
</p>
            </div>
        </div>
        <br>
        <div style="display:flex;align-items:flex-start;gap:1rem;flex-wrap:wrap;box-sizing:border-box;">
            <div style="flex:1;min-width:220px;border:1px solid #e6e6e6;padding:16px;background:#fbfbfb;border-radius:6px;box-sizing:border-box;">
                <p style="margin:0;">The pedalbox is mounted to the frame using quick-release pins attached to side wave rails for adjustable positioning. Shoulder bolts on the rear tube slide into the wave rail slots, while quick-release pins secure the front tube, allowing the pedalbox to be adjusted to three distinct positions in seconds. The wave rails were precision-cut on a waterjet, reamed on a manual mill for accuracy, and formed using a sheet metal bender.</p>
            </div>
            <figure style="max-width:400px;width:100%;margin:0px auto;text-align:flex-start;position:relative;">
            <div style="max-width:400px;width:100%;height:320px;display:flex;
                        justify-content:center;overflow:hidden; text-align:flex-start;
                        border-radius:8px;position:relative;margin:0 auto;">
                <img src="/assets/img/uploads/rails.png" alt="brakecad"
                    style="max-width:100%;height:auto;position:absolute;">
            </div>
            <!-- Caption -->
            <figcaption style="margin-top:8px;font-size:0.95rem;color:#555;">
                Side Wave Rails CAD
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

  setupCarousel('left');
  setupCarousel('right');
  setupCarousel('third');
  setupCarousel('fourth');
  setupCarousel('fifth');
</script>

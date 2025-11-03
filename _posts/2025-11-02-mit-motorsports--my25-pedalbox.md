---
date: 2025-06-21 07:16:27
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
            <p style="margin:0;">For the Model Year 2025 season, I was tasked with designing a <strong>custom pedalbox</strong> to integrate the throttle, brake, master cylinders, and potentiometers into a single, adjustable platform. This project required balancing <strong>structural strength</strong>, <strong>adjustability</strong>, and <strong>minimal weight</strong> to enhance driver control and vehicle performance.</p>
        </div>
    </div>
    <img src="/assets/img/uploads/pedalbox.png" alt="Featured image" style="max-width:600px;width:100%;height:auto">
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
            <figure style="max-width:400px;width:100%;margin:40px auto;text-align:center;position:relative;">
            <div class="image-carousel"
                style="max-width:400px;width:100%;height:320px;display:flex;
                        justify-content:center;align-items:center;overflow:hidden;
                        border-radius:8px;position:relative;margin:0 auto;">
                <!-- Images -->
                <img src="/assets/img/uploads/ergo1.png" class="carousel-image third active" alt="Ergo Design 3"
                    style="max-width:100%;height:auto;position:absolute;transition:opacity 0.6s ease;opacity:1;">
                <img src="/assets/img/uploads/ergo2.png" class="carousel-image third" alt="Ergo Design 3B"
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
                Ergonomic Jig Layout to Inform Design Requirements
            </figcaption>
            </figure>
        </div>
        <br>
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

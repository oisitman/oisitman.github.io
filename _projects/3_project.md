---
layout: page
title: Robo-Mag-CE
description: Trajectory Planning and Control for Robotic Magnetic Manipulation
img: assets/img/GI_EPM.png
importance: 1
category: Academic
related_publications: isitman2024trajectory
---



<script type="text/javascript" async
    src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>
<style>
    .justify-text {
        text-align: justify;
    }
</style>


<div class="row align-items-center">
    <!-- Image Section -->
    <div class="col-md-6">
        {% include figure.html path="assets/img/GI_EPM.png" class="img-fluid rounded z-depth-1" %}
    </div>

    <!-- Text Section -->
    <div class="col-md-6 justify-text">
    <p>
        <strong>Robotic magnetic manipulation</strong> offers a minimally invasive approach to gastrointestinal examinations 
        through capsule endoscopy. However, controlling such systems using external permanent magnets (EPM) is challenging 
        due to <strong>nonlinear magnetic interactions</strong>, especially when there are complex navigation requirements such 
        as avoidance of sensitive tissues.
    </p>
    <p>
        In this work, we present a novel <strong>trajectory planning and control</strong> method incorporating dynamics and 
        navigation requirements, using a single EPM fixed to a robotic arm to manipulate an internal permanent magnet (IPM). 
        Our approach employs a <strong>constrained iterative linear quadratic regulator</strong> that considers the dynamics 
        of the IPM to generate optimal trajectories for both the EPM and IPM.
    </p>
    </div>
</div>

<p class="justify-text">
    Extensive <strong>simulations</strong> and <strong>real-world</strong> experiments, motivated by capsule endoscopy operations, 
    demonstrate the robustness of the method, showcasing resilience to <strong>external disturbances</strong> and 
    <strong>precise control</strong> under varying conditions. The experimental results show that the IPM reaches the goal 
    position with a maximum mean error of 0.18 cm and a standard deviation of 0.21 cm. This work introduces a unified 
    framework for constrained trajectory optimization in magnetic manipulation, directly incorporating both the IPM's 
    dynamics and the EPM's manipulability.
</p>


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/block.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Block diagram of the control and planning phases for robotic magnetic capsule endoscopy. The planning phase (left) utilizes iLQR to generate optimal state trajectories \( \mathbf{x}^* \), input trajectories \( \mathbf{u}^* \), and time-varying optimal controller gains \( \mathbf{K}(k) \), based on user-defined constraints and initial/goal positions. 

    In the control phase (right), joint angles \( \mathbf{q} \) are measured from the robotic arm encoders, and the 3D position of the IPM is obtained through object detection and triangulation using two orthogonal cameras. The Extended Kalman Filter (EKF) then estimates the IPM's position \( \mathbf{p}_I \) and velocity \( \mathbf{v}_I \), which are used to update the control input \( \mathbf{u} \) and follow the optimal trajectories. 

    The system includes the EPM for external magnetic manipulation and the IPM within the targeted environment, with the IPM dimensions shown in the figure and given in millimeters.
</div>


<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/video/rmce.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true  %}
    </div>
</div>
<div class="caption">
    Real world experimentation of the proposed method
</div>


<div class="caption">
    <iframe src="https://github.com/oisitman/RMM_figures/blob/main/fig_3d.html" width="100%" height="600" style="border:none;"></iframe>
</div>

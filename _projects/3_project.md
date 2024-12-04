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





<div class="row justify-content-sm-center">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/sim1.gif" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/sim1.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    (a) Simulation Case 1 visualization. (b) Time series data of the optimal IPM trajectory. (c) IPM velocities along the trajectory. (d) Time series data of the optimal EPM trajectory. (e) Joint angles of the robotic arm. (f) Time series data of the IPM orientation. (g) Condition number (Κ) analysis of the robotic arm’s manipulability.
</div>



<div class="row justify-content-sm-center">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/sim2.gif" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/sim2.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    In Case 2, the initial configuration of the robot is chosen to achieve the same IPM position and orientation but with a poorer initial condition number (5, compared to 2.7 in Case 1). The optimal trajectory is designed to improve the condition number over time while adhering to the imposed constraints on position, velocity, joint limits, and orientation. 
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.html path="assets/img/exp.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
<div class="col-sm-4 mt-3 mt-md-0">
    <iframe src="https://oisitman.github.io/RMM_figures/fig_3d.html" width="100%" height="270" style="border:none;"></iframe>
</div>
<div class="caption">
    Real-world experimental results showing repetitive IPM trajectories in 3D space under the given constraints, including obstacle avoidance (red sphere). Each colored line represents an individual trial of the IPM navigating around the obstacle, demonstrating the system's ability to consistently follow the desired path while respecting imposed constraints.
</div>


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/exp_res.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Experimental results showing the time evolution of IPM position, IPM velocity, and EPM position along the X, Y, and Z axes under closed-loop control. The left column shows the IPM position, with mean position (solid line) and standard deviation (shaded area) around the mean, alongside goal positions (red crosses). The middle column displays IPM velocity, with mean velocity and standard deviation, and includes velocity constraints (dashed red line) in the Y-axis plot. The right column represents EPM position with mean position (solid line) and standard deviation (shaded area) around the mean, as well as position constraints in the Z-axis plot (dashed red line). This figure demonstrates the tracking accuracy and stability of both IPM and EPM under the control framework.
</div>

<div class="caption">
    <iframe src="https://drive.google.com/file/d/1idN0-IWbAEmW1vUn6zzecPUowe1d8bLj/view" width="100%" height="600" style="border:none;"></iframe>
</div>




---
title: "Inverted Pendulum Experiment"
layout: default
permalink: /experiments/Experiment_inverted_pendulum/
---


## Inverted Pendulum

The **ball and beam** system is a classic **benchmark problem in control engineering** that is widely used to analyze and evaluate feedback control strategies.

### System Description
The system consists of:
- A **beam** that rotates about a pivot point  
- A **ball** that rolls along the beam under the influence of gravity  
- An **actuator** (such as a motor or servo) that adjusts the beam angle  
- A **sensor** that measures the position of the ball along the beam  

By changing the angle of the beam, the position of the ball can be controlled.

### Importance in Control Engineering
The ball and beam system is:
- **Open loop unstable**: without feedback control, the ball will roll off the beam  
- **Nonlinear**: due to trigonometric relationships and rolling dynamics  
- **Underactuated**: the ball position is controlled indirectly through the beam angle  

### Applications
This system is commonly used for:
- Teaching **classical and modern control methods** (PID, state space, LQR, nonlinear control)  
- Validating **control algorithms** in simulation and experiments  
- Demonstrating concepts such as **stability, feedback, and robustness**


## Simulation Setup in MATLAB and Simulink

To simulate the **ball and beam** system, the MATLAB and Simulink software environment is used. In the first step, after opening a Blank Model in the Simulink environment of MATLAB, the initial simulation settings must be configured. These include the sampling time, the solver type, and the initialization of the system model parameters.

To set the sampling time and the solver type, right click on the model workspace and select the *Model Configuration Parameters* option. In the *Solver Selection* section, set the solver type to *Fixed Step* and assign the sampling time as Ts. Figure 1 provides a suitable guide for performing these steps.

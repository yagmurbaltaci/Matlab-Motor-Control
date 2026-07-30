# Motor Speed Control Simulations (MATLAB/Simulink)

## About This Project
Hi! I'm an Engineering Sciences student at University of Rome Tor Vergata, and this repository contains my simulation models and the final report for my feedback control systems coursework. 

In this project, I built and analyzed different control methods for a motor speed system using MATLAB and Simulink. The main goal was to observe how the system behaves when transitioning from a simple open-loop control to closed-loop Proportional (P) and Proportional-Integral (PI) controllers.

## What I Explored
I simulated several scenarios to see how the controllers would react under different conditions:
* **Open-Loop Control (Fig 1.5):** I started with a basic open-loop model. It worked fine under perfect conditions, but as expected, it couldn't handle any initial speed mismatches or external errors.
* **Proportional (P) Control (Fig 1.6 - 1.12):** Adding a feedback loop helped a lot. I tested the system with incorrect load estimations (like 1.8 Nm instead of 2.0 Nm) and sinusoidal load disturbances. Increasing the proportional gain ($k$) reduced the steady-state error. However, when I pushed the gain too high, the system became super sensitive to high-frequency sensor noise and started oscillating wildly.
* **Proportional-Integral (PI) Control (Fig 2.5 - 2.7):** This was the final and most stable step. By adding the integral term, the controller successfully "learned" the unknown disturbance and completely eliminated the steady-state error. I also tested the characteristic equation ($s^2 + ks + k_I = 0$) with different gain sets to observe undamped, critically damped, and steady-state error behaviors.

## Files in This Repository
* `Yağmur_Baltacı_Report.pdf`: My full detailed report with all scope graphs, block diagrams, and step-by-step mathematical explanations.
* `.slx files`: The Simulink models I created for the simulations.

Feel free to check out the PDF report for the full technical breakdown!

## Tools Used
* MATLAB & Simulink

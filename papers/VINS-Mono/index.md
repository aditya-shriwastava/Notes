# VINS-Mono: A Robust and Versatile Monocular Visual-Inertial State Estimator

## Abstract
- Camera + IMU (Minimum sensor suit for metric 6 DOF state estimation)
- A tightly-coupled, nonlinear optimization-based method is used to obtain high accuracy visual-inertial odometry by fusing pre-integrated IMU measurements and feature observations.

## Introduction
- Integration of IMU measurements can dramatically improve motion tracking performance by bridging the gap between losses of visual tracks due to illumination changes, texture-less area, or motion blur.
- **core:** VIO based on tightly-coupled sliding window nonlinear optimization.

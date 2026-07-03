# PX4-Ardupoilt

PX4 v1.17.0 firmware integration project for Pixhawk 6C Mini.

This repository ports the geometric controller and L1 adaptive augmentation from `sigma-pi/L1Quad/L1AC_customization/ArduCopter/mode_adaptive.cpp` into a PX4-native module. PX4 `control_allocator` remains responsible for motor allocation; the ArduPilot direct-PWM mixer is not used.

The firmware target is:

```text
px4_fmu-v6c_default
```

Safety defaults keep the experimental controller disabled until aircraft-specific mass, inertia, limits, and gains are configured.

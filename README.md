# Crown_Vision
Head level object detection device for the visually impaired
Crowned Vision

Crowned Vision is a wearable head-level obstacle detection device designed to help visually impaired individuals navigate complex environments safely and affordably. Built as part of UC Davis's Engineering 3 design course, the project combines ultrasonic sensing with haptic feedback to alert users to obstacles that traditional aids like walking sticks and guide dogs — which primarily detect ground-level obstacles — often miss.

Show Image

The Problem

Visually impaired individuals, especially in under-resourced communities, have limited affordable options for detecting obstacles at head height (branches, signs, shelves, etc.). Existing assistive tools are often expensive, slow to acquire, or simply don't address this specific gap.

Our Solution

A headwear-mounted device using an Arduino Uno, ultrasonic distance sensors, and haptic (vibration) motors to give real-time proximity feedback — built with low-cost, accessible components.

Features


Arduino Uno–based control system running a simple, real-time distance-sensing loop
Ultrasonic distance sensors (x4) for head-level obstacle detection across multiple directions
Graduated haptic feedback — vibration intensity scales with proximity:

≤20cm → Strong vibration
≤40cm → Medium vibration
≤60cm → Mild vibration
≤120cm → Soft vibration
>120cm → No vibration



Low-latency logic flow with a 2ms polling delay for continuous distance updates
Wearable headband form factor designed for hands-free use
Low-cost, accessible build using basic electronics and materials


How It Works


Pins are set for sensors and haptic motors on startup
The system continuously polls each ultrasonic sensor for distance
Measured distance is compared against threshold bands (20/40/60/120cm)
The corresponding haptic motor vibrates at an intensity matched to the distance band
Loop repeats with a 2ms delay for near-continuous feedback


Hardware


Arduino Uno R3
4x Ultrasonic distance sensors (HC-SR04 or similar)
Haptic vibration motors
220Ω resistor
Wearable headband housing


Testing & Results


Validated in both stationary and walking (~10 ft) test scenarios with simulated obstacles
Reliably detected objects within 40cm, with haptic feedback correlating to proximity
Identified limitations: signal inconsistency beyond 40cm, sensitivity to sensory overload in crowded settings, and a form factor that needs adjustability for different head sizes


Future Work


Refined, adjustable, and more comfortable headwear housing
Improved sensor calibration and code tuning for more reliable feedback
Expanded sensor coverage beyond cardinal directions
More distinguishable motor intensity levels for clearer distance gauging


Team


Varun Gidwani — Computer Engineering
Griffin Carson — Biological Systems Engineering
Jonathan Wop — Civil Engineering
Jake Moffat — Civil Engineering


University of California, Davis — College of Engineering

Acknowledgements

Thank you to Professor Vuong, Momchil Gavrilov, Payam Farhadi, and all ENG3 TAs for their guidance throughout the design process.

References


Arduino
Instructables

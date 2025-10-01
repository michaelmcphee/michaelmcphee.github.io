---
layout: post
title: Digital Caliper-Style Measurement Device
description: A custom-built displacement measurement tool using a potentiometer, rack-and-pinion mechanism, and Arduino-based calibration with gauge blocks.
skills:
  - Arduino
  - SolidWorks
  - 3D Printing
  - Data Collection
  - Calibration & Uncertainty Analysis
  - Excel
  - Analog-to-Digital Conversion
  - Error Analysis
main-image: /ruler.png
---

## Design Objectives
- Design and build a custom displacement measurement system from first principles without prefabricated sensors.  
- Implement a potentiometer-driven **rack and pinion mechanism** to translate linear motion into voltage output.  
- Use Arduino to digitize analog voltage signals and display calibrated distance measurements.  
- Perform calibration with precision **gauge blocks** to establish an accurate measurement equation.  
- Quantify **systematic and random error** using statistical uncertainty analysis.  

## Outcomes
- Successfully designed and 3D printed a digital caliper-style measurement device.  
- Implemented an Arduino-based data acquisition system that converted potentiometer voltage into real distance values.  
- Derived a **linear calibration curve** with R² = 0.9978, showing strong accuracy across the operating range.  
- Conducted an uncertainty analysis, determining maximum error of ±0.13 inches.  
- Identified key improvements for future iterations, including a more robust potentiometer–gear interface.  

📄 [Read the full Executive Summary (PDF)](/assets/pdfs/MTE201_Lab1_Executive_Summary.pdf)


## Technical Details
### Mechanical
<div class="section-flex">
  <div class="text">
    <ul>
      <li>Rack-and-pinion design modeled in SolidWorks and fully 3D printed.</li>
      <li>Custom housing with sliding sleeve to guide rack movement and secure the potentiometer.</li>
      <li>Designed to measure distances up to ~10 cm (three stacked LEGO 2×4 bricks).</li>
      <li>Considered print tolerances, wall thickness, and gear strength during design iterations.</li>
    </ul>
  </div>
  <div class="image">
    <img src="/assets/images/ruler-photos/device_solidworks.png" alt="SolidWorks CAD model of device" />
  </div>
</div>

---

### Electronics
<div class="section-flex">
  <div class="text">
    <ul>
      <li>10-bit Arduino Uno ADC used to capture potentiometer output voltage (0–1023 range).</li>
      <li>Potentiometer directly coupled to pinion gear for rotation-based signal generation.</li>
      <li>Voltage readings mapped to distance values using calibration curve.</li>
      <li>Limitations included restricted potentiometer rotation range (200°) and gear coupling tolerance issues.</li>
    </ul>
  </div>
  <div class="image">
    <img src="/assets/images/ruler-photos/electronics.png" alt="Arduino wiring with potentiometer" />
  </div>
</div>

---

### Calibration & Analysis
<div class="section-flex">
  <div class="text">
    <ul>
      <li>Used **gauge block standards** for calibration reference distances (0–4 inches).</li>
      <li>Collected repeated measurements (3 trials per block) to evaluate repeatability.</li>
      <li>Generated calibration curve: <code>y(x) = -0.0045x + 4.1862</code>, mapping ADC value <em>x</em> to distance <em>y</em> (inches).</li>
      <li>Uncertainty analysis identified maximum deviation of ±0.13 inches.</li>
      <li>Evidence of both systematic error (gear–potentiometer fit) and random error (voltage noise).</li>
    </ul>
  </div>
  <div class="image">
    <img src="/assets/images/ruler-photos/device_calibration.png" alt="Calibration curve of potentiometer vs true distance" />
  </div>
</div>

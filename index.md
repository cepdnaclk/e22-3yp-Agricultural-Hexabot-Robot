---
layout: default
title: Agricultural Hexabot Robot
---

<div class="project-hero">
  <p class="eyebrow">TEAM NOVA · CO3060 · TEAM 13</p>
  <h1>Agricultural Hexabot Robot</h1>
  <p class="hero-subtitle">INSECT — IoT Networked System for Environmental and Crop Telemetry</p>
  <p class="hero-copy">A six-legged agricultural robot designed to explore uneven farm terrain, monitor soil and environmental conditions, and help identify weeds and pests using computer vision.</p>
  <div class="hero-actions"><a class="button button-primary" href="#project-overview">Explore the project</a><a class="button button-secondary" href="https://github.com/cepdnaclk/e22-3yp-Agricultural-Hexabot-Robot">View repository</a></div>
  <p class="image-note">Add your robot or CAD image as <code>assets/images/hexabot.jpg</code> to display it here.</p>
  <img class="hero-image" src="{{ '/assets/images/hexabot.jpg' | relative_url }}" alt="Agricultural Hexabot robot prototype" onerror="this.style.display='none'">
</div>

<nav class="section-nav" aria-label="Project sections"><a href="#project-overview">Overview</a><a href="#architecture">Architecture</a><a href="#designs">Designs</a><a href="#testing">Testing</a><a href="#timeline">Timeline</a><a href="#team">Team</a></nav>

## Project overview
{: #project-overview }

Farmers often inspect fields manually, which takes time and can make early signs of pests, weeds, or changing soil conditions easy to miss. Wheeled machines may also struggle on muddy or uneven ground.

Our proposed Agricultural Hexabot uses six legs to move across rough terrain while collecting environmental readings. A camera-based computer vision system is planned to help identify weeds and pests. The robot will send data wirelessly to an online dashboard that farmers can access from a phone or computer.

### Main objectives
<div class="feature-grid">
  <div class="feature-card"><span class="feature-icon">🤖</span><h3>Six-legged mobility</h3><p>Develop stable walking using servo-driven legs and a tripod gait.</p></div>
  <div class="feature-card"><span class="feature-icon">🌡️</span><h3>Environmental sensing</h3><p>Collect air and soil temperature, humidity, and soil-moisture readings.</p></div>
  <div class="feature-card"><span class="feature-icon">📷</span><h3>Crop observation</h3><p>Use camera images and computer vision to assist weed and pest detection.</p></div>
  <div class="feature-card"><span class="feature-icon">📡</span><h3>IoT telemetry</h3><p>Send readings and alerts to an online dashboard for remote monitoring.</p></div>
</div>

## Solution architecture
{: #architecture }

The system is planned as a set of cooperating components. The main controller prioritizes stable walking and coordinates sensor readings. A separate processing board can handle camera and image-analysis tasks so they do not interfere with movement control.

<div class="architecture">
  <div class="architecture-node">Environmental sensors<br><small>Temperature · Humidity · Soil moisture</small></div><div class="architecture-arrow">↓</div>
  <div class="architecture-node">Main controller<br><small>Gait control · Sensor collection · Data queue</small></div><div class="architecture-arrow">↔</div>
  <div class="architecture-node">Camera processing<br><small>Image capture · Weed/pest recognition</small></div><div class="architecture-arrow">↓</div>
  <div class="architecture-node">Wi-Fi / mobile connectivity<br><small>Telemetry and alerts</small></div><div class="architecture-arrow">↓</div>
  <div class="architecture-node architecture-node-accent">Online farmer dashboard<br><small>Readings · Trends · Notifications</small></div>
</div>
<p class="image-note">Architecture illustration is conceptual. Replace it with your finalized system diagram when available.</p>

## Hardware and software designs
{: #designs }

### Hardware
- Six-legged mechanical frame and joints
- Servo motors and suitable motor-power circuitry
- Main microcontroller and, if required, a separate camera-processing board
- Air-temperature, soil-temperature, humidity, and soil-moisture sensors
- Camera module, battery, power management, and wireless connectivity

### Software
- Embedded code for gait control and sensor acquisition
- State machine for walking phases: lift, swing, lower, and push
- Queues to buffer telemetry during temporary network interruptions
- Python-based image-processing and model experimentation
- Online service and dashboard for sensor readings and alerts

### Planned data flow
1. Sensors collect readings as the robot moves.
2. The controller timestamps and queues measurements.
3. The camera system captures images and runs the selected detection model.
4. Telemetry and detection results are sent over the network.
5. The dashboard presents readings, trends, and alerts.

## Testing and evaluation
{: #testing }

The following are planned evaluation targets; update this section with measured results as testing is completed.

| Area | Evaluation method | Target |
| --- | --- | --- |
| Walking stability | Repeat trials on flat ground and uneven soil | Cross the test area without falling |
| Sensor accuracy | Compare readings with reference instruments | Define acceptable error margins before testing |
| Weed/pest detection | Test against a labelled image set | Initial target: at least 80% correct test images |
| Dashboard updates | Compare device readings with displayed values | Updates arrive within seconds under test conditions |
| Reliability | Repeat trials and inspect missing readings | Record data loss and connection interruptions |

## Project timeline
{: #timeline }

<div class="timeline">
  <div class="timeline-item"><span>Weeks 1–7</span><div><h3>Milestone 1 · Mobility</h3><p>Build the frame and demonstrate standing and walking on flat ground, followed by uneven soil.</p></div></div>
  <div class="timeline-item"><span>Weeks 8–14</span><div><h3>Milestone 2 · Sensing</h3><p>Integrate sensors and compare measurements with reference instruments.</p></div></div>
  <div class="timeline-item"><span>Weeks 15–21</span><div><h3>Milestone 3 · Computer vision</h3><p>Collect weed and pest images, train or configure a model, and evaluate its results.</p></div></div>
  <div class="timeline-item"><span>Weeks 22–28</span><div><h3>Milestone 4 · IoT dashboard</h3><p>Connect telemetry, finish the dashboard, and perform integrated testing.</p></div></div>
</div>

## Team Nova
{: #team }

Project team · CO3060: Computer Systems Design Project · Team 13

| Registration number | Team member |
| --- | --- |
| E/22/131 | Add member name |
| E/22/322 | Add member name |
| E/22/323 | Add member name |
| E/22/427 | Add member name |

Replace the placeholders above with the team's names and optionally add university email links.

## Project links
{: #links }

- [Project repository](https://github.com/cepdnaclk/e22-3yp-Agricultural-Hexabot-Robot)
- [Department of Computer Engineering](http://www.ce.pdn.ac.lk/)
- [Faculty of Engineering, University of Peradeniya](https://eng.pdn.ac.lk/)

<p class="back-to-top"><a href="#top">↑ Back to top</a></p>

---
layout: post
title: 3D-Printed Wind Tunnel
description: A compact, modular wind tunnel designed around 3D-printed components for airflow visualization and repeatable aerodynamic testing. This page is a project outline ready for final dimensions, performance data, and design details.
skills:
  - 3D Printing
  - CAD
  - Aerodynamics
  - Rapid Prototyping
  - Design for Manufacturing
  - Testing & Validation
main-image: /wind-tunnel-cad.png
---

## Overview

This project explores the design and fabrication of a **3D-printed wind tunnel** for testing small models and visualizing airflow. Built as a personal hobby project to get hands-on experience with aerodynamics, the tunnel is an open-circuit (blower-style) design, modular and easy to iterate as the test section, fan, and flow-conditioning components are refined.

{% include image-gallery.html images="wind-tunnel-hero.png" height="400" %}

---

## Design Overview

The wind tunnel is divided into three main sections: the inlet, the viewing chamber, and the outlet. Each section was designed in Onshape to guide air smoothly through the system while remaining practical to 3D print in PLA and assemble by hand.

- **Test section size:** Small-scale, sized for roughly 4-6in models (wing sections, simplified car bodies, Hot Wheels and LEGO Cars)
- **Fan:** 6" HVAC fan driving airflow through the tunnel
- **Manufacturing constraint:** Tunnel split into multiple printable sections to stay within build-plate limits, then assembled into the full duct

---

## Inlet Design

Describe how the inlet brings air into the wind tunnel. Explain the shape, dimensions, and any features intended to reduce turbulence or prepare the airflow before it enters the viewing chamber.

- **Inlet geometry:** Designed with a **4:1 contraction ratio**, within the typical 4:1–9:1 range recommended for this scale of open-circuit wind tunnel to accelerate and settle the incoming air before the test section
- **Flow conditioning:** A honeycomb flow straightener sits at the inlet to break up turbulence and straighten the airflow before it reaches the test section — this went through several design iterations (see Results below) to get airflow clean enough for reliable visualization

{% include image-gallery.html images="wind-tunnel-inlet.png" height="400" %}

---

## Flow Visualization System

This subsystem uses an **ultrasonic mist maker (fogger disc)** and tubes routed into the inlet to introduce visible streams into the airflow. These mist lines make it possible to observe how air moves through the viewing chamber and around a test model.

- **Mist source:** Ultrasonic fogger disc, generating visible water-vapor mist

{% include image-gallery.html images="wind-tunnel-flow-visualization.png, wind-tunnel-flow-visualization1.png" height="400" %}

---

## Viewing Chamber Design

The central viewing chamber is where models are tested and airflow is observed, sized for models in the 4-6in range and fitted with a clear panel for visibility.

- **Test-section size:** ~4-6in model capacity
- **Viewing features:** Clear acrylic/plexiglass panel on the viewing chamber for direct observation and photography of airflow
- **Model mounting:** Test models were rested directly on the floor of the viewing chamber or propped up using Lego bricks as simple, adjustable stands
- **Fan protection:** A second honeycomb panel sits at the far end of the viewing chamber, ahead of the outlet, to keep test models or loose debris from being pulled into the fan

{% include image-gallery.html images="wind-tunnel-viewing-chamber.png" height="400" %}

---

## Outlet Design

Air exits the viewing chamber through the rear honeycomb panel, which keeps test models and loose debris from reaching the fan, before passing into the outlet. Since this is an open-circuit, suck-down design, the 6" HVAC fan is mounted directly at the outlet and pulls air through the entire tunnel rather than pushing it in from the inlet — drawing air in through the contraction, across the test section, and out through the fan.

- **Fan integration:** 6" HVAC fan mounted at the outlet, pulling air through the tunnel (open-circuit/suck-down configuration)

{% include image-gallery.html images="wind-tunnel-outlet.png" height="400" %}

---

## CAD, Printing & Assembly

- **CAD approach:** Modeled entirely in Onshape, with the tunnel broken into modular sections (inlet, viewing chamber, outlet) sized to fit the printer's build volume and bolt/fit together afterward
- **Materials:** PLA filament throughout

---

## Testing Setup

| Measurement / Method | Setup | Result / Observation |
|---|---|---|
| Airspeed | Not instrumented in this version | Planned upgrade — see Future Improvements |
| Flow visualization | Ultrasonic mist maker + acrylic viewing panel | Achieved steady, usable airflow suitable for observing flow patterns |

{% include image-gallery.html images="wind-tunnel-testing1.png, wind-tunnel-testing2.png" height="400" %}
{% include youtube-video.html id="Hl_rFnjx6ew" autoplay="false" width="900px" %}

---

## Results & Next Steps

### What Worked

- The tunnel achieved steady, usable airflow overall after iterating on the honeycomb flow straightener design
- The mist maker produced clean, laminar flow lines that were easy to visualize and photograph around test models

### Future Improvements

- Add real airspeed and pressure sensors (e.g. a pitot tube or anemometer) to move from qualitative to quantitative testing
- Build a proper model mounting fixture to replace the Lego stands, for more consistent and repeatable positioning

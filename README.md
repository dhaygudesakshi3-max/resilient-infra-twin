# Resilient Infra-Twin

AI-powered Digital Twin platform for infrastructure monitoring and predictive maintenance.

> **SIMULATION MODE:** All sensor data in this project is simulated. No physical sensors are connected.

**Live demo:** https://yourusername.github.io/resilient-infra-twin/

## Overview
Resilient Infra-Twin transforms infrastructure maintenance from a reactive process into a predictive, AI-driven system. It monitors an aging bridge through a digital twin, combines sensor readings, and highlights components at risk so maintenance can be planned before failures happen.

## Features
- **Dashboard:** health, risk score, failure probability and charts
- **Digital Twin:** clickable bridge components (deck, columns, beams, foundation, expansion joints) coloured by risk
- **Sensor Monitoring:** vibration, strain, temperature, displacement, tilt and crack width with live simulated updates and time filters
- **AI Risk Prediction:** risk gauges and per-component failure probability
- **Knowledge Graph:** interactive graph linking bridge, component, sensor, measurement, defect, risk and inspection
- **Predictive Maintenance:** prioritised action table and timeline
- **Alerts, Infrastructure Assets, Analytics, Technology and About pages**

## Risk model (simulated)
Risk score = 35% vibration + 35% strain + 30% displacement (each normalised).
Failure probability is about 53% of the risk score, and health = 100 − failure probability.
With the demo values this gives risk 34/100, failure probability 18% and health 82%.

## Technology concepts
Digital Twin, IoT sensor fusion, Knowledge Graph (Neo4j), Graph Neural Networks (PyTorch Geometric), Python, machine learning.
This repository contains the front end only. Neo4j and PyTorch Geometric are represented with simulated data and are planned as future work.

## Project structure
```
style.css, functions.php, header.php, footer.php,
front-page.php, page.php, single.php, index.php,
sidebar.php, template-app.php   -> WordPress theme files
assets/css/main.css             -> styling
assets/js/app.js                -> pages, charts and interactions
assets/js/demo-data.js          -> editable demo data
index.html                      -> standalone version (no WordPress needed)
```

## How to run
**Standalone:** open `index.html` in any browser.

**WordPress:** zip the theme files into a folder named `resilient-infra-twin`, then go to Appearance → Themes → Add New → Upload Theme, and activate. The theme creates the 12 pages and the menu automatically.

## Editing demo data
Edit `assets/js/demo-data.js` (sensors, components, assets, alerts, maintenance).

## Future work
Connect real IoT sensors, store the graph in Neo4j, train a PyTorch Geometric model on real data, and add real-time alerts.

## Author
Sakshi Dhaygude, Bharati vidyapeeth college of engineering for women pune / Computer Engineering

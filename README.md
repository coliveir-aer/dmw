# GOES-R ABI Derived Motion Winds (DMW) Viewer

A browser-based visualization tool for exploring, analyzing, and animating GOES-18 and GOES-19 ABI Derived Motion Winds (DMW) products. The application fetches and renders data directly from NOAA's public S3 archives entirely on the client side.

## 🚀 Live Demo
The application is hosted via GitHub Pages:
**[https://coliveir-aer.github.io/dmw/](https://coliveir-aer.github.io/dmw/)**

## 🛰️ Key Features

### Data Access & Scope
- **Multi-Satellite Support:** Seamlessly switch between GOES-19 (East) and GOES-18 (West) data streams.
- **Comprehensive Domain Coverage:** Scan and visualize Full Disk (F), CONUS (C), Meso 1 (M1), and Meso 2 (M2) sectors.
- **Multi-Band Selection:** Access wind data derived from various channels including Visible (Band 2), Shortwave IR (Band 7), Water Vapor (Bands 8, 9, 10), and IR Window (Band 14).
- **Direct Download:** Option to download the raw NetCDF (`.nc`) files directly to your local machine.

### Interactive Visualization
- **Dynamic Wind Barbs:** Automatically calculates and renders meteorological wind barbs from raw speed and direction vectors.
- **Color-Mapped Intensity:** Wind vectors are dynamically colored based on speed, complete with an auto-scaling legend for rapid visual analysis.
- **Fluid Navigation:** Full support for mouse (click/drag, scroll to zoom) and touch gestures (pinch-to-zoom, drag) for navigating dense point clouds.
- **Coastline Overlays:** Toggleable high-resolution global coastline and border overlays for geographic context.

### Customization & Analysis
- **Threshold Filtering:** Interactively filter out wind vectors below a specified minimum speed (m/s).
- **Density Control:** Adjust the skip factor (barb spacing) to declutter the display during dense atmospheric events.
- **High-Res Export:** Capture and export the current viewport as a high-resolution PNG image.

### Temporal Animation
- **Custom Time Ranges:** Select a target UTC date and define specific start/end bounds to generate custom animation sequences.
- **Playback Controls:** Play, pause, and manually scrub through time-series data to track atmospheric motion over time.

## 📖 Usage
1. **Select Source:** Choose the target satellite (GOES-18/19) and date from the sidebar.
2. **Scan & Load:** Open a domain accordion (e.g., CONUS) and click "Scan Domain" to locate available datasets, then click any time slot to render the snapshot.
3. **Animate:** Use the Animation Settings section to define a UTC range and spectral band, then click "Load Animation".
4. **Tweak Settings:** Open the floating "⚙️ Settings" panel in the viewer to adjust barb density, speed thresholds, or export the view.

---
*Developed for rapid visualization of GOES-R ABI Level 2 Derived Motion Winds.*

# GOES-R ABI Derived Motion Winds (DMW) Viewer

A high-performance, browser-based visualization tool for GOES-R (GOES-18/19) ABI Derived Motion Winds (DMW) products. This application interacts directly with NOAA's Big Data Program S3 buckets to scan, fetch, and render NetCDF (.nc) files using `h5wasm` and React.

## 🚀 Live Demo
The application is hosted via GitHub Pages:
**[https://coliveir-aer.github.io/dmw/](https://coliveir-aer.github.io/dmw/)**

## 🛰️ Features
- **Direct S3 Integration:** Scans `noaa-goes18` and `noaa-goes19` buckets in real-time to locate DMW products.
- **Client-Side NetCDF Processing:** Uses WebAssembly (`h5wasm`) to parse HDF5/NetCDF4 data directly in the browser, eliminating the need for a backend server.
- **Wind Barb Rendering:** Dynamically generates meteorological wind barbs from `wind_speed` and `wind_direction` vectors.
- **Animation Engine:** Fetches sequences of files across specific time ranges to generate temporal animations of wind motion.
- **Customizable Visualization:**
    - Filter by minimum wind speed.
    - Adjust vector density (barb spacing).
    - Toggle coastline overlays using TopoJSON.
    - Export current views as high-resolution PNGs.
- **Multi-Domain Support:** Full Disk (F), CONUS (C), and Mesoscale (M1/M2) sectors.

## 🛠️ Tech Stack
- **Frontend:** React (UMD), Tailwind CSS.
- **Wasm:** `h5wasm` for NetCDF4/HDF5 parsing.
- **Mapping:** `topojson-client` for coastline rendering.
- **Data Source:** NOAA GOES-R Series Public S3 Buckets.

## 📖 Usage
1. **Select Satellite & Date:** Choose between GOES-East (19) or GOES-West (18) and a target UTC date.
2. **Scan Domain:** Click "Scan Domain" on a specific sector (e.g., CONUS) to populate available time slots.
3. **View Data:** - Click a time button to load a single snapshot.
   - Use the **Animation Settings** in the sidebar to define a UTC range and channel, then click "Load Animation" to fetch a sequence.
4. **Interact:** Drag to pan, scroll to zoom. Use the floating control panel to adjust visualization parameters.

## 📂 Project Structure
- `index.html`: The monolithic application file containing the dashboard UI, S3 scanning logic, and the React-based visualization engine.

---
*Developed for rapid visualization of GOES-R ABI Level 2 Derived Motion Winds.*

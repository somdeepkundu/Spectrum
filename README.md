# Interactive Electromagnetic Spectrum: Satellite Navigation & Microwave Bands

An interactive, zoomable, and responsive web visualization mapping the microwave spectrum from **L-band through Ka-band (~1 GHz to 40 GHz)**. This application provides real-time logarithmic scaling, precise physical wavelength conversions, and an integrated technical reference guide for global satellite navigation systems (GNSS) and communication standards.

🔗 **Live Deployment:** [somdeepkundu.github.io/Spectrum](https://somdeepkundu.github.io/Spectrum/)

---

## 🛰️ Spectrum Architecture & Data Specs

The visualization covers the core frequencies vital to modern remote sensing, geodesy, and telecommunications. Every band boundary and calculation has been meticulously cross-verified against official Interface Control Documents (ICDs):

| Band / Signal ID | Min Freq (GHz) | Max Freq (GHz) | Center Freq (GHz) | Wavelength ($\lambda$) | Primary Technical Applications & Constellations |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **L-Band** | 1.000 | 2.000 | 1.500 | ~30.0–15.0 cm | General Satellite Communications, Synthetic Aperture Radar (SAR). |
| ↳ *L5 / E5a / NavIC L5* | 1.164 | 1.189 | 1.176 | ~25.5 cm | Safety-of-life GNSS services (GPS, Galileo, NavIC). |
| ↳ *L2 / G2 / B1-2* | 1.227 | 1.237 | 1.227 | ~24.4 cm | Secondary dual-frequency civilian/military GNSS (GPS, GLONASS, BeiDou). |
| ↳ *L1 / E1 / B1* | 1.565 | 1.585 | 1.575 | ~19.0 cm | Primary civilian GNSS band (GPS L1 C/A, Galileo E1, BeiDou B1). |
| **S-Band** | 2.000 | 4.000 | 3.000 | ~15.0–7.5 cm | Weather radar networks, mobile satellite services, and Deep Space communications. |
| **C-Band** | 4.000 | 8.000 | 6.000 | ~7.5–3.75 cm | Satellite uplink/downlink, altimetry, and spaceborne SAR systems. |
| **X-Band** | 8.000 | 12.000 | 10.000 | ~37.5–25.0 mm | Military telecommunications, high-resolution imaging radars, and weather monitoring. |
| **Ku-Band** | 12.000 | 18.000 | 15.000 | ~25.0–16.7 mm | Direct Broadcast Satellite (DBS) TV, satellite VSAT internet terminals. |
| **K-Band** | 18.000 | 26.500 | 22.250 | ~16.7–11.3 mm | Water vapor absorption research, automotive radars, short-range terrestrial links. |
| **Ka-Band** | 26.500 | 40.000 | 33.250 | ~11.3–7.5 mm | High-capacity geostationary broadband backhauls, 5G networking, planetary science. |

### 📐 Physical Verification Equation
Wavelength values dynamically render based on the classic wave relationship:
$$\lambda = \frac{c}{f}$$

Where $c \approx 300,000 \text{ km/s}$ (speed of light in a vacuum), $f$ is frequency in GHz, and $\lambda$ is resulting wavelength in millimeters.

---

## ⚡ Key Features

* **Logarithmic Spectrum Analyzer Interface:** Accurately visualizes nested narrow bands (like GPS L1 vs. broad L-Band) side-by-side using real-time canvas rendering.
* **Dynamic Drag & Zoom Controls:** Built-in programmatic zoom inputs alongside mouse-wheel or trackpad pinch-to-zoom actions for examining hyper-specific signal limits.
* **Physical Size Reference Ruler:** Translates complex abstract microwave gigahertz metrics into tangible metric units (cm and mm lengths).
* **GNSS Constellation Reference Guide:** Embedded technical overview map tracking frequency utilization signatures across major international orbital platforms:
    * **GPS (NavSTAR)** — USA
    * **GLONASS** — Russian Federation
    * **Galileo** — European Union
    * **BeiDou** — China
    * **NavIC (IRNSS)** — India

---

## 🛠️ Verified Reference Standards

This tool aligns completely with active global regulatory frameworks:
* **ITU-R V.431:** Radiofrequency band designations for satellite Earth stations.
* **IEEE 521-2002:** Standard Letter Designations for Radar-Frequency Bands.
* **GPS / Galileo / BeiDou System ICDs:** Official Signal-in-Space Interface Control Documents verifying civilian band centers down to sub-megahertz levels.

---

## 🚀 Local Development Installation

The application is completely self-contained within a single, optimized file structure containing no external runtime package dependencies. 

1. Clone this repository directly into your local workspace:
   ```bash
   git clone [https://github.com/somdeepkundu/Spectrum.git](https://github.com/somdeepkundu/Spectrum.git)
   cd Spectrum

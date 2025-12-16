# Indonesia CSV Map Plotter

A lightweight, browser-based tool for plotting coordinate data from CSV files onto an interactive map of Indonesia. This application runs entirely in the client's browser—no server setup required.

## Features

* **Privacy-Focused:** All CSV parsing and rendering happens locally in your browser. Your data is never uploaded to a server.

* **Flexible CSV Support:** Automatically detects common column names for latitude, longitude, and labels (e.g., `lat`, `latitude`, `lng`, `Label`, `City`).

* **Multiple Map Styles:**

  * Standard OpenStreetMap

  * Satellite Imagery (Esri)

  * Light & Dark modes (CartoDB)

  * **Indonesia Vector Only:** A specialized mode that isolates Indonesia on a clean background, ideal for professional vector exports.

* **Export Capabilities:**

  * **PNG Export:** Capture high-resolution screenshots of the map.

  * **Area Selection:** Draw a rectangle to crop the PNG export to a specific region.

  * **SVG Export:** (Exclusive to Vector Mode) Download a scalable vector file containing the Indonesia map and your plotted pins as vector objects.

* **Interactive Layers:** Toggle province borders and data labels.

## Usage Guide

### 1. Preparation

Prepare your data in a `.csv` file. The file must have headers.
**Example CSV:**
```
City,Lat,Lon,Description
Jakarta,-6.2088,106.8456,Capital City
Bali,-8.4095,115.1889,Tourism Hub
Surabaya,-7.2575,112.7521,Industrial Center
```
### 2. Plotting Data

1. Open `indonesia_map.html` in your web browser.

2. Click **Choose File** in the control panel.

3. Select your `.csv` file.

4. If the map doesn't plot automatically, check the **Column Mapping** section in the control panel to ensure the correct columns are selected for Latitude, Longitude, and Label.

### 3. Customizing the View

* Use the **Map Style** dropdown to switch between Satellite, Standard, or the Indonesia Vector map.

* If using **Indonesia Only (Vector)**, a color picker will appear allowing you to change the land color.

* Toggle **Show Province Borders** or **Show Labels** to adjust the density of information.

### 4. Exporting

* **For PNG:**

  1. (Optional) Click **Select Area** to draw a box around the specific region you want to capture.

  2. Select your resolution (Scale).

  3. Click **Download PNG**.

* **For SVG (Vector):**

  1. Select the **Indonesia Only (Vector)** map style.

  2. Click the **Download SVG** button that appears.

  3. The resulting file can be opened in Adobe Illustrator, Inkscape, or Figma.


## Technologies Used

* [**Leaflet.js**](https://leafletjs.com/)**:** Interactive maps.

* [**PapaParse**](https://www.papaparse.com/)**:** Fast CSV parsing.

* [**html2canvas**](https://html2canvas.hertzen.com/)**:** DOM screenshots.

* [**Tailwind CSS**](https://tailwindcss.com/)**:** Styling.

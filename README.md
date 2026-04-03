# Trip Visualizer

A simple, single-file HTML tool that plots your geotagged photos on an interactive map with a timeline slider. See your trip unfold chronologically — no server, no install, just open the file in a browser.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d9e7e24f-39b5-4171-bc93-046962790840" />

## Features

- **Drag & drop or browse** a folder of photos
- Reads GPS coordinates and timestamps from EXIF data (JPEG, PNG, TIFF, HEIC)
- Plots photos on a [Leaflet](https://leafletjs.com/) map with color-coded markers (one color per day)
- Draws a path connecting photos in chronological order
- **Timeline slider** lets you scrub through your trip and see photos appear over time
- Click day labels to jump to a specific day
- Hover over markers to preview photos

## How to Use

1. **Open** `trip-visualizer.html` in any modern browser.
2. **Select a folder** of photos using the "Choose Folder" button, or **drag & drop** a folder onto the page.
3. Wait for EXIF data to be read — a progress bar shows how many photos have GPS data.
4. Use the **timeline slider** at the bottom to scrub through your trip chronologically.
5. **Hover** on map markers to see photo previews. Click **day labels** to jump to a specific day.

> **Note:** Photos must contain GPS EXIF data to appear on the map. Most phone cameras embed this automatically; some cameras do not.

## Tech

Single HTML file — no build step, no dependencies to install. Libraries are loaded from CDN:

- [Leaflet](https://leafletjs.com/) — interactive map
- [exifr](https://github.com/MikeKovarik/exifr) — EXIF/GPS parsing
- [CARTO](https://carto.com/) — map tiles

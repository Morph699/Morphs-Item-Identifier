<img width="1280" height="1856" alt="Item Identifier" src="https://github.com/user-attachments/assets/1f941fda-3906-420f-aab8-a278df916cbd" />

# Morphs Item Identifier 
### High-Performance Computer Vision, Colorimetry & Hardware Viewfinder Suite

---

### Overview
**Morphs Item Identifier** is a standalone, lightweight visual analysis suite engineered for Android WebViews, mobile browsers, and desktop environments. Combining automated scene recognition, on-device color quantization, and hardware camera telemetry, the utility transforms standard device camera sensors into an all-in-one visual inspection and data-collection workstation—operating entirely client-side with zero framework overhead.

---

### Key Operational Modes

#### 1. 🔍 Visual AI Scene Recognition
* **Point-and-Snap Search:** Instant optical capture and query routing for real-world items, products, landmarks, media, and objects.
* **Dual-Relay Transmission:** Dual-edge payload dispatch with automatic failover to deliver fast, unmetered visual searches.
* **Smart Frame Conditioning:** Automatic pre-flight bicubic clamping to prevent buffer bloat while maintaining high visual definition for identification engines.

#### 2. 🎨 Pantone & Color Harmony Studio
* **64×64 Pixel Quantization:** Real-time on-device pixel sampling that reduces camera frames into discrete 32-value color clusters in RAM.
* **Dominant 5-Swatch Extraction:** Automatically isolates the primary base, secondary accent, and supporting color harmonies.
* **One-Tap Hex Export:** Instant clipboard copying for individual hex codes, batch palette strings, and downloadable `.txt` color manifests.

#### 3. 🎬 Batch Scan Queue Console
* **Continuous Multi-Frame Ingestion:** Rapid-fire capture mode allowing users to snap consecutive items without leaving the viewfinder HUD.
* **Miniature Thumbnail Strip:** Live persistent HUD queue displaying captured items with status badges (Ready / Inspected).
* **Deep Session Exporters:** One-click structured dataset exports to **CSV** and **JSON** with timestamps, inspection state, and image reference indices.

#### 4. 🎬 IMDb & Media Verification Bridge
* **Direct Celebrity & Actor Lookup:** Integrated biography resolver for rapid verification of actors, films, directors, and production media.

---

### Hardware Engine & Sensor Controls

* **Resilient 3-Stage Camera Ingestion Driver:**
  * *Stage 1 (Ideal Precision):* Requests exact optical sensor orientation (`environment` rear or `user` front) clamped to 1280×720 HD.
  * *Stage 2 (Relaxed Profile):* Gracefully steps down to ideal sensor constraints without strict resolution boundaries if hardware restricts 720p.
  * *Stage 3 (Generic Stream):* Fallback audio-less video stream ensuring immediate sensor initialization across legacy digitizers and budget hardware.
* **Hardware Zoom & Two-Finger Pinch Engine:**
  * True 1.0× to 8.0× continuous magnification slider.
  * Interrogates `track.getCapabilities()` to map zoom levels directly to physical optical motor coils when supported by device lenses.
  * Native multi-touch pinch-to-zoom calculation (`Math.hypot`) with smooth slider synchronization.
* **Network Telemetry Radar & Bandwidth Shield:**
  * Live monitoring of connection quality (`navigator.connection`) and metered data states.
  * Automatically downsamples upload payloads to 800px at 0.78 JPEG quality on cellular or data-saver connections to preserve user carrier data.
  * Gracefully transitions to offline local processing (color extraction and queuing) when connectivity drops.
* **Screen WakeLock Protocol:**
  * Automatically requests an operating system display wake lock upon sensor feed activation to prevent dimming or standby during active bench inspections.

---

### Architecture & Interface Ergonomics

* **Zero Page-Reload Hot Reset (`executeInMemReset`):**
  * Factory reset routines execute purely in memory—clearing DOM states, camera sensor locks, IndexedDB caches, and telemetry queues without triggering `location.reload()`, completely protecting Android WebViews from white-screen stalls or `ERR_CONNECTION_REFUSED` crashes.
* **Android Hardware Back-Button Guard:**
  * Uses synthetic history stack states (`pushState` / `popstate`) to intercept physical back gestures, gracefully closing active modals without dropping the app container.
* **Universal 10-Theme Palette Matrix (WCAG AAA):**
  * Full spectrum of contrast-compliant themes including Soft Slate Light, OLED Stealth Dark, Matrix Green, Cyber Yellow, Cyberpunk Pink, Dracula Purple, Blood Matrix, Nordic Frost, Solarized Ocean, and Sunset Amber.
* **Dynamic Typography Scaling Engine:**
  * Selectable font scale configurations (Small, Medium Baseline, Large, and Extra Large) with automatic rem-calculation across all HUD cards and overlays.

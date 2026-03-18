# PixelSculpt v1.0 beta
Free and OpenSource Litophane Maker & Color Lithophane for 3D printing

Upload a photo, configure filament layers with Transmission Depth simulation, preview in 3D, and export print-ready STL files — 100% client-side, no server needed, no cloud files upload!!


<br><br><br>
<h1 align="center">🔶 PixelSculpt v1.0 Beta
<br><br>

<p align="center">
  <img src="https://img.shields.io/badge/version-1.0_Beta-ff6b2b?style=for-the-badge" alt="Version 1.0 Beta">
  <img src="https://img.shields.io/badge/license-MIT-00d4aa?style=for-the-badge" alt="MIT License">
  <img src="https://img.shields.io/badge/100%25-client--side-8888a8?style=for-the-badge" alt="Client-Side">
  <img src="https://img.shields.io/badge/no_server-required-44dd88?style=for-the-badge" alt="No Server">
</p></h1><br>
<p align="center">
  <strong>Open Source Lithophane & Color Lithophane Generator</strong><br>
  From pixel to sculpture — all in your browser.
</p>

<p align="center">
  <a href="#english">English</a> · <a href="#italiano">Italiano</a>
</p>

---

<a name="english"></a>

## 🇬🇧 English

### What is PixelSculpt?

PixelSculpt is a free, open-source web application that transforms any photograph into a 3D-printable lithophane. Everything runs directly in your browser — no server, no upload, no account required. Your images never leave your computer.

Load a photo, adjust parameters, preview in real-time 3D, and export a ready-to-print STL file in seconds.

### ✨ Features

#### 🖼️ Image Processing
- Drag & drop or click to upload (PNG, JPG, WebP)
- **Auto Optimize** — analyzes image luminance histogram and automatically calculates optimal brightness, contrast, gamma, and pixel sampling for the best lithophane result
- Manual adjustments: brightness, contrast, gamma correction
- Image inversion and mirroring (for backlit orientation)
- Bilinear sampling for smooth gradients
- Gaussian smoothing (separable, multi-pass)
- Layer quantization to eliminate print banding artifacts
- Configurable pixel sampling (1x–4x) for file size control

#### 📐 Dimensions & Presets
- Width and height in mm with aspect ratio lock
- **15 size presets** organized in 3 groups:
  - **Photo formats**: 10×15, 13×18, 15×20, 20×25, 20×30 cm
  - **Paper formats**: A6, A5, A4, Letter, Postcard
  - **Aspect ratios**: 1:1, 4:3, 3:2, 16:9, 9:16
- mm ↔ px unit toggle with live DPI calculation
- Quick swap width/height button

#### 🎨 Filament Layer System (Transmission Depth Support!)
- **Multi-layer filament stack** with per-layer color, height, and Transmission Depth (TD) values
- Beer-Lambert optical absorption simulation — realistic light transmission through colored filament layers
- **AMS mode**: automatic multi-color filament change with full layer configuration
- **Manual Swap mode**: single or multi-filament with precise pause-at-layer instructions for hand swapping
- Layer persistence when switching between AMS and Manual modes
- Drag & drop layer reordering
- **Filament Change Schedule** with exact layer numbers for each color change
- Real-time TD preview with auto-contrast labels
- Color ramp visualization

#### 🧵 Filament Presets
- **28+ built-in presets**: Generic, Prusament, eSun, Polymaker, Bambu Lab
- Custom preset creation with brand, name, color, and TD value
- Import/Export presets as JSON
- Brand filter dropdown

#### 🖨️ Print Orientation & Supports
- **Flat mode**: standard horizontal print on bed
- **Vertical mode**: standing lithophane with automatic support generation
  - **Triangle supports**: two removable triangular prisms at 25% and 75% width, with 0.15mm gap for easy removal
  - **Stand base**: full-width permanent base plate with rear extension for stability
  - Configurable stabilizer height (20–100%) and thickness (0.5–4mm)
- Real-time 3D preview of supports (blue semi-transparent)

#### 🌐 3D Viewport
- Real-time Three.js preview with orbit, pan, and zoom
- **5 camera presets**: Front, Back, Top, 3/4 Tilt, Reset — with smooth animated transitions
- **Mouse controls**: left-drag rotate, right/middle-drag pan, scroll zoom
- **Keyboard controls**: arrow keys rotate (Shift = fast), WASD pan, +/- zoom, 1-4 camera presets
- **Backlight simulation** with adjustable intensity slider (5–100%)
- Wireframe toggle
- Touch support for mobile devices

#### 📦 Export
- **STL Binary** (compact) and **STL ASCII** formats
- Watertight manifold mesh generation — no slicer repair needed
- Optional border frame with adjustable width
- Estimated file size display (KB/MB + triangle count)
- Automatic filename suffix (_flat / _vertical)

#### 🌍 Multilingual
- **5 languages**: English, Italiano, Deutsch, Français, Español
- External `lang.json` for easy translation contributions
- Language preference saved in localStorage

#### ⚡ Technical
- 100% client-side — zero server dependency, no cloud upload for your privacy, your images stays yours!
- Single HTML file + one JSON translation file
- Three.js r128 for 3D rendering
- Works offline after initial page load
- GitHub Pages ready

### 🚀 Getting Started

1. Visit the [live demo](https://fr33n0w.github.io/pixelsculpt/) 
2. Open in any modern browser
3. Drop a photo
4. Click **Auto Optimize** or adjust parameters manually
5. Choose Flat or Vertical orientation
6. Click **Export STL**
7. Import into your slicer and print!

### 🖨️ Recommended Print Settings

| Parameter | Value |
|-----------|-------|
| Orientation | Vertical (for best quality) |
| Layer height | 0.08–0.12 mm |
| Infill | 100% (solid) |
| Walls | 1–2 perimeters |
| Nozzle | 0.4 mm |
| Material | PLA (white for classic lithophanes) |
| Speed | 30–40 mm/s |

### 📁 File Structure

```
pixelsculpt/
├── index.html    ← The complete application
├── lang.json     ← Translations (EN, IT, DE, FR, ES)
├── README.md     ← This file
└── LICENSE        ← MIT License
```

---

<a name="italiano"></a>

## 🇮🇹 Italiano

### Cos'è PixelSculpt?

PixelSculpt è un'applicazione web gratuita e open-source che trasforma qualsiasi fotografia in una litofania stampabile in 3D. Tutto funziona direttamente nel tuo browser — nessun server, nessun upload, nessun account necessario. Le tue immagini non lasciano mai il tuo computer.

Carica una foto, regola i parametri, visualizza l'anteprima 3D in tempo reale ed esporta un file STL pronto per la stampa in pochi secondi.

### ✨ Funzionalità

#### 🖼️ Elaborazione Immagine
- Drag & drop o click per caricare (PNG, JPG, WebP)
- **Ottimizzazione Automatica** — analizza l'istogramma di luminanza dell'immagine e calcola automaticamente luminosità, contrasto, gamma e campionamento pixel ottimali per il miglior risultato
- Regolazioni manuali: luminosità, contrasto, correzione gamma
- Inversione e specchiatura dell'immagine (per orientamento retroilluminato)
- Campionamento bilineare per gradazioni uniformi
- Smoothing Gaussiano (separabile, multi-passata)
- Quantizzazione ai layer per eliminare artefatti di banding in stampa
- Campionamento pixel configurabile (1x–4x) per controllo dimensione file

#### 📐 Dimensioni e Formati Predefiniti
- Larghezza e altezza in mm con blocco proporzioni
- **15 formati predefiniti** organizzati in 3 gruppi:
  - **Formati fotografici**: 10×15, 13×18, 15×20, 20×25, 20×30 cm
  - **Formati carta**: A6, A5, A4, Letter, Cartolina
  - **Rapporti d'aspetto**: 1:1, 4:3, 3:2, 16:9, 9:16
- Commutazione mm ↔ px con calcolo DPI in tempo reale
- Pulsante scambio rapido larghezza/altezza

#### 🎨 Sistema Layer Filamento (Supporto Profondità di Trasmissione!)
- **Stack multi-layer** con colore, altezza e valore TD (Transmission Depth) per ogni layer
- Simulazione ottica di assorbimento Beer-Lambert — trasmissione realistica della luce attraverso strati di filamento colorato
- **Modalità AMS**: cambio filamento automatico multicolore con configurazione completa dei layer
- **Modalità Cambio Manuale**: filamento singolo o multiplo con istruzioni precise di pausa-al-layer per cambio manuale
- Persistenza dei layer quando si passa tra modalità AMS e Manuale
- Riordinamento layer tramite drag & drop
- **Programma Cambio Filamento** con numero esatto di layer per ogni cambio colore
- Anteprima TD in tempo reale con etichette auto-contrasto
- Visualizzazione rampa colore

#### 🧵 Preset Filamento
- **28+ preset inclusi**: Generic, Prusament, eSun, Polymaker, Bambu Lab
- Creazione preset personalizzati con brand, nome, colore e valore TD
- Import/Export preset in formato JSON
- Filtro dropdown per brand

#### 🖨️ Orientamento Stampa e Supporti
- **Modalità Piatto**: stampa orizzontale standard sul piano
- **Modalità Verticale**: litofania in piedi con generazione automatica dei supporti
  - **Supporti triangolari**: due prismi triangolari rimovibili al 25% e 75% della larghezza, con gap di 0.15mm per facile rimozione
  - **Base di appoggio**: base permanente a tutta larghezza con estensione posteriore per stabilità
  - Altezza (20–100%) e spessore (0.5–4mm) stabilizzatori configurabili
- Anteprima 3D in tempo reale dei supporti (blu semi-trasparente)

#### 🌐 Viewport 3D
- Anteprima Three.js in tempo reale con orbita, pan e zoom
- **5 preset camera**: Fronte, Retro, Alto, Vista 3/4, Reset — con transizioni animate fluide
- **Controlli mouse**: click sinistro ruota, click destro/centrale pan, scroll zoom
- **Controlli tastiera**: frecce ruotano (Shift = veloce), WASD pan, +/- zoom, 1-4 preset camera
- **Simulazione retroilluminazione** con slider intensità regolabile (5–100%)
- Toggle wireframe
- Supporto touch per dispositivi mobili

#### 📦 Esportazione
- Formati **STL Binario** (compatto) e **STL ASCII**
- Generazione mesh manifold stagna — nessuna riparazione nello slicer necessaria
- Cornice opzionale con larghezza regolabile
- Stima dimensione file in tempo reale (KB/MB + conteggio triangoli)
- Suffisso automatico nel nome file (_flat / _vertical)

#### 🌍 Multilingua
- **5 lingue**: English, Italiano, Deutsch, Français, Español
- File `lang.json` esterno per contributi di traduzione facili
- Preferenza lingua salvata nel localStorage

#### ⚡ Dettagli Tecnici
- 100% client-side — zero dipendenze server
- Un singolo file HTML + un file JSON di traduzione
- Three.js r128 per il rendering 3D
- Funziona offline dopo il caricamento iniziale della pagina
- Pronto per GitHub Pages

### 🚀 Come Iniziare

1. Visita la [demo live](https://fr33n0w.github.io/pixelsculpt/)
2. Apri in qualsiasi browser moderno
3. Trascina una foto
4. Clicca **Ottimizzazione Auto** o regola i parametri manualmente
5. Scegli orientamento Piatto o Verticale
6. Clicca **Esporta STL**
7. Importa nel tuo slicer e stampa!

### 🖨️ Impostazioni di Stampa Consigliate

| Parametro | Valore |
|-----------|--------|
| Orientamento | Verticale (per migliore qualità) |
| Altezza layer | 0.08–0.12 mm |
| Riempimento | 100% (solido) |
| Pareti | 1–2 perimetri |
| Ugello | 0.4 mm |
| Materiale | PLA (bianco per litofanie classiche) |
| Velocità | 30–40 mm/s |

---

## 🔮 Roadmap

- [ ] **Tealight & LED holder supports** — integrated support structures compatible with standard tealight candles and Bambu Lab LED modules, directly in the stabilizer system
- [ ] **Selective 3D relief extrusion** — paint or select regions of the lithophane to extrude beyond the surface, creating dramatic three-dimensional relief effects (imagine elements popping out of the frame)
- [ ] Additional filament preset packs
- [ ] Curved and cylindrical lithophane shapes
- [ ] Multi-image lithophane box/lamp generator
- [ ] G-code preview with layer-by-layer simulation

---

## 🤝 Contributing

Contributions are welcome! You can help by:
- Adding translations to `lang.json`
- Submitting filament preset packs
- Reporting bugs or suggesting features via Issues
- Opening Pull Requests

## 📄 License

MIT License — free for personal use.

---

<p align="center">
  <strong>Made with ❤️ for the 3D printing community</strong><br>
  <em>From pixel to sculpture.</em>
</p>


<p align="center">
  <img src="assets/banner.svg" alt="OceanGuard AI Banner" width="100%"/>
</p>

<p align="center">
  <img src="assets/logo.png" alt="OceanGuard AI Logo" width="120"/>
</p>

<h1 align="center">OceanGuard AI</h1>

<p align="center">
  <strong>On-device marine debris detection in images and videos for Android</strong><br/>
  <sub>100% offline &bull; Private &bull; AI-powered &bull; 6 languages</sub>
</p>

<p align="center">
  <a href="https://github.com/asferrer/OceanguardAI/releases/latest">
    <img src="https://img.shields.io/github/v/release/asferrer/OceanguardAI?style=for-the-badge&color=00d4ff&label=Latest%20Release" alt="Latest Release"/>
  </a>
  &nbsp;
  <img src="https://img.shields.io/badge/Platform-Android%208.0%2B-3DDC84?style=for-the-badge&logo=android&logoColor=white" alt="Android 8.0+"/>
  &nbsp;
  <img src="https://img.shields.io/badge/Offline-100%25-10b981?style=for-the-badge" alt="100% Offline"/>
  &nbsp;
  <img src="https://img.shields.io/badge/Languages-6-8b5cf6?style=for-the-badge" alt="6 Languages"/>
  &nbsp;
  <img src="https://img.shields.io/badge/License-Research-f59e0b?style=for-the-badge" alt="License"/>
</p>

<p align="center">
  <a href="https://github.com/asferrer/OceanguardAI/releases/latest/download/OceanGuard-AI-latest.apk">
    <img src="https://img.shields.io/badge/%E2%AC%87%EF%B8%8F%20DOWNLOAD%20APK-00d4ff?style=for-the-badge&logo=android&logoColor=white" alt="Download APK"/>
  </a>
  &nbsp;&nbsp;
  <a href="https://asferrer.github.io/OceanguardAI">
    <img src="https://img.shields.io/badge/%F0%9F%8C%8A%20LANDING%20PAGE-0d1225?style=for-the-badge" alt="Landing Page"/>
  </a>
</p>

---

## About

OceanGuard AI is an Android application that detects and classifies marine debris in **images and videos** using on-device artificial intelligence. No internet connection required, no data sent to any server.

Built as part of a doctoral research project on computer vision applied to marine debris detection at the **Universidad de Alicante**, with multiple peer-reviewed publications backing the underlying detection models.

## Features

<table>
<tr>
<td width="50%">

### Detection
- **Image & video analysis** — photos, gallery, and recorded video
- **Batch processing** — analyze multiple files at once
- **8 debris categories** — Bottle, Can, Fishing Net, Glove, Mask, Metal Debris, Plastic Debris, Tire
- **Bounding box visualization** — corner brackets with glow effects

</td>
<td width="50%">

### AI Deep Analysis
- **Gemma 3n VLM** — on-device vision-language model
- **Environmental reports** — detailed risk assessment per zone
- **PDF export** — share or archive analysis reports
- **Markdown rendering** — tables, charts, and structured output

</td>
</tr>
<tr>
<td width="50%">

### Mapping & Tracking
- **GPS geotagging** — automatic from EXIF or device GPS
- **Interactive map** — MapLibre vector tiles with clustering
- **Detection history** — browse, filter, and review past analyses
- **Ecosystem health score** — aggregated per zone

</td>
<td width="50%">

### Privacy & Gamification
- **100% offline** — no cloud, no telemetry, no accounts
- **All data on-device** — deletable at any time
- **6 languages** — EN, ES, FR, DE, IT, PT
- **MarineDex** — collect debris types and unlock achievements

</td>
</tr>
</table>

## Tech Stack

| Component | Technology |
|-----------|-----------|
| **Fast Detection** | RT-DETRv2 (TensorFlow Lite) — FP16 & INT8 models |
| **Deep Analysis** | Gemma 3n E2B (MediaPipe LLM Inference) — 3.4GB INT4 |
| **UI** | Jetpack Compose + Material 3 |
| **Camera** | CameraX 1.5 |
| **Database** | Room 2.7 + DataStore |
| **Maps** | MapLibre Compose + OpenFreeMap |
| **Language** | Kotlin 2.2, min SDK 26 (Android 8.0) |

## Installation

> **Requirements:** Android 8.0+, ~200 MB storage (~3.6 GB additional for deep analysis model).

### Quick Install

1. **[Download the latest APK](https://github.com/asferrer/OceanguardAI/releases/latest/download/OceanGuard-AI-latest.apk)** directly to your device
2. On your Android device: **Settings > Apps > ⋯ > Special access > Install unknown apps**
3. Enable installation for your browser (Chrome, Firefox, etc.)
4. Open the downloaded APK and tap **Install**

> [!NOTE]
> Google Play Protect may show a warning — this is normal for apps distributed outside the Play Store. Tap **"Install anyway"** to proceed. The app is signed with a developer certificate and is safe to install.

### Optional: Deep Analysis Model

The app includes an optional AI model (Gemma 3n) for advanced environmental analysis and detailed report generation. It can be downloaded from within the app's settings. Without it, the app works perfectly for fast detection.

## Privacy

All processing happens **entirely on your device**. No data is collected, transmitted, or shared with any server. Camera images, GPS coordinates, and detection results are stored locally and can be deleted at any time from within the app.

| Data | Storage | Shared? |
|------|---------|---------|
| Photos & videos | Device only | Never |
| GPS coordinates | Device only | Never |
| Detection results | Device only | Never |
| AI model weights | Device only | Never |

## Research & Publications

OceanGuard AI is built on peer-reviewed research and ongoing doctoral work:

### Papers

- **An experimental study on marine debris location and recognition using object detection**
  A. Sánchez-Ferrer, J.J. Valero-Mas, A.J. Gallego, J. Calvo-Zaragoza — *Pattern Recognition Letters*, 2023
  [ScienceDirect](https://www.sciencedirect.com/science/article/pii/S0167865522003889)

- **The CleanSea Set: A Benchmark Corpus for Underwater Debris Detection and Recognition**
  A. Sánchez-Ferrer, A.J. Gallego, J.J. Valero-Mas, J. Calvo-Zaragoza — *IbPRIA 2022*, LNCS Springer
  [Springer](https://link.springer.com/chapter/10.1007/978-3-031-04881-4_49)

### Hackathon

- **OceanGuard AI: Mapping and Mitigating Marine Pollution with Gemma 3N**
  Google Gemma 3N Hackathon — Kaggle, 2025
  [Kaggle Writeup](https://www.kaggle.com/competitions/google-gemma-3n-hackathon/writeups/oceanguard-ai-mapping-and-mitigating-marine-pollut)

### Theses

- **Modelos de difusión aplicados a la detección de objetos en el fondo marino**
  A. Sánchez-Ferrer — Master's Thesis, Universidad de Alicante, 2024
  [RUA](https://rua.ua.es/entities/publication/88244474-6165-4cd9-a4af-68eff29d65c6)

- **Deep Learning aplicado a la detección de residuos en el fondo marino**
  A. Sánchez-Ferrer — Bachelor's Thesis, Universidad de Alicante, 2021
  [RUA](https://rua.ua.es/entities/publication/92c34588-9842-4ec3-8b15-97a8ce718e04)

## License

The application binary (APK) is provided for research and evaluation purposes.

---

<p align="center">
  <sub>Doctoral research on computer vision for marine debris detection — <a href="https://www.ua.es">Universidad de Alicante</a></sub>
</p>

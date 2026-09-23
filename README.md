# 🏗️ GeoCrop AI v2.0 - Civil Geotechnical & Precision Agriculture Platform (ANN Powered)

[![React](https://img.shields.io/badge/React-18.3.1-blue.svg)](https://reactjs.org/)
[![Vite](https://img.shields.io/badge/Vite-5.4-purple.svg)](https://vitejs.dev/)
[![ANN Model](https://img.shields.io/badge/AI_Engine-ANN_Neural_Network-emerald.svg)](src/engine/annModel.js)
[![Capacitor](https://img.shields.io/badge/Capacitor-Android-green.svg)](https://capacitorjs.com/)
[![License](https://img.shields.io/badge/License-MIT-emerald.svg)](LICENSE)

**GeoCrop AI v2.0** is an advanced, AI-powered dual-domain engineering platform designed for **Civil Geotechnical Engineering** and **Precision Agronomy**. Driven by an **Artificial Neural Network (ANN) Machine Learning Inference Engine** (`annModel.js`), it combines Terzaghi bearing capacity soil mechanics with ANN multi-layer weight models (`ann_weights.json`, `foundation_ann_weights.json`, `crop_ann_weights.json`) to deliver instant structural safety simulations, foundation recommendations, fertilizer dosage calculations, executive PDF reports, and interactive AI assistant guidance.

---

## 🧠 Artificial Neural Network (ANN) Model Engine

GeoCrop AI v2.0 integrates dedicated **Artificial Neural Network (ANN)** forward-pass inference models running directly in JavaScript without external latency:

1. **Geotechnical Soil CBR & Bearing Capacity ANN Model** (`ann_weights.json`):
   * Inputs moisture content and bulk density to predict exact California Bearing Ratio (CBR) and Safe Bearing Capacity ($q_{safe}$ in $kN/m^2$).
2. **Foundation Type Selection ANN Model** (`foundation_ann_weights.json`):
   * Evaluates soil texture, CBR, bearing capacity, and building floor count to compute multi-class probability scores across **Isolated Footings**, **Strip Footings**, **Raft Foundations**, **Pile Foundations**, and **Rock Anchors**.
3. **Agronomic Crop Suitability ANN Model** (`crop_ann_weights.json`):
   * Evaluates soil NPK nutrient profile, pH, electrical conductivity, organic carbon, and climate zones to output precision suitability percentages for 45+ plant species.

---

## 🌟 Key Features

### 🏢 1. Civil Geotechnical Engineering (ANN Powered)
* **17 Soil Parameters Audit**: Specific Gravity ($G_s$), Sand/Silt/Clay %, Bulk Density ($g/cm^3$), Porosity, Moisture %, Permeability, Cohesion ($c$), Friction Angle ($\phi$), Liquid Limit ($LL$), Plastic Limit ($PL$), Foundation Depth ($D_f$), Water Table Depth, and SPT $N$-Value.
* **ANN Soil Bearing Capacity Engine**: Predicts Safe Bearing Capacity ($q_{safe}$ in $kN/m^2$) with Factor of Safety $FOS = 3.0$ using neural network regression.
* **Hero Building Floor Simulator**: Interactive visual building stacker simulating safe structural floor capacity ($G+N$) based on ANN load analysis.
* **ANN Foundation Recommendation**: Neural network classifier automatically recommends optimal foundation types (**Isolated Column Footings**, **Strip Footings**, **Raft/Mat Foundations**, **Deep Piles**, or **Rock Anchor Footings**) with confidence scores.
* **Target Construction Floor Advisor**: Enter any target floor count (e.g. 4 floors) to get ANN feasibility certification and specific footing dimensions.

### 🌾 2. Precision Agriculture & Agronomy (ANN Powered)
* **45+ Plant Database**: Covers 18 Crops, 14 Vegetables, and 13 Fruits (`soilDatabase.js`).
* **ANN Crop Suitability Ranking**: Neural network classifier ranks top crops, vegetables, and fruits with percentage match scores.
* **NPK Fertilizer Dosage Calculator**: Computes exact Urea (46% N), DAP (18% N, 46% $P_2O_5$), and MOP (60% $K_2O$) bags (50kg) required per hectare.
* **Soil Health Score & Radar Chart**: Visualizes nutrient balance against optimal target curves.

### 🤖 3. AI Assistant with Natural Language Auto-Filling
* **Raw Text Parameter Parser**: Paste unformatted soil test lab reports into the chatbot to automatically populate all application input forms across Geotechnical and Agriculture modules.
* **Dual Language Support**: Context-aware engineering assistance in English and Tamil (தமிழ்).

### 📄 4. Certified White Executive PDF Report
* Official letterhead layout with GPS location stamp, 17-parameter audit table, ANN geotechnical foundation box, custom target floor advisory, precision fertilizer schedule, and certified sign-off stamp.

### 📱 5. Multi-Platform Support (Web, PWA, Android APK)
* Progressive Web App (PWA) support with offline service workers.
* Integrated **Capacitor Android** configuration for compiling native `.apk` files for Android smartphones.

---

## 🚀 Getting Started

### Prerequisites
* [Node.js](https://nodejs.org/) (v18.0 or higher)
* [npm](https://www.npmjs.com/) (v9.0 or higher)

### Installation
```bash
# 1. Clone the repository
git clone https://github.com/muthu-16/geocrop-ai.git

# 2. Navigate to project directory
cd geocrop-ai

# 3. Install dependencies
npm install
```

### Running Locally
```bash
npm run dev
```
Open **[http://localhost:5173/](http://localhost:5173/)** (or `http://localhost:3001/`) in your browser.

---

## 📱 Building Native Android App (.apk)

This project uses **Ionic Capacitor** for cross-platform Android builds:

```bash
# 1. Build web production bundle
npm run build

# 2. Sync web assets with Capacitor Android
npx cap sync android

# 3. Open project in Android Studio to build APK
npx cap open android
```
*(In Android Studio, click **Build > Build Bundle(s) / APK(s) > Build APK(s)** to generate `app-debug.apk`)*

---

## 🛠️ Technology Stack

| Domain | Technology |
| :--- | :--- |
| **Artificial Intelligence** | ANN Neural Network Engine (`annModel.js`, JSON Model Weights) |
| **Frontend UI** | React 18, Vite 5, Tailwind CSS |
| **Icons & Charts** | Lucide React, Recharts |
| **PDF Engine** | jsPDF, html2canvas |
| **Native Mobile** | Capacitor Android 6 |
| **Localization** | Dual Language (English & தமிழ்) |

---

## 📄 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.


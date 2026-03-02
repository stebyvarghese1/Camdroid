<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=240&section=header&text=CamDroid&fontSize=80&fontColor=ffffff&fontAlignY=42&desc=Turn%20your%20smartphone%20into%20a%20wireless%20webcam.%20Instantly.&descAlignY=63&descSize=17&descColor=94a3b8&animation=fadeIn" width="100%"/>

</div>

<br>

<div align="center">

```
   Wireless  ·  QR Pairing  ·  Secure  ·  Cross-Platform
```

</div>

<br>

<div align="center">

[![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Flask](https://img.shields.io/badge/Flask-Backend-000000?style=for-the-badge&logo=flask&logoColor=white)](https://flask.palletsprojects.com)
[![PyQt5](https://img.shields.io/badge/PyQt5-Desktop_GUI-41CD52?style=for-the-badge&logo=qt&logoColor=white)](https://riverbankcomputing.com/software/pyqt)
[![Kivy](https://img.shields.io/badge/Kivy-Mobile_App-2B5590?style=for-the-badge&logo=kivy&logoColor=white)](https://kivy.org)
[![OpenCV](https://img.shields.io/badge/OpenCV-Vision-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)](https://opencv.org)
[![License](https://img.shields.io/badge/License-MIT-fbbf24?style=for-the-badge)](LICENSE)

<br>

[![Stars](https://img.shields.io/github/stars/stebyvarghese1/Camdroid?style=flat-square&color=fbbf24&label=⭐%20Stars)](https://github.com/stebyvarghese1/Camdroid/stargazers)
&nbsp;
[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux%20%7C%20macOS%20%7C%20Android-38bdf8?style=flat-square)](#)
&nbsp;
[![Built by](https://img.shields.io/badge/by-Steby%20Varghese-a78bfa?style=flat-square)](https://github.com/stebyvarghese1)

</div>

<br>
<br>

---

<div align="center">

## &nbsp;&nbsp;&nbsp;` 01 `&nbsp;&nbsp; THE PRODUCT

</div>

<br>

<div align="center">

| 🖥️ Desktop Receiver | 📱 Mobile Sender |
|:-------------------:|:----------------:|
| <img src="https://github.com/user-attachments/assets/53092bb8-a4a2-4ecc-928b-3ad7823cc87d" width="440"/> | <img src="https://github.com/user-attachments/assets/681cef3e-91cc-438e-9f9a-257168f2cbd7" width="280"/> |
| *Sleek borderless PyQt5 receiver window* | *Minimal Kivy sender app* |

</div>

<br>
<br>

---

<div align="center">

## &nbsp;&nbsp;&nbsp;` 02 `&nbsp;&nbsp; THE IDEA

</div>

<br>

> ### *"No USB. No drivers. No IP addresses. Just scan a QR code and your phone becomes a webcam."*

<br>

**CamDroid** bridges your mobile device and your desktop over local Wi-Fi. The receiver generates a QR code — you scan it on your phone — and within seconds you have a live, secure wireless camera feed on your PC.

Built on a Flask HTTP backend, a modern PyQt5 desktop interface, and a Kivy mobile sender that compiles to Android APK.

```
  ┌─────────────────────────────────────────────────────────┐
  │  No USB cables                                          │
  │  No manual IP typing                                    │
  │  No third-party accounts or cloud routing               │
  │  Everything stays on your local network                 │
  └─────────────────────────────────────────────────────────┘
```

<br>
<br>

---

<div align="center">

## &nbsp;&nbsp;&nbsp;` 03 `&nbsp;&nbsp; FEATURES

</div>

<br>

<div align="center">

| &nbsp; | Feature | Description |
|--------|---------|-------------|
| 📲 | **Instant QR Pairing** | Scan once — no IP addresses, no config files |
| 🔒 | **Secure Token Auth** | UUID-based session token — only your device streams |
| ⚡ | **Low-Latency Streaming** | Direct HTTP POST over LAN — fast and responsive |
| 🎨 | **Sleek Desktop GUI** | Borderless PyQt5 window with smooth animations |
| 📱 | **Android Ready** | Kivy sender compiles to APK via Buildozer |
| 🔄 | **Camera Toggle** | Switch between front and rear cameras on-the-fly |

</div>

<br>
<br>

---

<div align="center">

## &nbsp;&nbsp;&nbsp;` 04 `&nbsp;&nbsp; HOW IT WORKS

</div>

<br>

<div align="center">

```
  ┌──────────────────────────┐              ┌───────────────────────────┐
  │     SENDER  (Mobile)     │              │    RECEIVER  (Desktop)    │
  ├──────────────────────────┤              ├───────────────────────────┤
  │                          │              │                           │
  │  1. Opens app            │              │  1. Launches app          │
  │                          │              │                           │
  │                          │              │  2. Generates UUID token  │
  │                          │◀── QR Code ──│     + local IP address    │
  │  3. Scans QR code        │              │  3. Displays QR code      │
  │                          │              │                           │
  │  4. Captures frame       │              │  4. Validates token       │
  │     via OpenCV           │─HTTP POST──▶│  5. Updates PyQt5 GUI     │
  │  5. Streams JPEG bytes   │   (JPEG)     │  6. Displays live frame   │
  └──────────────────────────┘              └───────────────────────────┘
```

</div>

<br>
<br>

---

<div align="center">

## &nbsp;&nbsp;&nbsp;` 05 `&nbsp;&nbsp; TECH STACK

</div>

<br>

<div align="center">

| Layer | Component | Technology |
|-------|-----------|-----------|
| 📱 **Mobile App** | Sender | Kivy · OpenCV · pyzbar · requests |
| 🖥️ **Desktop App** | Receiver | PyQt5 · Flask · OpenCV · qrcode · Pillow |
| 🔗 **Transport** | Streaming | HTTP POST · JPEG byte frames |
| 🔐 **Security** | Auth | UUID token validation per session |

</div>

<br>
<br>

---

<div align="center">

## &nbsp;&nbsp;&nbsp;` 06 `&nbsp;&nbsp; GETTING STARTED

</div>

<br>

**Step 1 — Clone**
```bash
git clone https://github.com/stebyvarghese1/Camdroid.git
cd Camdroid
```

**Step 2 — Set up the Receiver (Desktop)**
```bash
pip install -r requirements_receiver.txt
# numpy · opencv-python · qrcode · Pillow · Flask · PyQt5
```

**Step 3 — Set up the Sender (Mobile / Client)**
```bash
pip install -r requirements_sender.txt
# kivy · opencv-python · pyzbar · requests
```

> **Android?** Package `sender.py` into an APK using [Buildozer](https://buildozer.readthedocs.io/en/latest/).

<br>
<br>

---

<div align="center">

## &nbsp;&nbsp;&nbsp;` 07 `&nbsp;&nbsp; USAGE

</div>

<br>

**On your desktop — start the receiver**
```bash
python receiver.py
```

```
  1.  A borderless window opens
  2.  Click "Generate QR" → QR code appears on screen
```

**On your phone — start the sender**
```bash
python sender.py   # or launch the Android APK
```

```
  1.  Tap "Scan QR"
  2.  Point your camera at the QR on your desktop
  3.  Tap "Start Streaming"
  4.  Done — your phone is now a live wireless webcam
```

<div align="center">

> 🟢 &nbsp;No cables. No config. Streaming in seconds.

</div>

<br>
<br>

---

<div align="center">

## &nbsp;&nbsp;&nbsp;` 08 `&nbsp;&nbsp; PROJECT STRUCTURE

</div>

<br>

```
CamDroid/
│
├── receiver.py                ← PyQt5 + Flask desktop app
├── sender.py                  ← Kivy mobile camera sender
├── requirements_receiver.txt  ← Desktop dependencies
├── requirements_sender.txt    ← Mobile dependencies
└── README.md
```

<br>
<br>

---

<br>

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=130&section=footer&animation=fadeIn" width="100%"/>

### Built with ❤️ by [Steby Varghese](https://github.com/stebyvarghese1)

[![GitHub](https://img.shields.io/badge/GitHub-stebyvarghese1-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/stebyvarghese1)
&nbsp;
[![Portfolio](https://img.shields.io/badge/Portfolio-Visit-a78bfa?style=flat-square&logo=firefox&logoColor=white)](https://portfolio-v3ia.onrender.com/)
&nbsp;
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/steby-varghese)

<br>

**⭐ Star this repo if it made you ditch your USB cable!**

Licensed under [MIT](LICENSE)

</div>

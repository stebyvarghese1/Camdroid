
# 📡 CamDroid — Wireless Webcam via QR Scan

**CamDroid** transforms your smartphone into a wireless webcam!  
Just scan a QR code, and start live-streaming your camera feed to your desktop — no wires, no hassle.

---

## 🚀 Features

🖥️ Real-time webcam feed to desktop  
🔒 Secure tokenized connection via QR code  
📷 Mirror-mode display for natural preview  
🧭 Set and identify Receiver with custom ID  
🆗 Auto-hide QR code after successful connection  
🎥 Switch between front and back cameras  
📡 Works over local Wi-Fi network  
🖤 Sleek modern UI (Dark Mode)

---

## 🛠️ Built With

- **Python 3**
- **PyQt5** – Desktop GUI  
- **Flask** – Lightweight stream server  
- **OpenCV** – Image processing  
- **Kivy** – Mobile App framework  
- **qrcode & pyzbar** – QR generation & scanning  
- **Requests** – Sending frames over HTTP

---

## 📁 Project Structure

```
CamDroid/
├── receiver.py         # PyQt5 desktop receiver
├── sender.py           # Kivy mobile sender
├── requirements.txt    # Dependencies
├── README.md           # You're reading it!
```

---

## 🧭 How It Works

### Receiver:
- Starts a local Flask server (`/upload`) to accept video frames.
- Generates a QR code containing IP, token, and Receiver ID.
- Displays live feed with mirror view using OpenCV.

### Sender:
- Uses OpenCV to capture video.
- Scans the QR code and connects securely.
- Streams frames to the receiver via HTTP POST.

---

## 📸 Demo Screenshot

> Add screenshots here (e.g., QR scanning, live stream on receiver)

---

## 🎯 Gesture-Free Controls

| Action                    | Method                         |
|--------------------------|--------------------------------|
| Connect to Receiver       | Scan QR Code                   |
| Start Streaming           | Tap "Start Streaming"          |
| Stop Streaming            | Tap "Stop Streaming"           |
| Switch Camera             | Tap "Switch Camera"            |
| Set Receiver ID           | Tap "Set Receiver ID" on Desktop |
| Disconnect                | Tap "Disconnect" on Desktop    |

---

## ✅ Requirements

Install the following with pip:

```bash
# Receiver
pip install pyqt5 flask opencv-python qrcode numpy

# Sender
pip install kivy opencv-python pyzbar requests
```

---

## 🔧 How to Run

### 💻 Desktop Receiver

```bash
python receiver.py
```

- Click **Generate QR**
- Scan with your mobile app to start streaming

### 📱 Mobile Sender

```bash
python sender.py
```

- Tap **Scan QR**
- Then tap **Start Streaming**

> ✅ Make sure both devices are on the **same local network (Wi-Fi)**

---

## 📦 Packaging Ideas

- 📲 Deploy sender as Android APK using Buildozer
- 💻 Convert receiver to Windows executable using PyInstaller

---

## 📄 License

This project is licensed under the **MIT License**

```
MIT License

Copyright (c) 2025 King'sGuard

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction...
```

---

## 💡 Credits

- Powered by **OpenCV** and **Kivy**
- Inspired by a need for cable-free webcam streaming
- Created with ❤️ by **King'sGuard**

---

## ⭐️ Like this project?

Give it a ⭐ on GitHub and share it with others!

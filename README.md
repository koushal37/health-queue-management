# 🏥 NIT Health: Smart Queue & AI Assistant

> **A contactless, AI-powered OPD management system that eliminates physical lines and "ghost patients" in university health centers.**

![Status](https://img.shields.io/badge/Status-Hackathon_MVP-success)
![Tech](https://img.shields.io/badge/Tech-Google_Firebase_|_Gemini-blue)

## 🚩 The Problem
University health centers suffer from three major issues:
1.  **Overcrowding:** Sick students stand in long physical lines for hours.
2.  **Anxiety:** No visibility on wait times ("When is my turn?").
3.  **Wasted Time:** "Ghost Patients" book slots but don't show up, leaving doctors idle.

## 💡 The Solution
**NIT Health** is a dual-interface web application that digitizes the entire patient journey. It uses **Edge Computing** for privacy and **Cloud Sync** for speed.

### 🌟 Key Features

#### 📱 For Students (Mobile PWA)
* **🛡️ Edge-AI Verification:** Scans Student ID cards locally in the browser using **Tesseract.js**. No personal ID photos are sent to the cloud, ensuring 100% privacy.
* **🤖 AI Nurse:** Integrated **Google Gemini AI** analyzes symptoms instantly to provide comforting home remedy advice while waiting.
* **🔔 Smart Alerts:** Sends a "Run!" notification and starts a **2-Minute Emergency Timer** when the doctor calls.
* **📋 Live Queue:** A real-time, collapsible board showing exactly who is ahead.

#### 👨‍⚕️ For Doctors (Dashboard)
* **⚡ Zero-Latency Sync:** Powered by **Firebase Firestore**, the dashboard updates instantly without refreshing.
* **⏱️ Anti-Ghosting Protocol:** If a student doesn't arrive within the 2-minute timer, the system allows the doctor to mark them as "Expired" and move to the next patient.
* **🩺 3-Step Workflow:** Call $\rightarrow$ Patient Entered $\rightarrow$ Finish.

---

## 🛠️ Tech Stack (Google Technologies)

| Component | Technology | Use Case |
| :--- | :--- | :--- |
| **Backend / DB** | **Google Firebase** | Firestore (Real-time DB) & Hosting |
| **Artificial Intelligence** | **Google Gemini Pro** | Symptom Analysis & Triage Advice |
| **Edge Processing** | **Tesseract.js** | Client-side OCR (ID Verification) |
| **Frontend** | **HTML5 / CSS3** | Medical-Blue Responsive UI |

---

## 📸 Usage Guide

### 1. Student Check-In
1.  Enter Roll Number and upload ID Card image.
2.  **Edge-AI** verifies the ID locally.
3.  Enter Symptoms and click "Get Token".
4.  **AI Nurse** provides immediate health advice.

### 2. The Waiting Room
* Monitor the **Live Queue** to see your position.
* Wait for the **"Doctor Calling"** alert.

### 3. The Doctor's Action
1.  Doctor sees the student on the dashboard.
2.  Clicks **"📢 CALL"** $\rightarrow$ Triggers Red Timer on Student's phone.
3.  Student arrives $\rightarrow$ Doctor clicks **"✅ PATIENT ENTERED"**.
4.  Consultation done $\rightarrow$ Doctor clicks **"🏁 DONE"**.

---

## ⚙️ How to Run Locally

This project is serverless and runs directly in the browser!

1.  **Clone the Repo:**
    ```bash
    git clone [https://github.com/your-username/nit-health-project.git](https://github.com/your-username/nit-health-project.git)
    ```
2.  **Open Student Portal:**
    Open `index.html` in your browser (Mobile view recommended).
3.  **Open Doctor Dashboard:**
    Open `doctor.html` in a separate tab/window (Desktop view).

---

### 🔮 Future Roadmap
* [ ] Integration with Campus Pharmacy for digital prescriptions.
* [ ] "Health Heatmap" for admin to track disease outbreaks in hostels.
* [ ] Offline Mode support using PWA Service Workers.

---
*Built with ❤️ for the Google Developer Student Clubs Hackathon.*
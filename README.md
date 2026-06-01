````markdown
# ⠃⠗ BrailleVision

## Real-Time Physical Braille to English Using Camera-Based AI

### BrailleVision Hackathon 2026 Submission  
Virtual · OpenAI × Rotary India

---

# 🔍 Overview

BrailleVision is an AI-powered accessibility tool that converts **real physical Braille** into spoken and readable English in real time using a camera.

Unlike traditional Unicode Braille translators, this system works directly with:
- embossed Braille
- handwritten Braille
- printed Braille patterns

The application captures live camera frames or uploaded images and uses AI vision analysis to detect Braille dot structures, segment them into cells, decode the text, and read the result aloud using text-to-speech.

The goal of BrailleVision is to make Braille more accessible for caregivers, students, teachers, volunteers, and visually impaired users through a lightweight browser-based solution.

---

# ✨ Key Features

| Feature | Description |
|---|---|
| Live Camera Scanning | Scan Braille in real time using WebRTC camera access |
| Image Upload Support | Upload JPEG, PNG, or HEIC images |
| AI-Based Braille Recognition | Detects actual physical dot structures instead of Unicode symbols |
| Grade 1 & Grade 2 Support | Supports standard English Braille decoding |
| Confidence Scoring | Displays HIGH / MEDIUM / LOW confidence for scans |
| Text-to-Speech | Reads decoded text aloud using Web Speech API |
| Voice Guidance | Spoken instructions for easier accessibility |
| Session History | Saves previous scans with timestamps |
| Export Functionality | Download decoded results as `.txt` |
| Accessibility-First UI | High contrast, large controls, responsive layout |
| Zero Installation | Runs directly in the browser |

---

# 🧠 How It Works

```text
Camera / Uploaded Image
        │
        ▼
Image Compression & Base64 Encoding
        │
        ▼
Claude Vision API (claude-sonnet-4)
        │
        ├── Detect physical Braille dots
        ├── Segment 6-dot Braille cells
        ├── Decode Grade 1 / Grade 2 Braille
        ├── Extract English text
        └── Return confidence + metadata
        ▼
Frontend Response Parser
        ▼
Display Result + Text-to-Speech Output
````

---

# 💡 Why AI Vision Instead of Traditional Computer Vision?

Traditional Braille recognition systems often require:

* large labeled datasets
* custom-trained models
* GPU training infrastructure
* controlled lighting environments

BrailleVision instead uses a vision-language model to handle:

* variable lighting
* shadows
* tilted camera angles
* inconsistent embossing depth
* handwritten Braille patterns

This significantly reduces development complexity while improving flexibility during real-world usage.

---

# 🛠 Technology Stack

| Layer          | Technology Used                 |
| -------------- | ------------------------------- |
| Frontend       | HTML5, CSS3, Vanilla JavaScript |
| Camera Access  | WebRTC (`getUserMedia`)         |
| AI Recognition | Anthropic Claude Vision API     |
| Speech Output  | Web Speech API                  |
| File Handling  | FileReader API + Drag & Drop    |
| Hosting        | GitHub Pages / Netlify          |

---

# 🚀 How to Run

## Option 1 — Open Directly

1. Download the project files
2. Open `index.html`
3. Allow camera permissions
4. Point the camera at physical Braille
5. Press **Scan**

---

## Option 2 — Run with Local Server

```bash
python3 -m http.server 8080
```

Then open:

```text
http://localhost:8080
```

---

## Option 3 — Deploy on GitHub Pages

1. Upload files to a GitHub repository
2. Open repository settings
3. Enable GitHub Pages from the `main` branch
4. Access the deployed website link

---

# 📋 Hackathon Requirements Covered

* [x] Real physical Braille recognition
* [x] Camera-based image capture
* [x] AI-powered Braille detection
* [x] English text conversion
* [x] Real-time / near real-time processing
* [x] Text-to-speech support
* [x] Accessibility-focused interface
* [x] Working demo support
* [x] Source code documentation
* [x] Browser-based deployment

---

# 🔮 Future Improvements

1. OpenCV.js preprocessing for better dot isolation
2. Fully offline on-device AI support
3. Perspective correction for tilted pages
4. Mobile application version
5. Continuous multiline Braille scanning
6. Nemeth Braille support for mathematics
7. Multi-language Braille decoding
8. Edge AI using ONNX/WebNN
9. Haptic feedback integration
10. Simplified caregiver mode

---

# 📂 Built During the Hackathon

The following components were designed and implemented during the hackathon period:

* Full UI/UX design
* Camera scanning pipeline
* AI prompt engineering workflow
* Braille response parsing system
* Accessibility and voice guidance features
* Session history and export functionality

### External APIs / Libraries Used

* Anthropic Claude Vision API
* WebRTC APIs
* Web Speech API
* Google Fonts

---

# 👤 Developer

**Mrunal Gangurde**
Developer · AI & Data Science Enthusiast

GitHub: *(add your GitHub link)*
LinkedIn: *(add your LinkedIn link)*

---

# 📄 License

MIT License

---

## Built for BrailleVision Hackathon 2026

Making Braille more accessible through AI-powered assistive technology.

```
```

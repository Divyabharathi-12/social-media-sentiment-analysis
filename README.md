
# Social Media Sentiment Analyzer

A full-stack web application that performs real-time sentiment analysis on social media text using Natural Language Processing (NLP).

## 🏗️ System Architecture

The application follows a classic **Client-Server Architecture** split into distinct operational layers:

1. **Presentation Layer (Client):** Built with HTML5, CSS3, and JavaScript. It uses **Chart.js** to render a dynamic, real-time doughnut chart tracking sentiment distribution.
2. **Application Layer (Server):** Powered by **Python Flask**, managing routing, request handling, and JSON API exposures.
3. **AI/ML Engine Layer:** Utilizes the **NLTK VADER** (Valence Aware Dictionary and sEntiment Reasoner) model to evaluate text intensity and classify sentiment.
4. **Data Layer:** Currently uses an volatile, in-memory list (`mock_history`) to track session logs temporarily.

---

## 🔌 API Specification

### 1. Health Check
* **Endpoint:** `/api/health`
* **Method:** `GET`
* **Description:** Verifies that the backend server layer is live and running.
* **Success Response (200 OK):**
  ```json
  {
    "environment": "development",
    "status": "healthy",
    "timestamp": "2026-06-27 16:30:00.123456"
  }

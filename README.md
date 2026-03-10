# WaveForm Service

> An interactive waveform player component for the StreamBoard audio platform — built as a self-contained frontend microservice.

---

## Overview

This service renders a fully interactive audio waveform for individual song pages within the StreamBoard application. Users can visualize the audio structure of a track and click anywhere along the waveform to jump to that point in the song. All visual feedback — including playback progress and seek position — is rendered in real time using the **HTML5 Canvas API**.

It is one of several independently deployable frontend services that compose the larger StreamBoard platform.

---

## Features

- 🎵 **Interactive waveform playback** — click anywhere on the waveform to seek to that position
- 🎨 **Canvas-rendered visuals** — smooth, real-time graphical updates driven by the HTML5 Canvas API
- ⚛️ **React component architecture** — embeddable into any parent application
- 🐳 **Dockerized** — ships with a `Dockerfile` and `docker-compose` for easy local setup and deployment

---

## Tech Stack

| Layer | Technology |
|---|---|
| **UI Framework** | React |
| **Graphics** | HTML5 Canvas API |
| **Backend** | Node.js |
| **Database** | MongoDB |
| **Bundler** | Webpack + Babel |
| **Testing** | Jest |
| **CI/CD** | CircleCI |
| **Containerization** | Docker + Docker Compose |
| **Linting** | ESLint |

---

## Project Structure

```
waveFormService/
├── client/       # React component and Canvas rendering logic
├── server/       # API layer
├── db/           # MongoDB models and connection
├── images/       # Component screenshots
└── dataGen.js    # Database seed script
```

---

## Getting Started

### Prerequisites

- Node.js 6.4.1+
- MongoDB (running locally)
- npm

### Installation

```bash
npm install -g webpack
npm install
```

### Seed the Database

```bash
node dataGen.js
```

### Run the Service

```bash
npm start
```

### Run with Docker

```bash
docker-compose up
```

---

## Part of StreamBoard

This service is one component in the StreamBoard microservice ecosystem:

| Service | Description |
|---|---|
| [waveFormService](https://github.com/StreamBoard98/waveFormService) | ← **You are here** — Waveform player UI |
| [suggestedTrackService](https://github.com/StreamBoard98/suggestedTrackService) | Recommended tracks sidebar |
| [commentsListandSubmissionService](https://github.com/StreamBoard98/commentsListandSubmissionService) | Comments section |
| [videoPlayerSkeletonService](https://github.com/StreamBoard98/videoPlayerSkeletonService) | Video player shell |

## Images
[![rendered component](./images/waveform.png)](https://youtu.be/j5EBjo9fPQ4)<!-- .element height="50%" width="50%" -->

Tech Stack Summary - FitFlow Redesign

Frontend
Recommended: React Native (with React Native Web)

- Reuses the existing FitFlow codebase and the team's JS/TS skills - directly aligned with the
  startup's need for speed to market.
- One codebase serves iOS, Android and Web (via React Native Web).
- Mature Firebase SDKs, TensorFlow.js and native camera/ML bridges directly support the AI
  workout engine and computer-vision nutrition logger.
- Hybrid approach: performance-critical modules (on-device TensorFlow Lite inference, camera
  pipeline) implemented as native modules bridged into React Native, keeping 90%+ code sharing.

Rejected alternatives: Flutter (would require a full rewrite despite similar performance), Kotlin
Multiplatform (still needs native UI written twice), Swift/SwiftUI (iOS-only, no Android/Web).

Backend
Recommended: Node.js + Express (microservices)

- Consistent with the case study's existing choice of Node.js/Express + Firebase for real-time
  social features and scalable notifications.
- Keeps the mid-sized team productive in a single primary language (JavaScript/TypeScript).
- AI/computer-vision workloads isolated into a separate FastAPI (Python) microservice, called over
  REST/gRPC, for best-in-class ML tooling without forcing the whole backend into Python.

Database
Recommended: PostgreSQL + Firebase (Firestore/RTDB)

- PostgreSQL for structured, relationally-sensitive data (user profiles, workout history, billing)
  — ACID guarantees and strong reporting/query support.
- Firebase Firestore/RTDB for real-time social feeds and lightweight profile data — native
  real-time sync, minimal setup.

Authentication
Recommended: Firebase Auth

- Integrates natively with the Firestore/RTDB layer already used for social features.
- Pre-built SDKs, social login, MFA support, GDPR-compliant infrastructure.
- Minimal setup and low cost for a mid-sized team.

AI / Computer Vision
Recommended: FastAPI (Python) microservice

- TensorFlow Lite for on-device personalization (fast, privacy-preserving).
- Cloud ML service for heavier/advanced model updates.
- ML Kit for camera-based food recognition in the nutrition logger.

## Summary
Frontend| React Native (+ Web) 
Backend | Node.js + Express 
Database| PostgreSQL + Firebase 
Auth    | Firebase Auth 
AI/CV   | FastAPI + TensorFlow Lite + ML Kit 

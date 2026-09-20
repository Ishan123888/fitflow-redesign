# FitFlow Redesign

A full-scale redesign of the FitFlow fitness tracking app, addressing retention issues through
AI-powered personalized workout plans, social community features, and improved nutrition tracking.

Project for IT3060 - Human Computer Interaction

## Project Structure
- `frontend/` - React Native app (iOS / Android / Web)
- `backend/` - Node.js/Express microservices (Workout, Social, Nutrition, Notification)
- `ai-service/` - FastAPI Python microservice (AI personalization + computer-vision nutrition logging)
- `docs/` - Supporting documentation for the lab report

## Documentation
- [Tech Stack Summary](docs/tech-stack-summary.md) - frontend, backend, database & auth recommendations
- [Comparison Matrix](docs/comparison-matrix.md) - weighted technology comparison
- [Architecture Diagram](docs/architecture.png)
- [ADR-001](docs/adr-001.md) - Architecture Decision Record

## Recommended Technology Stack
- **Frontend:** React Native (+ React Native Web)
- **Backend:** Node.js + Express (microservices)
- **Database:** PostgreSQL + Firebase (Firestore/RTDB)
- **Auth:** Firebase Auth
- **AI/Computer Vision:** FastAPI (Python) + TensorFlow Lite + ML Kit

## Author
IT23810464 - Ekanayaka E.W.I.D

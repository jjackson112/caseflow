CaseFlow is an internal case management system designed to handle client intake, case tracking, and real-time collaboration for small teams.

The application allows authenticated users to create clients, manage cases, track status changes, and append internal notes through an audit-friendly, append-only log. Real-time updates ensure all connected users stay in sync without manual refreshes.

CaseFlow is built as a full-stack application using Flask and PostgreSQL on the backend, with a lightweight React frontend consuming a REST API and live update stream.

# Key Features
Role-based authentication and access control

Client intake and multi-case tracking

Case status workflows with real-time updates

Append-only internal notes for auditability

Live activity synchronization across connected clients

# Tech Stack
Backend: Flask, SQLAlchemy, PostgreSQL

Auth: JWT-based authentication

Real-Time: WebSockets (or SSE — be explicit which one)

Frontend: React

Architecture: Flask app factory, blueprints 
# Architecture Decisions
Used Flask blueprints and an app factory pattern to maintain a modular and scalable backend structure

Chose an append-only notes model to preserve historical accuracy and support audit-style workflows

Implemented real-time updates to ensure state consistency across clients without polling

Centralized error handling and validation to prevent silent failures and inconsistent state

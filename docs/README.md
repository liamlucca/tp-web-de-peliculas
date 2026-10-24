# CineWeb — Documentation

## 1. Project Overview

CineWeb is a web application for managing and viewing audiovisual content, including movies and series. The system includes functionality for content management, ratings, a watch-later list, content reports, appeals, and administrative moderation.

For the project description, team members, domain model, and functional scope, see the [Project Proposal](../proposal.md).

## 2. Repositories

- **Frontend:** [CineWeb Frontend](https://github.com/liamlucca/cineweb-frontend)
- **Backend:** [CineWeb Backend](https://github.com/EduardoMarino73/TP-BackEnd)
- **Documentation and Proposal:** [CineWeb Documentation](https://github.com/liamlucca/tp-web-de-peliculas)

## 3. Installation and Execution

See [Installation and Execution](instalacion.md) for instructions on configuring the database, installing dependencies, and running the frontend and backend.

## 4. Team Coordination and Project Progress

See [Team Coordination and Project Progress](minutas.md) for information about team communication, task coordination, and project progress.

## 5. Task and Issue Tracking

See [Task and Issue Tracking](seguimiento.md) for information about collaborative development, task coordination, and issues identified during implementation.

## 6. Development History

This section highlights important commits that document the project's development progress.

### Backend

- [User and Moderation System](https://github.com/EduardoMarino73/TP-BackEnd/commit/9d30d59a33fbbbf0ac39682f1c2a3e0414af9ec9) — Added user-related functionality, audiovisual reports, and appeal management.
- [ORM Integration](https://github.com/EduardoMarino73/TP-BackEnd/commit/e87e2cb40bea49bd53e2bc587c22846798ed47a2) — Integrated the Object-Relational Mapper (ORM) into the project architecture for database access.
- [Series CRUD Operations](https://github.com/EduardoMarino73/TP-BackEnd/commit/7877d762e1db51ccb28487ceec833d58f3f10917) — Implemented create, read, update, and delete operations for series.
- [Audiovisual Hierarchy](https://github.com/EduardoMarino73/TP-BackEnd/commit/6436ddf6282221e933515f774b082d16025538d0) — Added the audiovisual hierarchy for movies and episodes.
- [Watch Later List](https://github.com/EduardoMarino73/TP-BackEnd/commit/154271a1e93807f192f77ebd4f1272eabbfcca2b) — Added the `/api/watch-later` endpoint.
- [Report Types Catalog](https://github.com/EduardoMarino73/TP-BackEnd/commit/390f6c8a52fb10394d2ec263e7e5dbb9faedf174) — Implemented CRUD operations for `/api/report-types`.
- [Authentication for Movie Creation](https://github.com/EduardoMarino73/TP-BackEnd/commit/60e78988253e71d26360d7372653d7939c9a0e07) — Protected movie creation with an authentication token and identified the uploader through the authenticated user.
- [Audiovisual Thumbnails and Series Covers](https://github.com/EduardoMarino73/TP-BackEnd/commit/024256adb45fe1d2a84020bed61a04100bc8cb8f) — Added thumbnails for movies and episodes, as well as optional series cover images.

### Backend Pull Requests

- [Pull Request #7](https://github.com/EduardoMarino73/TP-BackEnd/pull/7)
- [Pull Request #8](https://github.com/EduardoMarino73/TP-BackEnd/pull/8)

### Frontend

Frontend commits and pull requests documenting major features, improvements, and integration work will be added here.

## 7. Project Proposal

See the [Project Proposal](../proposal.md) for the project description, team members, domain model, and functional scope.

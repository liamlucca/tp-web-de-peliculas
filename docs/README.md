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

The following commits highlight important milestones in the development of the CineWeb frontend.

1. **[Initial Project Structure](https://github.com/liamlucca/cineweb-frontend/commit/94c8558851e326d55204c6ad7bc0cb430053102b)** — Established the initial project structure.

2. **[Fetching Movies from the Backend](https://github.com/liamlucca/cineweb-frontend/commit/75132696bd416900ba7ffe0e2970d30daf9fd03d)** — Implemented the retrieval of movie data from the backend.

3. **[Authentication Context and Protected Routes](https://github.com/liamlucca/cineweb-frontend/commit/1b10c010c33939197d3d269ae3b05371546b79b1)** — Added authentication context, the `useAuth` hook, and protected routes.

4. **[Login and Registration Forms](https://github.com/liamlucca/cineweb-frontend/commit/6b011fdfe3d9acfb48884d573ae8d54304966436)** — Connected the login and registration forms to the authentication service.

5. **[Authentication Unit Tests](https://github.com/liamlucca/cineweb-frontend/commit/6c648a17ecec36f192dd830d365cde3b40c43a03)** — Added unit tests for `ProtectedRoute` and `AuthPage` using Vitest.

6. **[Content Catalog Design](https://github.com/liamlucca/cineweb-frontend/commit/f15596964ea02d648d18d840f712f2efa4239d0f)** — Presented the content catalog using cards, thumbnails, a featured banner, and carousels.

7. **[Series Integration](https://github.com/liamlucca/cineweb-frontend/commit/2bfd7815a35782d72ec2d8f1cf6db7535c0339b3)** — Connected the series pages to the backend through `seriesService`.

8. **[Series Upload Page](https://github.com/liamlucca/cineweb-frontend/commit/e6d136a055b242867e60a923b85e6f9d1044fd2e)** — Added forms for uploading series, seasons, and episodes.

9. **[Watch Later Feature](https://github.com/liamlucca/cineweb-frontend/commit/7a56752f0433921a8d9ccb91135ae4462087b0b0)** — Added controls to save movies and series for later viewing, along with a dedicated list page.

10. **[Audiovisual Reporting](https://github.com/liamlucca/cineweb-frontend/commit/a374eb187971a49753e725633c60e5990e0f98a9)** — Implemented the submission of reports for movies and series.

11. **[Administration Page](https://github.com/liamlucca/cineweb-frontend/commit/c59b94110f115f3d0b944c0207b9bc26feb24582)** — Added an administration interface for managing pending appeals and accounts.

12. **[Backend User Authentication Integration](https://github.com/liamlucca/cineweb-frontend/commit/a5fc3c1d4be790657b7d4ea8ddb9c237d65a5573)** — Connected login and registration to the backend's `/api/users` endpoints.

### Frontend Pull Requests

- [Pull Request #1](https://github.com/liamlucca/cineweb-frontend/pull/1)
- [Pull Request #2](https://github.com/liamlucca/cineweb-frontend/pull/2)

## 7. Project Proposal

See the [Project Proposal](../proposal.md) for the project description, team members, domain model, and functional scope.

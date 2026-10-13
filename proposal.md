# DSW Project Proposal

## Team
### Members
* 54617 - Marino, Eduardo
* 55197 - Requelme, Candela M
* 54720 - Lucca, Liam Santiago

### Repositories
* [design](https://app.diagrams.net/#G1eFO_b5KQ9T8M1xZn47CeNbCgubCR8u94)
* [frontend app](https://github.com/liamlucca/cineweb-frontend)
* [backend app](https://github.com/EduardoMarino73/TP-BackEnd)
*Note*: if you use a monorepo, give a single link to the fullstack app.

### Pull requests
* Frontend: https://github.com/liamlucca/cineweb-frontend/pull/2
* Backend: https://github.com/EduardoMarino73/TP-BackEnd/pull/7

## Topic
### Description
A management system for series and movies, where users can upload and delete audiovisual content they authored, watch it, rate it with "Like" / "Dislike" and save it to "Watch later". A user can also report audiovisual content by choosing a reason from a catalog; when a piece of content gathers 3 reports a case opens, which the content's owner can appeal. Then an administrator reviews the appeal: if it is rejected, the content is suspended.

### Model
https://drive.google.com/file/d/16af4iugaq9fV1vGB6cZFufNQbk7T6Gk6/view?usp=sharing

## Functional Scope

### Minimum Scope

Regularity:
|Req|Detail|
|:-|:-|
|Simple CRUD|1. Audiovisual CRUD: movies and series (with seasons and episodes); create with video, thumbnail and duration, view, edit and logical delete, only by the uploader<br>2. Report Type CRUD: catalog of report reasons managed by the administrators<br>3. Report CRUD: created by the viewer (one reason from the catalog + optional details, required for "Other"); viewed, filtered and its status changed by the administrator through the appeal<br>4. User CRUD: sign-up, login, view and edit the profile, activate and deactivate accounts|
|Dependent CRUD|1. Administrator CRUD {depends on} User CRUD<br>2. Viewer CRUD {depends on} User CRUD<br>3. Appeal CRUD {depends on} Report CRUD: created and withdrawn by the content's owner, viewed and resolved (accept / reject) by the administrator|
|List<br>+<br>detail| 1. List of audiovisual content filtered by category, type (movie / series) and partial title match => detail of the content with the user who uploaded it and its ratings<br> 2. List of reports (moderation cases) filtered by case number, status and reason; shows the reported user's name, the content's title and the grouped reasons => the detail shows every report with its reason and details, and the appeal|
|Use case/Epic|1. Add audiovisual content to "Watch later"<br>2. Look up a report's data<br>3. Rate with "Like" / "Dislike"|


Additional for Approval<br>

|Req|Detail|
|:-|:-|
|CRUD |1. Audiovisual CRUD<br>2. Report Type CRUD<br>3. Report CRUD<br>4. User CRUD<br>5. Administrator CRUD<br>6. Viewer CRUD<br>7. Appeal CRUD<br>8. Watch Later CRUD<br>9. Review CRUD|
|Use case/Epic|1. Add audiovisual content to "Watch later"<br>2. Look up a report's data<br>3. Rate with "Like" / "Dislike"|


### Voluntary Additional Scope

*Note*: The Voluntary Additional Scope is optional, but it helps complete the system's functionality and will be taken into account in the grade according to its complexity and effort.

|Req|Detail|
|:-|:-|
|Lists |1. "Reports about my content": the viewer sees the open cases about the content they uploaded, with their status and the status of their appeal|
|Use case/Epic|1. Withdraw an appeal that has not been reviewed yet (the case can be appealed again)|
|Other|1. Thumbnail and duration of each video read in the browser when it is uploaded; optional cover for series<br>2. Logical delete of movies, series, seasons and episodes|

### Technical notes
* The backend's persistence uses the Repository pattern with `mysql2` and SQL instead of an ORM (team decision).

# ALAB 318.3.1: Expanding a RESTful API

This assignment will ask you to expand the example REST API application that was explored during the lesson, adding additional routes and features that are common with an API of its kind.
Feel free to reference the lesson materials, express documentation, and other resources when creating these additional features, but think critically about how you want to approach your own solution. Sometimes, the way things are presented the first time are not the best way to do them!
When working on a team, especially with legacy code, you can never assume that something is correct just because it was previously the accepted way of doing it. Look for ways to increase the efficiency of the application and the efficiency of the development process!

## Objectives
Add additional features to an existing RESTful Express API.
Refactor existing code for efficiency, organization, and/or performance.

### Part 1: Exploring Existing Routes
The application has the following routes as a starting point:
- GET / 
- GET /api
- GET /api/users
- POST /api/users
- GET /api/users/:id
- PATCH /api/users/:id
- DELETE /api/users/:id
- GET /api/posts
- POST /api/posts
- GET /api/posts/:id
- PATCH /api/posts/:id
- DELETE /api/posts/:id

### Part 2: Adding Additional Routes
Create the following routes, using good organizational and coding practices:
- GET /api/users/:id/posts
Retrieves all posts by a user with the specified id.
- GET /api/posts?userId=<VALUE>
Retrieves all posts by a user with the specified postId.
It is common for APIs to have multiple endpoints that accomplish the same task. This route uses a "userId" query parameter to filter posts, while the one above uses a route parameter.
- GET /comments
Note that we do not have any comments data yet; that is okay! Make sure that you create a place to store comments, but you do not need to populate that data.
- POST /comments
When creating a new comment object, it should have the following fields:
id: a unique identifier.
userId: the id of the user that created the comment.
postId: the id of the post the comment was made on.
body: the text of the comment.
- GET /comments/:id
Retrieves the comment with the specified id.
- PATCH /comments/:id
Used to update a comment with the specified id with a new body.
- DELETE /comments/:id
Used to delete a comment with the specified id.
- GET /comments?userId=VALUE 
Retrieves comments by the user with the specified userId.
- GET /comments?postId=VALUE
Retrieves comments made on the post with the specified postId.
- GET /posts/:id/comments
Retrieves all comments made on the post with the specified id.
- GET /users/:id/comments
Retrieves comments made by the user with the specified id.
- GET /posts/:id/comments?userId=VALUE
Retrieves all comments made on the post with the specified id by a user with the specified userId.
- GET /users/:id/comments?postId=VALUE
Retrieves comments made by the user with the specified id on the post with the specified postId.

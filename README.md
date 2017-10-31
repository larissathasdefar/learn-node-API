
**API Documentation** -  project of social media.
===================

### About
The objective of this project is the develop an API in NodeJs to learn how is create an node API, and use this like a default backend on projects to learn about Ruby, ReactJs, React Native and other languages.

### Tables

_Legenda:_
*: Primary Key
+: Foreign key

| Account  |
| -------- |
| *id      |
| name     |
| email    |
| photo    |
| password |


| Post     |
| -------- |
| *id      |
| content  |
| photo    |
| +owner   |

| Comment   |
| --------  |
| *id       |
| +post     |
| +user     |
| content   |
| date      |

| Friendship              |
| ----------------------- |
| *+user                  |
| *+friend_account        |
| status (waiting/friend) |


### What is this going to do?

**The user will be able to:**

* Create, edit or delete a post with a text and/or a photo
* Comment, edit or delete a comment in a post
* Add or delete a friend
* Create, edit or delete your account

### Routes

Login
- **[POST] "/login"**: Verify if the email and password are correct
- **[POST] "/signup"**: Create an account

Account
- **[GET] "/account"**: Returns the data about the logged user
- **[PATCH] "/account"**: Edit the logged user
- **[DELETE] "/account"**: Delete the logged user

Post
- **[POST] "/post"**: Create a post
- **[GET] "/post/:id"**: Returns the data about the post
- **[PATCH] "/post/:id"**: Edit the post
- **[DELETE] "/post/:id"**: Delete the post

Comment
- **[POST] "/comment/:post"**: Create a comment
- **[GET] "/comment/:id"**: Returns the comment
- **[GET] "/comments/:post"**: Returns all the comments on the post
- **[PATCH] "/comment/:id"**: Edit the comment
- **[DELETE] "/comment/:id"**: Delete the comment

Friendship
- **[POST] "/friendship/"**: Create a request of friendship
- **[GET] "/friendship/:id"**: Returns the data about the friendship
- **[DELETE] "/friendship/:id"**: Delete the friendship
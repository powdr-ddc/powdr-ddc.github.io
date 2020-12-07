# Powdr Endpoints

# Global
## Server context path

`/Powdr`

## Authentication

All endpoints are secured by OAuth 2.0. Any requests not including an `Authorization` header with a valid `Bearer` token will result in `401 Unauthorized` status.

## Content types

Except where noted, all endpoints produce and/or consume `application/json`. (Some property-specific `PUT` endpoints produce and consume `text/plain`.)


## Endpoints

`GET /users`

**Description**  
Return list of `users` by name  
**Path parameters**  
(None)  
**Query Parameters**  
- `name`  
**Request body**  
(None)  
**Response body**  
`User``[]`  
**Response status**  
- `200 OK`

`GET /users/me`

**Description**   
Return the current `User` (profile)  
**Path parameters**  
(None)  
**Query Parameters**     
- `name`  
**Request body**  
(None)  
**Response body**  
`User`  
**Response status**  
- `200 OK`

`PUT /users/me/picture`

**Description**  
Set profile picture for the current `User`  
**Path parameters**  
(None)  
**Query Parameters**  
(None)  
**Request body**  
(None)  
**Response body**  
`User`  
**Response status**    
- `200 OK`

`GET /users/me/name`

**Description**  
Retrieves the display name of current `user`  
**Path parameters**  
(None)  
**Query Parameters**  
(None)  
**Request body**  
(None)  
**Response body**  
`String (Content-type: text/plain)`  
**Response status**  
- `200 OK`

`PUT /users/me/name`

**Description**  
Change name of current `user`  
**Path parameters**  
(None)  
**Query Parameters**  
(None)  
**Request body**  
`String (Content-type: text/plain)`  
**Response body**  
`String (Content-type: text/plain)`  
**Response status**  
- `200 OK`  
- `400 BAD REQUEST`  
    Empty request body
    
`GET /ski-resorts`

**Description**  
Return  all `ski-resort`  
**Path parameters**  
(None)  
**Query Parameters**  
- `name`  
- `latitude`  
- `longitude`  
**Request body**  
(None)  
**Response body**  
`SkiResort[]`  
**Response status**  
- `200 OK`  
- `404 NOT FOUND`

`GET /ski-resorts/{skiResortId}`

**Description**  
Return `ski-resort`  
**Path parameters**  
- `skiResortId`  
    `SkiResort` identifier  
**Query Parameters**  
- `name`  
- `latitude`  
- `longitude`  
**Request body**  
(None)  
**Response body**  
`SkiResort`  
**Response status**  
- `200 OK`  
- `404 NOT FOUND`
  
`GET /trips`
  
**Description**  
Returns all `Trips`  
**Path parameters**  
(None)  
**Query Parameters**  
(None)  
**Request body**  
(None)  
**Response body**  
`Trip[]`  
**Response status**  
- `200 OK`  
- `404 NOT FOUND`

`GET trips/{tripId}`

**Description**  
Return the specified `trip`  
**Path parameters**  
`tripId`  
**Query Parameters**  
(None)  
**Request body**  
(None)  
**Response body**  
`Trip`  
**Response status**  
- `200 OK`  
- `404 NOT FOUND`

`POST trips/`

**Description**  
Create a new `trip`  
**Path parameters**  
(None)  
**Query Parameters**  
(None)  
**Request body**  
`Trip`  
**Response body**  
`Trip`  
**Response status**  
- `201 CREATED`  
- `400 BAD REQUEST`  
    One or more invalid `Trip` properties
      
`GET favorite-ski-resorts/`

**Description**  
Return favorite ski resorts for the current `user`  
**Path parameters**  
(None)  
**Query Parameters**  
(None)  
**Request body**  
(None)  
**Response body**  
`SkiResort[]`  
**Response status**  
- `200 OK`

`POST /favorite-ski-resorts`

**Description**  
Adds ski resort to favorites of current `user`  
**Path parameters**  
(None)  
**Query Parameters**  
(None)  
**Request body**  
`SkiResort`  
**Response body**  
`SkiResort`  
**Response status**  
- `201 OK`  
- `400 BAD REQUEST`  
    Empty request body
    
`DELETE /favorite-ski-resorts/{skiResortId}`

**Description**  
Deletes ski resort from favorites of current `user`  
**Path parameters**  
`skiResortId`  
**Query Parameters**  
(None)  
**Request body**  
`SkiResort`  
**Response body**  
(None)  
**Response status**  
- `204 NO CONTENT`

`GET /friends`

**Description**  
Returns friends of the current `User`  
**Path parameters**  
(None)  
**Query Parameters**  
(None)  
**Request body**  
(None)  
**Response body**  
`User[]`  
**Response status**  
- `200 OK`

`POST /friends`

**Description**  
Add a user to current list of `friends`  
**Path parameters**  
(None)  
**Query Parameters**  
(None)  
**Request body**  
`User`  
**Response body**  
`User`  
**Response status**  
- `201 OK`  
- `400 BAD REQUEST`  
    Empty request body

`DELETE /friends/{userId}`

**Description**  
Remove specified user from current list of `friends`  
**Path parameters**  
`userId`  
**Query Parameters**  
(None)  
**Request body**  
(None)  
**Response body**  
(None)  
**Response status**  
- `204 NO CONTENT`

`GET users/{userId}`

**Description**  
Returns a specific friend of the current `user`  
**Path parameters**  
- `userId`  
    Friend `user` identifier  
**Query Parameters**  
(None)  
**Request body**  
(None)  
**Response body**  
`User`  
**Response status**  
- `200 OK`  
- `404 NOT FOUND`

`GET /posts`

**Description**  
Return posts optionally filtered  
**Path parameters**  
(None)  
**Query Parameters**  
- `user`  
- `start`  
- `end`  
- `content`  
- `keyword`  
**Request body**  
(None)  
**Response body**  
`Post[]`  
**Response status**  
- `200 OK`

`GET /posts/{postId}`

**Description**  
Returns a specific post  
**Path parameters**  
`postId`  
**Query Parameters**  
(None)  
**Request body**  
(None)  
**Response body**  
`Post[]`  
**Response status**  
- `200 OK`

`POST /posts`

**Description**  
Creates a new post for the current `User`  
**Path parameters**  
(None)  
**Query Parameters**  
(None)  
**Request body**  
`Post`  
**Response body**  
`Post`  
**Response status**  
- `201 CREATED`  
- `400 BAD REQUEST`  
    One or more invalid `Post` properties
    
`PUT /posts/{postId}`

**Description**  
Updates or replaces specified post  
**Path parameters**  
`postId`  
**Query Parameters**  
(None)  
**Request body**  
`Post`  
**Response body**  
`Post`  
**Response status**  
- `200 OK`  
- `400 BAD REQUEST`  
    Empty request body  

`DELETE /posts/{postId}`

**Description**  
Deletes specified post  
**Path parameters**  
`postId`  
**Query Parameters**  
(None)  
**Request body**  
(None)  
**Response body**  
(None)  
**Response status**  
- `204 NO CONTENT`

`GET /messages`

**Description**  
Returns recent messages of current `user`  
**Path parameters**  
(None)  
**Query Parameters**  
- `sent`  
    Date sent (`yyyy-MM-dd`)  
**Request body**  
(None)  
**Response body**  
`Message[]`  
**Response status**  
- `200 OK`

`DELETE /messages`

**Description**  
Deletes messages  
**Path parameters**  
(None)  
**Query Parameters**  
(None)  
**Request body**  
(None)  
**Response body**  
(None)  
**Response status**  
- `204 NO CONTENT`

`POST /messages`

**Description**  
Creates a new message for the current `User`  
**Path parameters**  
(None)  
**Query Parameters**  
(None)  
**Request body**  
`Message`  
**Response body**  
`Message`  
**Response status**  
- `201 CREATED`



    


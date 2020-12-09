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
- `id`  
**Request body**  
(None)  
**Response body**  
`User``[]`  
**Response status**  
- `200 OK`

`GET /users/{userId}`

**Description**   
Return the current `User` (profile) by id  
**Path parameters**  
`userId`  
**Query Parameters**     
(None)  
**Request body**  
(None)  
**Response body**  
`User`  
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

`GET /users/me/image`

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

`PUT /users/me/image`

**Description**  
Set profile picture for the current `User`  
**Path parameters**  
(None)  
**Query Parameters**  
(None)  
**Request body**  
`MultipartFile`  
**Response body**  
`User`  
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

`PUT /users/{friendshipId}`

**Description**  
Sets a User to a User's friends  
**Path parameters**  
`friendshipId`  
**Query Parameters**  
(None)  
**Request body**  
`boolean friend`  
**Response body**  
(None)  
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

`GET /ski-resorts/location`

**Description**  
Return `ski-resort` according to its latitude and longitude.  
**Path parameters**  
    `SkiResort` identifier  
**Query Parameters**  
(None)  
**Request body**  
- `latitude`  
- `longitude`  
**Response body**  
`SkiResort`  
**Response status**  
- `200 OK`  
- `404 NOT FOUND`

`PUT /ski-resorts/{skiResortId}/favorite`

**Description**  
Posts a single `ski-resort`  
**Path parameters**  
`skiResortId`  
**Query Parameters**  
(None)
**Request body**  
`boolean favorite`  
**Response body**  
(None)  
**Response status**  
- `200 OK`  
- `404 NOT FOUND`
  
`POST /ski-resorts`

**Description**  
Posts a single `ski-resort`  
**Path parameters**  
(None)  
**Query Parameters**  
(None)
**Request body**  
`skiResort`  
**Response body**  
`SkiResort`  
**Response status**  
- `200 OK`  
- `404 NOT FOUND`

`DELETE /ski-resorts/{skiResortId}`

**Description**  
Deletes a single `ski-resort`  
**Path parameters**  
`skiResortId`  
**Query Parameters**  
(None)  
**Request body**  
`skiResort`  
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
`distance`  
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

`GET /trips/end-time`
  
**Description**  
Returns all `Trips` by end-time  
**Path parameters**  
(None)  
**Query Parameters**  
`distance`  
**Request body**  
`date`  
**Response body**  
`Trip[]`  
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

`GET /trips/duration`
  
**Description**  
Returns all `Trips` by duration 
**Path parameters**  
(None)  
**Query Parameters**  
`distance`  
**Request body**  
- `date`
    -`start`  
    -`end`
**Response body**  
`Trip[]`  
**Response status**  
- `200 OK`  
- `404 NOT FOUND`

`DELETE /trips`
  
**Description**  
Deletes all `Trips`  
**Path parameters**  
(None)  
**Query Parameters**  
`distance`  
**Request body**  
(None)  
**Response body**  
`Trip[]`  
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

`GET /posts/{keyword}`

**Description**  
Gets and displays posts gathered by a keyword.  
**Path parameters**  
`keyword`  
**Query Parameters**  
(None)  
**Request body**  
(None)  
**Response body**  
(None)  
**Response status**  
- `204 NO CONTENT`

`GET /messages/{messageId}`

**Description**  
Returns recent messages of current `user`  
**Path parameters**  
`messageId`  
**Query Parameters**  
(None)
**Request body**  
(None)  
**Response body**  
`Message[]`  
**Response status**  
- `200 OK`

`GET /messages`

**Description**  
Returns recent messages of current `user`  
**Path parameters**  
(None)  
**Query Parameters**  
- `sent`  
    Date sent (`yyyy-MM-dd`)  
**Request body**  
- `User`
    `sender`  
    `receiver`  
**Response body**  
`Message[]`  
**Response status**  
- `200 OK`

`DELETE /messages/{messageId}`

**Description**  
Deletes messages  
**Path parameters**  
`messageId`  
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



    


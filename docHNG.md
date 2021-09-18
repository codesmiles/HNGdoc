# End game by forfeiting an ongoing game

This basically end game and choose the winner based on the user who forfeit the game against user that did not forfeit the game.

## Features

1. By ending a game through forfeiting an ongoing making a PATCH request enables you to make changes as part of the resourses at that location

2. It accepts a user_ID (In Integer) and game_ID (In string) in JSON format.

 ```sh
 {
  "user_id": 3,
  "game_id": "string"
 }
 ```

3. If the request is successful it gives a code 200 for successful response

4. It wil give 404 response for game not found request if the request doesn't match the game already

Response body

```sh
{
  "message": "Game does not exist",
  "data": null,
  "success": false
}
```

Response header

```sh
 connection: keep-alive 
 content-length: 61 
 content-type: application/json; charset=utf-8 
 date: Wed,15 Sep 2021 18:22:48 GMT 
 etag: W/"3d-geJitolmACn5u3T7flRgtvCftcM" 
 server: nginx/1.21.1 
 vary: Origin 
 x-powered-by: Express
```

5. The 500 response is for an internal server error if theres no data to read as an internal server error

Response header

```sh
{
  "message": "Cannot read property '1' of null",
  "data": null,
  "success": false
}
```

Response header

```sh
 connection: keep-alive 
 content-length: 74 
 content-type: application/json; charset=utf-8 
 date: Wed,15 Sep 2021 18:27:28 GMT 
 etag: W/"4a-eWv+OPszuwPpMTVFsrnpMBXLWhw" 
 server: nginx/1.21.1 
 vary: Origin 
 x-powered-by: Express 
 ```
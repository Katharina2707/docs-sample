# Users Guide

This document contains information about the endpoints and the components of the **User API**.


## Endpoints

### `GET /v1/users`
This endpoint returns a complete list of users in the system, including each user's ID, name, and email address.

### `POST /v1/users`
This endpoint lets you add a new user to the system.
To create a new user, follow the User schema, including all required fields such as ID, name and email address.
You will receive a confirmation when the user was successfully added.


#### `User` Schema
```yaml
type: object
properties:
  id:
    type: string
    description: Unique identifier for the user   #Suggestion to add a description
  name:
    type: string
    description: Full name of the user            #Suggestion to add a description
  email:                                          #Suggestion to add email
    type: string
    format: email                                 #Suggestion to add format to indicates that the string should follow a valid email format
    description: email address of the user

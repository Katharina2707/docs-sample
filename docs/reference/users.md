# Users Guide

This document contains information about the endpoints and the User schema of the **User API**.


## Endpoints

### `GET /v1/users`
- `GET`: List all users
     - `summary`: List all users
     - `responses`:
       - `200 OK`: Returns a JSON array of User objects.



### `POST /v1/users`
- `POST`: Create a new user
     - `summary`: Create a new user
     -  `requestBody`:
        - `application/json`: Expects a User object.
     - `responses`:
        - `201 Created`: Indicates successful creation.

## User schema
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
